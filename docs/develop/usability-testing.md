---
title: Office 加载项的可用性测试
description: ''
ms.date: 01/23/2018
ms.openlocfilehash: 0c90cc4e573d24f9c7c4e5c4f6a77853ec9fc93e
ms.sourcegitcommit: 30435939ab8b8504c3dbfc62fd29ec6b0f1a7d22
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2018
ms.locfileid: "23945602"
---
# <a name="usability-testing-for-office-add-ins"></a>Office 加载项的可用性测试

出色的外接程序设计会考虑到用户行为。因为自己的预想会影响设计决策，所以务必要通过实际用户测试设计来确保客户可正常使用外接程序。 

可以使用不同方法运行可用性测试。对于许多外接程序开发人员而言，远程、未经审阅的可用性研究最为节省时间且最具有成本效益。一些热门测试服务使其变得简单；以下是部分示例： 

 - [UserTesting.com](https://www.UserTesting.com)
 - [Optimalworkshop.com](https://www.Optimalworkshop.com)
 - [Userzoom.com](https://www.Userzoom.com)

这些测试服务可帮助你简化测试计划的创建并且不需要寻找参与者或审阅测试。 

你只需五名参与者即可发现设计中的大多数可用性问题。在整个开发周期内定期进行小型测试，以确保产品以用户为中心。

> [!NOTE]
> 建议跨多个平台测试加载项的可用性。若要[将加载项发布到 AppSource](https://docs.microsoft.com/office/dev/store/submit-to-the-office-store)，加载项必须适用于[支持已定义方法的所有平台](../overview/office-add-in-availability.md)。

## <a name="1---sign-up-for-a-testing-service"></a>1. 注册测试服务

有关详细信息，请参阅[选择在线工具进行不受监管的远程用户测试](https://www.nngroup.com/articles/unmoderated-user-testing-tools/)。

## <a name="2-develop-your-research-questions"></a>2.制定研究问题
 
研究问题定义研究的目标并指导测试计划。这些问题将帮助你确定要招募的参与者及其要执行的任务。将研究问题尽可能地具体化。还可以尽量回答较为宽泛的问题。
 
以下是研究问题的一些示例：
  
**具体**  

 - 用户是否注意到了登陆页面上的“免费试用版”链接？
 - 用户将内容从外接程序插入他们的文档时，用户是否知道内容在文档何处插入？

**宽泛**  

 - 用户在我们的外接程序中遇到的最大问题是什么？
 - 用户在单击命令栏中的图标前是否了解他们的含义？
 - 用户能否轻松地找到设置菜单？

获取从发现外接程序到安装并使用外接程序的整个用户操作体验的相关数据至关重要。考虑可解决外接程序用户体验以下方面的研究问题：
 
 - 在 AppSource 中查找加载项
 - 选择安装加载项
 - 初次运行体验
 - 功能区命令
 - 外接程序 UI
 - 外接程序如何与 Office 应用程序的文档空间交互
 - 用户对任意内容插入流的掌控程度如何

有关详细信息，请参阅[编写有效问题](http://help.usertesting.com/customer/en/portal/articles/2077663-writing-effective-questions)。
 
## <a name="3-identify-participants-to-target"></a>3.确定所要面向的参与者
 
通过远程测试服务，你可以控制测试参与者的许多特性。认真考虑想要将哪类用户确定为目标。在数据收集的早期阶段，最好招募各种类型的参与者以识别出较为显著的可用性问题。后面可以选择将类似高级 Office 用户、特定职业或特定年龄段的组确定为目标。
 
## <a name="4-create-the-participant-screener"></a>4.创建参与者筛选器
 
筛选程序是将向潜在测试参与者提供的问题和要求集，以对其进行测试筛选。请注意 UserTesting.com 等服务的参与者参加测试是想要获得经济收益。如果想要将特定用户从测试排除，那么在筛选程序中加入技巧性问题是个不错的主意。 
 
例如，想要找出熟悉 GitHub 的参与者，要筛选出对自己进行了不当描述的用户，包括可能的答案列表中的不实之处。

**熟悉下面哪些源代码存储库？**  
 a. SourceShelf  [*拒绝*]  
 b. CodeContainer  [*拒绝*]  
 c. GitHub  [*必选*]  
 d. BitBucket  [*可选*]  
 e. CloudForge  [*可选*]  

如果计划测试外接程序的实时生成，以下问题可以筛选出可以执行此任务的用户。 

**此测试需要具有最新版本的 Microsoft PowerPoint。您是否有最新版本的 PowerPoint？**  
 a. 是 [*必选*]  
 b. 否 [*拒绝*]  
 c. 不知道 [*拒绝*]  

**此测试要求安装适用于 PowerPoint 2016 的免费外接程序，并创建免费帐户以进行使用。是否愿意安装外接程序并创建免费帐户？**  
 a. 是 [*必选*]  
 b. 否 [*拒绝*]  

有关详细信息，请参阅[筛选器问题最佳做法](http://help.usertesting.com/customer/en/portal/articles/2077835-screener-question-best-practices)。
 
## <a name="5-create-tasks-and-questions-for-participants"></a>5.创建针对参与者的任务和问题
 
尝试对要测试的内容设置优先级，以便限制针对参与者的任务和问题数量。一些服务仅在特定时间内向参与者付费，你需要确保不会超过该时间。

尽可能地尝试观察参与者行为，而不是向其提问。如果需要询问其行为，询问参与者过去做过什么，而不是询问其在某个场景下会做什么。这样提供的结果往往更为可靠。
 
未经审阅的测试的主要挑战在于确保参与者了解你的任务和方案。你的指示应*简洁明了*。不可避免的是，如果可能存在混淆，则某些人会感到困惑。 

在测试期间的任何给定时刻，都不要假设用户会位于其应位于的屏幕上。考虑告诉用户要开始下一个任务他们需要位于哪个屏幕。 

有关详细信息，请参阅[编写出色任务](http://help.usertesting.com/customer/en/portal/articles/2077824-writing-great-tasks)。

## <a name="6-create-a-prototype-to-match-the-tasks-and-questions"></a>6.创建用于匹配任务和问题的原型
 
可以测试实时外接程序，或者可以测试原型。注意，如果要测试实时外接程序，则需要筛选出已安装 Office 2016、愿意安装外接程序且愿意注册帐户的参与者（除非你具有可以向参与者提供的登录凭据）。然后需要确保他们成功安装外接程序。 

通常，逐步指导用户如何安装外接程序需要大约 5 分钟。以下是简洁明了的安装步骤示例。请根据测试的具体情况调整步骤。

**请使用以下说明安装适用于 PowerPoint 2016 的外接程序（在此处插入外接程序名称）：** 

1. 打开 Microsoft PowerPoint 2016。
2. 选择“**空白演示文稿**”。
3. 转到“**插入 > 我的外接程序**”。
5. 在弹出窗口中，选择“**应用商店**”。
6. 在搜索框中键入（外接程序名称）。
7. 选择（外接程序名称）。
8. 花费一些时间查看“应用商店”页面以熟悉外接程序。
9. 选择“**添加**”安装外接程序。

可以以任意基本的交互和外观一致性来测试原型。对于更为复杂的链接和交互性，请考虑使用 [InVision](https://www.invisionapp.com) 等原型制作工具。如果只想测试静态屏幕，可以在线托管图像并向参与者发送相应的 URL，或向其提供指向在线 PowerPoint 演示文稿的链接。 

## <a name="7-run-a-pilot-test"></a>7.运行试点测试

正确设置原型和任务/问题列表可能会比较困难。用户可能会对任务感到疑惑，或者对原型不知所措。应通过 1-3 名用户运行试点测试来解决测试格式存在的难以避免的问题。这将有助于确保问题清楚明了、原型得到正确设置并捕获所寻找的数据类型。

## <a name="8-run-the-test"></a>8.运行测试

指令进行测试后，参与者完成测试后你将获得电子邮件通知。除非你将特定参与者组确定为目标，否则测试通常会在数小时内完成。

## <a name="9-analyze-results"></a>9.分析结果

在这一部分中，你将尝试分析所收集到的数据。在观看测试视频时，记录用户遇到的问题和成功之处。避免尝试在查看所有结果后才解释数据的含义。 

单个参与者具有可用性问题不足以作为更改设计的依据。两个或更多参与者遇到同一问题则表明普通人群中的其他用户也会遇到此问题。

通常，要谨慎对待使用数据作出结论的方式。不要陷入尝试将数据匹配特定叙述的困境；对数据实际证明、驳斥或者无法提供任何相关见解的内容实事求是。保持开放的心态；用户行为经常会违背设计人员的预期。
 

## <a name="see-also"></a>另请参阅
 
 - [如何执行可用性测试](http://whatpixel.com/howto-conduct-usability-testing/)  
 - [最佳实践](http://help.usertesting.com/customer/en/portal/articles/1680726-best-practices)  
 - [最小化偏差](http://downloads.usertesting.com/white_papers/TipSheet_MinimizingBias.pdf)  
