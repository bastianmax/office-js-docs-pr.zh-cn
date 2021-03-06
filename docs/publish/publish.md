---
title: 部署和发布 Office 外接程序 |Microsoft Docs
description: 用以测试或向用户发布的部署 Office 外接程序的方法和选项。
ms.date: 01/23/2018
ms.openlocfilehash: ada786ed7ded1f34d564389c09c2cd5c25c2a331
ms.sourcegitcommit: eb74e94d3e1bc1930a9c6582a0a99355d0da34f2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "25004929"
---
# <a name="deploy-and-publish-your-office-add-in"></a>部署和发布 Office 外接程序

可以使用几种方法之一来部署 Office 外接程序，以用于对用户进行测试或分发：

|**方法**|**使用...**|
|:---------|:------------|
|[旁加载](../testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins.md)|在开发过程中测试在 Windows、Office Online、iPad 或 Mac 上运行的加载项。|
|[集中部署](centralized-deployment.md)|在云或混合部署中，使用 Office 365 管理中心将加载项分发给组织中的用户。|
|[SharePoint 目录](publish-task-pane-and-content-add-ins-to-an-add-in-catalog.md)|在本地环境中，用于向组织用户分发加载项。|
|[AppSource](https://docs.microsoft.com/office/dev/store/submit-to-the-office-store)|用于向用户公开分发加载项。|
|[Exchange 服务器](#outlook-add-in-deployment)|在本地或在线环境中，用于向用户分发 Outlook 加载项。|
|[网络共享](../testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins.md)|在网络上的 Windows 计算机中（要在其中托管加载项），转到要用作共享文件夹目录的文件夹的父文件夹或驱动器号。|

> [!NOTE]
> 如果计划将加载项[发布](../publish/publish.md)到 AppSource 并适用于 Office 体验，请务必遵循 [AppSource 验证策略](https://docs.microsoft.com/office/dev/store/validation-policies)。例如，加载项必须适用于支持已定义方法的所有平台，才能通过验证（有关详细信息，请参阅[第 4.12 部分](https://docs.microsoft.com/office/dev/store/validation-policies#4-apps-and-add-ins-behave-predictably)以及 [Office 加载项主机和可用性](../overview/office-add-in-availability.md)页面）。

## <a name="deployment-options-by-office-host"></a>Office 主机提供的部署选项

可用的部署选项具体取决于你定位的 Office 主机以及所创建的加载项的类型。

### <a name="deployment-options-for-word-excel-and-powerpoint-add-ins"></a>Word、Excel 和 PowerPoint 加载项的部署选项

| 扩展点 | 旁加载 | Office 365 管理中心 |AppSource   | SharePoint 目录\* |
|:----------------|:-----------:|:-----------------------:|:----------:|:--------------------:|
| 内容         | X           | X                       | X          | X                    |
| 任务窗格       | X           | X                       | X          | X                    |
| 命令         | X           | X                       | X          |                      |

* SharePoint 目录不支持 Office for Mac。

### <a name="deployment-options-for-outlook-add-ins"></a>Outlook 外接程序的部署选项

| 扩展点 | 旁加载 | Exchange 服务器 | AppSource    |
|:----------------|:-----------:|:---------------:|:------------:|
| 邮件应用        | X           | X               | X            |
| 命令         | X           | X               | X            |

## <a name="deployment-methods"></a>部署方法

以下各节提供了有关向组织中的用户分发 Office 加载项的最常用部署方法的其他信息。

有关最终用户如何获取、插入和运行加载项的信息，请参阅[开始使用 Office 加载项](https://support.office.com/en-ie/article/Start-using-your-Office-Add-in-82e665c4-6700-4b56-a3f3-ef5441996862?ui=en-US&rs=en-IE&ad=IE)。

### <a name="centralized-deployment-via-the-office-365-admin-center"></a>通过 Office 365 管理中心进行集中部署 

通过 Office 365 管理中心，管理员可以为组织中的用户和组轻松部署 Office 加载项。在管理员通过管理中心部署加载项后，用户可以立即在 Office 应用中使用加载项，而无需进行任何客户端配置。通过集中部署，可以部署内部加载项和 ISV 提供的加载项。

有关详细信息，请参阅[通过 Office 365 管理中心进行集中部署来发布 Office 加载项](centralized-deployment.md)。

### <a name="sharepoint-catalog-deployment"></a>SharePoint 目录部署

SharePoint 加载项目录是特殊网站集，创建后可用于托管 Word、Excel 和 PowerPoint 加载项。由于 SharePoint 目录不支持在清单的 `VersionOverrides` 节点中实现的新加载项功能（包括加载项命令），因此建议尽可能通过管理中心进行集中部署。通过 SharePoint 目录部署的加载项命令默认在任务窗格中打开。

如果要在本地环境中部署外接程序，请使用 SharePoint 目录。有关详细信息，请参阅[将任务窗格和内容外接程序发布到 SharePoint 目录](publish-task-pane-and-content-add-ins-to-an-add-in-catalog.md)。

> [!NOTE]
> SharePoint 目录不支持 Office for Mac。 若要部署 Office 外接程序到 Mac 客户端，您必须将它们提交给 [AppSource](https://docs.microsoft.com/office/dev/store/submit-to-the-office-store)。 

### <a name="outlook-add-in-deployment"></a>Outlook 加载项部署

对于不使用 Azure AD 标识服务的本地和联机环境，可以通过 Exchange 服务器部署 Outlook 外接程序。 

Outlook 外接程序部署需要以下内容：

- Office 365、Exchange Online 或 Exchange Server 2013 或更高版本
- Outlook 2013 或更高版本

若要将加载项分配给租户，请使用 Exchange 管理中心通过文件或 URL 直接上传清单，或从 AppSource 添加加载项。若要将加载项分配给单个用户，必须使用 Exchange PowerShell。有关详细信息，请参阅 TechNet 上的[为组织安装或删除 Outlook 加载项](https://technet.microsoft.com/library/jj943752(v=exchg.150).aspx)。

## <a name="see-also"></a>另请参阅

- [旁加载 Outlook 加载项以供测试](../testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins.md)
- [提交到 AppSource][AppSource]
- [Office 加载项设计指南](../design/add-in-design.md)
- [创建有效的 AppSource 一览](https://docs.microsoft.com/office/dev/store/create-effective-office-store-listings)
- [排查 Office 加载项中的用户错误](../testing/testing-and-troubleshooting.md)

[AppSource]: https://docs.microsoft.com/office/dev/store/submit-to-the-office-store
[Office Add-in host and platform availability]: ../overview/office-add-in-availability
