---
title: 安装最新版 Office 2016
description: ''
ms.date: 12/04/2017
---

# <a name="install-the-latest-version-of-office-2016"></a>安装最新版 Office 2016

新开发人员功能（包括仍处于预览阶段的功能）会先向选择获取最新版 Office 的订阅者提供。 

## <a name="opt-in-to-getting-the-latest-builds"></a>选择获取最新版

若要选择获取最新版 Office 2016，请执行以下操作： 

- 如果是 Office 365 家庭版、个人版或大专院校版订阅者，请参阅[成为 Office 预览体验成员](https://products.office.com/zh-cn/office-insider)。
- 如果你是 Office 365 商业版客户，请参阅 [为 Office 365 商业版客户安装首次发布](https://support.office.com/zh-cn/article/Install-the-First-Release-build-for-Office-365-for-business-customers-4dd8ba40-73c0-4468-b778-c7b744d03ead?ui=en-US&rs=en-US&ad=US)。
- 如果在 Mac 上运行 Office 2016：
    - 启动 Office 2016 for Mac 程序。
    - 选择“帮助”菜单上的“**检查更新**”。
    - 选中“Microsoft 自动更新”框，以加入 Office 预览体验成员计划。 

## <a name="get-the-latest-build"></a>获取最新版

若要获取最新版 Office 2016，请执行以下操作： 

1. 下载 [Office 2016 部署工具](https://www.microsoft.com/en-us/download/details.aspx?id=49117)。 
2. 运行该工具。这会提取以下两个文件：Setup.exe 和 configuration.xml。
3. 将 configuration.xml 文件替换为[首次发布配置文件](https://raw.githubusercontent.com/OfficeDev/Office-Add-in-Commands-Samples/master/Tools/FirstReleaseConfig/configuration.xml)。
4. 以管理员身份运行下面的命令：`setup.exe /configure configuration.xml` 

    > [!NOTE]
    > 此命令可能需要运行很长时间才能完成，而且不会显示进度。

在安装进程完成后，你已安装最新的 Office 2016 应用程序。要验证你是否拥有最新版本，请从任何 Office 应用程序转到“**文件**” > “**帐户**”。在“Office 更新”下，你将看到版本号上面的 (Office Insiders) 标签。

![显示产品信息的屏幕截图（带有 Office Insiders 标签）](../images/office-insiders.png)

## <a name="minimum-office-builds-for-office-javascript-api-requirement-sets"></a>Office JavaScript API 要求集对应的最低 Office 内部版本

若要了解 API 要求集对应的各个平台的最低产品内部版本，请参阅以下资源：

- [Word JavaScript API 要求集](https://dev.office.com/reference/add-ins/requirement-sets/word-api-requirement-sets)
- [Excel JavaScript API 要求集](https://dev.office.com/reference/add-ins/requirement-sets/excel-api-requirement-sets)
- [OneNote JavaScript API 要求集](https://dev.office.com/reference/add-ins/requirement-sets/onenote-api-requirement-sets)
- [对话框 API 要求集](https://dev.office.com/reference/add-ins/requirement-sets/dialog-api-requirement-sets)
- [Office 通用 API 要求集](https://dev.office.com/reference/add-ins/requirement-sets/office-add-in-requirement-sets)