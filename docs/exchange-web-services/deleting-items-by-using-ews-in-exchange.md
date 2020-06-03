---
title: 使用 Exchange 中的 EWS 删除项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c81e3160-e12b-47e0-b3d6-4be28537f301
description: 了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 通过将项目移动到 "已删除邮件" 文件夹或转储程序来删除项目。
localization_priority: Priority
ms.openlocfilehash: 83317ccd0fa1db64e14df68652489009fea4ea07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456119"
---
# <a name="deleting-items-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 删除项目

了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 通过将项目移动到 "已删除邮件" 文件夹或转储程序来删除项目。
  
您是否曾问自己，在将项目移动到 "已删除邮件" 文件夹之间有什么区别，并将它们移动到转储程序？ 您可能希望了解处理已删除项目的不同选项以及如何在应用程序中实现这些选项。 Exchange Web 服务（EWS）包括用于处理已删除项目的三个选项。 本文将向你表明你可能会遇到的任何有关它们之间的差异的混乱。
  
## <a name="deleting-items---what-are-my-options"></a>删除项目-什么是我的选项？
<a name="bk_DeletingItemsOptions"> </a>

必须先了解以下各项之间的差异，然后才能了解用于删除项目的总体前景：
  
- "已删除邮件" 文件夹-当您删除邮箱中的邮件时，这就是他们要转到的位置。
    
- 转储程序（也称为 "可恢复项目" 文件夹）-当您从邮箱中删除项目时，这就是他们要转到的位置。
    
图1和图2显示了删除过程对邮箱中的项目和文件夹的外观。 

**图1。删除邮箱中的项目的过程**

![此说明显示邮件去向和删除时间。 已删除邮件移动到 "已删除邮件" 文件夹中，然后将其移到 "可恢复的项目" 文件夹中，每个保留策略在过期且被 permantently 删除。](media/Ex_DeleteItems_Source.png)

<br/>

**图2。从邮箱中删除文件夹的过程**

![此说明显示如何将已删除文件夹移动到“已删除邮件”文件夹，从而可以从邮箱中永久删除。](media/Ex_.png)
   
您可以通过三种不同的方式删除项目和文件夹，具体取决于您希望删除的 "永久" 方式。
  
**表1：使用 EWS 删除项目的选项**

