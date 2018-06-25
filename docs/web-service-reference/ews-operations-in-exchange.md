---
title: Exchange 中的 EWS 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: 查找有关可在 Exchange 中的 EWS 操作的信息。
ms.openlocfilehash: c56c3be746138cec251836fcb61ee3738d168869
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754192"
---
# <a name="ews-operations-in-exchange"></a>Exchange 中的 EWS 操作

查找有关可在 Exchange 中的 EWS 操作的信息。
  
Exchange Web Services (EWS) 提供了使您能够从 Exchange 存储中访问信息的多个操作。 本节中的文章提供有关请求、 响应和错误响应消息 EWS 操作，以及对于每个操作的 XML 示例的总体结构的信息。 它们提供客户端和服务器之间发送的消息结构的概述。 调试消息结构并查找 EWS 请求中可以实现的功能的信息，您可以使用此信息。 有关详细信息哪些 XML 结构表示，请参阅- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)。
  
EWS 的所有功能都相关联的架构的版本。 在 Exchange 服务器或 Exchange Online 的新版本中引入新 EWS 架构版本。 [RequestServerVersion](requestserverversion.md)元素包含**版本**属性映射到的架构版本的服务器版本。 本文提供有关每个操作引入时信息。 操作中的特定功能可能需要更高版本的服务。 以便旨在针对 EWS 旧版本的客户端将使用新版本的 EWS 实现版本控制的架构。 
  
这些操作可以目标 services 您的邮箱的 EWS 终结点。 您可以通过使用在结构类似于 http:// URL 浏览到 EWS 终结点<clientaccessserver>.com/ews/exchange.asmx，其中<clientaccessserver>是 services 您的邮箱的 Exchange 客户端访问服务器。 您可以使用自动发现服务邮箱的客户端访问服务器获取 URL。 有关自动发现的详细信息，请参阅[exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)。
  
## <a name="ediscovery-operations"></a>电子数据展示操作
<a name="bk_eDiscovery"> </a>

电子数据展示操作提供的法律保留项搜索操作，并确定无法编制索引和发现搜索结果中返回的邮箱数据。
  
