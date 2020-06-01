---
title: ResponseCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 4b84d670-74c9-4d6d-84e7-f0a9f76f0d93
description: ResponseCode 元素提供有关请求的状态信息。
ms.openlocfilehash: 6481272c61aab3dc9aeb2fd988e3544169306f06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457464"
---
# <a name="responsecode"></a>ResponseCode

**ResponseCode**元素提供有关请求的状态信息。 
  
- [ResponseMessage](responsemessage.md) 
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|元素|说明|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | 提供有关响应状态的描述性信息。<br/><br/>  以下是此元素的可能的 XPath 表达式：<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |包含单个[DeleteItem 操作](deleteitem-operation.md)请求的状态和结果。  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |包含单个[SendItem 操作](senditem-operation.md)请求的状态和结果。  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |包含单个[DeleteFolder 操作](deletefolder-operation.md)请求的状态和结果。  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含单个[DeleteAttachment 操作](deleteattachment-operation.md)请求的状态和结果。  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |包含单个[取消订阅操作](unsubscribe-operation.md)请求的状态和结果。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含单个[CreateFolder 操作](createfolder-operation.md)请求的状态和结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含单个[GetFolder 操作](getfolder-operation.md)请求的状态和结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含单个[UpdateFolder 操作](updatefolder-operation.md)请求的状态和结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含单个[MoveFolder 操作](movefolder-operation.md)请求的状态和结果。  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含单个[CopyFolder 操作](copyfolder-operation.md)请求的状态和结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含单个[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求的状态和结果。  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含单个[FindFolder 操作](findfolder-operation.md)请求的状态和结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含单个[CreateItem 操作](createitem-operation.md)请求的状态和结果。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含单个[GetItem 操作](getitem-operation.md)请求的状态和结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含单个[UpdateItem 操作](updateitem-operation.md)请求的状态和结果。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含单个[MoveItem 操作](moveitem-operation.md)请求的状态和结果。  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含单个[CopyItem 操作](copyitem-operation.md)请求的状态和结果。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含单个[CreateAttachment 操作](createattachment-operation.md)请求的状态和结果。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含单个[GetAttachment 操作](getattachment-operation.md)请求的状态和结果。  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含单个[FindItem 操作](finditem-operation.md)请求的状态和结果。  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含[ResolveNames 操作](resolvenames-operation.md)请求的状态和结果。  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含单个[ExpandDL 操作](expanddl-operation.md)请求的状态和结果。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含单个[订阅操作](subscribe-operation.md)请求的状态和结果。  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含单个[GetEvents 操作](getevents-operation.md)请求的状态和结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含单个 SendNotification 操作请求的状态和结果。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)请求的状态和结果。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含[SyncFolderItems 操作](syncfolderitems-operation.md)请求的状态和结果。  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含[ConvertId 操作](convertid-operation.md)请求的状态和结果。  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |包含[AddDelegate 操作](adddelegate-operation.md)请求的状态和结果。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含[GetDelegate 操作](getdelegate-operation.md)请求的状态和结果。  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |包含[RemoveDelegate 操作](removedelegate-operation.md)请求的状态和结果。  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |包含[UpdateDelegate 操作](updatedelegate-operation.md)请求的状态和结果。  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |包含[GetServerTimeZones 操作](getservertimezones-operation.md)请求的状态和结果。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含[GetSharingFolder 操作](getsharingfolder-operation.md)请求的状态和结果。  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |定义对[GetSharingFolder 操作](getsharingfolder-operation.md)请求的响应。  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |包含[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的状态和结果。  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |包含[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的状态和结果。  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |定义对[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的响应。  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |包含[FindConversation 操作](findconversation-operation.md)响应的状态和结果。  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |包含[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的状态和结果。  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |包含单个[EmptyFolder 操作](emptyfolder-operation.md)请求的状态和结果。  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |包含[UpdateInboxRules 操作](updateinboxrules-operation.md)请求的状态和结果。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含[UploadItems 操作](uploaditems-operation.md)请求的状态和结果。  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |包含对[GetInboxRules 操作](getinboxrules-operation.md)* * * * 请求的响应。  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |包含对[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)请求的响应。  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个 text 值。 下表介绍了使用此元素返回的值。
  
|值|说明|
|:-----|:-----|
|NoError  <br/> |请求未发生错误。  <br/> |
|ErrorAccessDenied  <br/> |当呼叫帐户没有执行请求的操作的权限时，将发生此错误。  <br/> |
|ErrorAccessModeSpecified  <br/> |此错误仅供内部使用。 不返回此错误。  <br/> |
|ErrorAccountDisabled  <br/> |如果已禁用 "有问题的帐户"，则会发生此错误。  <br/> |
|ErrorAddDelegatesFailed  <br/> |当无法保存包含已添加委派的列表时，将发生此错误。  <br/> |
|ErrorAddressSpaceNotFound  <br/> |在 Active Directory 数据库中找不到用于跨林可用性的地址空间记录或域名系统（DNS）域名时，将发生此错误。  <br/> |
|ErrorADOperation  <br/> |当操作因 Active Directory 域服务（AD DS）的通信问题而失败时，将发生此错误。  <br/> |
|ErrorADSessionFilter  <br/> |**ResolveNames**操作请求指定无效的名称时，将返回此错误。  <br/> |
|ErrorADUnavailable  <br/> |当 AD DS 不可用时，将发生此错误。 请稍后重试你的请求。  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |此错误指示未指定**AffectedTaskOccurrences**属性。 当[DeleteItem](deleteitem.md)元素用于至少删除一个任务的项目，而不管该任务是否定期发生时，必须指定**AffectedTaskOccurrences**属性，以便**DeleteItem**可以确定是删除当前事件还是整个数据系列。  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |指示存档文件夹路径创建中有一个错误。  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |指示未启用存档邮箱。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |指示存档邮箱服务发现失败。  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |指定尝试创建嵌套的附件超过10个的项目。 此值是在 Exchange Server 2010 Service Pack 2 （SP2）中引入的。  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |如果尝试创建大小超过 Int32 的附件（以字节为单位）， [CreateAttachment](createattachment.md)元素将返回此错误。  <br/> 如果尝试检索大小超过 Int32 的现有附件（以字节为单位）， [GetAttachment](getattachment.md)元素将返回此错误。  <br/> |
|ErrorAutoDiscoverFailed  <br/> |此错误指示 Exchange Web 服务尝试确定运行 Exchange 2010 且使用自动发现服务安装了客户端访问服务器角色的跨林计算机的位置，但对自动发现服务的调用失败。  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |此错误指示 AD DS 中缺少本地林的可用性配置信息。  <br/> |
|ErrorBatchProcessingStopped  <br/> | 此错误指示在处理项时出现异常，且随后的项可能会发生此异常。 请求可能包含多个项;例如，GetItem 操作请求可能包含多个标识符。 通常情况下，一次处理一个项目。 如果在处理项目时发生异常，且随后的项目可能发生此异常，则后续的项目将不会得到处理。  <br/><br/>  以下是将停止处理以下项目的错误示例：<br/>  <br/>- ErrorAccessDenied  <br/>- ErrorAccountDisabled  <br/>- ErrorADUnavailable  <br/>- ErrorADOperation  <br/>- ErrorConnectionFailed  <br/>- ErrorMailboxStoreUnavailable  <br/>- ErrorMailboxMoveInProgress  <br/>- ErrorPasswordChangeRequired  <br/>- ErrorPasswordExpired  <br/>- ErrorQuotaExceeded  <br/>- ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |当尝试移动或复制定期日历项的匹配项时，将发生此错误。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | 当尝试更新 "已删除邮件" 文件夹中的日历项目，并且根据**SendMeetingInvitationsOrCancellations**属性的值发送会议更新或取消通知时，将出现此错误。 <br/><br/>以下是该属性可能的值：  <br/><br/>- SendToAllAndSaveCopy  <br/>- SendToChangedAndSaveCopy  <br/>- SendOnlyToAll  <br/>- SendOnlyToChanged  <br/>  <br/>但是，仅当此属性的值设置为 SendToNone 时，才允许此类更新。  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |当调用 UpdateItem、GetItem、DeleteItem、MoveItem、CopyItem 或 SendItem 操作，并且指定的 ID 不是任何定期日历项的发生 ID 时，将发生此错误。  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |调用**UpdateItem**、 **GetItem**、 **DeleteItem**、 **MoveItem**、 **COPYITEM**或**SendItem**操作时，如果指定的 id 不是任何定期主项目的 id，则会出现此错误。  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |在**CreateItem**或**UpdateItem**操作期间，如果日历项目持续时间超过了允许的最大值（当前为5年），则会发生此错误。  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |当日历结束时间设置为相同时间或晚于开始时间时，将发生此错误。  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |当具有[CalendarView](calendarview.md)元素的**FindItem**操作的指定文件夹不是 "日历" 文件夹类型时，将发生此错误。  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |不使用此响应代码。  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |在**CreateItem**或**UpdateItem**操作期间，当 Day、WeekendDay 和 Weekday 的无效值用于定义时间更改模式时，将发生此错误。  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |在**CreateItem**或**UpdateItem**操作期间，如果使用无效的日、工作日和 WeekendDay 指定每周重复周期，则会发生此错误。  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |当 Exchange 存储中的日历项目定期二进制大型对象（BLOB）的状态无效时，将出现此错误。  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |不使用此响应代码。  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |当无法创建指定的定期项时，将发生此错误。  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |当遇到无效的时区时，将发生此错误。  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |此错误指示[AcceptItem](acceptitem.md)元素对委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |此错误指示[DeclineItem](declineitem.md)元素对委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |此错误指示在委派方案中， [RemoveItem](removeitem.md)元素对于会议取消无效。  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |此错误指示[TentativelyAcceptItem](tentativelyacceptitem.md)元素对委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |此错误指示日历项目上的操作（当前 CancelItem）对与会者无效。 只有会议组织者可以取消会议。  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |此错误指示[AcceptItem](acceptitem.md)对组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |此错误指示[DeclineItem](declineitem.md)对组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |此错误指示[RemoveItem](removeitem.md)对组织者的日历项目无效。 若要从日历中删除会议，组织者必须使用 CancelCalendarItem。  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |此错误指示[TentativelyAcceptItem](tentativelyacceptitem.md)对组织者的日历项目无效。  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |此错误指示会议请求已过期，无法更新。  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |此错误指示匹配项索引未指向当前定期中的事件。 例如，如果您的定期模式定义了三个会议事件的集合，并且您尝试访问第五个事件，则会导致此响应代码。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |此错误指示对已删除事件（通过定期主 ID 和匹配项索引解决）的任何操作都无效。  <br/> |
|ErrorCalendarOutOfRange  <br/> |当属性值超出范围时，将在 CreateItem 和 UpdateItem 操作中为日历项目或任务周期属性报告此错误。 例如，指定一个月的第十五周将导致此响应代码。  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |当[CalendarView](calendarview.md)元素的开始日期范围大于允许的最大值（当前为2年）时，将发生此错误。  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |此错误指示请求帐户不是目录数据库中的有效帐户。  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |指示试图存档日历联系人任务文件夹。  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |指示试图对公用文件夹中的项目进行存档。  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |指示尝试对存档邮箱中的项目进行存档。  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |当正在创建日历项目，而**SavedItemFolderId**属性引用非日历文件夹时，将发生此错误。  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |当正在创建联系人且**SavedItemFolderId**属性引用非联系人文件夹时，将发生此错误。  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |此错误指示无法在邮件文件夹之外的文件夹（如 "日历"、"联系人"、"任务"、"便笺" 等）中创建公告项。  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |当正在创建任务且**SavedItemFolderId**属性引用非任务文件夹时，将发生此错误。  <br/> |
|ErrorCannotDeleteObject  <br/> |当无法删除项目或文件夹删除时，将发生此错误。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |当[DeleteItem 操作](deleteitem-operation.md)未能删除定期任务的当前事件时，该操作将返回此错误。 仅当**AffectedTaskOccurrences**属性已设置为 SpecifiedOccurrenceOnly 时，才会发生这种情况。  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |指示试图禁用 mandatorty 扩展。  <br/> |
|ErrorCannotEmptyFolder  <br/> |如果服务器不能清空文件夹，则必须返回此错误。  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |指示无法检索源文件夹路径。  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |指定服务器无法检索 Outlook Web App 选项的外部 URL。  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |如果不能检索文件附件的正文， **GetAttachment**操作将返回此错误。  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |此错误指示呼叫者尝试在非日历文件夹上设置日历权限。  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |此错误指示呼叫者尝试在 "日历" 文件夹上设置非日历权限。  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |此错误指示您无法在权限集中设置未知权限。  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |指示尝试将搜索文件夹指定为源文件夹。  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |当为需要项目标识符的请求提供文件夹标识符时，将发生此错误。  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |当为需要文件夹标识符的请求提供项标识符时，将发生此错误。  <br/> |
|ErrorChangeKeyRequired  <br/> |此响应代码已由**ErrorChangeKeyRequiredForWriteOperations**替换。 <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |当项的更改密钥丢失或过期时，将返回此错误。 <br/><br/>对于 SendItem、UpdateItem 和 UpdateFolder 操作，调用方必须传入项的正确和当前更改键。 请注意，即使将冲突解决设置为 "始终覆盖"，也会出现这种情况。 UpdateItem  <br/> |
|ErrorClientDisconnected  <br/> |指定客户端已断开连接。  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |此错误仅供内部使用。  <br/> |
|ErrorClientIntentNotFound  <br/> |此错误仅供内部使用。  <br/> |
|ErrorConnectionFailed  <br/> |当 Exchange Web 服务无法连接到邮箱时，将发生此错误。  <br/> |
|ErrorContainsFilterWrongType  <br/> |此错误指示为包含筛选器而检查的属性不是字符串类型。  <br/> |
|ErrorContentConversionFailed  <br/> |当 Exchange Web 服务无法检索请求的项目的 MIME 内容时， **GetItem**操作将返回此错误。 <br/><br/>当 Exchange Web 服务无法从提供的 MIME 内容创建项目时， **CreateItem**操作将返回此错误。 通常情况下，这表示 item 属性已损坏或被截断。  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |当使用 QueryString 选项进行搜索请求时，如果没有为目标邮箱启用内容索引，则会发生此错误。  <br/> |
|ErrorCorruptData  <br/> |当数据损坏且无法处理时，将发生此错误。  <br/> |
|ErrorCreateItemAccessDenied  <br/> |当调用方没有创建项目的权限时，将发生此错误。  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |当未能创建在 CreateManagedFolder 操作请求中指定的一个或多个托管文件夹时，将出现此错误。 搜索每个文件夹以确定哪些文件夹已创建以及哪些文件夹不存在。  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |当呼叫帐户不具有创建子文件夹所需的权限时，将发生此错误。  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |当尝试将项目或文件夹从一个邮箱移动到另一个邮箱时，将发生此错误。 如果源邮箱和目标邮箱不同，则会出现此错误。  <br/> |
|ErrorCrossSiteRequest  <br/> |此错误指示不允许请求，因为应为请求服务的客户端访问服务器位于不同的站点中。  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |在下列情况下可能会发生此错误：<br/>  <br/>-尝试访问或写入某个项的属性，并且该属性值太大。<br/>-请求 XML 中的 base64 编码的 MIME 内容长度超过限制。<br/>-现有项目正文的大小超出限制。<br/>-使用者尝试设置一个 HTML 或文本正文，其长度（或追加的大小写的组合）超出了限制。 |
|ErrorDataSourceOperation  <br/> |当基础数据提供程序无法完成此操作时，将发生此错误。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |当指定的用户已经存在于代理列表中时， **AddDelegate**操作中会出现此错误。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |当要添加的指定用户是邮箱的所有者时， **AddDelegate**操作中会出现此错误。  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |如果本地 FreeBusy 邮件上没有代理信息或没有 Active Directory 公用代理（在 AD DS 中没有 "公用代理" 或 "代表发送" 条目），则**GetDelegate**操作中会出现此错误。  <br/> |
|ErrorDelegateNoUser  <br/> |当无法将指定的用户映射到 AD DS 中的用户时，将发生此错误。  <br/> |
|ErrorDelegateValidationFailed  <br/> |当添加的代理用户无效时， **AddDelegate**操作中会出现此错误。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |当尝试删除可分辨文件夹时，将发生此错误。  <br/> |
|ErrorDeleteItemsFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |此错误仅供内部使用。  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |此错误指示可分辨用户 ID 对该操作无效。 **DistinguishedUserType**不应出现在请求中。  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |此错误指示通讯组列表中不存在请求通讯组列表成员。  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |当在**CreateManagedFolder**操作请求的[FolderNames](foldernames.md)元素中指定重复的文件夹名称时，将发生此错误。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |此错误指示存在重复的 SOAP 标头。  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |此错误指示在权限集中找到了重复的用户 ID，默认设置或匿名设置了一次，或者存在重复的 Sid 或收件人。  <br/> |
|ErrorEmailAddressMismatch  <br/> |当请求尝试创建/更新搜索文件夹的搜索参数时，将发生此错误。 例如，当在邮箱中创建搜索文件夹，但搜索文件夹定向到另一个邮箱中时，可能会发生这种情况。  <br/> |
|ErrorEventNotFound  <br/> |如果在返回事件之前删除了与水印相关联的事件，则会发生此错误。 返回此错误时，也会删除订阅。  <br/> |
|ErrorExceededConnectionCount  <br/> |此错误-指示对服务器的并发请求数超过用户策略所允许的数量。  <br/> |
|ErrorExceededSubscriptionCount  <br/> |此错误指示已超出用户的限制策略最大订阅数。  <br/> |
|ErrorExceededFindCountLimit  <br/> |此错误指示搜索操作调用已超过可返回的项目总数。  <br/> |
|ErrorExpiredSubscription  <br/> |如果[GetEvents 操作](getevents-operation.md)因订阅已过期而被删除，则会出现此错误。  <br/> |
|ErrorExtensionNotFound  <br/> |指示找不到扩展。  <br/> |
|ErrorFolderCorrupt  <br/> |如果文件夹已损坏且无法保存，则会发生此错误。  <br/> |
|ErrorFolderExists  <br/> |如果尝试创建的文件夹与同一父文件夹中的另一个文件夹具有相同的名称，则会发生此错误。 不允许使用重复的文件夹名称。  <br/> |
|ErrorFolderNotFound  <br/> |此错误指示指定的文件夹 ID 不对应于有效的文件夹，或者该代理无权访问该文件夹。  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |此错误指示无法检索请求的属性。 这并不表示属性不存在，而是以某种方式损坏属性，从而导致检索失败。  <br/> |
|ErrorFolderSave  <br/> |此错误指示由于状态无效，无法创建或更新文件夹。  <br/> |
|ErrorFolderSaveFailed  <br/> |此错误指示由于状态无效，无法创建或更新文件夹。  <br/> |
|ErrorFolderSavePropertyError  <br/> |此错误指示无法创建或更新文件夹，因为属性值无效。 响应代码将列出导致问题的属性。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |此错误指示为获取通讯组列表的忙/闲信息而达到了最大组成员数。  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |当由于发生插入故障而无法检索忙/闲信息时，将返回此错误。  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorImContactLimitReached  <br/> |当无法添加新的即时消息（IM）联系人时，将返回此错误，因为已达到最大联系人数。 此错误是在 Exchange Server 2013 中引入的。  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |当现有组已具有相同的显示名称时，当尝试添加组显示名称时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorImGroupLimitReached  <br/> |当无法添加新的 IM 组时，将返回此错误，因为已达到最大组数。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorImpersonateUserDenied  <br/> |当呼叫者不具有模拟相关特定用户的适当权限时，将在 Exchange 模拟的服务器到服务器授权事例中返回该错误。 此错误映射到 Exch-EPI 的 "可能模拟" 扩展 Active Directory 权限。  <br/> |
|ErrorImpersonationDenied  <br/> |当呼叫者不具有通过其发出请求的客户端访问服务器进行模拟的适当权限时，将在 Exchange 模拟的服务器到服务器授权中返回此错误。 这将映射到 Exch-EPI 扩展 Active Directory 权限。  <br/> |
|ErrorImpersonationFailed  <br/> |此错误指示在尝试执行服务器到服务器身份验证时出现意外错误。 此响应代码通常指示运行 Exchange Web 服务应用程序池的服务帐户配置不正确，Exchange Web 服务无法与目录通信，或者未正确配置林之间的信任。  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |此错误指示请求对当前 Exchange Server 版本有效，但对于指定的请求服务器版本无效。  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |此错误指示[UpdateItem](updateitem.md)或[UpdateFolder](updatefolder.md)元素中的每个更改说明都必须仅列出一个要更新的属性。  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |当请求包含过多要解析的与会者时，将发生此错误。 默认情况下，要解析的与会者的最大数量为100。  <br/> |
|ErrorInsufficientResources  <br/> |当邮箱服务器超载时，将发生此错误。 请稍后重试你的请求。  <br/> |
|ErrorInternalServerError  <br/> |此错误指示 Exchange Web 服务遇到无法从中恢复的错误，并且与所发生的错误关联的更具体的响应代码不存在。  <br/> |
|ErrorInternalServerTransientError  <br/> |此错误指示发生了内部服务器错误，应稍后重试你的请求。  <br/> |
|ErrorInvalidAccessLevel  <br/> |此错误指示呼叫者对忙/闲数据的访问级别无效。  <br/> |
|ErrorInvalidArgument  <br/> |此错误指示传递给[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的所有无效参数所导致的错误。<br/><br/> 在以下情况下，将返回此错误： <br/><br/>-在 "_发送-as_ " 参数中指定的用户在目录中不存在。 <br/>-在 "_发送-_ " 参数中指定的用户在目录中不是唯一的。 <br/>-"_发送为_" 地址为空。<br/>-"_发送_" 地址不是有效的电子邮件地址。  <br/> |
|ErrorInvalidAttachmentId  <br/> |当找不到与指定 ID 对应的附件时， [GetAttachment 操作](getattachment-operation.md)或[DeleteAttachment 操作](deleteattachment-operation.md)将返回此错误。  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |当您尝试使用复杂附件表限制绑定到现有搜索文件夹时，将发生此错误。 Exchange Web 服务仅支持对附件表的简单筛选器。 如果尝试绑定到具有更复杂的附件表限制（subfilter）的现有搜索文件夹，则 Exchange Web 服务无法为该筛选器呈现 XML，并返回此响应代码。 <br/><br/>请注意，仍可以对文件夹调用 GetFolder 操作，但不要请求[SearchParameters](searchparameters.md)元素。  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |当您尝试使用复杂附件表限制绑定到现有搜索文件夹时，将发生此错误。 Exchange Web 服务仅支持对附件表的简单筛选器。 <br/><br/>如果您尝试绑定到具有更复杂的附件表限制的现有搜索文件夹，则 Exchange Web 服务无法为该筛选器呈现 XML。 在这种情况下，附件 subfilter 包含文本筛选器，但它不会查看附件显示名称。<br/><br/> 请注意，仍可以对文件夹调用 GetFolder 操作，但不要请求[SearchParameters](searchparameters.md)元素。  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | 此错误指示请求者的授权过程失败。  <br/> |
|ErrorInvalidChangeKey  <br/> |当使用者使用无法分析的更改键传入文件夹或项目标识符时，将发生此错误。 例如，这可能是无效的 base64 内容或空字符串。  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |此错误指示在尝试解析调用方的标识时发生了内部错误。  <br/> |
|ErrorInvalidCompleteDate  <br/> |当尝试将任务的[CompleteDate](completedate.md)元素值设置为将来某个时间时，将返回此错误。 在转换为客户端访问服务器的本地时间时，不能将任务的[CompleteDate](completedate.md)设置为晚于客户端访问服务器上的本地时间的值。  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |此错误指示为联系人提供了无效的电子邮件地址。  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |此错误指示为电子邮件条目提供了无效的电子邮件索引值。  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |当用于将请求代理到不同目录服务林的凭据未通过身份验证时，将发生此错误。  <br/> |
|ErrorInvalidDelegatePermission  <br/> |此错误指示指定的文件夹权限无效。  <br/> |
|ErrorInvalidDelegateUserId  <br/> |此错误指示指定的代理用户 ID 无效。  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |当呼叫者未指定 UPN、电子邮件地址或用户 SID 时，在 Exchange 模拟期间会发生此错误。 如果呼叫者指定其中一个或多个，并且值为空，也会发生这种情况。  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |如果无法分析传递到[排除](excludes.md)元素限制中的位掩码，则会出现此错误。  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidExtendedProperty  <br/> | 当发生以下事件时，将发生此错误： <br/> <br/>-调用方尝试使用 Exchange Web 服务不支持的扩展属性。  <br/>-调用方传递的扩展属性的属性值组合无效。 如果未传递任何属性，也会发生这种情况。 仅允许某些组合。  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |当扩展属性的值部分与属性的类型不匹配时，将发生此错误。 <br/><br/>例如，将具有 Recordtype = "String" 的扩展属性设置为整数数组将导致此错误。 任何不强制为扩展属性指定的类型的字符串表示形式都将提供此错误。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |此错误指示共享邀请发件人未创建共享邀请元数据。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |此错误指示共享邮件不是针对呼叫者的。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |此错误指示请求者的组织联合对象未正确配置。  <br/> |
|ErrorInvalidFolderId  <br/> |当文件夹 ID 损坏时，将发生此错误。  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |此错误指示指定的文件夹类型对当前操作无效。 例如，不能在公用文件夹中创建 "搜索文件夹"。  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | 当用户已指定以下选项之一时，将在分数分页过程中出现此错误： <br/> <br/>-大于分母的分子  <br/>-小于零的分子  <br/>-小于或等于零的分母  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |此错误指示[DataType](datatype.md)和 ShareFolderId 元素都存在于请求中。  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |调用[GetUserAvailability 操作](getuseravailability-operation.md)时，如果[FreeBusyViewType](freebusyviewtype.md)为 None，则会发生此错误。  <br/> |
|ErrorInvalidId  <br/> |此错误指示 ID 和/或更改键的格式不正确。  <br/> |
|ErrorInvalidIdEmpty  <br/> |当调用方指定的**Id**属性为空时，将发生此错误。  <br/> |
|ErrorInvalidLikeRequest  <br/> |当无法对项目进行赞时，将发生此错误。 从内部版本号开始的 Exchange 版本15.00.0913.09 包含此值。  <br/> |
|ErrorInvalidIdMalformed  <br/> |当调用方指定的**Id**属性格式不正确时，将发生此错误。  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |此错误指示为具有 Exchange 2007 SP1 版本或更高版本的请求指定了使用 Exchange 2007 格式的文件夹或项目 ID。 您不能在 Exchange 2007 SP1 或更高版本请求中使用 Exchange 2007 Id。 您必须先使用[ConvertId 操作](convertid-operation.md)来转换它们。  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |当调用方指定的**Id**属性过长时，将发生此错误。  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |每当不是项目附件 ID 的 ID 传递给需要附件 ID 的 Web 服务方法时，将返回此错误。  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |当邮箱中的联系人损坏时，将发生此错误。  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |当调用方指定的**Id**属性过长时，将发生此错误。  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |当项目的附件层次结构超出了最大深度为255个级别时，将返回此错误。  <br/> |
|ErrorInvalidIdXml  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidImContactId  <br/> |当指定的 IM 联系人标识符不代表有效的标识符时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |当指定的 IM 通讯组 SMTP 地址标识符不代表有效的标识符时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidImGroupId  <br/> |当指定的 IM 组标识符不代表有效的标识符时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |如果索引分页的偏移量为负，则会发生此错误。  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |指示项目对于**ArchiveItem**操作无效。  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |当尝试对除会议请求或日历项目之外的项目类型使用 AcceptItem 响应对象时，或者在尝试接受 "已删除邮件" 文件夹中出现的日历项目时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |当试图对项目类型（而不是日历项目）使用 CancelItem 响应对象时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | 当尝试创建不受支持的类型的项附件时，将返回此错误。  <br/><br/>  项目附件支持的项目类型包括以下对象：  <br/><br/>- [Item](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [任务](task.md) <br/>- [信息](contact.md) <br/> <br/> 例如，如果您尝试创建一个[MeetingMessage](meetingmessage.md)附件，您将遇到此响应代码。  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | 如果请求包含不受支持的项目类型， [CreateItem 操作](createitem-operation.md)将返回此错误。 <br/><br/>支持的项目包括以下对象：<br/>  <br/>- [Item](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [任务](task.md) <br/>- [信息](contact.md) <br/><br/>  某些类型作为执行其他操作的副作用而创建。 例如，当您向与会者发送日历项目时，将会创建会议邮件;它们不是显式创建的。  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |当尝试对除会议请求或日历项目之外的项目类型使用 DeclineItem 响应对象时，或者在尝试拒绝 "已删除邮件" 文件夹中出现的日历项目时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |此错误指示[ExpandDL 操作](expanddl-operation.md)仅对专用通讯组列表有效。  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |如果请求指定不是会议取消项目的项目，则 RemoveItem 响应对象将返回此错误。  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |如果请求指定不是邮件项目的项目，则[SendItem 操作](senditem-operation.md)将返回此错误。  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |当尝试对除会议请求或日历项目之外的项目类型使用[TentativelyAcceptItem](tentativelyacceptitem.md)时，或者在尝试暂时接受 "已删除邮件" 文件夹中出现的日历项目时，将发生此错误。  <br/> |
|ErrorInvalidLogonType  <br/> |此错误仅供内部使用。 不返回此错误。  <br/> |
|ErrorInvalidMailbox  <br/> |此错误指示在创建或更新个人通讯组列表时， [CreateItem 操作](createitem-operation.md)或[UpdateItem 操作](updateitem-operation.md)失败。  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |当托管文件夹的结构损坏且无法呈现时，将发生此错误。  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |当托管文件夹上设置的配额小于零，从而指示托管文件夹已损坏时，将发生此错误。  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |如果在托管文件夹上设置的大小小于零，表示托管文件夹已损坏，则会发生此错误。  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |当所提供的合并闲/忙内部值无效时，将出现此错误。 默认的最小值为5分钟。 默认的最大值为1440分钟。  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |如果[ResolveNames 操作](resolvenames-operation.md)的名称无效，则会出现此错误。 例如，零长度字符串、一个空格、一个逗号和一个短划线都是无效的名称。  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |此错误指示客户端访问服务器上的网络服务帐户中有错误。  <br/> |
|ErrorInvalidOofParameter  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidOperation  <br/> | 这是在请求的操作无效时使用的常规错误。 <br/><br/>例如，您无法执行以下操作： <br/> <br/>-使用对公用文件夹的[FindFolder 操作](findfolder-operation.md)执行 "深度" 遍历。  <br/>-移动或复制公用文件夹根目录。  <br/>-使用除 "硬" 删除之外的任意模式删除关联的项目。  <br/>-移动或复制关联的项目。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |此错误指示呼叫者请求其他组织中某个用户的忙/闲信息，但该组织关系未启用忙/闲信息。  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |当使用者将零值或负值传递给要返回的最大行时，将发生此错误。  <br/> |
|ErrorInvalidParentFolder  <br/> |当使用者在某个操作的无效父文件夹中传递时，将发生此错误。 例如，如果您尝试在搜索文件夹中创建文件夹，则会返回此错误。  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |当尝试将任务完成百分比设置为无效值时，将返回此错误。 该值必须介于0到100（含）之间。  <br/> |
|ErrorInvalidPermissionSettings  <br/> |此错误指示权限级别与权限设置不一致。  <br/> |
|ErrorInvalidPhoneCallId  <br/> |此错误指示呼叫者标识符无效。  <br/> |
|ErrorInvalidPhoneNumber  <br/> |此错误指示电话号码不正确或不适合拨号计划规则。  <br/> |
|ErrorInvalidPropertyAppend  <br/> | 当您尝试追加到的属性不支持追加时，将发生此错误。 <br/><br/>以下是支持追加的唯一属性： <br/> <br/>-收件人集合（ToRecipients、CcRecipients、BccRecipients）  <br/>-与会者集合（RequiredAttendees、OptionalAttendees、Resources）  <br/>-正文  <br/>-ReplyTo  <br/><br/>  此外，如果在请求中指定的格式与存储区中的项的格式不匹配，则在追加邮件正文时会发生此错误。  <br/> |
|ErrorInvalidPropertyDelete  <br/> |如果为不支持删除操作的属性在[UpdateItem 操作](updateitem-operation.md)或[UpdateFolder 操作](updatefolder-operation.md)调用中指定了 delete 操作，则会发生此错误。 例如，不能删除[Item](item.md)对象的[ItemId](itemid.md)元素。  <br/> |
|ErrorInvalidPropertyForExists  <br/> |如果使用者在[存在](exists.md)筛选器中的某个标志属性中传递，则会发生此错误。 例如，如果在[Exists](exists.md)元素中指定了[IsRead](isread.md)或[IsFromMe](isfromme.md)标志，则会发生此错误。 请求应改用[IsEqualTo](isequalto.md)元素，因为它们是标志，因此是单个属性的一部分。  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |如果您尝试操作的属性不支持正在对其执行的操作，则会出现此错误。  <br/> |
|ErrorInvalidPropertyRequest  <br/> | 如果请求中指定的属性对项目类型不可用，则会发生此错误。 例如，如果在某个邮件的[GetItem 操作](getitem-operation.md)调用中请求仅在日历项目上可用的属性，或者在[UpdateItem 操作](updateitem-operation.md)调用中为邮件更新的属性，则会返回此错误。 <br/> <br/>  在以下操作中会发生这种情况： <br/> <br/>- [GetItem 操作](getitem-operation.md) <br/>- [GetFolder 操作](getfolder-operation.md) <br/>- [UpdateItem 操作](updateitem-operation.md) <br/>- [UpdateFolder 操作](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |此错误指示您尝试操作的属性不支持正在对其执行的操作。 例如，如果您尝试设置的属性是只读的，则会返回此错误。  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | 当客户端尝试更新已发送邮件的某些属性时， [UpdateItem 操作](updateitem-operation.md)过程中会发生此错误。<br/><br/> 例如，无法在已发送的邮件上更新以下属性： <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |如果使用推送订阅 ID 调用[GetEvents 操作](getevents-operation.md)或[取消订阅操作](unsubscribe-operation.md)，则会发生此错误。 若要取消订阅推送订阅，必须使用取消订阅响应响应推送请求，或者断开 Web 服务并等待推送通知超时。  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | 此错误在创建 "推送" 订阅时由[订阅操作](subscribe-operation.md)返回，并指示包含在请求中的 URL 无效。<br/><br/>若要接受 URL 的 Exchange Web 服务，必须满足以下条件： <br/> <br/>-字符串长度 \> 0 和 \< 2083.  <br/> -协议为 http 或 https。  <br/>-URL 可由 URI Microsoft .NET Framework 类进行分析。  <br/> |
|ErrorInvalidRecipients  <br/> |此错误指示您的邮件或日历项目上的与会者集合中的收件人集合无效。 例如，当尝试发送没有收件人的项目时，将返回此错误。  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |此错误指示搜索文件夹具有一个 Exchange Web 服务无法表示的收件人表筛选器。 若要避免此错误，请在不请求搜索参数的情况下检索该文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |此错误指示搜索文件夹具有一个 Exchange Web 服务无法表示的收件人表筛选器。 若要避免此错误，请在不请求搜索参数的情况下检索该文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |此错误指示搜索文件夹具有一个 Exchange Web 服务无法表示的收件人表筛选器。 若要避免此错误，请在不请求搜索参数的情况下检索该文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |此错误指示搜索文件夹具有一个 Exchange Web 服务无法表示的收件人表筛选器。 若要避免此错误，请在不请求搜索参数的情况下检索该文件夹。  <br/> |
|ErrorInvalidReferenceItem  <br/> | 在下列情况下，CreateItem 操作会从 "转发" 和 "答复" 响应对象的[操作](createitem-operation.md)中返回此错误：<br/>  <br/>-引用的项目标识符不是[message](message-ex15websvcsotherref.md)、 [CalendarItem](calendaritem.md)或**message**或**CalendarItem**的后代。  <br/>-引用项目标识符适用于**CalendarItem** ，并且组织者正在尝试答复或 ReplyAll 他自己。  <br/>-邮件为草稿并选中 "答复" 或 "ReplyAll"。  <br/>- [SuppressReadReceipt](suppressreadreceipt.md)的引用项**不是邮件或****邮件**的后代。  <br/> |
|ErrorInvalidRequest  <br/> |当 SOAP 请求具有 SOAP 操作头，但 SOAP 正文中没有任何内容时，会发生此错误。 请注意，SOAP 操作头不是必需的，因为 Exchange Web 服务可以确定要从 SOAP 正文中的根元素的本地名称调用的方法。  <br/> |
|ErrorInvalidRestriction  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |当指定的保留标记与之关联的操作不正确时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |当尝试对**PolicyTag**属性设置不存在或不可见的标记时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |当尝试在**PolicyTag**属性上设置隐式标记时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |指示保留标记 GUID 无效。  <br/> |
|ErrorInvalidRoutingType  <br/> |如果为[RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)元素传递的路由类型无效，则会发生此错误。 通常情况下，路由类型设置为简单邮件传输协议（SMTP）。  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |如果指定的持续时间结束时间不大于开始时间，或者在未来不会发生结束时间，则会出现此错误。  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |此错误指示由于版本控制不匹配，发送到另一台服务器的代理请求无法为请求服务。  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |此错误指示存储中的 "日历" 文件夹上的 Exchange 安全描述符已损坏。  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |在尝试发送在请求中指定了[SavedItemFolderId](saveditemfolderid.md)但**SaveItemToFolder**属性设置为**false**的项的过程中，会发生此错误。  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |此错误指示在头中传递的令牌格式不正确，不引用目录中的有效帐户，或者缺少 primary group **ConnectingSID**。  <br/> |
|ErrorInvalidSharingData  <br/> |此错误指示共享元数据无效。 这可能是由无效的 XML 引起的。  <br/> |
|ErrorInvalidSharingMessage  <br/> |此错误指示共享邮件无效。 这可能是由于缺少属性造成的。  <br/> |
|ErrorInvalidSid  <br/> |当在请求中传递无效的 SID 时，将发生此错误。  <br/> |
|ErrorInvalidSIPUri  <br/> |此错误指示 SIP 名称、拨号计划或电话号码是无效的 SIP Uri。  <br/> |
|ErrorInvalidServerVersion  <br/> |此错误指示请求中指定了无效的请求服务器版本。  <br/> |
|ErrorInvalidSmtpAddress  <br/> |当无法解析 SMTP 地址时，将发生此错误。  <br/> |
|ErrorInvalidSubfilterType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubscription  <br/> |此错误指示订阅已不再有效。 这可能是因为客户端访问服务器正在重新启动或订阅已过期。  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |此错误指示订阅请求包含多个公用文件夹 Id。 订阅可以包含来自同一个邮箱或一个公用文件夹 ID 的多个文件夹。  <br/> |
|ErrorInvalidSyncStateData  <br/> |如果传递的[SyncState](syncstate-ex15websvcsotherref.md)数据无效， [SyncFolderItems](syncfolderitems.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)将返回此错误。 若要修复此错误，必须在不进行同步状态的情况下重新同步。 请确保如果要持久化同步状态 Blob，则不会意外截断 BLOB。  <br/> |
|ErrorInvalidTimeInterval  <br/> |此错误指示指定的时间间隔无效。 开始时间必须大于或等于结束时间。  <br/> |
|ErrorInvalidUserInfo  <br/> |此错误指示为权限操作指定了内部不一致的[UserId](userid.md) 。 例如，如果指定了一个可分辨的用户 ID （默认或匿名），如果您还尝试为此用户指定一个 SID 或主 SMTP 地址或显示名称，则会返回此错误。  <br/> |
|ErrorInvalidUserOofSettings  <br/> |此错误指示由于缺少内部或外部答复而导致用户 "外出" （OOF）设置无效。  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |此错误发生在 Exchange 模拟期间。 传递到 SOAP 标头中的无效 UPN 的调用方在目录中无法访问。  <br/> |
|ErrorInvalidUserSid  <br/> |当在请求中传递无效的 SID 时，将发生此错误。  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidValueForProperty  <br/> |此错误指示限制中的比较值对于您要与之进行比较的属性无效。<br/><br/> 例如， [DateTimeCreated](datetimecreated.md)  >  **true**的比较值将返回此响应代码。 <br/><br/>如果在比较中指定了枚举属性，但要对其进行比较的值不是该枚举的有效值，也会返回此响应代码。  <br/> |
|ErrorInvalidWatermark  <br/> |此错误是由无效的水印造成的。  <br/> |
|ErrorIPGatewayNotFound  <br/> |此错误指示有效的 VoIP 网关不可用。  <br/> |
|ErrorIrresolvableConflict  <br/> |此错误指示冲突解决无法解析属性的更改。 存储中的项目可能已更改，必须进行更新。 检索更新后的更改密钥，然后重试。  <br/> |
|ErrorItemCorrupt  <br/> |此错误指示对象的状态已损坏，无法检索。 检索项目时，只有某些元素将处于此状态，如[Body](body.md)和[MimeContent](mimecontent.md)。 请省略这些元素，然后重试该操作。  <br/> |
|ErrorItemNotFound  <br/> |如果找不到该项目或你没有权限访问该项目，则会出现此错误。  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |如果对某项的属性请求失败，则会发生此错误。 该属性可能存在，但无法对其进行检索。  <br/> |
|ErrorItemSave  <br/> |当尝试保存项或文件夹失败时，将发生此错误。  <br/> |
|ErrorItemSavePropertyError  <br/> |当由于属性值无效而导致保存项或文件夹的尝试失败时，将发生此错误。 响应代码包括无效属性的路径。  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |不使用此响应代码。  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |不使用此响应代码。  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |此错误指示可用性服务无法以网络服务的形式登录，以向相应的网站或林发出代理请求。 此响应通常表示配置错误。  <br/> |
|ErrorMailboxConfiguration  <br/> |此错误指示 AD DS 中的邮箱信息配置不正确。  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |此错误指示请求中的[MailboxDataArray](mailboxdataarray.md)元素为空。 您必须至少提供一个邮箱标识符。  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |当[MailboxDataArray](mailboxdataarray.md)元素中提供多于100个条目时，将发生此错误。  <br/> |
|ErrorMailboxFailover  <br/> |此错误指示尝试访问邮箱失败，因为邮箱处于故障转移过程中。  <br/> |
|ErrorMailboxHoldNotFound  <br/> |指示找不到邮箱保留。  <br/> |
|ErrorMailboxLogonFailed  <br/> |当与邮箱的连接获取日历视图信息失败时，将发生此错误。  <br/> |
|ErrorMailboxMoveInProgress  <br/> | 此错误指示要将邮箱移动到不同的邮箱存储或服务器。 此错误也可能表示邮箱位于另一台服务器或邮箱数据库上。  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | 此错误指示发生了以下错误情况之一：  <br/><br/>-邮箱存储已损坏。  <br/>-邮箱存储正在停止。  <br/>-邮箱存储处于脱机状态。  <br/>-尝试访问邮箱存储时发生网络错误。  <br/>-邮箱存储超载，无法接受更多的连接。  <br/>-邮箱存储已暂停。  <br/> |
|ErrorMailRecipientNotFound  <br/> |如果[MailboxData](mailboxdata.md)元素信息无法映射到有效的邮箱帐户，则会出现此错误。  <br/> |
|ErrorMailTipsDisabled  <br/> |此错误指示邮件提示已禁用。  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |如果您尝试创建的托管文件夹已存在于邮箱中，则会发生此错误。  <br/> |
|ErrorManagedFolderNotFound  <br/> |当请求中指定的文件夹名称未映射到 AD DS 中的托管文件夹定义时，将出现此错误。 您只能为在 AD DS 中定义的文件夹创建托管文件夹的实例。 请检查名称，再试一次。  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |此错误指示已从邮箱中删除了托管文件夹根，或者文件夹存在于具有托管文件夹根目录名称的同一父文件夹中。 如果创建根托管文件夹的尝试失败，也会发生这种情况。  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |此错误指示建议引擎在尝试生成建议时遇到问题。  <br/> |
|ErrorMessageDispositionRequired  <br/> | 如果未设置**MessageDisposition**属性，则会发生此错误。<br/><br/> 此属性是以下项所必需的： <br/> <br/>-要创建或更新的项目为[邮件](message-ex15websvcsotherref.md)时的[CreateItem 操作](createitem-operation.md)和[UpdateItem 操作](updateitem-operation.md)。  <br/>- [CancelCalendarItem](cancelcalendaritem.md)、 [AcceptItem](acceptitem.md)、 [DeclineItem](declineitem.md)或[TentativelyAcceptItem](tentativelyacceptitem.md) response 对象。  <br/> |
|ErrorMessageSizeExceeded  <br/> |此错误指示您尝试发送的邮件超过了允许的限制。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |此错误指示找不到给定的域。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |此错误指示邮件跟踪服务无法跟踪邮件。  <br/> |
| ErrorMessageTrackingTransientError  <br/> |此错误指示邮件跟踪服务已关闭或繁忙。 此错误代码指示暂时性错误。 在收到此错误时，客户端可以重试连接到服务器。  <br/> |
|ErrorMimeContentConversionFailed  <br/> |当 MIME 内容不是[CreateItem 操作](createitem-operation.md)的有效 iCal 时，将发生此错误。 对于[GetItem 操作](getitem-operation.md)，此响应指示无法生成 MIME 内容。  <br/> |
|ErrorMimeContentInvalid  <br/> |当 MIME 内容无效时，将发生此错误。  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |当请求中的 MIME 内容不是有效的 base 64 字符串时，将发生此错误。  <br/> |
|ErrorMissingArgument  <br/> |此错误指示请求中缺少必需的参数。 响应消息文本指示要检查的参数。  <br/> |
|ErrorMissingEmailAddress  <br/> |此错误指示您在请求中指定了可分辨文件夹 ID，但发出请求的帐户在系统上没有邮箱。 在这种情况下，您必须在[DistinguishedFolderId](distinguishedfolderid.md)下提供一个[邮箱](mailbox.md)子元素。  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |此错误指示您在请求中指定了可分辨文件夹 ID，但发出请求的帐户在系统上没有邮箱。 在这种情况下，您必须在[DistinguishedFolderId](distinguishedfolderid.md)下提供一个[邮箱](mailbox.md)子元素。 此响应从[CreateManagedFolder 操作](createmanagedfolder-operation.md)返回。  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |如果缺少[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)元素，则会发生此错误。  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |如果缺少[ReferenceItemId](referenceitemid.md) ，则会发生此错误。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |永远不会返回此错误代码。  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |当尝试不将 item 元素包含在[CreateAttachment 操作](createattachment-operation.md)请求的**ItemAttachment**元素中时，将返回此错误。  <br/> |
|ErrorMissingManagedFolderId  <br/> |当缺少文件夹的策略 Id 属性、属性标记0x6732 时，将发生此错误。 应将其视为已损坏的文件夹。  <br/> |
|ErrorMissingRecipients  <br/> |此错误指示您尝试发送不包含收件人的项目。 请注意，如果使用邮件处置（导致发送邮件）调用[CreateItem 操作](createitem-operation.md)，将会收到以下响应代码： **ErrorInvalidRecipients**。  <br/> |
|ErrorMissingUserIdInformation  <br/> |此错误指示未在权限集中完全指定[UserId](userid.md) 。  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |此错误指示您在一个请求中指定了多个[ExchangeImpersonation](exchangeimpersonation.md)元素值。  <br/> |
|ErrorMoveCopyFailed  <br/> |此错误指示移动或复制操作失败。 当您接受 "已删除邮件" 文件夹中的会议请求时，在[CreateItem 操作](createitem-operation.md)中发生移动。 此外，如果您拒绝会议请求、取消日历项目或从日历中删除会议，则会将其移动到 "已删除邮件" 文件夹中。  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |如果您尝试移动可分辨文件夹，则会发生此错误。  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |当请求试图访问多个邮箱服务器时，将发生此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |如果[ResolveNames 操作](resolvenames-operation.md)返回多个结果或指定的模糊名称与目录中的多个对象匹配，则会发生此错误。 响应代码在响应数据中包含匹配的名称。  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |此错误指示呼叫者在系统上没有邮箱。 [ResolveNames 操作](resolvenames-operation.md)或[ExpandDL 操作](expanddl-operation.md)对于连接没有邮箱的用户是无效的。  <br/> |
|ErrorNameResolutionNoResults  <br/> |此错误指示[ResolveNames 操作](resolvenames-operation.md)未返回任何结果。  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |当 Web 服务找不到用于处理请求的服务器时，必须返回此错误代码。  <br/> |
|ErrorNoCalendar  <br/> |如果没有邮箱的日历文件夹，则会发生此错误。  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但未为目标站点中的任何客户端访问服务器配置 Windows 身份验证，因此无法代理请求。  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但未为 SSL 连接配置目标站点中的客户端访问服务器，因此无法代理请求。  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但目标站点中没有客户端访问服务器可接受的产品版本来接收请求，因此无法代理请求。  <br/> |
|ErrorNoFolderClassOverride  <br/> |如果您在创建非常规文件夹的项目时设置[FolderClass](folderclass.md)元素，则会发生此错误。 对于类型化的文件夹（如[CalendarFolder](calendarfolder.md)和[TasksFolder](tasksfolder.md)），文件夹类是隐含的。 使用[UpdateFolder 操作](updatefolder-operation.md)将 folder 类设置为不同的文件夹类型将导致**ErrorObjectTypeChanged**响应。 而是使用通用文件夹类型，但将 folder 类设置为您需要的值。 Exchange Web 服务将创建正确的强类型文件夹。  <br/> |
|ErrorNoFreeBusyAccess  <br/> |此错误指示呼叫者对所述的 "日历" 文件夹没有忙/闲查看权限。  <br/> |
|ErrorNonExistentMailbox  <br/> | 在以下情况下会发生此错误： <br/> <br/>-电子邮件地址在[CreateManagedFolder](createmanagedfolder.md)中为空。  <br/>-电子邮件地址不引用在正文或 SOAP 头中采用电子邮件地址的请求中的有效帐户，如 Exchange 模拟呼叫中。  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |当呼叫者传入非主 SMTP 地址时，将发生此错误。 响应包括要使用的正确 SMTP 地址。  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |此错误指示自定义范围（0x8000 和更高）中的 MAPI 属性不能由属性标记引用。 必须使用 EWS 托管 API [PropertySetId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)属性或带 PropertySetId 属性的 ews [ExtendedFieldURI](extendedfielduri.md)元素。  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |不使用此响应代码。  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |如果公用文件夹服务器不可用或呼叫者没有主公用服务器，则必须返回此错误代码。  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但该站点中没有任何客户端访问服务器做出响应，因此无法代理请求。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |此错误指示呼叫者尝试向另一个组织中的用户授予其 "日历" 或 "联系人" 文件夹中的权限，并且尝试失败。  <br/> |
|ErrorNotDelegate  <br/> |此错误指示用户不是邮箱的代理人。 当在委派列表中找不到指定的委派用户时， [GetDelegate 操作](getdelegate-operation.md)、 [RemoveDelegate 操作](removedelegate-operation.md)和[UpdateDelegate 操作](updatedelegate-operation.md)返回此方法。  <br/> |
|ErrorNotEnoughMemory  <br/> |此错误指示由于内存不足，无法完成操作。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |此错误指示共享邮件不受支持。  <br/> |
|ErrorObjectTypeChanged  <br/> |如果对象类型发生更改，则会发生此错误。  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |此错误发生在更新事件的[开始](start.md)或[结束](end-ex15websvcsotherref.md)时间以便将具体值计划为早于或晚于相应的上一个或下一个事件时。  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |此错误指示给定事件的时间配额与同一定期项的另一个匹配项重叠。 如果给定出现的时间长度大于 Int32，也会发生此响应。  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |此错误指示当前操作对公用文件夹根目录无效。  <br/> |
|ErrorOrganizationNotFederated  <br/> |此错误指示请求者的组织不是联合的，因此请求者无法创建要发送给外部用户的共享邮件，或者无法接受从外部用户接收的共享邮件。  <br/> |
|ErrorParentFolderIdRequired  <br/> |不使用此响应代码。  <br/> |
|ErrorParentFolderNotFound  <br/> |如果找不到父文件夹，则[CreateFolder 操作](createfolder-operation.md)中会出现此错误。  <br/> |
|ErrorPasswordChangeRequired  <br/> |此错误指示您必须先更改密码，然后才能访问此邮箱。 如果已创建新帐户，并且管理员指示用户必须在首次登录时更改密码，则会发生这种情况。 无法使用 Exchange Web 服务更新密码。 您必须使用 Microsoft Office Outlook Web App 等工具更改您的密码。  <br/> |
|ErrorPasswordExpired  <br/> |此错误指示密码已过期。 您不能使用 Exchange Web 服务更改密码。 您必须使用 Outlook Web App 等工具来更改您的密码。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |此错误指示请求者尝试将其 "日历" 或 "联系人" 文件夹中的权限授予外部用户，但分配给请求者的共享策略指示请求的权限级别高于共享策略允许的权限级别。  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |此错误指示电话号码的格式不正确。  <br/> |
|ErrorPropertyUpdate  <br/> |此错误指示更新因属性值无效而失败。 响应消息包含无效的属性路径。  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorPropertyValidationFailure  <br/> |不使用此响应代码。  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |此错误指示请求引用了另一个客户端访问服务器上存在的订阅，但尝试将请求代理到该客户端访问服务器时失败。  <br/> |
|ErrorProxyCallFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，而原始呼叫者是超过3000个组的成员。  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |此错误指示在尝试满足[GetUserAvailabilityRequest](getuseravailabilityrequest.md)请求时，Exchange Web 服务发送到另一个客户端访问服务器的请求无效。 此响应代码通常指示发生了配置或权限错误，或者有人尝试模拟可用性代理请求失败。  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |此错误指示 Exchange Web 服务尝试将可用性请求代理到另一个客户端访问服务器以进行执行，但请求失败。 此响应可能是由网络连接问题或请求超时问题导致的。  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |如果 Web 服务无法确定请求是在目标服务器上运行，还是将代理到另一台服务器，则必须返回此错误代码。  <br/> |
|ErrorProxyTokenExpired  <br/> |不使用此响应代码。  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |如果找不到公用文件夹邮箱 URL，则会发生此错误。 此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |当尝试访问公用文件夹且尝试不成功时，将发生此错误。 此错误是在 Exchange 2013Exchange Server 2013 中引入的。  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |当传递到[GetUserAvailability 操作](getuseravailability-operation.md)的收件人位于运行早于 exchange 2007 的 exchange Server 版本的计算机上，并且从公用文件夹服务器检索收件人的忙/闲信息的请求失败时，将发生此错误。  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |当传递到[GetUserAvailability 操作](getuseravailability-operation.md)的收件人位于运行早于 exchange 2007 的 exchange Server 版本的计算机上，并且从公用文件夹服务器检索收件人的忙/闲信息的请求失败时，将发生此错误，因为该组织单位没有关联的公用文件夹服务器。  <br/> |
|ErrorPublicFolderSyncException  <br/> |此错误发生在对主公用文件夹邮箱的同步操作后，但对辅助公用文件夹邮箱不会成功。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorQueryFilterTooLong  <br/> |此错误指示搜索文件夹限制可能有效，但 EWS 不支持它。 Exchange Web 服务限制限制最多包含255个筛选表达式。 如果尝试绑定到超过255的现有搜索文件夹，则会返回此响应代码。  <br/> |
|ErrorQuotaExceeded  <br/> |当超出邮箱配额时，将发生此错误。  <br/> |
|ErrorReadEventsFailed  <br/> |此错误在检索事件信息时出现故障时， [GetEvents 操作](getevents-operation.md)或推送通知返回。 返回此错误时，将删除订阅。 根据上一已知的水印重新创建事件同步。  <br/> |
|ErrorReadReceiptNotPending  <br/> |如果在邮件发件人未请求 "已读" 回执的邮件中，或邮件位于 "垃圾邮件" 文件夹中时， [CreateItem 操作](createitem-operation.md)将返回此错误。  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |当定期的结束日期为9/1/4500 之后，则会发生此错误。  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |当指定的重复项在指定范围中没有任何实例发生时，将出现此错误。  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |此错误指示删除委派后未能保存委派列表。  <br/> |
|ErrorRequestAborted  <br/> |不使用此响应代码。  <br/> |
|ErrorRequestStreamTooBig  <br/> | 当请求流大于 400 KB 时，将发生此错误。  <br/> |
|ErrorRequiredPropertyMissing  <br/> |[CreateAttachment 操作](createattachment-operation.md)请求中缺少必需的属性时，将返回此错误。 响应中包含缺少的属性 URI。  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |此错误指示调用方指定的文件夹不是 "联系人" 文件夹到[ResolveNames 操作](resolvenames-operation.md)。  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |此错误指示调用方已将多个联系人文件夹指定为[ResolveNames 操作](resolvenames-operation.md)。  <br/> |
|ErrorResponseSchemaValidation  <br/> |不使用此响应代码。  <br/> |
|ErrorRestrictionTooLong  <br/> |如果限制包含超过255个节点，则会出现此错误。  <br/> |
|ErrorRestrictionTooComplex  <br/> |当 Exchange Web 服务无法评估限制时，将发生此错误。  <br/> |
|ErrorResultSetTooBig  <br/> |此错误指示给定收件人的日历条目数超过了允许的最大限制（1000）。 请缩小窗口，然后重试。  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |如果找不到[SavedItemFolderId](saveditemfolderid.md) ，则会发生此错误。  <br/> |
|ErrorSchemaValidation  <br/> | 当无法针对架构验证请求时，将发生此错误。  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |此错误指示搜索文件夹已创建，但从未对该文件夹设置搜索条件。 仅当您访问使用另一个 API 或客户端创建的损坏的搜索文件夹时，才会发生这种情况。 若要修复此错误，请使用[UpdateFolder 操作](updatefolder-operation.md)将[SearchParameters](searchparameters.md)元素设置为包含文件夹上应包含的限制。  <br/> |
|ErrorSendAsDenied  <br/> | 当同时发生以下两种情况时，将发生此错误： <br/> <br/>-已向用户授予 CanActAsOwner 权限，但未向其授予对主体邮箱的代理权限。  <br/>-相同的用户尝试使用 SendAndSaveCopy 选项在主体的邮箱中创建和发送电子邮件。<br/>  <br/>  结果是一个 ErrorSendAsDenied 错误，并在主体的 "草稿" 文件夹中创建电子邮件。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |如果请求中缺少**SendMeetingCancellations**属性，并且要删除的项目是日历项目，则[DeleteItem 操作](deleteitem-operation.md)将返回此错误。  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |如果请求中缺少**SendMeetingInvitationsOrCancellations**属性，并且要更新的项目是日历项目，则[UpdateItem 操作](updateitem-operation.md)将返回此错误。  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |如果请求中缺少**SendMeetingInvitations**属性，并且要创建的项目是日历项目，则[CreateItem 操作](createitem-operation.md)将返回此错误。  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |此错误指示组织者发送会议请求之后，无法更新该请求。 若要修改会议，请修改日历项目，而不是会议请求。  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |此错误指示任务发起人发送任务请求后，不能更新该请求。  <br/> |
|ErrorServerBusy  <br/> |当服务器正忙时，将发生此错误。  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |此错误指示 Exchange Web 服务尝试将用户可用性请求代理到收件人的相应林，但由于服务发现失败，无法确定将请求发送到的位置。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |此错误指示未在 Active Directory 数据库中设置外部 URL 属性。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |此错误指示同步共享文件夹的尝试失败。 <br/><br/>当发生以下情况时，将返回此错误代码：<br/><br/>-找不到共享文件夹的订阅。<br/>-找不到共享文件夹。<br/>-找不到相应的目录用户。<br/>-用户已不再存在。<br/>-约会无效。<br/>-联系人项目无效。<br/>-远程服务器出现通信故障。  <br/> |
|ErrorStaleObject  <br/> |在[UpdateItem 操作](updateitem-operation.md)或[SendItem 操作](senditem-operation.md)中，如果更改的键不是最新的或未提供，则会发生此错误。 调用[GetItem 操作](getitem-operation.md)以检索更新的更改密钥，然后再次尝试该操作。  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |此错误指示用户不能立即发送更多请求，因为已达到提交配额。  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |当您尝试使用未创建该订阅的帐户访问订阅时，将发生此错误。 每个订阅仅可由订阅者访问。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |此错误指示您不能创建订阅（如果您不是所有者），也不具有对邮箱的所有者访问权限。  <br/> |
|ErrorSubscriptionNotFound  <br/> |如果找不到与指定的[SubscriptionId （GetEvents）](subscriptionid-getevents.md)对应的订阅，则会发生此错误。 订阅可能已过期，Exchange Web 服务进程可能已重新启动，或者传入了无效订阅。 如果订阅有效，请使用最新的水印重新创建订阅。 这是由[取消订阅操作](unsubscribe-operation.md)或[GetEvents 操作](getevents-operation.md)响应返回的。  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |对已取消订阅的订阅发出请求时，必须返回此错误代码。  <br/> |
|ErrorSyncFolderNotFound  <br/> |如果找不到指定的父文件夹， [SyncFolderItems 操作](syncfolderitems-operation.md)将返回此错误。  <br/> |
|ErrorTeamMailboxNotFound  <br/> |此错误指示找不到团队邮箱。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |此错误指示找到了一个团队邮箱，但它未链接到 SharePoint 服务器。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |此错误指示找到了一个团队邮箱，但指向 SharePoint Server 的链接无效。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |不使用此错误代码。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |不使用此错误代码。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |此错误指示尝试向团队邮箱所有者发送通知时失败。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |此错误指示在尝试访问团队邮箱时可能出现的常规错误。 请稍后再尝试提交请求。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTimeIntervalTooBig  <br/> |此错误指示指定的时间窗口大于允许的限制。 默认情况下，允许的限制为42。  <br/> |
|ErrorTimeoutExpired  <br/> | 当没有足够的时间来完成请求的处理时，将发生此错误。  <br/> |
|ErrorTimeZone  <br/> |此错误指示存在时区错误。  <br/> |
|ErrorToFolderNotFound  <br/> |此错误指示目标文件夹不存在。  <br/> |
|ErrorTokenSerializationDenied  <br/> |如果调用方尝试执行令牌序列化请求，但在客户端访问服务器上没有 Exch-EPI-TokenSerialization 权限，则会发生此错误。  <br/> |
|ErrorTooManyObjectsOpened  <br/> |当超出打开的对象的内部限制时，将发生此错误。  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |此错误指示用户的拨号计划不可用。  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |此错误指示找不到用户。  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |此错误指示可以找到用于拨号计划的有效服务器来处理该请求。  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |不使用此响应代码。  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |当尝试从组中删除 IM 联系人失败时，将发生此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnsupportedCulture  <br/> |当您尝试将**区域性**属性设置为无法通过**系统. 全球化**类解析的值时，将发生此错误。  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |当调用方尝试使用类型对象、对象数组、错误或 null 的扩展属性时，将发生此错误。  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |当您尝试检索或设置项目（而不是[PostItem](postitem.md)、 [Message](message-ex15websvcsotherref.md)或[CalendarItem](calendaritem.md)对象）的 MIME 内容时，会发生此错误。  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |当调用方传递对查询无效的属性时，将发生此错误。 使用计算属性时，可能会发生这种情况。  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |当调用方传递对 sort 或 group by 属性无效的属性时，将发生此错误。 使用计算属性时，可能会发生这种情况。  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |不使用此响应代码。  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |此错误指示搜索文件夹限制可能有效，但 EWS 不支持它。  <br/> |
|ErrorUnsupportedRecurrence  <br/> |此错误指示任务不支持指定的定期。  <br/> |
|ErrorUnsupportedSubFilter  <br/> |不使用此响应代码。  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |此错误指示 Exchange Web 服务在存储区中找到了属性类型，但它无法为属性类型生成 XML。  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |此错误指示在更新代理后未能保存委派列表。  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |当更改说明中列出的单个属性路径与实际[项目](item.md)或[文件夹](folder.md)对象中设置的单个属性路径不匹配时，将发生此错误。  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |此错误指示请求者未启用。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |此错误指示请求者尝试将其 "日历" 或 "联系人" 文件夹中的权限授予外部用户，但分配给请求者的共享策略指示该策略中未列出外部用户的域。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指示请求者的组织具有一组联合域，但请求者的组织没有与其中一个联合域的任何 SMTP 代理地址。  <br/> |
|ErrorValueOutOfRange  <br/> |此错误指示日历视图的开始日期或结束日期设置为 1/1/0001 12:00:00 AM 或 12/31/9999 11:59:59 PM。  <br/> |
|ErrorVirusDetected  <br/> |此错误指示 Exchange 存储在邮件中检测到病毒。  <br/> |
|ErrorVirusMessageDeleted  <br/> |此错误指示 Exchange 存储在邮件中检测到病毒并将其删除。  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |不使用此响应代码。  <br/> |
|ErrorWebRequestInInvalidState  <br/> |不使用此响应代码。  <br/> |
|ErrorWin32InteropError  <br/> |此错误指示在与非托管代码通信的过程中发生内部错误。  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |不使用此响应代码。  <br/> |
|ErrorWrongServerVersion  <br/> |此错误指示仅可对与邮箱服务器版本相同的服务器发出请求。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |此错误指示代理与主体的邮箱服务器具有不同的服务器版本的请求。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |永远不会返回此错误代码。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |指定存在重复的 SOAP 标头。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | 指定同步共享文件夹的尝试失败。<br/><br/> 以下情况时，必须返回以下错误代码：<br/><br/>-找不到共享文件夹的订阅。  <br/>-找不到共享文件夹。  <br/>-找不到相应的目录用户。  <br/>-用户已不再存在。  <br/>-约会无效。  <br/>-联系人项目无效。  <br/>-远程服务器出现通信故障。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |指定未在 Active Directory 数据库中设置外部 URL 属性。 如果未在 Active Directory 数据库中设置外部 URL 属性，则必须返回此错误代码。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |指定为获取通讯组列表的忙/闲信息而达到的最大组成员数。 如果达到了获取通讯组列表的忙/闲信息的最大组成员数，则必须返回此错误。  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |指定 DataType 和 ShareFolderId 元素都存在于请求中。 如果 DataType 和 ShareFolderId 元素都存在于请求中，则必须返回此错误代码。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |指定呼叫者尝试将其 "日历" 或 "联系人" 文件夹中的权限授予另一个组织中的用户，并且尝试失败。 当为呼叫者禁用共享策略时，或者当分配给呼叫者的共享策略不允许对请求的级别或请求的文件夹类型进行共享时，必须返回此错误代码。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |指定请求者尝试将其 "日历" 或 "联系人" 文件夹中的权限授予外部用户，但分配给请求程序的共享策略指定外部用户的域未在策略中列出。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |指定请求者尝试将其 "日历" 或 "联系人" 文件夹中的权限授予外部用户，但分配给请求程序的共享策略指定了请求的权限级别高于共享策略所允许的级别。  <br/> |
|ErrorOrganizationNotFederated  <br/> |指定请求者的组织不是联合的，因此请求者无法创建要发送给外部用户的共享邮件或无法接受从外部用户接收的共享邮件。 如果请求者的组织不是联合的，则必须返回此错误代码。  <br/> |
|ErrorMailboxFailover  <br/> |指定尝试访问邮箱失败，因为邮箱处于故障转移过程中。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |指定共享邀请发件人未创建共享邀请元数据。 如果共享邀请发件人未创建共享邀请元数据，则必须返回此错误代码。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |指定邮件跟踪服务无法跟踪邮件。  <br/> |
|ErrorMessageTrackingTransientError  <br/> |指定邮件跟踪服务为 "关闭" 或 "忙"。 此错误代码指定一个暂时性错误。 在收到此错误时，客户端可以重试连接到服务器。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |指定找不到给定的域。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指定请求者的组织具有一组联合域，但请求者的组织没有与其中一个联合域的任何 SMTP 代理地址。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |指定呼叫者请求其他组织中某个用户的忙/闲信息，但该组织关系未启用忙/闲信息。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |指定未正确配置请求者的组织联合对象。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |指定不应将共享邮件用于呼叫者。  <br/> |
|ErrorInvalidSharingData  <br/> |指定共享元数据无效。 这可能是由无效的 XML 引起的。  <br/> |
|ErrorInvalidSharingMessage  <br/> |指定共享邮件无效。 这可能是由于缺少属性造成的。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |指定不支持共享邮件。  <br/> |
|ErrorApplyConversationActionFailed  <br/> |如果无法将操作应用于会话中的一个或多个项目，则必须返回此错误。  <br/> |
|ErrorInboxRulesValidationError  <br/> |如果任何规则未验证，则必须返回此错误。  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |当另一个客户端访问收件箱规则后尝试管理收件箱规则时，必须返回此错误。  <br/> |
|ErrorRulesOverQuota  <br/> |当超过用户的规则配额时，必须返回此错误。  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |如果打开第二个订阅连接，则必须将此错误返回到第一个订阅连接。  <br/> |
|ErrorMissedNotificationEvents  <br/> |如果事件通知丢失，则必须返回此错误。  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |当 Active Directory 域服务（AD DS）中存在重复的旧版可分辨名称时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |此错误指示获取客户端访问令牌的请求无效。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorNoSpeechDetected  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUMServerUnavailable  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorRecipientNotFound  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorRecognizerNotInstalled  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSpeechGrammarError  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |如果 SOAP 标头中的[get-managementrole](managementrole.md)标头不正确，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesDisabled  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |此错误仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorWeatherServiceDisabled  <br/> |此错误仅供内部使用。  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |在未使用[QueryString （String）](querystring-string.md)元素进行内容索引搜索的情况下执行范围搜索尝试时，将返回此错误。 这适用于**SearchMailboxes**和**FindConversation**操作。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |当存档邮箱搜索不成功时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |当存档邮箱的 URL 不可发现时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |如果获取远程存档邮箱文件夹的操作失败，则会出现此错误。  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |如果查找远程存档邮箱文件夹的操作失败，则会出现此错误。  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |当无法获取远程存档邮箱项目的操作失败时，将发生此错误。  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |当导出远程存档邮箱项目的操作失败时，将发生此错误。  <br/> |
|ErrorInvalidPhotoSize  <br/> |如果从服务器请求的照片大小无效，则会返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |在**GetUserPhoto**操作请求中请求意外的照片大小时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |当**SearchMailboxes**操作请求包含过多要搜索的邮箱时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |此错误指示未找到此用户的保留标记。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |在租户或服务器上禁用发现搜索时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |当尝试使用[SeekToConditionPageItemView](seektoconditionpageitemview.md)调用[FindItem 操作](finditem-operation.md)以获取日历项目（不受支持）时，将发生此错误。  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |此错误仅供内部使用。  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |租户被标记为要删除。  <br/> |
|ErrorInvalidLicense  <br/> |用户没有有效的许可证。  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |已超出每个文件夹接收配额的邮件。  <br/> |
   
## <a name="remarks"></a>备注

此元素不是必需的，也不包含在所有响应中。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