|**选项**|**发生的情况**|
|:-----|:-----|
|移动到已删除邮件文件夹  <br/> |这是删除项目的最不永久方法。<br/><br/>这类似于在你的办公桌的回收站中放置一张纸。 如果需要，你可以轻松地获取它。<br/><br/>您可以使用任何实现 "移动到已删除邮件" 文件夹选项的[删除操作](deleting-items-by-using-ews-in-exchange.md#bk_howdoIdeleteitems)来执行此操作。<br/><br/>您还可以使用[MoveItem 操作](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)（ [move （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx)）或[MoveFolder 操作](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)（[文件夹. move （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx)）将项目或文件夹移动到 "已删除邮件" 文件夹中。  <br/> |
|软删除  <br/> |将项目移动到转储程序中的 "删除" 文件夹。<br/><br/>这类似于将回收站清空到 curbside 容器中。 如果需要，仍可以访问该项目，这只是一个更难的方法。  <br/><br/>有关转储程序（也称为 "可恢复的项目" 文件夹）和方案（如电子数据展示或诉讼保留）的详细信息，请参阅 TechNet 上的 "[可恢复的项目" 文件夹](https://technet.microsoft.com/library/ee364755%28v=exchg.150%29.aspx)。<br/><br/>对于以 Exchange 2007 为目标的应用程序，不建议使用软删除。 在 Exchange 2007 中，通过在项目上设置一个位来指示将其在未指定时间移动到转储程序，可以处理软删除。<br/><br/>"软删除" traversals 或搜索通过[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)软删除的项目不受 exchange Online、exchange Online 作为 Office 365 的一部分，以及从 exchange 2010 开始的 exchange 版本。  <br/><br/>**注意**：不能软删除文件夹。           |
|硬删除  <br/> |项目或文件夹将被永久删除。<br/><br/>硬删除的项目放置在转储程序的 "清除" 文件夹中。 这类似于回收卡车清空 curbside 回收容器的情况。 无法从 Outlook 或 Outlook Web App 等电子邮件客户端访问这些项目，除非邮箱中设置了保留，否则会在设定的一段时间后永久删除这些项目。<br/><br/>有关项目保留的详细信息，请参阅[配置已删除邮件的保留和可恢复的项目配额](https://technet.microsoft.com/library/ee364752%28v=exchg.150%29.aspx)一文。<br/><br/>**注意**：文件夹在硬删除时不会放置在 "清除" 文件夹中。 硬删除的文件夹将从邮箱中删除。  |
   
移动到 "已删除邮件" 文件夹和硬删除选项都是事务性的，这意味着在 web 服务调用完成时，项目已移动到 "已删除邮件" 文件夹或转储程序。
  
为了帮助您更好地了解用于存储已删除项目的文件夹生态系统，下图显示了可以包含已删除项目的文件夹的层次结构。 文件夹名称在**DistinguishedFolderIdNameType**架构类型中显示，或在 EWS 托管 API 中的**WellKnownFolderName**枚举中显示。 
  
**图3。包含已删除项目的文件夹的层次结构**

![此图显示文件夹的文件夹层次结构，其中可包含主邮箱和存档邮箱中的已删除邮件。图像中的每个文件夹由其可分辨的文件夹名称表示。](media/Ex_FolderHierarchyDeletedItems.png)
  
**表2：包含已删除项目的文件夹**

|**文件夹名**|**引入版本**|**说明**|
|:-----|:-----|:-----|
|deleteditems  <br/> |Exchange 2007  <br/> |默认的 "已删除邮件" 文件夹。 项目将保留在此文件夹中，直到它们软或硬删除，或者超过保留期。 然后，将它们移动到转储程序中的文件夹。 已删除的文件夹放在 "已删除邮件" 文件夹中，当它们是软或硬删除的，它们将从邮箱中永久删除且不可恢复。  <br/> |
|recoverableitemsroot  <br/> |Exchange 2010  <br/> |转储程序或 "可恢复的项目" 文件夹的根。 转储程序访问在 Exchange 2010 中是在 EWS 中实现的。 此文件夹的显示名称是 "可恢复的项目"。  <br/> |
|recoverableitemsdeletions  <br/> |Exchange 2010  <br/> |邮箱的主转储程序文件夹。 从 "已删除邮件" 文件夹中的保留策略移动的软删除项目和项目放置在此文件夹中。 此文件夹的显示名称为 "删除"。  <br/> |
|recoverableitemsversions  <br/> |Exchange 2010  <br/> |项目的较旧版本的存储位置。 项目的旧版本在更新项目时创建。 草稿项目版本不会保存到此文件夹中。 此文件夹的显示名称为 "版本"。  <br/> |
|recoverableitemspurges  <br/> |Exchange 2010  <br/> |存储从 "删除" 文件夹中删除的项目的位置。 所有存储硬删除项目都将移到此文件夹。 此文件夹的显示名称为 "清除"。  <br/> |
|archiveddeletedtitems  <br/> |Exchange 2010  <br/> |存档邮箱的默认 "已删除邮件" 文件夹。  <br/> |
|archiverecoverablesitemsroot  <br/> |Exchange 2010  <br/> |存档邮箱的根转储程序文件夹。 软删除的已存档项目将移至此文件夹中的子文件夹。  <br/> |
|archiverecoverableitemsdeletions  <br/> |Exchange 2010  <br/> |存档邮箱的主转储程序文件夹。 移动到转储程序的存档项目放置在此处。  <br/> |
|archiverecoverableitemsversions  <br/> |Exchange 2010  <br/> |存档项目的较旧版本的存储位置。  <br/> |
|archiverecoverableitemspurges  <br/> |Exchange 2010  <br/> |从转储程序中的 "存档删除" 文件夹中硬删除的项目存储。 所有存储硬删除的存档项目都将移到此文件夹。  <br/> |
   
## <a name="how-do-i-delete-items"></a>如何删除项目？
<a name="bk_howdoIdeleteitems"> </a>

使用下列命令之一来指示是将项目移动到 "已删除邮件" 文件夹，还是执行软删除或硬删除：
  
- **DisposalType**简单类型（如果您使用 EWS 访问 Exchange）。 
    
- [DeleteMode 枚举](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx)（如果使用 EWS 托管 API）。
    
您可以使用许多不同的 EWS 操作或 EWS 托管 API 方法从邮箱中删除项目和文件夹。
  
**表3：用于删除项目的 EWS 操作和 EWS 托管的 API 方法**

|**EWS 操作**|**EWS 托管的 API 方法**|**引入版本**|**功能**|
|:-----|:-----|:-----|:-----|
|[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |[文件夹. Delete 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |从邮箱中删除文件夹。 使用 EWS，可以批量删除文件夹。 使用 EWS 托管 API，您只能删除每个调用的单个文件夹。  <br/> |
|[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Item. Delete 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)<br/><br/>[ExchangeService 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.exchangeservice.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |删除邮箱中的项目。  <br/> |
|[EmptyFolder 操作](https://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <br/> |[Folder. 空方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.folder.empty%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |删除文件夹中的所有项目，也可以选择删除文件夹中的所有子文件夹。  <br/> |
|[ApplyConversationAction 操作](https://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |[EnableAlwaysDeleteItems 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx)<br/><br/>[DeleteItems 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.conversation.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |对对话中的电子邮件设置删除处理操作，以便将其删除。  <br/> |
|[DeleteUserConfiguration 操作](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration 方法](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |删除一个与文件夹相关联的项目，并将其移动到转储程序。  <br/> |
|[CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |[约会. Accept 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.accept%28v=exchg.80%29.aspx) <br/><br/>[AcceptTentatively 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[CancelMeeting 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)<br/><br/>[约会：拒绝](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.decline%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.accept%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.decline%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |无论何时发送会议请求的响应或在约会上设置响应，都会将项目间接移动到 "已删除邮件" 文件夹。<br/><br/>此操作上未设置删除类型。 当服务成功处理响应对象时，会将会议邮件移至 "已删除邮件" 文件夹。  <br/> |
   
您还可以使用收件箱规则将项目移动到 "已删除邮件" 文件夹。 例如，您可以创建具有 "删除" 操作的[规则](inbox-management-and-ews-in-exchange.md)。 
  
有关删除项目的几点注意事项：
  
- 删除定期项目的事件不会触发移动到 "已删除邮件" 文件夹或转储程序。 这将导致对定期系列定期主项目的更新。
    
- 您不能从邮箱中删除默认文件夹。
    
- 避免删除会议或会议邮件，如会议请求和会议更新。 而是使用 response 对象来响应这些项目。 这样一来，将更新关联的日历项目以反映响应者或组织者的操作。
    
- 将项目移动到 "已删除邮件" 或 "删除内容" 文件夹中时，不会更新项目的更改密钥。
    
- 如果对项目执行硬删除，然后调用[SyncFolderHierarchy 操作](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)或[SYNCFOLDERHIERARCHY](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) EWS 托管 API 方法，或[SyncFolderItems 操作](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)或[SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)方法，则将返回 "**删除**更改" 条目。 如果将项目移动到 "已删除邮件" 文件夹中，则会返回 "**更新**更改" 条目。 这是因为项目或文件夹将具有新的[ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)属性值。 若要了解同步已删除项目属于方案的一部分，请[阅读有关同步的详细信息](mailbox-synchronization-and-ews-in-exchange.md)。 
    
## <a name="find-out-more-about-deleting-items"></a>查找有关删除项目的详细信息
<a name="findoutmore"> </a>

- [Exchange 中有关与 EWS 删除相关邮箱事件的拉取通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中的与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 中的文件夹和项目](folders-and-items-in-ews-in-exchange.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)    
- ["可恢复的项目" 文件夹](https://technet.microsoft.com/library/ee364755.aspx)    
- [Exchange Server 2010 中的单个项目恢复](https://blogs.technet.com/b/exchange/archive/2009/09/25/3408389.aspx#_Single_Item_Recovery)    
- [Exchange 2013：以编程方式从 Exchange 服务器中删除定期系列](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-a-e1c7b89d)    
- [Exchange 2013：以编程方式从 Exchange 服务器上的帐户中删除任务](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-tasks-13824637)    
- [Exchange 2013：以编程方式清空 Exchange 服务器上的文件夹](https://code.msdn.microsoft.com/exchange/Exchange-2013-Empty-6487df37)    
- [Exchange 2013：以编程方式从 Exchange 服务器删除文件夹](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-aa1a5823)    
- [Exchange 2013：以编程方式从 Exchange 服务器删除多个项目](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-many-064f8760)    
- [Exchange 2013：以编程方式从 Exchange 服务器删除联系人](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-3b8b0640)    
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)    
- [使用 Exchange 中的 EWS 管理持久应用程序设置](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    