下表列出的电子数据展示操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration 操作](getdiscoverysearchconfiguration-operation.md) <br/> |Exchange 2013  <br/> |
|[GetHoldOnMailboxes 操作](getholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemDetails 操作](getnonindexableitemdetails-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemStatistics 操作](getnonindexableitemstatistics-operation.md) <br/> |Exchange 2013  <br/> |
|[GetSearchableMailboxes 操作](getsearchablemailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SearchMailboxes 操作](searchmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="exchange-mailbox-data-operations"></a>Exchange 邮箱数据操作
<a name="bk_Exchange_mailbox_data"> </a>

Exchange 邮箱数据操作使客户端处理和组织项目、 文件夹和附件，以及模糊名称解析和通讯组列表扩展。 Exchange 邮箱数据操作包括项目、 文件夹、 附件和实用程序操作。
  
下表列出了 Exchange 邮箱数据操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[ArchiveItem 操作](archiveitem-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateItem 操作](createitem-operation.md) <br/> |Exchange 2007  <br/> |
|[CopyItem 操作](copyitem-operation.md) <br/> |Exchange 2007  <br/> |
|[删除项操作](deleteitem-operation.md) <br/> |Exchange 2007  <br/> |
|[FindItem 操作](finditem-operation.md) <br/> |Exchange 2007  <br/> |
|[GetItem 操作](getitem-operation.md) <br/> |Exchange 2007  <br/> |
|[MarkAllItemsAsRead 操作](markallitemsasread-operation.md) <br/> |Exchange 2013  <br/> |
|[MoveItem 操作](moveitem-operation.md) <br/> |Exchange 2007  <br/> |
|[SendItem 操作](senditem-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateItem 操作](updateitem-operation.md) <br/> |Exchange 2007  <br/> |
   
下表列出了 Exchange 邮箱数据文件夹操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateFolder Operation](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[CreateFolderPath 操作](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateManagedFolder 操作](createmanagedfolder-operation.md) <br/> |Exchange 2007。 此功能具有已 deemphasized 中启动与 Exchange 2010 的 Exchange 版本。 有关如何迁移到用于保留标记和策略邮件记录管理的详细信息，请参阅[从托管文件夹迁移](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.141%29.aspx)。  <br/> |
|[CopyFolder 操作](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteFolder 操作](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[EmptyFolder 操作](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[FindFolder Operation](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[GetFolder Operation](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[MoveFolder 操作](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateFolder Operation](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
下表列出了 Exchange 邮箱数据附件操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateAttachment 操作](createattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[GetAttachment 操作](getattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteAttachment 操作](deleteattachment-operation.md) <br/> |Exchange 2007  <br/> |
   
下表列出了 Exchange 邮箱提醒操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetReminders 操作](getreminders-operation.md) <br/> |Exchange 2013  <br/> |
|[PerformReminderAction 操作](performreminderaction-operation.md) <br/> |Exchange 2013  <br/> |
   
下表列出了 Exchange 邮箱数据对话操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[ApplyConversationAction 操作](applyconversationaction-operation.md) <br/> |Exchange 2010 Service Pack 1 (SP1)  <br/> |
|[FindConversation Operation](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[GetConversationItems 操作](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
下表列出了 Exchange 邮箱数据实用程序操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[ConvertId 操作](convertid-operation.md) <br/> |Exchange 2007 Service Pack 1  <br/> |
|[ExpandDL 操作](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[GetUserPhoto 操作](getuserphoto-operation.md) <br/> |Exchange 2013。 此操作具有 REST 和 SOAP 实现。  <br/> |
|[MarkAsJunk 操作](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[ResolveNames 操作](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="availability-operations"></a>可用性操作
<a name="bk_Availability"> </a>

可用性操作改进的日历和忙/闲共享提供了更多安全、 最新的且丰富忙/闲信息的体验。 忙/闲数据是安排会议的关键组成部分。 可用性操作提供有效安排的可靠基础。 
  
下表列出了可用性操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetUserAvailability 操作](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[GetRoomLists 操作](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[GetRooms 操作](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserOofSettings 操作](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[SetUserOofSettings 操作](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="bulk-transfer-operations"></a>批量传输操作
<a name="bk_bulk_transfer"> </a>

批量传输操作使流项目的客户端和注销邮箱。 
  
下表列出了批量传输操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[UploadItems 操作](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[ExportItems 操作](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="delegate-management-operations"></a>委派管理操作
<a name="bk_delegate_management"> </a>

委托管理操作使客户端可以添加、 获取、 更新和删除其邮箱的代理人。 
  
下表列出了委托管理操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[AddDelegate 操作](adddelegate-operation.md) <br/> |Exchange 2007 Service Pack 1 (SP1)  <br/> |
|[GetDelegate 操作](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[UpdateDelegate 操作](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[RemoveDelegate 操作](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## <a name="inbox-rules-operations"></a>收件箱规则操作
<a name="bk_inbox_rules"> </a>

收件箱规则操作使客户端获取收件箱规则和更新这些服务器上的邮件。 收件箱规则是条件和启用自动组织、 分类和消息传递到文件夹用作邮件客户端中的关联的操作的集合。 
  
下表列出的收件箱规则操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetInboxRules 操作](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[UpdateInboxRules 操作](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="mail-app-management-operations"></a>邮件应用程序管理操作
<a name="bk_mail_apps"> </a>

邮件应用程序管理操作使您能够管理 outlook 邮件应用程序。 您可以使用这些操作来安装、 卸载、 禁用，并获取有关可用于 Outlook Web App 和 Outlook 2013 的邮件应用程序的信息。
  
下表列出了邮件应用程序管理操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[DisableApp 操作](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppManifests 操作](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppMarketplaceUrl 操作](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[GetClientAccessToken 操作](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[InstallApp 操作](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[UninstallApp 操作](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="mail-tips-operation"></a>邮件提示操作
<a name="bk_mail_tips"> </a>

邮件提示操作作者撰写邮件时允许从有关收件人的邮箱服务器请求信息的客户端。 下表列出了邮件提示操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetMailTips 操作](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="message-tracking-operations"></a>邮件跟踪操作
<a name="bk_message_tracking"> </a>

邮件跟踪操作使客户端来查找满足指定的条件的邮件并获取邮件跟踪报告中的每封邮件的详细的跟踪信息。 
  
下表列出的邮件跟踪操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="notification-operations"></a>通知操作
<a name="bk_notification"> </a>

通知操作通知的项目和文件夹与相关联的事件的客户端应用程序指定的邮箱。 订阅模型可以基于推送的、 基于拉或基于流式处理的。 
  
下表列出了通知操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetEvents 操作](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[GetStreamingEvents 操作](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[订阅操作](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[取消操作](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="persona-operations"></a>个人操作
<a name="bk_personas"> </a>

个人操作提供查找和获取有关链接的联系人信息的接口。 下表列出了个人操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[FindPeople 操作](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[GetPersona 操作](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="retention-policy-operation"></a>保留策略操作
<a name="bk_retention_policy"> </a>

保留策略操作提供的所有保留标记链接到用户的保留策略的列表。 
  
下表列出了保留策略操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetUserRetentionPolicyTags 操作](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="service-configuration-operation"></a>服务配置操作
<a name="bk_service_config"> </a>

服务配置操作使客户端若要获取的统一消息、 保护规则、 策略提示和邮件提示服务的配置信息。 
  
下表列出的服务配置操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetServiceConfiguration 操作](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="sharing-operations"></a>共享操作
<a name="bk_sharing"> </a>

共享操作使客户端共享日历数据和联系人数据。 
  
下表列出的共享的操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010。 适用于所有版本的 EWS **CreateItem** operation，尽管**AcceptSharingInvitation** response 对象才适用于 EWS 中启动与 Exchange 2010 的 Exchange 版本。  <br/> |
|[GetSharingFolder 操作](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[GetSharingMetadata 操作](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[RefreshSharingFolder 操作](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="synchronization-operations"></a>同步操作
<a name="bk_synchronization"> </a>

同步操作提供用户的文件夹和项目的单向同步缓存的副本。 
  
下表列出的同步操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[SyncFolderItems 操作](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="time-zone-operation"></a>所在的时区操作
<a name="bk_timezone"> </a>

所在的时区操作使客户端以获取服务器支持的时区定义的列表。 
  
下表列出了所在的时区操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetServerTimeZones 操作](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="unified-messaging-operations"></a>统一的消息操作
<a name="bk_um"> </a>

统一消息操作使客户端读取有关统一消息属性的信息以及通过电话播放语音邮件。 
  
下表列出了统一消息操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[DisconnectPhoneCall 操作](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[GetPhoneCallInformation 操作](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[PlayOnPhone 操作 (EWS)](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
使用[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)获取邮箱的统一消息配置信息。 使用面向 Exchange 2007 的统一消息的应用程序的统一消息 web 服务。 有关详细信息，请参阅[exchange 统一消息 web 服务的引用](unified-messaging-web-service-reference-for-exchange.md)。
  
## <a name="unified-contact-store-operations"></a>统一的联系人存储库操作
<a name="bk_ucs"> </a>

统一联系人存储库跨 Office 产品提供一致的联系人体验，并用作第三方应用程序可以使用相同的联系人存储库的集成点。 使用户和应用程序存储、 管理和访问联系人信息并使其可全局之间 Lync、 Exchange 2013、 Outlook、 Outlook Web App 和实现对统一联系人存储库的访问的任何其他应用程序。 Exchange 的统一联系人存储库体验的内容存储。
  
下表列出了统一联系人存储库操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[AddNewImContactToGroup 操作](addnewimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImContactToGroup 操作](addimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImGroup 操作](addimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddNewTelUriContactToGroup 操作](addnewteluricontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddDistributionGroupToImList 操作](adddistributiongrouptoimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItemList 操作](getimitemlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItems 操作](getimitems-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveContactFromImList 操作](removecontactfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImContactFromGroup 操作](removeimcontactfromgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveDistributionGroupFromImList 操作](removedistributiongroupfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImGroup 操作](removeimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[SetImGroup 操作](setimgroup-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="user-configuration-operations"></a>用户配置操作
<a name="bk_user_config"> </a>

用户配置操作使客户端可以创建、 删除和获取，并更新用户配置信息。 
  
下表列出了用户配置操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateUserConfiguration 操作](createuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[DeleteUserConfiguration 操作](deleteuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserConfiguration 操作](getuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[UpdateUserConfiguration 操作](updateuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
    

