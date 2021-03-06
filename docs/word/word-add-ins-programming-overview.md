---
title: Word 加载项概述
description: ''
ms.date: 09/24/2018
ms.openlocfilehash: 5cfae87c44f2a3004e4cd755614d15261b43945f
ms.sourcegitcommit: c53f05bbd4abdfe1ee2e42fdd4f82b318b363ad7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "25505943"
---
# <a name="word-add-ins-overview"></a>Word 加载项概述

要创建解决方案来扩展 Word 功能？例如，涉及自动文档程序集的解决方案？或从其他数据源绑定到并访问 Word 文档中数据的解决方案？可以使用 Office 加载项平台，其中包含 Word JavaScript API 和适用于 Office 的 JavaScript API，可用于扩展在 Windows 桌面设备、Mac 或云中运行的 Word 客户端。

Word 加载项是 [Office 加载项平台](../overview/office-add-ins.md)上众多开发选项中的一项。加载项命令可用于扩展 Word 用户界面并启动运行 JavaScript 并与 Word 文档中内容交互的任务窗格。在浏览器中可以运行的任何代码均可在 Word 加载项中运行。与 Word 文档内容进行交互的加载项可创建作用于 Word 对象的请求并同步对象状态。 

> [!NOTE]
> 生成加载项时，如果计划将加载项[发布](../publish/publish.md)到 AppSource，请务必遵循 [AppSource 验证策略](https://docs.microsoft.com/office/dev/store/validation-policies)。例如，加载项必须适用于支持已定义方法的所有平台，才能通过验证（有关更多信息，请参阅[第 4.12 部分](https://docs.microsoft.com/office/dev/store/validation-policies#4-apps-and-add-ins-behave-predictably)以及 [Office 加载项主机和可用性](../overview/office-add-in-availability.md)页面）。

下图中的示例展示了在任务窗格中运行的 Word 加载项。

*图 1：在 Word 的任务窗格中运行的加载项*

![在 Word 的任务窗格中运行的加载项](../images/word-add-in-show-host-client.png)

Word 加载项 (1) 可以将请求发送到 Word 文档 (2) 可以使用 JavaScript 来访问段落对象和更新、删除或移动段落。例如，下面的代码显示如何将一个新句子附加到该段落。

```js
Word.run(function (context) {
    var paragraphs = context.document.getSelection().paragraphs;
    paragraphs.load();
    return context.sync().then(function () {
        paragraphs.items[0].insertText(' New sentence in the paragraph.',
                                       Word.InsertLocation.end);
    }).then(context.sync);
});

```

若要托管 Word 加载项，可以使用任何 Web 服务器技术（如 ASP.NET、NodeJS 或 Python）。可以使用常用的客户端框架（Ember、Backbone、Angular、React），也可以坚持使用 VanillaJS 开发解决方案，并能使用 Azure 等服务[验证](../develop/use-the-oauth-authorization-framework-in-an-office-add-in.md)和托管应用。

通过 Word JavaScript API 可使应用程序访问 Word 文档中的对象和元数据。你可以使用这些 API 创建面向以下应用程序的加载项：

* 适用于 Windows 的 Word 2013 或更高版本
* Word Online
* 适用于 Mac 的 Word 2016 或更高版本
* 适用于 iOS 的 Word

加载项只需编写一次，即可跨多个平台在所有版本 Word 中运行。有关详细信息，请参阅 [Office 加载项主机和平台可用性](../overview/office-add-in-availability.md)。

## <a name="javascript-apis-for-word"></a>适用于 Word 的 JavaScript API

有两组 JavaScript Api 可用于与 Word 文档中的对象和元数据进行交互。第一组是[适用于 Office 的 JavaScript API](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office?view=office-js?product=word)，在 Office 2013 进行了引入。这是一个共享 API --许多对象可以在由两个或多个 Office 客户端托管的加载项中使用。此 API 广泛使用回调。

第二组是 [Word JavaScript API](https://docs.microsoft.com/office/dev/add-ins/reference/overview/word-add-ins-reference-overview?view=office-js)。这是强类型对象模型，可用于创建针对 Word 2016 for Mac 和 Windows 的 Word 加载项。此对象模型使用承诺模式，并提供对特定于 Word 对象（如[正文](https://docs.microsoft.com/javascript/api/word/word.body?view=office-js)、[内容控件](https://docs.microsoft.com/javascript/api/word/word.contentcontrol?view=office-js)、[内联图片](https://docs.microsoft.com/javascript/api/word/word.inlinepicture?view=office-js)和[段落](https://docs.microsoft.com/javascript/api/word/word.paragraph?view=office-js)）的访问权限。Word JavaScript API 包括 TypeScript 定义和 vsdoc 文件，这样，你可以在 IDE 中获取代码提示。

目前，所有 Word 客户端均支持共享的适用于 Office 的 JavaScript API，大多数客户端支持 Word JavaScript API。有关受支持的客户端的详细信息，请参阅 [API 参考文档](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office?view=office-js?product=word)。

我们建议从 Word JavaScript API 开始，因为对象模型更易于使用。如果需要执行以下操作，请使用 Word JavaScript API：

* 访问 Word 文档中的对象。

在需要执行以下操作时，使用共享的适用于 Office 的 JavaScript API：

* 面向 Word 2013。
* 执行应用程序的初始操作。
* 检查支持的要求集。
* 访问文档的元数据、设置和环境信息。
* 绑定到文档中的部分并捕获事件。
* 使用自定义 XML 部件。
* 打开一个对话框。

## <a name="next-steps"></a>后续步骤

准备好创建首个 Word 加载项了吗？请参阅[生成首个 Word 加载项](word-add-ins.md)。还可以尝试感受交互式[入门体验](https://docs.microsoft.com/office/dev/add-ins/?product=Word)。请使用[加载项清单](../develop/add-in-manifests.md)描述加载项的托管位置和显示方式，并定义权限和其他信息。

要更多了解如何设计世界一流的 Word 加载项来为用户打造具有吸引力的体验，请参阅[设计准则](../design/add-in-design.md)和[最佳做法](../concepts/add-in-development-best-practices.md)。

开发加载项后，可以将它[发布](../publish/publish.md)到网络共享、应用目录或 AppSource。

## <a name="whats-coming-up-for-word-add-ins"></a>Word 加载项未来发展趋势如何？

随着我们设计和开发适用于 Word 加载项的新 API，我们将会发布这些 API，以供大家在 [API 开放性规范](https://docs.microsoft.com/office/dev/add-ins/reference/openspec?view=office-js)页面上提供反馈。请了解即将推出的 Word JavaScript API 新功能，并提供对设计规范的宝贵意见。

## <a name="see-also"></a>另请参阅

* [Office 加载项平台概述](../overview/office-add-ins.md)
* [Word JavaScript API 参考](https://docs.microsoft.com/office/dev/add-ins/reference/overview/word-add-ins-reference-overview?view=office-js)

