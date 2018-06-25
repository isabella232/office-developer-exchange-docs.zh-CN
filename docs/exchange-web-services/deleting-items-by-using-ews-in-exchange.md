---
title: 使用 EWS 在 Exchange 中删除项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c81e3160-e12b-47e0-b3d6-4be28537f301
description: 了解如何使用 EWS 托管 API 或删除 Exchange 中的 EWS 项可通过将它们移动到已删除邮件文件夹或转储程序。
ms.openlocfilehash: a475ebc6677e5f5003cc790a2d4d2b83c513f309
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752730"
---
# <a name="deleting-items-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange 中删除项

了解如何使用 EWS 托管 API 或删除 Exchange 中的 EWS 项可通过将它们移动到已删除邮件文件夹或转储程序。
  
具有以往任何时候都要求您自己的区别是什么之间将项目移动到已删除邮件文件夹中，并移到转储程序？ 您可能希望了解处理删除项和如何在您的应用程序中实现这些选项的不同选项。 Exchange Web Services (EWS) 包括三个选项的处理删除项目。 本文提供将清除任何混淆情况，您可能必须有关它们之间的差异。
  
## <a name="deleting-items---what-are-my-options"></a>删除项目-我的选项是什么？
<a name="bk_DeletingItemsOptions"> </a>

您可以了解删除项的总体形势之前，请务必识别以下区别：
  
- 已删除邮件文件夹中的删除邮箱中的项时，这是他们在哪里。
    
- 转储程序 （也称为可恢复邮件文件夹）-当您从邮箱中删除项目时，这是他们在哪里。
    
图 1 和 2 显示项和文件夹邮箱中的删除过程的外观。 

**图 1。从邮箱中删除项的过程**

![此插图显示位置项转时被删除。 已删除项目移至已删除邮件文件夹中，然后移至每个保留策略，其中它们的过期时间可并且可删除 permantently 可恢复邮件文件夹。](media/Ex_DeleteItems_Source.png)

<br/>

**图 2。过程的邮箱中删除文件夹**

![此说明显示如何将已删除文件夹移动到“已删除邮件”文件夹，从而可以从邮箱中永久删除。](media/Ex_.png)
   
您可以删除项目和文件夹三种不同方法，具体取决于如何"永久"您想要删除。
  
**表 1： 通过使用 EWS 删除项选项**

