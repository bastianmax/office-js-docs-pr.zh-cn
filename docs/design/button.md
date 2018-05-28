---
title: Office UI Fabric 中的按钮组件
description: ''
ms.date: 12/04/2017
---

# <a name="button-component-in-office-ui-fabric"></a>Office UI Fabric 中的按钮组件

Office 加载项中的按钮组件可便于用户提交更改或完成任务步骤。请确保按钮文本传达了交互目的。请在任务窗格、对话框或内容窗格的 UI 容器底部添加按钮组件。例如，按钮可便于用户提交表单、关闭对话框或移到下一页。
  
#### <a name="example-buttons-in-a-task-pane"></a>示例：任务窗格中的按钮组件

![显示按钮的图像](../images/overview-with-app-button.png)

## <a name="best-practices"></a>最佳做法

|**允许事项**|**禁止事项**|
|:-----|:--------|
|默认按钮应始终在加载项中执行安全操作。 |请勿将默认焦点放置在销毁数据的按钮上。而应将焦点放置在执行安全操作或取消操作的按钮上。|
|应仅在按钮标签中使用单行文本。文本尽量保持简短。|请勿在按钮中添加任何非文本内容。|
|请确保标签向用户传达按钮的明确目的。请使用简洁、具体、一目了然的标签。请考虑使用单个词。|不得使用按钮进行导航，“上一步”和“下一步”除外。对于导航，请考虑使用链接。|
|应仅向用户公开一个或两个按钮（操作），例如，“接受”和“取消”。如果需要公开更多操作，请考虑使用复选框或单选按钮，以便用户选择操作，并提供一个按钮来启动选定操作。||
|应将“提交”、“确定”和“应用”按钮设置为主按钮样式。如果其中一个按钮旁边出现“重置”或“取消”按钮，将它们设置为默认按钮。| |

## <a name="variants"></a>变体

|**变体**|**说明**|**示例**|
|:------------|:--------------|:----------|
|**主按钮**|主按钮继承静止状态下的主题颜色。主按钮可用于突出显示主号召性用语。|![主按钮图像](../images/button-primary.png)|
|**默认按钮**|默认按钮应始终执行安全操作，不得执行删除操作。|![默认按钮图像](../images/button-default.png)|
|**复合按钮**|复合按钮可用于执行完成任务所需的操作或执行过渡任务。|![复合按钮图像](../images/button-compound.png)|

## <a name="implementation"></a>实现

有关详细信息，请参阅[按钮](https://dev.office.com/fabric#/components/button)和 [Fabric React 代码示例入门](https://github.com/OfficeDev/Word-Add-in-GettingStartedFabricReact)。

## <a name="see-also"></a>另请参阅

- [用户体验设计模式](https://github.com/OfficeDev/Office-Add-in-UX-Design-Patterns-Code)
- [Office 加载项中的 Office UI Fabric](office-ui-fabric.md)