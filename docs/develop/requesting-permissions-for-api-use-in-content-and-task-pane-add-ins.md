---
title: 在内容和任务窗格加载项中请求获取 API 使用权限
description: ''
ms.date: 12/04/2017
ms.openlocfilehash: 2105dab859cdfa114c4b6f3c9eeaa73d3ae49ce8
ms.sourcegitcommit: c53f05bbd4abdfe1ee2e42fdd4f82b318b363ad7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "25505305"
---
# <a name="requesting-permissions-for-api-use-in-content-and-task-pane-add-ins"></a>在内容和任务窗格加载项中请求获取 API 使用权限

本文说明您可以在内容或任务窗格加载项清单中声明的不同权限级别，以指定加载项功能所需的 JavaScript API 访问的级别。 




## <a name="permissions-model"></a>权限模型


5 级 JavaScript API 访问权限模型为内容和任务窗格加载项的用户提供基本的隐私和安全功能。图 1 显示可以在加载项清单中声明的 API 权限的 5 个级别。


*图 1：内容和任务窗格加载项的 5 级权限模型*

![任务窗格应用程序的权限级别](../images/office15-app-sdk-task-pane-app-permission.png)



这些权限指定加载项运行时在用户插入然后激活（信任）加载项时允许内容或任务窗格加载项使用的 API 子集。若要声明内容或任务窗格加载项所需的权限级别，请在加载项清单的 [Permissions](https://docs.microsoft.com/office/dev/add-ins/reference/manifest/permissions?view=office-js) 元素中指定任一权限文本值。以下示例要求 **WriteDocument** 权限，仅允许可以对文档进行写入（而非阅读）的方法。




```XML
<Permissions>WriteDocument</Permissions>
```

作为最佳做法，应该根据_最小特权_原则请求权限。也就是说，应该请求仅可访问加载项正常运行所需的 API 最小子集的权限。例如，如果加载项的功能只需要读取用户文档中的数据，应该请求的权限不应高于 **ReadDocument** 权限。

下表描述了每个权限级别启用的 JavaScript API 子集。



|**权限**|**启用的 API 子集**|
|:-----|:-----|
|**Restricted**|[Settings](https://docs.microsoft.com/javascript/api/office/office.settings?view=office-js) 对象的方法和 [Document.getActiveViewAsync](https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#getactiveviewasync-options--callback-) 方法。这是内容或任务窗格加载项可以请求的最低级别权限。|
|**ReadDocument**|除了 **Restricted** 权限允许的 API，添加对 API 成员的必要访问权限，以读取文档和管理绑定。这包括对以下内容的使用：<br/><ul><li><a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#getselecteddataasync-coerciontype--options--callback-" target="_blank">Document.getSelectedDataAsync</a> 方法，用于获取所选文本、HTML（仅限 Word）或表格数据，但不可用于包含文档中所有数据的基础 Open Office XML (OOXML) 代码。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#getfileasync-filetype--options--callback-" target="_blank">Document.getFileAsync</a> 方法，用于获取文档中的所有文本，但不是文档的下层 OOXML 二进制副本。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.binding?view=office-js#getdataasync-options--callback-" target="_blank">Binding.getDataAsync</a> 方法，用于读取文档中的绑定数据。</p></li><li><p><span class="keyword">Bindings</span> 对象的 <a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#addfromnameditemasync-itemname--bindingtype--options--callback-" target="_blank"> addFromNamedItemAsync</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#addfrompromptasync-bindingtype--options--callback-" target="_blank">   addFromPromptAsync</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#addfromselectionasync-bindingtype--options--callback-" target="_blank">addFromSelectionAsync</a> 方法，用于在文档中创建绑定。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#getallasync-options--callback-" target="_blank">Bindings</a> 对象的 <a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#getbyidasync-id--options--callback-" target="_blank">getAllAsync</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.bindings?view=office-js#releasebyidasync-id--options--callback-" target="_blank">getByIdAsync</a> 和 <span class="keyword">releaseByIdAsync</span> 方法，用于访问和删除文档中的绑定。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#getfilepropertiesasync-options--callback-" target="_blank">Document.getFilePropertiesAsync</a> 方法，用于访问文档文件属性，例如文档的 URL。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#gotobyidasync-id--gototype--options--callback-" target="_blank">Document.goToByIdAsync</a> 方法，用于导航到文档中的已命名对象和位置。</p></li><li><p>对于项目的任务窗格加载项，<a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js" target="_blank">ProjectDocument</a> 对象的所有“get”方法。 </p></li></ul>|
|**ReadAllDocument**|除了 **Restricted** 和 **ReadDocument** 权限允许的 API，允许以下对文档数据的额外访问权：<br/><ul><li><p><span class="keyword">Document.getSelectedDataAsync</span> 和 <span class="keyword">Document.getFileAsync</span> 方法可以访问文档的下层 OOXML 代码（除了文本，还可能包含格式、链接、嵌入图片、注释、修订等）。</p></li></ul>|
|**WriteDocument**|除了 **Restricted** 权限允许的 API，添加对以下 API 成员的访问权：<br/><ul><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#setselecteddataasync-data--options--callback-" target="_blank">Document.setSelectedDataAsync</a> 方法，用于在文档中写入用户所选内容。</p></li></ul>|
|**ReadWriteDocument**|除了 **Restricted**、**ReadDocument**、**ReadAllDocument** 和 **WriteDocument** 权限允许的 API，将对内容和任务窗格加载项支持的所有其他 API 的访问权包含在内，包括订阅事件的方法。必须声明 **ReadWriteDocument** 权限才能访问这些额外的 API 成员：<br/><ul><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.binding?view=office-js#setdataasync-data--options--callback-" target="_blank">Binding.setDataAsync</a> 方法，用于将内容写入到文档的绑定区域。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#addrowsasync-rows--options--callback-" target="_blank">TableBinding.addRowsAsync</a> 方法，用于将行添加到绑定表格中。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#addcolumnsasync-tabledata--options--callback-" target="_blank">TableBinding.addColumnsAsync</a> 方法，用于将列添加到绑定表格中。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#deletealldatavaluesasync-options--callback-" target="_blank">TableBinding.deleteAllDataValuesAsync</a> 方法，用于删除绑定表格中的所有数据。</p></li><li><p><span class="keyword">TableBinding</span> 对象的 <a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#setformatsasync-cellformat--options--callback-" target="_blank">setFormatsAsync</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#clearformatsasync-options--callback-" target="_blank">clearFormatsAsync</a> 和 <a href="https://docs.microsoft.com/javascript/api/office/office.tablebinding?view=office-js#settableoptionsasync-tableoptions--options--callback-" target="_blank">setTableOptionsAsync</a> 方法，用于设置绑定表格中的格式和选项。</p></li><li><p><a href="https://docs.microsoft.com/javascript/api/office/office.customxmlnode?view=office-js" target="_blank">CustomXmlNode</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.customxmlpart?view=office-js" target="_blank">CustomXmlPart</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.customxmlparts?view=office-js" target="_blank">CustomXmlParts</a> 和 <a href="https://docs.microsoft.com/javascript/api/office/office.customxmlprefixmappings?view=office-js" target="_blank">CustomXmlPrefixMappings</a> 对象的所有成员。</p></li><li><p>所有订阅受内容和任务窗格加载项支持的事件的方法，特别是 <a href="https://docs.microsoft.com/javascript/api/office/office.binding?view=office-js" target="_blank">Binding</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.customxmlpart?view=office-js" target="_blank">CustomXmlPart</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js" target="_blank">Document</a>、<a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js" target="_blank">ProjectDocument</a> 和 <a href="https://docs.microsoft.com/javascript/api/office/office.document?view=office-js#settings" target="_blank">Settings</a> 对象的 <span class="keyword">addHandlerAsync</span> 和 <span class="keyword">removeHandlerAsync</span> 方法。</p></li></ul>|

## <a name="see-also"></a>另请参阅

- [Office 加载项的隐私和安全](../concepts/privacy-and-security.md)
    


