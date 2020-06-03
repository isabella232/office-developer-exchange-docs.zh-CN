---
title: Exchange 中的 EWS 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: 查找有关 Exchange 中可用的 EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 143903d9198a7e31e876adcbbb336df34ecf01fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526121"
---
# <a name="ews-operations-in-exchange"></a>Exchange 中的 EWS 操作

查找有关 Exchange 中可用的 EWS 操作的信息。
  
Exchange Web 服务（EWS）提供了许多可让您访问 Exchange 存储中的信息的操作。 本节中的文章提供有关 EWS 操作的请求、响应和错误响应消息的整体结构的信息，以及每个操作的 XML 示例。 它们提供在客户端和服务器之间发送的邮件结构的概述。 您可以使用此信息来调试邮件结构，并查找有关在 EWS 请求中可以执行的操作的信息。 有关 XML 结构表示的内容的详细信息，请参阅- [EWS xml 元素在 Exchange 中](ews-xml-elements-in-exchange.md)。
  
所有 EWS 功能都与架构的一个版本相关联。 Exchange Server 或 Exchange Online 的新版本中引入了新的 EWS 架构版本。 [RequestServerVersion](requestserverversion.md)元素包含一个**version**属性，该属性将服务器版本映射到架构版本。 本文提供有关每个操作的引入时间的信息。 操作中的特定功能可能需要更高版本的服务。 已对版本化架构进行了实现，以便针对较旧版本的 EWS 设计的客户端将在新版本的 EWS 中运行。 
  
这些操作可面向为您的邮箱服务的 EWS 终结点。 您可以使用结构中类似于 http:///EWS/的 URL 浏览到 EWS 终结点 <clientaccessserver> ，其中 <clientaccessserver> 是为您的邮箱服务的 Exchange 客户端访问服务器。 您可以使用自动发现获取服务于您的邮箱的客户端访问服务器的 URL。 有关自动发现的详细信息，请参阅[Exchange 的自动发现](../exchange-web-services/autodiscover-for-exchange.md)。
  
## <a name="ediscovery-operations"></a>电子数据展示操作
<a name="bk_eDiscovery"> </a>

电子数据展示操作提供了用于法律保留的搜索操作，并可识别在发现搜索结果中无法编制索引和返回的邮箱数据。
  
下表列出了电子数据展示操作。
  
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

Exchange 邮箱数据操作使客户端能够处理和组织项目、文件夹和附件，以及不明确的名称解析和通讯组列表扩展。 Exchange 邮箱数据操作包括项目、文件夹、附件和实用工具操作。
  
下表列出了 Exchange 邮箱数据操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[ArchiveItem 操作](archiveitem-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateItem 操作](createitem-operation.md) <br/> |Exchange 2007  <br/> |
|[CopyItem 操作](copyitem-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteItem 操作](deleteitem-operation.md) <br/> |Exchange 2007  <br/> |
|[FindItem 操作](finditem-operation.md) <br/> |Exchange 2007  <br/> |
|[GetItem 操作](getitem-operation.md) <br/> |Exchange 2007  <br/> |
|[MarkAllItemsAsRead 操作](markallitemsasread-operation.md) <br/> |Exchange 2013  <br/> |
|[MoveItem 操作](moveitem-operation.md) <br/> |Exchange 2007  <br/> |
|[SendItem 操作](senditem-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateItem 操作](updateitem-operation.md) <br/> |Exchange 2007  <br/> |
   
