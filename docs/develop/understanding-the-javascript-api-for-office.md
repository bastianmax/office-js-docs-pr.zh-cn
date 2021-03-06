---
title: 了解适用于 Office 的 JavaScript API
description: ''
ms.date: 10/17/2018
ms.openlocfilehash: 266014305af67d53046dac9a5492e08dbbb8dc29
ms.sourcegitcommit: 2ac7d64bb2db75ace516a604866850fce5cb2174
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2018
ms.locfileid: "26298556"
---
# <a name="understanding-the-javascript-api-for-office"></a>了解适用于 Office 的 JavaScript API

本文提供了有关适用于 Office 的 JavaScript API 的信息以及使用方法。有关参考信息，请参阅 [适用于 Office 的 JavaScript API](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office?view=office-js)。有关将 Visual Studio 项目文件更新到适用于 Office 的 JavaScript API 的最新当前版本的信息，请参阅 [更新适用于 Office 的 JavaScript API 版本和清单架构文件](update-your-javascript-api-for-office-and-manifest-schema-version.md)。

> [!NOTE]
> 如果计划将加载项[发布](../publish/publish.md)到 AppSource 并适用于 Office 体验，请务必遵循 [AppSource 验证策略](https://docs.microsoft.com/office/dev/store/validation-policies)。例如，加载项必须适用于支持已定义方法的所有平台，才能通过验证（有关详细信息，请参阅[第 4.12 部分](https://docs.microsoft.com/office/dev/store/validation-policies#4-apps-and-add-ins-behave-predictably)以及 [Office 加载项主机和可用性](../overview/office-add-in-availability.md)页面）。 

## <a name="referencing-the-javascript-api-for-office-library-in-your-add-in"></a>在加载项中引用适用于 Office 的 JavaScript API 库

[适用于 Office 的 JavaScript](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office?view=office-js) 库包含 Office.js 文件和关联的特定于主机应用程序的 .js 文件，例如 Excel-15.js 和 Outlook-15.js。引用该 API 最简单的方法是通过添加以下 `<script>` 到你的页面的 `<head>` 标记来使用我们的 CDN：  

```html
<script src="https://appsforoffice.microsoft.com/lib/1/hosted/Office.js" type="text/javascript"></script>
```

这将在加载项首次加载时下载并缓存适用于 Office 的 JavaScript API 文件，以确保对特定版本使用 Office.js 及其关联文件的最新实现。

有关 Office.js CDN 的详细信息，包括如何处理版本控制和向后兼容性，请参阅[从适用于 Office 的 JavaScript API 的内容传送网络 (CDN) 引用适用于 Office 的 JavaScript API 库](referencing-the-javascript-api-for-office-library-from-its-cdn.md)。

## <a name="initializing-your-add-in"></a>初始化加载项

**适用于：** 所有加载项类型

Office 加载项通常使用启动逻辑执行以下操作：

- 检查用户的 Office 版本是否支持代码调用的所有 Office API。

- 确保存在某些项目，例如具有特定名称的工作表。

- 提示用户选择 Excel 中的某些单元格，然后插入使用这些所选值进行初始化的图表。

- 建立绑定。

- 使用 Office 对话框 API 提示用户使用默认的加载项设置值。

但在完全加载库前，启动代码不得调用任何 Office.js API。 有两种方法可让代码确保已加载库。 以下各部分介绍了这两种方法： 

- [使用 Office.onReady() 进行初始化](#initialize-with-officeonready)
- [使用 Office.initialize 进行初始化](#initialize-with-officeinitialize)

有关这两种方法之间的差别信息，请参阅 [Office.initialize 和 Office.onReady() 之间的主要差别](#major-differences-between-officeinitialize-and-officeonready)。 有关初始化加载项时的事件顺序的更多详细信息，请参阅 [加载 DOM 和运行时环境](loading-the-dom-and-runtime-environment.md)。

### <a name="initialize-with-officeonready"></a>使用 Office.onReady() 进行初始化

`Office.onReady()` 是一个异步方法，它在查看是否完全加载 Office.js 库时返回 Promise 对象。 仅在加载库时，它才将 Promise 解析为一个对象，该对象指定具有 `Office.HostType` 枚举值（`Excel`、`Word` 等）的 Office 主机应用程序的对象和具有 `Office.PlatformType` 枚举值（`PC`、`Mac`、`OfficeOnline` 等）的平台。 如果在调用 `Office.onReady()` 时已加载库，则 Promise 将立即解析。

调用 `Office.onReady()` 的一种方法是向其传递一个回调方法。 下面是一个示例：

```js
Office.onReady(function(info) {
    if (info.host === Office.HostType.Excel) {
        // Do Excel-specific initialization (for example, make add-in task pane's
        // appearance compatible with Excel "green").
    }
    if (info.platform === Office.PlatformType.PC) {
        // Make minor layout changes in the task pane.
    }
    console.log(`Office.js is now ready in ${info.host} on ${info.platform}`);
});
```

或者，可以将 `then()` 方法链接到 `Office.onReady()` 的调用，而不是传递回调。 例如，以下代码检查用户的 Excel 版本是否支持加载项可能调用的所有 API。

```js
Office.onReady()
    .then(function() {
        if (!Office.context.requirements.isSetSupported('ExcelApi', '1.7')) {
            console.log("Sorry, this add-in only works with newer versions of Excel.");
        }
    });
```

以下是在 TypeScript 中使用 `async` 和 `await` 关键字的同一示例：

```typescript
(async () => {
    await Office.onReady();
    if (!Office.context.requirements.isSetSupported('ExcelApi', '1.7')) {
        console.log("Sorry, this add-in only works with newer versions of Excel.");
    }
})();
```

如果使用的是其他 JavaScript 框架，其中包括它们自己的初始化处理程序或测试，那么它们*通常*应放置在 `Office.onReady()` 的响应内。 例如，会对 [JQuery 的](https://jquery.com) `$(document).ready()` 函数进行以下引用：

```js
Office.onReady(function() {
    // Office is ready
    $(document).ready(function () {
        // The document is ready
    });
});
```

但是，此做法存在例外情况。 例如，假设想要在浏览器中打开加载项（而不是在 Office 主机中旁加载它）以使用浏览器工具调试 UI。 由于 Office.js 将不会在浏览器中加载，所以，`onReady` 将不会运行，且如果在 Office `$(document).ready` 内调用它，则 `onReady` 将不会运行。 另一个例外情况：希望在加载项加载时在任务窗格中显示进度指示器。 在此方案中，代码应调用 jQuery `ready` 并使用其回调来呈现进度指示器。 然后，Office `onReady` 的回调可将进度指示器替换为最终 UI。 

### <a name="initialize-with-officeinitialize"></a>使用 Office.initialize 进行初始化

当 Office.js 库完全加载并准备好用于用户交互时将触发初始化事件。 可将处理程序分配到实现初始化逻辑的 `Office.initialize`。 以下是检查用户的 Excel 版本是否支持加载项可能调用的所有 API 的示例。

```js
Office.initialize = function () {
    if (!Office.context.requirements.isSetSupported('ExcelApi', '1.7')) {
        console.log("Sorry, this add-in only works with newer versions of Excel.");
    }
};
```

如果使用的是其他 JavaScript 框架，其中包含它们自己的初始化处理程序或测试，那么它们*通常*应放置在 `Office.initialize` 事件内。 （但在之前**使用 Office.onReady() 进行初始化**部分中所述的例外情况也适用于此情况。）例如，会对 [JQuery 的](https://jquery.com) `$(document).ready()` 函数进行以下引用：

```js
Office.initialize = function () {
    // Office is ready
    $(document).ready(function () {
        // The document is ready
    });
  };
```

对于任务窗格和内容加载项，`Office.initialize` 提供了其他 _reason_ 参数。 此参数指定如何将加载项添加到当前文档。 可以使用此参数针对首次插入加载项时和加载项已存在于文档中时实施不同的逻辑。

```js
Office.initialize = function (reason) {
    $(document).ready(function () {
        switch (reason) {
            case 'inserted': console.log('The add-in was just inserted.');
            case 'documentOpened': console.log('The add-in is already part of the document.');
        }
    });
 };
```

有关详细信息，请参阅 [Office.initialize 事件](https://docs.microsoft.com/javascript/api/office?view=office-js)和 [InitializationReason 枚举](https://docs.microsoft.com/javascript/api/office/office.initializationreason?view=office-js)。

> [!NOTE]
> 目前，无论是否同时调用 `Office.onReady()`均必须设置 `Office.Initialize`。 如果无需使用 `Office.Initialize`，可以将其设置为一个空函数，如以下示例中所示。
> 
>```js
>Office.initialize = function () {};
>```

### <a name="major-differences-between-officeinitialize-and-officeonready"></a>Office.initialize 和 Office.onReady 之间的主要差别

- 可以仅将一个处理程序分配到 `Office.initialize` 并仅由 Office 基础结构调用一次，但可以在代码中的不同位置调用 `Office.onReady()` 并使用不同的回调。 例如，只要自定义脚本使用运行初始化逻辑的回调进行加载，代码就可以调用 `Office.onReady()`。代码还可以在任务窗格中设置一个按钮，其脚本会使用不同的回调调用 `Office.onReady()`。 如果是这样，则会在单击该按钮后运行第二个回调。

- `Office.initialize` 事件将在 Office.js 初始化其本身的内部过程的末尾处触发。 并且它会在内部过程结束后*立即*触发。 如果将处理程序分配到事件所使用的代码在事件触发后执行的时间过长，则处理程序将不会运行。 例如，如果使用的是 WebPack 任务管理器，则在加载 Office.js 后但在加载自定义 JavaScript 前，它会配置加载项的主页以加载填充代码文件。 在脚本加载和分配处理程序时，初始化事件已经发生。 但调用 `Office.onReady()` 永远不会“太迟”。 如果初始化事件已经发生，则回调将立即运行。

> [!NOTE]
> 即使没有启动逻辑，也应在加载项 JavaScript 加载时将空函数分配到 `Office.initialize`，如以下示例中所示。 在初始化事件触发且指定的事件处理程序函数运行前，某些 Office 主机和平台组合将不会加载任务窗格。
> 
>```js
>Office.initialize = function () {};
>```

## <a name="office-javascript-api-object-model"></a>Office JavaScript API 对象模型

初始化后，加载项可与主机进行交互（例如，Excel、Outlook）。 [Office JavaScript API 对象模型](office-javascript-api-object-model.md)页提供了有关特定使用模式的更为详细的信息。 还提供了有关[共享 API](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office?view=office-js) 和特定主机的详细参考文档。

## <a name="api-support-matrix"></a>API 支持矩阵

下表总结了各种类型的加载项（内容、任务窗格和 Outlook）支持的 API 和功能，以及使用[适用于 Office 的 JavaScript API v1.1 支持的 1.1 加载项清单架构和功能](update-your-javascript-api-for-office-and-manifest-schema-version.md)指定加载项支持的 Office 主机应用时，可以托管它们的 Office 应用。


|||||||||
|:-----|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
||**主机名**|数据库|工作簿|邮箱|演示文稿|文档|Project|
||**支持的****主机应用程序**|Access Web App|Excel、<br/>Excel Online|Outlook、<br/>Outlook Web App、<br/>适用于设备的 OWA|PowerPoint、<br/>PowerPoint Online|Word|项目|
|**支持的外接程序类型**|内容|Y|Y||Y|||
||任务窗格||Y||Y|Y|Y|
||Outlook|||Y||||
|**支持的 API 功能**|读/写文本||Y||Y|Y|是<br/>（只读）|
||读/写矩阵||Y|||Y||
||读/写表||Y|||Y||
||读/写 HTML|||||是||
||读/写<br/>Office Open XML|||||是||
||读取任务、资源、视图和字段属性||||||Y|
||选择已更改事件||Y|||Y||
||获取整个文档||||Y|是||
||绑定和绑定事件|是<br/>（仅限完全和部分表格绑定）|是|||是||
||读/写自定义 XML 部分|||||是||
||暂留加载项状态数据（设置）|是<br/>（每主机加载项）|是<br/>（每文档）|是<br/>（每邮箱）|是<br/>（每文档）|是<br/>（每文档）||
||设置更改事件|Y|Y||Y|是||
||获取活动视图模式<br/>和视图更改事件||||是|||
||转到文档中<br/>的相应位置||是||Y|是||
||使用规则和 RegEx <br/>执行上下文式激活|||是||||
||读取项目属性|||Y||||
||读取用户配置文件|||Y||||
||获取附件|||Y||||
||获取用户标识令牌|||Y||||
||调用 Exchange Web 服务|||Y||||