|**选项**|**时会发生什么情况**|
|:-----|:-----|
|将移动到已删除邮件文件夹  <br/> |这是最小的永久方式，若要删除项。<br/><br/>这就像您桌面的回收站中放置一张纸。 如果您再次需要可以轻松会获得其情况。<br/><br/>您可以使用实现移动到已删除邮件文件夹选项才能执行此操作的任何[删除操作](deleting-items-by-using-ews-in-exchange.md#bk_howdoIdeleteitems)。<br/><br/>您还可以使用[MoveItem 操作](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)( [Item.Move()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx)) 或[MoveFolder 操作](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)( [Folder.Move()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx)) 移动到已删除邮件文件夹的项目或文件夹。  <br/> |
|软删除  <br/> |项目移动到中的删除文件夹转储程序。<br/><br/>这就像您 curbside 容器到清空回收站。 如果需要仍可以访问的项目，只需有点更加复杂。  <br/><br/>有关详细信息转储程序 （也称为可恢复邮件文件夹） 和方案如电子数据展示或诉讼保留项，请参阅 TechNet 上的[Recoverable Items Folder](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx) 。<br/><br/>软删除 Exchange 2007 的目标不建议用于应用程序。 在 Exchange 2007，软删除的处理有点项上的设置，以指示将移至转储程序在未指定的时间。<br/><br/>在 Exchange Online 中，Exchange Online 作为 Office 365 的一部分和版本的 Exchange 启动与 Exchange 2010 不支持软删除遍历或在已软[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)，通过删除的项的搜索。  <br/><br/>**注意**： 不能软删除文件夹。           |
|硬删除  <br/> |永久删除项目或文件夹。<br/><br/>硬已删除邮件被清除文件夹中放置转储程序。 这就像回收卡车时清空 curbside 回收站容器。 无法从 Outlook 或 Outlook Web App，如电子邮件客户端访问项目，并且没有保留邮箱上设置，除非将设定的时间段后永久删除项目。<br/><br/>您可以阅读更多有关[配置删除项目的保留和可恢复项目配额](http://technet.microsoft.com/en-us/library/ee364752%28v=exchg.150%29.aspx)一文中的项目保留。<br/><br/>**注意**： 硬被删除时的文件夹不放置在清除文件夹中。 从邮箱中删除硬删除文件夹。  |
   
移动到已删除邮件文件夹和硬删除选项是事务性的这意味着，web 服务调用完成时，该项目已移至已删除邮件文件夹或转储程序。
  
为了帮助您更好地了解用于存储已删除的项目的文件夹的生态系统下, 图显示可以包含的文件夹的层次结构中删除项目。 文件夹名称是在**DistinguishedFolderIdNameType**架构类型或在 EWS 托管 API **WellKnownFolderName**枚举中的显示。 
  
**图 3。包含已删除的项目的文件夹层次结构**

![此图显示文件夹的文件夹层次结构，其中可包含主邮箱和存档邮箱中的已删除邮件。图像中的每个文件夹由其可分辨的文件夹名称表示。](media/Ex_FolderHierarchyDeletedItems.png)
  
**表 2： 包含的文件夹中删除项目**

|**文件夹名称**|**引入版本**|**说明**|
|:-----|:-----|:-----|
|DeletedItems  <br/> |Exchange 2007  <br/> |默认删除邮件文件夹中。 直到它们是软或硬-删除或已超出保留期，项目保留在此文件夹中。 然后他们会移动到文件夹中转储程序。 已删除文件夹放置在已删除邮件文件夹中，并且他们何时软或硬-删除，它们从邮箱中永久删除和不可恢复。  <br/> |
|recoverableitemsroot  <br/> |Exchange 2010  <br/> |根目录转储程序，或可恢复邮件文件夹。 在 Exchange 2010 中的 EWS 中已实现转储程序访问。 此文件夹的显示名称是"可恢复项目"。  <br/> |
|recoverableitemsdeletions  <br/> |Exchange 2010  <br/> |主转储程序邮箱的文件夹。 软删除项目和项目的保留策略移动从已删除邮件文件夹位于此文件夹中。 此文件夹的显示名称是"删除"。  <br/> |
|recoverableitemsversions  <br/> |Exchange 2010  <br/> |较旧版本的项目存储在何处。 更新项目时创建一个项目的旧版本。 草稿项目版本不会保存到此文件夹中。 此文件夹的显示名称为"版本"。  <br/> |
|recoverableitemspurges  <br/> |Exchange 2010  <br/> |从删除文件夹中删除的项目存储在何处。 存储硬已删除的所有项目都移至该文件夹中。 此文件夹的显示名称为"清除"。  <br/> |
|archiveddeletedtitems  <br/> |Exchange 2010  <br/> |存档邮箱的默认删除邮件文件夹。  <br/> |
|archiverecoverablesitemsroot  <br/> |Exchange 2010  <br/> |根转储程序存档邮箱的文件夹。 存档的项目的软删除移到此文件夹中的子文件夹。  <br/> |
|archiverecoverableitemsdeletions  <br/> |Exchange 2010  <br/> |主转储程序存档邮箱的文件夹。 项目移动到已存档转储程序放在此处。  <br/> |
|archiverecoverableitemsversions  <br/> |Exchange 2010  <br/> |较旧版本已存档的项目的存储在何处。  <br/> |
|archiverecoverableitemspurges  <br/> |Exchange 2010  <br/> |其中项将被硬删除从存档删除文件夹中的转储程序存储。 硬删除存储的存档的所有项目都移至该文件夹中。  <br/> |
   
## <a name="how-do-i-delete-items"></a>如何删除项目？
<a name="bk_howdoIdeleteitems"> </a>

使用下列任一以指示是否将项目移至已删除邮件文件夹，或执行软删除或硬删除：
  
- 在**DisposalType**简单类型，如果您使用 EWS 访问 Exchange。 
    
- [DeleteMode 枚举](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx)，如果您使用 EWS 托管 API。
    
许多不同的 EWS 操作或 EWS 托管 API 方法可用于从邮箱中删除项目和文件夹。
  
**表 3: EWS 操作和用于删除项的 EWS 托管 API 方法**

|**EWS 操作**|**EWS 托管的 API 方法**|**引入版本**|**它的用途**|
|:-----|:-----|:-----|:-----|
|[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |[Folder.Delete 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |从邮箱中删除文件夹。 使用 EWS，您可以批处理删除文件夹。 使用 EWS 托管 API，您只能删除单个文件夹每个呼叫。  <br/> |
|[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Item.Delete 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)<br/><br/>[ExchangeService.DeleteItems 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.exchangeservice.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |从邮箱中删除项目。  <br/> |
|[EmptyFolder 操作](http://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <br/> |[Folder.Empty 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.folder.empty%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |删除文件夹中的所有项目，并 （可选） 都删除文件夹中的所有子文件夹。  <br/> |
|[ApplyConversationAction 操作](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |[Conversation.EnableAlwaysDeleteItems 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx)<br/><br/>[Conversation.DeleteItems 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.conversation.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |设置删除处理电子邮件对话中的操作，以便被删除。  <br/> |
|[DeleteUserConfiguration 操作](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete 方法](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |删除项关联的文件夹，并将其移转储程序。  <br/> |
|[CreateItem 操作](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |[Appointment.Accept 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.accept%28v=exchg.80%29.aspx) <br/><br/>[Appointment.AcceptTentatively 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[Appointment.CancelMeeting 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)<br/><br/>[Appointment.Decline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.decline%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Accept 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.accept%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.AcceptTentatively 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Decline 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.decline%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |间接到已删除邮件文件夹移动项目发送响应会议请求或约会上设置响应。<br/><br/>删除类型不是设置此操作。 会议邮件移动到已删除邮件文件夹时服务成功处理响应对象。  <br/> |
   
您可以通过使用收件箱规则将项目移至已删除邮件文件夹。 例如，您可以[创建规则](inbox-management-and-ews-in-exchange.md)已删除操作。 
  
有关删除项注意一些事项：
  
- 删除重复项匹配项不会触发移动到已删除邮件文件夹或转储程序。 这将导致更新到定期系列的定期主项目。
    
- 无法从邮箱中删除默认文件夹。
    
- 避免删除会议或会议的邮件，如会议请求和或会议更新。 而是使用响应对象响应这些项。 这种方式，关联的日历项目将更新以反映响应器的或组织者的操作。
    
- 当项目移至已删除邮件或删除文件夹未更新的项目更改密钥。
    
- 如果您执行硬，删除项目，然后调用[SyncFolderHierarchy 操作](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)或[SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) EWS 托管 API 方法或[SyncFolderItems 操作](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)或[SyncFolderItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)方法中，**删除**更改将返回条目。 如果将项目移动到已删除邮件文件夹中，则返回的**更新**更改条目。 这是因为的项目或文件夹将具有新的[ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)属性值。 [了解更多关于同步](mailbox-synchronization-and-ews-in-exchange.md)如果同步已删除项目属于您的方案。 
    
## <a name="find-out-more-about-deleting-items"></a>找出有关删除项的详细信息
<a name="findoutmore"> </a>

- [在 Exchange 拉 EWS 删除相关邮箱事件通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [在 Exchange 处理删除相关 EWS 中的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)    
- [可恢复的项目文件夹](http://technet.microsoft.com/en-us/library/ee364755.aspx)    
- [Exchange Server 2010 中的单个项目恢复](http://blogs.technet.com/b/exchange/archive/2009/09/25/3408389.aspx#_Single_Item_Recovery)    
- [Exchange 2013： 删除定期系列以编程方式从 Exchange 服务器](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-a-e1c7b89d)    
- [Exchange 2013： 从 Exchange 服务器上的帐户中删除任务以编程方式](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-tasks-13824637)    
- [Exchange 2013： 以编程方式清空 Exchange 服务器上的文件夹](http://code.msdn.microsoft.com/exchange/Exchange-2013-Empty-6487df37)    
- [Exchange 2013： 删除文件夹以编程方式从 Exchange 服务器](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-aa1a5823)    
- [Exchange 2013： 删除多个项目以编程方式从 Exchange 服务器](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-many-064f8760)    
- [Exchange 2013： 删除联系人以编程方式从 Exchange 服务器](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-3b8b0640)    
- [删除约会，并在 Exchange 使用 EWS 取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)    
- [在 Exchange 中使用 EWS 管理持久的应用程序设置](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    

