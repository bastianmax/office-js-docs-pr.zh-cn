# <a name="color"></a>颜色
颜色通常用于强调品牌并加强视觉层次。 它有助于识别界面，并在体验中为客户提供引导。 在Office内部，颜色被用于相同的目标，但它被有目的地和最低限度地应用。 在任何时候它都不应过度影响客户的内容。 即使每个Office应用程序都使用自己的主色调进行标记，它也会被谨慎使用。

Office UI Fabric 包含一组默认主题颜色。当 Fabric 作为组件应用于 Office 外接程序或应用于布局时，相同的目标适用。颜色应传达层次结构，有目的地指导客户操作而不会干扰内容。Fabric 主题颜色可以向整体界面引入新的个性色。此新的个性色可能会与 Office 应用程序品牌产生冲突并干扰层次结构。换句话说，Fabric 在外接程序内部使用时可能会向整体界面引入新的个性色。此新的个性色可能会分散用户注意力并干扰整个层次结构。寻找避免冲突和干扰的方法。使用中性个性色或覆盖 Fabric 主题颜色，以匹配 Office 应用程序品牌或你自己的品牌颜色。

Office 应用程序使客户能够通过应用 Office UI 主题个性化设置其界面。客户可以在四个 UI 主题中进行选择来改变背景样式以及 Word、PowerPoint、Excel 和 Office 套件中其他应用程序的按钮。若要使外接程序感觉像是 Office 的一个固有部分并响应个性化设置，请使用我们的主题 API。例如，任务窗格背景颜色在某些主题中切换到深灰色。我们的主题 API 允许你照做并调整前景文本，以确保[辅助功能](../design/accessibility-guidelines.md)。

> [!NOTE]
> - 对于邮件和任务窗格外接程序，请使用 [Context.officeTheme](https://docs.microsoft.com/javascript/api/office/office.context?view=office-js) 元素匹配 Office 应用程序的主题。此 API 当前仅在 Office 2016 中可用。
> - 对于 PowerPoint 内容加载项，请参阅[在 PowerPoint 加载项中使用 Office 主题](../powerpoint/use-document-themes-in-your-powerpoint-add-ins.md)。

将下列一般原则应用于颜色：

* 尽量少使用颜色来显示层次结构和强调品牌。
* 过度使用单个应用于交互式和非交互式元素的个性色可能会导致混乱。例如，避免将相同颜色用于导航菜单中的选定和未选定项。
* 避免与 Office 品牌应用颜色产生不必要的冲突。
* 使用自己的品牌颜色来生成与服务或公司的关联。
* 确保可以访问所有文本。确保前景文本与后台之间的对比度比为 4.5:1。
* 注意色盲群体。不要仅使用颜色指示交互性和层次结构。
* 请参阅[图标指南](../design/add-in-icons.md)，详细了解如何使用 Office 图标调色板设计外接程序命令图标。