下表列出了 Exchange 邮箱数据文件夹操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateFolder 操作](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[CreateFolderPath 操作](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateManagedFolder 操作](createmanagedfolder-operation.md) <br/> |Exchange 2007。 此功能已在从 Exchange 2010 开始的 Exchange 版本中 deemphasized。 有关如何迁移到使用保留标记和邮件记录管理策略的详细信息，请参阅[从托管文件夹迁移](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx)。  <br/> |
|[CopyFolder 操作](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteFolder 操作](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[EmptyFolder 操作](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[FindFolder 操作](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[GetFolder 操作](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[MoveFolder 操作](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateFolder 操作](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
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
|[ApplyConversationAction 操作](applyconversationaction-operation.md) <br/> |Exchange 2010 Service Pack 1 （SP1）  <br/> |
|[FindConversation 操作](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[GetConversationItems 操作](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
下表列出了 Exchange 邮箱数据实用程序操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[ConvertId 操作](convertid-operation.md) <br/> |Exchange 2007 Service Pack 1  <br/> |
|[ExpandDL 操作](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[GetUserPhoto 操作](getuserphoto-operation.md) <br/> |Exchange 2013。 此操作同时具有 REST 和 SOAP 实现。  <br/> |
|[MarkAsJunk 操作](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[ResolveNames 操作](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="availability-operations"></a>可用性操作
<a name="bk_Availability"> </a>

可用性操作通过提供更安全、最新且丰富的忙/闲信息来改进日历和忙/闲共享体验。 闲/忙数据是安排会议的关键因素。 可用性操作为有效的日程安排提供了可靠的基础。 
  
下表列出了可用性操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetUserAvailability 操作](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[GetRoomLists 操作](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[GetRooms 操作](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserOofSettings 操作](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[SetUserOofSettings 操作](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="bulk-transfer-operations"></a>批量转移操作
<a name="bk_bulk_transfer"> </a>

批量传输操作使客户端能够将邮件流入或传出邮箱。 
  
下表列出批量转移操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[UploadItems 操作](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[ExportItems 操作](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="delegate-management-operations"></a>委派管理操作
<a name="bk_delegate_management"> </a>

代理管理操作使客户端能够在其邮箱中添加、获取、更新和删除委派。 
  
下表列出了代理管理操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[AddDelegate 操作](adddelegate-operation.md) <br/> |Exchange 2007 Service Pack 1 （SP1）  <br/> |
|[GetDelegate 操作](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[UpdateDelegate 操作](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[RemoveDelegate 操作](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## <a name="inbox-rules-operations"></a>收件箱规则操作
<a name="bk_inbox_rules"> </a>

"收件箱规则" 操作使客户端可以获取收件箱规则并更新服务器上的邮件。 收件箱规则是条件和关联操作的集合，使客户端能够在邮件传递到文件夹时自动对邮件进行组织、分类和操作。 
  
下表列出了收件箱规则操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetInboxRules 操作](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[UpdateInboxRules 操作](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="mail-app-management-operations"></a>邮件应用程序管理操作
<a name="bk_mail_apps"> </a>

邮件应用程序管理操作使您能够管理 Outlook 的邮件应用程序。 您可以使用这些操作来安装、卸载、禁用和获取适用于 Outlook Web App 和 Outlook 2013 的邮件应用程序的相关信息。
  
下表列出了邮件应用程序管理操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[DisableApp 操作](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[Getappmanifests 已操作](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppMarketplaceUrl 操作](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[GetClientAccessToken 操作](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[InstallApp 操作](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[UninstallApp 操作](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="mail-tips-operation"></a>邮件提示操作
<a name="bk_mail_tips"> </a>

通过邮件提示操作，客户端可以在作者撰写邮件时向服务器请求有关收件人邮箱的信息。 下表列出了邮件提示操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetMailTips 操作](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="message-tracking-operations"></a>邮件跟踪操作
<a name="bk_message_tracking"> </a>

邮件跟踪操作使客户端能够查找符合指定条件的邮件，并在邮件跟踪报告中获取有关每封邮件的详细跟踪信息。 
  
下表列出了邮件跟踪操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="notification-operations"></a>通知操作
<a name="bk_notification"> </a>

通知操作会将与项目和文件夹相关联的事件的客户端应用程序通知到指定的邮箱。 订阅模型可以是基于推送、基于请求的，也可以是基于流的。 
  
下表列出了通知操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetEvents 操作](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[GetStreamingEvents 操作](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[订阅操作](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[取消订阅操作](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="persona-operations"></a>角色操作
<a name="bk_personas"> </a>

角色操作提供了一个接口，用于查找和获取有关链接的联系人的信息。 下表列出了角色操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[FindPeople 操作](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[GetPersona 操作](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="retention-policy-operation"></a>保留策略操作
<a name="bk_retention_policy"> </a>

保留策略操作提供了链接到用户的保留策略的所有保留标记的列表。 
  
下表列出了保留策略操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetUserRetentionPolicyTags 操作](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="service-configuration-operation"></a>服务配置操作
<a name="bk_service_config"> </a>

服务配置操作使客户端能够获取统一消息、保护规则、策略提示和邮件提示服务的配置信息。 
  
下表列出了服务配置操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetServiceConfiguration 操作](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="sharing-operations"></a>共享操作
<a name="bk_sharing"> </a>

共享操作使客户端可以共享日历数据和联系人数据。 
  
下表列出了共享操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[CreateItem （AcceptSharingInvitation）](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010。 尽管**CreateItem**操作适用于所有的 EWS 版本，但**AcceptSharingInvitation**响应对象仅适用于从 Exchange 2010 开始的 EXCHANGE 版本中的 EWS。  <br/> |
|[GetSharingFolder 操作](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[GetSharingMetadata 操作](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[RefreshSharingFolder 操作](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="synchronization-operations"></a>同步操作
<a name="bk_synchronization"> </a>

同步操作提供用户文件夹和项目的单向同步缓存副本。 
  
下表列出了同步操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[SyncFolderItems 操作](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="time-zone-operation"></a>时区操作
<a name="bk_timezone"> </a>

时区操作使客户端可以获取服务器支持的时区定义的列表。 
  
下表列出了时区操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[GetServerTimeZones 操作](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="unified-messaging-operations"></a>统一消息操作
<a name="bk_um"> </a>

统一消息操作使客户端能够读取有关统一消息属性的信息，并通过电话播放语音邮件消息。 
  
下表列出了统一消息操作。
  
|**操作名称**|**引入版本**|
|:-----|:-----|
|[DisconnectPhoneCall 操作](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[GetPhoneCallInformation 操作](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[PlayOnPhone 操作（EWS）](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
使用[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)可获取邮箱的统一消息配置信息。 对面向 Exchange 2007 的统一消息应用程序使用统一消息 web 服务。 有关详细信息，请参阅[Exchange 统一消息 web 服务参考](unified-messaging-web-service-reference-for-exchange.md)。
  
## <a name="unified-contact-store-operations"></a>统一联系人存储操作
<a name="bk_ucs"> </a>

统一联系人存储跨 Office 产品提供一致的联系人体验，并充当第三方应用程序的集成点以使用同一联系人存储。 它使用户和应用程序能够存储、管理和访问联系人信息，并使其在 Lync、Exchange 2013、Outlook、Outlook Web App 和任何其他实现对统一联系人存储的访问权限的应用程序之间全局可用。 Exchange 是统一联系人存储区体验的内容存储区。
  
下表列出了统一的联系人存储操作。
  
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

用户配置操作使客户端能够创建、删除、获取和更新用户配置信息。 
  
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
    

