---
title: Office 加载项中的任务窗格
description: 任务窗格允许用户访问界面控件，此类控件运行代码以修改文档或电子邮件，或显示数据源的数据。
ms.date: 12/04/2017
ms.openlocfilehash: fefba14528a4fc3a75b0936c8f5e2ae1bf01ca1b
ms.sourcegitcommit: 30435939ab8b8504c3dbfc62fd29ec6b0f1a7d22
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2018
ms.locfileid: "23943941"
---
# <a name="task-panes-in-office-add-ins"></a>Office 加载项中的任务窗格
 
任务窗格是接口图面，通常出现在 Word、PowerPoint、Excel 和 Outlook 中窗口的右侧。使用任务窗格，用户可以访问接口控件，以运行代码来修改文档或电子邮件，或显示数据源中的数据。如果不需要将功能直接嵌入文档，请使用任务窗格。

*图 1：典型任务窗格布局*

![显示典型任务窗格布局的图像](../images/overview-with-app-task-pane.png)

## <a name="best-practices"></a>最佳做法

|**允许事项**|**禁止事项**|
|:-----|:--------|
|<ul><li>在标题中包括外接程序的名称。</li></ul>|<ul><li>请勿在标题中追加公司名称。</li></ul>|
|<ul><li>在标题中使用简短的描述性名称。</li></ul>|<ul><li>不要在外接程序标题中追加“add-in”、“for Word”或“for Office”等字符串。</li></ul>|
|<ul><li>在外接程序顶部包括某些导航或命令元素，如命令栏或透视。</li></ul>||
|<ul><li>在外接程序底部包括品牌元素，如品牌栏，除非要在 Outlook 内使用外接程序。</li></ul>||


## <a name="variants"></a>变量

下图显示分辨率为 1366x768 时 Office 功能区的各种任务窗格大小。对于 Excel，需要额外的垂直空间来容纳编辑栏。  

*图 2：Office 2016 桌面任务窗格尺寸*

![显示尺寸为 1366x768 的桌面任务窗格的图像](../images/add-in-taskpane-sizes-desktop.png)

- Excel - 320 x 455
- PowerPoint - 320 x 531
- Word - 320 x 531
- Outlook - 348x535

<br/>

*图 3：Office 365 任务窗格大小*

![显示尺寸为 1366x768 的桌面任务窗格的图像](../images/add-in-taskpane-sizes-online.png)

- Excel - 350 x 378
- PowerPoint - 348x391
- Word - 329 x 445
- Outlook Web 应用 - 320x570

## <a name="personality-menu"></a>“个性”菜单

“个性”菜单可能会妨碍靠近外接程序右上角的导航和命令元素。以下是 Windows 和 Mac 上的“个性”菜单的当前尺寸。

对于 Windows，个性菜单尺寸为 12x32 像素，如下所示。

*图 4：Windows 上的个性菜单*

![显示 Windows 桌面上个性菜单的图像](../images/personality-menu-win.png)

对于 Mac，“个性”菜单尺寸为 26x26 像素，但是从右侧浮动 8 个像素，再从顶部浮动 6 个像素，能将空间增加至 34x32 像素，如下所示。

*图 5：Mac 上的个性菜单*

![显示 Mac 桌面上个性菜单的图像](../images/personality-menu-mac.png)

## <a name="implementation"></a>实现

有关实现任务窗格的示例，请参阅 GitHub 上的 [Excel 加载项 JS WoodGrove 支出趋势](https://github.com/OfficeDev/Excel-Add-in-WoodGrove-Expense-Trends)。 


## <a name="see-also"></a>另请参阅

- [Office 加载项中的 Office UI Fabric](office-ui-fabric.md) 
- [适用于 Office 外接程序的 UX 设计模式](https://github.com/OfficeDev/Office-Add-in-UX-Design-Patterns-Code)


