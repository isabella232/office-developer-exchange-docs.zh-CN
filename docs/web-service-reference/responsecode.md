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
description: ResponseCode 元素提供了有关请求的状态信息。
ms.openlocfilehash: 7baeb0ab87ffb43ba9d6b4016477888aa4ed613e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827294"
---
# <a name="responsecode"></a>ResponseCode

**ResponseCode**元素提供了有关请求的状态信息。 
  
- [ResponseMessage](responsemessage.md) 
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|元素|说明|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | 提供有关的响应状态的描述性信息。<br/><br/>  以下是此元素可能 XPath 表达式：<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |包含状态和结果的一个[删除项操作](deleteitem-operation.md)请求。  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |包含状态和的单个结果[SendItem 操作](senditem-operation.md)请求。  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |包含状态和的单个结果[DeleteFolder 操作](deletefolder-operation.md)请求。  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含状态和的单个结果[DeleteAttachment 操作](deleteattachment-operation.md)请求。  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |包含状态和的单个结果[取消操作](unsubscribe-operation.md)请求。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含状态和的单个结果[CreateFolder 操作](createfolder-operation.md)请求。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含状态和的单个结果[GetFolder 操作](getfolder-operation.md)请求。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含状态和的单个结果[UpdateFolder 操作](updatefolder-operation.md)请求。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含状态和的单个结果[MoveFolder 操作](movefolder-operation.md)请求。  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含状态和的单个结果[CopyFolder 操作](copyfolder-operation.md)请求。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含状态和的单个结果[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求。  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含状态和的单个结果[FindFolder 操作](findfolder-operation.md)请求。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含状态和的单个结果[CreateItem operation，](createitem-operation.md)请求。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含状态和的单个结果[GetItem 操作](getitem-operation.md)请求。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含状态和的单个结果[UpdateItem 操作](updateitem-operation.md)请求。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含状态和的单个结果[MoveItem 操作](moveitem-operation.md)请求。  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含状态和的单个结果[CopyItem 操作](copyitem-operation.md)请求。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含状态和的单个结果[CreateAttachment 操作](createattachment-operation.md)请求。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含状态和的单个结果[GetAttachment 操作](getattachment-operation.md)请求。  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含状态和的单个结果[FindItem 操作](finditem-operation.md)请求。  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含状态和[ResolveNames 操作](resolvenames-operation.md)请求的结果。  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含状态和的单个结果[ExpandDL 操作](expanddl-operation.md)请求。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含状态和的单个结果[Subscribe 操作](subscribe-operation.md)请求。  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含状态和的单个结果[GetEvents 操作](getevents-operation.md)请求。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含状态和单个 SendNotification 操作请求的结果。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含状态和[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)请求的结果。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含状态和[SyncFolderItems 操作](syncfolderitems-operation.md)请求的结果。  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含状态和[ConvertId 操作](convertid-operation.md)请求的结果。  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |包含状态和[AddDelegate 操作](adddelegate-operation.md)请求的结果。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含状态和[GetDelegate 操作](getdelegate-operation.md)请求的结果。  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |包含状态和[RemoveDelegate 操作](removedelegate-operation.md)请求的结果。  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |包含状态和[UpdateDelegate 操作](updatedelegate-operation.md)请求的结果。  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |包含状态和[GetServerTimeZones 操作](getservertimezones-operation.md)请求的结果。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含状态和[GetSharingFolder 操作](getsharingfolder-operation.md)请求的结果。  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |定义[GetSharingFolder 操作](getsharingfolder-operation.md)请求的响应。  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |包含状态和[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的结果。  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |包含状态和[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的结果。  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |定义[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的响应。  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |包含状态和[FindConversation 操作](findconversation-operation.md)的响应的结果。  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |包含状态和[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的结果。  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |包含状态和的单个结果[EmptyFolder 操作](emptyfolder-operation.md)请求。  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |包含状态和[UpdateInboxRules 操作](updateinboxrules-operation.md)请求的结果。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含状态和[UploadItems 操作](uploaditems-operation.md)请求的结果。  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |包含对[GetInboxRules 操作](getinboxrules-operation.md)的响应 *** 请求。  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |包含[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)请求的响应。  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要的文本值。 下表介绍返回与此元素的值。
  
|值|说明|
|:-----|:-----|
|NoError  <br/> |请求不出现任何错误。  <br/> |
|ErrorAccessDenied  <br/> |调用帐户没有执行请求的操作的权限时，将发生此错误。  <br/> |
|ErrorAccessModeSpecified  <br/> |此错误是仅供内部使用。 不返回此错误。  <br/> |
|ErrorAccountDisabled  <br/> |问题的帐户已被禁用时，将发生此错误。  <br/> |
|ErrorAddDelegatesFailed  <br/> |无法保存具有添加代理人的列表时，将发生此错误。  <br/> |
|ErrorAddressSpaceNotFound  <br/> |无法在 Active Directory 数据库中找到的地址空间记录或域名系统 (DNS) 域名，跨林可用性时，将发生此错误。  <br/> |
|ErrorADOperation  <br/> |操作失败，因为与 Active Directory 域服务 (AD DS) 的通信问题时，将发生此错误。  <br/> |
|ErrorADSessionFilter  <br/> |当**ResolveNames**操作请求指定的名称，则返回此错误的无效。  <br/> |
|ErrorADUnavailable  <br/> |AD DS 不可用时，将发生此错误。 稍后重试您的请求。  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |此错误表明未指定了**AffectedTaskOccurrences**属性。 当[删除项](deleteitem.md)元素用于删除至少一个项目的任务，具有无论是否该任务定期与否， **AffectedTaskOccurrences**属性，以便**删除项**可以确定要指定是否删除当前的匹配项或整个数据系列。  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |指示创建存档文件夹路径中的错误。  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |指示已不启用存档邮箱。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |指示该存档邮箱服务发现失败。  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |指定尝试使用 10 个以上的嵌套附件创建项目。 此值是在 Exchange Server 2010 Service Pack 2 (SP2) 中引入的。  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |如果尝试创建具有超过 Int32.MaxValue，以字节为单位的大小的附件， [CreateAttachment](createattachment.md)元素返回此错误。  <br/> 如果尝试检索现有附件大小超过 Int32.MaxValue，以字节为单位， [GetAttachment](getattachment.md)元素返回此错误。  <br/> |
|ErrorAutoDiscoverFailed  <br/> |此错误指示 Exchange Web 服务尝试确定运行 Exchange 2010 的跨林计算机的位置具有使用自动发现服务，但对自动发现服务的调用安装了客户端访问服务器角色失败。  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |此错误指示 AD DS 中缺少本地林中的可用性配置信息。  <br/> |
|ErrorBatchProcessingStopped  <br/> | 此错误指示处理项目时出现异常并且例外是有可能出现的项之后。 请求可能包括多个项目;例如，GetItem 操作请求可能包含多个标识符。 一般情况下，项目是一次处理的一个。 如果在处理项目时发生异常和可能的项之后出现的异常，将不会处理之后的项。  <br/><br/>  将停止处理的项目执行的错误的示例如下：<br/>  <br/>-ErrorAccessDenied  <br/>-ErrorAccountDisabled  <br/>-ErrorADUnavailable  <br/>-ErrorADOperation  <br/>-ErrorConnectionFailed  <br/>-ErrorMailboxStoreUnavailable  <br/>-ErrorMailboxMoveInProgress  <br/>-ErrorPasswordChangeRequired  <br/>-ErrorPasswordExpired  <br/>-ErrorQuotaExceeded  <br/>-ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |当尝试移动或复制的定期日历项目，将发生此错误。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | 当尝试更新日历项目位于已删除邮件文件夹和时会议更新或取消要发送根据**SendMeetingInvitationsOrCancellations**属性的值，将发生此错误。 <br/><br/>以下是该属性可能的值：  <br/><br/>-SendToAllAndSaveCopy  <br/>-SendToChangedAndSaveCopy  <br/>-SendOnlyToAll  <br/>-SendOnlyToChanged  <br/>  <br/>但是，此属性的值设置为 SendToNone 时才允许此类更新。  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |调用 UpdateItem、 GetItem、 删除项、 MoveItem、 CopyItem 或 SendItem 操作，并指定 ID 不匹配项的 ID 的任何定期日历项目时，将发生此错误。  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |当调用**UpdateItem**、 **GetItem**、**删除项**、 **MoveItem**、 **CopyItem**或**SendItem**操作，并指定 ID 不是任何定期主项目的 ID，将发生此错误。  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |此操作期间发生错误**CreateItem**或**UpdateItem**如果日历项目持续时间超过最大允许，它是当前 5 年。  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |当日历结束时间设置为同时或开始时间后，将发生此错误。  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |**FindItem**操作[CalendarView](calendarview.md)元素指定的文件夹不是日历文件夹类型时，将发生此错误。  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |不使用此响应代码。  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |一天、 WeekendDay，和 Weekday 无效值用于定义时间更改模式时， **CreateItem**或**UpdateItem**操作期间发生此错误。  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |何时使用 Day、 WeekDay，和 WeekendDay 无效值来指定每周定期**CreateItem**或**UpdateItem**操作期间发生此错误。  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |日历项重复二进制大型对象 (BLOB) Exchange 存储中的状态无效时，将发生此错误。  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |不使用此响应代码。  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |无法创建指定的定期时，将发生此错误。  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |当遇到时区无效时，将发生此错误。  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |此错误指示日历项目已被取消。  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |此错误指示[AcceptItem](acceptitem.md)元素委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |此错误指示[DeclineItem](declineitem.md)元素委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |此错误指示[RemoveItem](removeitem.md)元素是无效的委派方案中取消会议。  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |此错误指示[TentativelyAcceptItem](tentativelyacceptitem.md)元素委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |此错误指示上的日历项目的操作 (当前 CancelItem) attendee 无效。 只有会议组织者可以取消会议。  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |此错误指示[AcceptItem](acceptitem.md)组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |此错误指示[DeclineItem](declineitem.md)组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |此错误指示[RemoveItem](removeitem.md)组织者的日历项目无效。 若要从日历中删除会议，组织者必须使用 CancelCalendarItem。  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |此错误指示[TentativelyAcceptItem](tentativelyacceptitem.md)组织者的日历项目无效。  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |此错误指示会议请求已过期，且无法更新。  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |此错误指示事件索引不指向当前重复周期内出现情况排序。 例如，如果您定期模式定义三个会议的一组并尝试访问的第五个匹配项，将导致此响应代码。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |此错误指示 （通过定期主控形状的 ID 和出现索引寻址） 已删除出现任何操作无效。  <br/> |
|ErrorCalendarOutOfRange  <br/> |该属性值超出范围时，将在日历项目或任务定期属性的 CreateItem 和 UpdateItem 操作报告此错误。 例如，指定相应月份的第十五个星期将导致此响应代码。  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |发生此错误的[CalendarView](calendarview.md)元素是多个允许，当前 2 年的最大时开始到结束范围。  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |此错误指示请求的帐户不是有效帐户目录数据库中。  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |指示尝试日历联系人任务文件夹进行存档。  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |指示尝试存档公用文件夹中的项目。  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |指示该尝试进行存档的存档邮箱中的项目。  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |正在创建日历项目和**SavedItemFolderId**属性引用了非日历文件夹时，将发生此错误。  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |正在创建联系人和**SavedItemFolderId**属性引用了非联系人文件夹时，将发生此错误。  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |此错误表明，不能在邮件文件夹，例如日历、 联系人、 任务、 注释等之外的文件夹中创建一个公告项目。  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |正在创建任务和**SavedItemFolderId**属性引用了非任务文件夹时，将发生此错误。  <br/> |
|ErrorCannotDeleteObject  <br/> |无法删除项目或文件夹以删除时，将发生此错误。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |[删除项操作](deleteitem-operation.md)删除定期任务的当前匹配项失败时返回此错误。 如果**AffectedTaskOccurrences**属性已设置为 SpecifiedOccurrenceOnly，这只会发生。  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |指示尝试禁用 mandatorty 扩展。  <br/> |
|ErrorCannotEmptyFolder  <br/> |当服务器无法清空文件夹时，必须返回此错误。  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |指示无法检索源文件夹路径。  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |指定服务器无法检索的 Outlook Web App 选项的外部 URL。  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |**GetAttachment**操作返回此错误，如果它不能检索文件附件的正文。  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |此错误指示呼叫者尝试设置非日历文件夹日历权限。  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |此错误指示呼叫者尝试设置非日历权限日历文件夹。  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |此错误指示您不能中设置的权限设置未知的权限。  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |指示尝试与源文件夹中指定的搜索文件夹。  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |当需要项标识符的请求都有一个文件夹标识符，将发生此错误。  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |需要文件夹标识符的请求给定项标识符时，将发生此错误。  <br/> |
|ErrorChangeKeyRequired  <br/> |已由**ErrorChangeKeyRequiredForWriteOperations**取代此响应代码 <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |为某个项目的更改密钥缺失或过期时，将返回此错误。 <br/><br/>SendItem、 UpdateItem 和 UpdateFolder 操作，呼叫者必须通过在项目的正确和当前更改键。 请注意这是与 UpdateItem 的情况，即使指定在冲突解决设置始终覆盖。  <br/> |
|ErrorClientDisconnected  <br/> |指定客户端已断开连接。  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorClientIntentNotFound  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorConnectionFailed  <br/> |Exchange Web 服务无法连接到邮箱时，将发生此错误。  <br/> |
|ErrorContainsFilterWrongType  <br/> |此错误指示被检测为包含筛选器的属性不是字符串类型。  <br/> |
|ErrorContentConversionFailed  <br/> |**GetItem**操作返回此错误时无法检索到该项目的 MIME 内容 Exchange Web 服务请求。 <br/><br/>Exchange Web 服务无法从提供的 MIME 内容中创建项时， **CreateItem** operation 返回此错误。 通常，这是指示 item 属性是损坏或被截断。  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |使用查询字符串选项进行搜索请求和对目标邮箱不启用内容索引时，将发生此错误。  <br/> |
|ErrorCorruptData  <br/> |当的数据已损坏，并且无法处理，将发生此错误。  <br/> |
|ErrorCreateItemAccessDenied  <br/> |当呼叫者没有权限来创建项时，将发生此错误。  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |此错误发生时一个或多个已 CreateManagedFolder 操作请求中指定的托管文件夹无法创建。 搜索来确定已创建的文件夹和文件夹不存在的每个文件夹。  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |调用帐户未安装所需创建子文件夹的权限时，将发生此错误。  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |尝试将项目或文件夹从一个邮箱移动到另一个时发生此错误。 如果具有不同源邮箱和目标邮箱，则会收到此错误。  <br/> |
|ErrorCrossSiteRequest  <br/> |此错误指示请求不允许，因为应为请求提供服务的客户端访问服务器位于不同的网站。  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |在下列情况下会出现此错误：<br/>  <br/>-尝试访问或写入项目上的一个属性，该属性值过大。<br/>-Base64 编码的 MIME 内容请求 XML 中的长度超过了限制。<br/>-的现有项目正文的正文大小超过此限制。<br/>-使用者会尝试设置其长度 （或对于 append 组合的长度） 超出限制 HTML 或文本正文。 |
|ErrorDataSourceOperation  <br/> |基础数据提供程序无法完成操作时，将发生此错误。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |当指定的用户的代理人列表中已存在，则将发生此错误**AddDelegate**操作中。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |指定要添加的用户时的邮箱的所有者，则将发生此错误**AddDelegate**操作中。  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |当也没有任何本地 FreeBusy 邮件上的委托信息或没有 Active Directory 公共委托 （没有"公共委托"或任何 AD DS 中的"代表发送"项），则将发生此错误**GetDelegate**操作中。  <br/> |
|ErrorDelegateNoUser  <br/> |当指定的用户无法映射到 AD DS 中的用户，将发生此错误。  <br/> |
|ErrorDelegateValidationFailed  <br/> |当添加的代理用户无效，则将发生此错误**AddDelegate**操作中。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |尝试删除的可分辨的文件夹时发生此错误。  <br/> |
|ErrorDeleteItemsFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |此错误指示的可分辨的用户 ID 操作无效。 **DistinguishedUserType**不应存在于请求中。  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |此错误指示请求通讯组列表成员不存在通讯组列表中。  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |重复的文件夹名称指定的**CreateManagedFolder**操作请求[FolderNames](foldernames.md)元素中时，将发生此错误。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |此错误指示有重复的 SOAP 标头。  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |此错误指示的重复的用户 ID 已找到权限集中有重复 Sid 或收件人或多次，设置默认或匿名。  <br/> |
|ErrorEmailAddressMismatch  <br/> |请求尝试创建/更新的搜索文件夹的搜索参数时，将发生此错误。 例如，这会时发生的邮箱中创建搜索文件夹，但搜索文件夹定向以查找另一个邮箱中。  <br/> |
|ErrorEventNotFound  <br/> |事件返回之前删除与水印相关联的事件时，将发生此错误。 返回此错误时，也将删除订阅。  <br/> |
|ErrorExceededConnectionCount  <br/> |此错误的指示有更多并发请求针对服务器所允许的用户策略。  <br/> |
|ErrorExceededSubscriptionCount  <br/> |此错误指示用户的限制的策略已超出最大订阅计数。  <br/> |
|ErrorExceededFindCountLimit  <br/> |此错误表明搜索操作调用超过的可返回的项目总数。  <br/> |
|ErrorExpiredSubscription  <br/> |如果正在被删除订阅，因为它已过期时调用[GetEvents 操作](getevents-operation.md)，将发生此错误。  <br/> |
|ErrorExtensionNotFound  <br/> |指示找不到该扩展名。  <br/> |
|ErrorFolderCorrupt  <br/> |在该文件夹已损坏，无法保存时，将发生此错误。  <br/> |
|ErrorFolderExists  <br/> |在尝试创建具有相同的名称为另一个文件夹中同一个父文件夹时，将发生此错误。 不允许重复的文件夹的名称。  <br/> |
|ErrorFolderNotFound  <br/> |此错误指示指定的文件夹 ID 不对应一个有效的文件夹，或委托不具有访问该文件夹的权限。  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |此错误指示无法检索请求的属性。 这并不表示，该属性不存在，但属性已损坏以某种方式，以便检索失败。  <br/> |
|ErrorFolderSave  <br/> |此错误指示文件夹无法创建或更新由于无效状态。  <br/> |
|ErrorFolderSaveFailed  <br/> |此错误指示文件夹无法创建或更新由于无效状态。  <br/> |
|ErrorFolderSavePropertyError  <br/> |此错误指示文件夹无法创建或更新由于无效的属性值。 响应代码列出导致问题的属性。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |此错误指示已获得忙/闲信息的通讯组列表已达到最大组成员计数。  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |因为中间失败而无法检索忙/闲信息时，将返回此错误。  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorImContactLimitReached  <br/> |由于已达到的最大联系人数，不能添加新的即时消息 (IM) 联系人时，将返回此错误。 此错误是在 Exchange Server 2013 中引入的。  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |当尝试现有组已具有相同的显示名称时，添加一个组显示名称，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorImGroupLimitReached  <br/> |由于已达到最大组数，则不能添加新的 IM 组时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorImpersonateUserDenied  <br/> |返回的错误是在服务器到服务器授权的情况下为 Exchange 模拟时调用方没有模拟特定用户的适当权限问题。 此错误映射到 ms-Exch-EPI-月-模拟扩展 Active Directory 权限。  <br/> |
|ErrorImpersonationDenied  <br/> |当呼叫者没有模拟通过他们正在对请求的客户端访问服务器的适当权限时，将在 Exchange 模拟的服务器到服务器授权返回此错误。 这将映射到 ms Exch-EPI-模拟扩展 Active Directory 权限。  <br/> |
|ErrorImpersonationFailed  <br/> |此错误指示尝试执行服务器到服务器身份验证时出现意外的错误。 此响应代码通常指示任一的 Exchange Web 服务不能与目录，或者林之间的信任不会正确运行应用程序池配置不正确，Exchange Web 服务的服务帐户配置。  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |此错误指示请求是有效的当前的 Exchange Server 版本，但无效已指定的请求服务器版本。  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |此错误指示[UpdateItem](updateitem.md)或[UpdateFolder](updatefolder.md)元素中的每个更改说明必须列出要更新的只有一个属性。  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |请求包含太多与会者解决时，将发生此错误。 默认情况下，与会者解析的最大数量为 100。  <br/> |
|ErrorInsufficientResources  <br/> |在邮箱服务器过载时，将发生此错误。 稍后重试您的请求。  <br/> |
|ErrorInternalServerError  <br/> |此错误指示 Exchange Web 服务遇到错误，无法恢复从，并且不存在与所发生的错误相关联的更多特定响应代码。  <br/> |
|ErrorInternalServerTransientError  <br/> |此错误指示发生了内部服务器错误和应稍后重新尝试您的请求。  <br/> |
|ErrorInvalidAccessLevel  <br/> |此错误指示的呼叫者对忙/闲数据的访问级别无效。  <br/> |
|ErrorInvalidArgument  <br/> |此错误指示由所有无效的参数传递到[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)导致的错误。<br/><br/> 在以下情况下会返回此错误： <br/><br/>指定中-用户_发送-作为_参数不存在目录中。 <br/>指定中-用户_发送-作为_参数不是唯一的目录中。 <br/>-_发送-作为_地址为空。<br/>-_发送-作为_地址不是有效的电子邮件地址。  <br/> |
|ErrorInvalidAttachmentId  <br/> |[GetAttachment 操作](getattachment-operation.md)返回此错误或找不到[DeleteAttachment 操作](deleteattachment-operation.md)时指定 ID 所对应的附件。  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |当您尝试使用复杂的附件表限制绑定到现有搜索文件夹时，将发生此错误。 Exchange Web 服务仅支持简单包含针对附件表筛选器。 如果您尝试绑定到现有搜索文件夹具有更复杂的附件表限制 （筛选），则 Exchange Web 服务无法呈现为该筛选器的 XML，并返回此响应代码。 <br/><br/>请注意，您仍然可以调用 GetFolder 操作的文件夹，但不是请求[SearchParameters](searchparameters.md)元素。  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |当您尝试使用复杂的附件表限制绑定到现有搜索文件夹时，将发生此错误。 Exchange Web 服务仅支持简单包含针对附件表筛选器。 <br/><br/>如果您尝试绑定到现有搜索文件夹具有更复杂的附件表限制，Exchange Web 服务无法呈现为该筛选器的 XML。 在这种情况下，附件筛选包含文本筛选器，但不是看附件显示名称。<br/><br/> 请注意，您仍然可以调用 GetFolder 操作的文件夹，但不是请求[SearchParameters](searchparameters.md)元素。  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | 此错误指示请求者的授权过程失败。  <br/> |
|ErrorInvalidChangeKey  <br/> |当使用者使用更改密钥是无法分析传入文件夹或项目标识符中时，将发生此错误。 例如，这可能是无效的 base64 内容或空字符串。  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |此错误指示当尝试解析的调用方标识存在内部错误。  <br/> |
|ErrorInvalidCompleteDate  <br/> |当尝试将一个任务的[CompleteDate](completedate.md)元素值设置为将来的时间，则返回此错误。 时将转换为本地时间的客户端访问服务器，则不能[CompleteDate](completedate.md)任务的设置为晚于客户端访问服务器上的本地时间值。  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |此错误表明，联系人提供电子邮件地址无效。  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |此错误指示无效的电子邮件的索引值已提供的电子邮件条目。  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |使用的凭据的到代理时，将发生此错误为不同的目录服务林请求而失败的身份验证。  <br/> |
|ErrorInvalidDelegatePermission  <br/> |此错误指示所指定的文件夹的权限无效。  <br/> |
|ErrorInvalidDelegateUserId  <br/> |此错误指示指定的委托用户 ID 无效。  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |当呼叫者不指定 UPN、 电子邮件地址或用户 SID，Exchange 模拟期间发生此错误。 如果调用方指定一个或多个那些和这些值为空，这也会发生。  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |无法分析传入[排除](excludes.md)元素限制的位掩码时，将发生此错误。  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidExtendedProperty  <br/> | 当发生以下事件时，将发生此错误： <br/> <br/>-呼叫者尝试使用 Exchange Web 服务不支持扩展的属性。  <br/>-呼叫者传入了无效的扩展属性的属性值的组合。 如果传递没有属性也会发生这种情况。 允许仅某些组合。  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |扩展属性的值部分与属性的类型不匹配时，将发生此错误。 <br/><br/>例如，设置的扩展的属性具有 PropertyType ="String"整数的数组将导致此错误。 并不强制为指定的扩展属性的类型的任何字符串表示将提供此错误。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |此错误指示共享邀请发件人未创建的共享邀请元数据。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |此错误指示的共享邮件，不应为呼叫者。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |此错误表明未正确配置请求者的组织联盟对象。  <br/> |
|ErrorInvalidFolderId  <br/> |文件夹 ID 已损坏时，将发生此错误。  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |此错误指示指定的文件夹类型为在当前操作无效。 例如，您无法在公用文件夹中创建搜索文件夹。  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | 当用户指定下列选项之一，则将发生此错误在分数分页： <br/> <br/>大于分母-分子  <br/>是-分子小于 0  <br/>小于或等于零-分母  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |此错误指示的[数据类型](datatype.md)和 ShareFolderId 元素都存在请求中。  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |当[GetUserAvailability 操作](getuseravailability-operation.md)的 None [FreeBusyViewType](freebusyviewtype.md)被调用时，将发生此错误。  <br/> |
|ErrorInvalidId  <br/> |此错误指示 ID 和/或更改密钥不正确。  <br/> |
|ErrorInvalidIdEmpty  <br/> |当呼叫者指定为空的**Id**属性时，将发生此错误。  <br/> |
|ErrorInvalidLikeRequest  <br/> |不能喜欢项目时发生此错误。 内部版本号 15.00.0913.09 开头的 Exchange 版本包括此值。  <br/> |
|ErrorInvalidIdMalformed  <br/> |调用方指定格式不正确的**Id**属性时，将发生此错误。  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |此错误指示正在使用的 Exchange 2007 格式的文件夹或项目 ID 的指定版本的 Exchange 2007 SP1 的请求或更高版本。 不能使用 Exchange 2007 SP1 或更高版本的请求中的 Exchange 2007 Id。 您需要使用[ConvertId 操作](convertid-operation.md)首先将转换。  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |当呼叫者指定太长**Id**属性时，将发生此错误。  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |只要不是项目附件 ID 传递给需要附件 ID 的 Web 服务方法的 ID，则返回此错误  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |当您的邮箱中的联系人已损坏时，将发生此错误。  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |当呼叫者指定太长**Id**属性时，将发生此错误。  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |当项目上的附件层次结构超过 255 个深度的最大时，将返回此错误。  <br/> |
|ErrorInvalidIdXml  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidImContactId  <br/> |当指定的 IM 联系人标识符不代表一个有效的标识符，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |指定的 IM 通讯组 SMTP 地址标识符不代表一个有效的标识符时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidImGroupId  <br/> |指定的 IM 组标识符不代表一个有效的标识符时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |如果索引分页的偏移量为负数，将发生此错误。  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |指示项目**ArchiveItem**操作无效。  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |尝试使用的会议请求或日历项目的项目类型 AcceptItem 响应对象或尝试接受的已删除邮件文件夹中的日历项匹配项时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |尝试使用非日历项目的项目类型 CancelItem response 对象时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | 当尝试创建项目附件的类型不受支持，则返回此错误。  <br/><br/>  支持的项目类型的项目附件包括下列对象：  <br/><br/>- [项目](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [日历项目](calendaritem.md) <br/>- [任务](task.md) <br/>- [联系人](contact.md) <br/> <br/> 例如，如果您尝试创建的[MeetingMessage](meetingmessage.md)附件，您将会遇到此响应代码。  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | 如果请求包含不受支持的项目类型，从[CreateItem operation，](createitem-operation.md)返回此错误。 <br/><br/>受支持的项包括下列对象：<br/>  <br/>- [项目](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [日历项目](calendaritem.md) <br/>- [任务](task.md) <br/>- [联系人](contact.md) <br/><br/>  某些类型都将创建为副作用执行其他操作。 会议邮件，例如，将日历项目发送给与会者; 时所创建他们不明确创建。  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |尝试使用会议请求或日历项目，项类型 DeclineItem response 对象或尝试拒绝的已删除邮件文件夹中的日历项匹配项时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |此错误指示[ExpandDL 操作](expanddl-operation.md)仅供私人通讯组列表。  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |如果请求指定项目不是会议，此错误从 RemoveItem 响应对象中返回取消项目。  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |如果请求指定不是邮件项的项，从[SendItem 操作](senditem-operation.md)返回此错误。  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |尝试使用会议请求或日历项目，项类型[TentativelyAcceptItem](tentativelyacceptitem.md)或尝试暂时接受的已删除邮件文件夹中的日历项匹配项时，将发生此错误。  <br/> |
|ErrorInvalidLogonType  <br/> |此错误是仅供内部使用。 不返回此错误。  <br/> |
|ErrorInvalidMailbox  <br/> |此错误指示[CreateItem operation](createitem-operation.md)或[UpdateItem 操作](updateitem-operation.md)失败时创建或更新个人通讯组列表。  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |托管文件夹的结构已损坏，并且无法呈现时，将发生此错误。  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |发生此错误的托管文件夹设置的配额时小于零，表示已损坏的托管的文件夹。  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |此错误发生时托管文件夹设置的大小小于零，表示已损坏的托管的文件夹。  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |提供合并忙/闲内部的值无效时，将发生此错误。 默认最小值为 5 分钟。 默认最大值为 1440 分钟。  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |名称无效[ResolveNames 操作](resolvenames-operation.md)时，将发生此错误。 例如，一个零长度字符串、 一个空格、 一个逗号和短划线是无效的所有名称。  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |此错误指示中的客户端访问服务器上的网络服务帐户的错误。  <br/> |
|ErrorInvalidOofParameter  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidOperation  <br/> | 这是无效请求的操作时使用常规错误。 <br/><br/>例如，您无法执行以下操作： <br/> <br/>-使用在公用文件夹[FindFolder 操作](findfolder-operation.md)执行"深入"遍历。  <br/>-移动或复制的公用文件夹根。  <br/>-使用任何模式，但"硬"删除删除关联的项目。  <br/>-移动或复制相关的项目。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |此错误指示呼叫者请求的其他组织中的用户的忙/闲信息但组织的关系时，没有启用忙/闲。  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |当使用者传入零或为要返回的最大行负值时，将发生此错误。  <br/> |
|ErrorInvalidParentFolder  <br/> |当使用者传入无效的父文件夹的操作时，将发生此错误。 例如，如果您尝试在搜索文件夹中创建文件夹，则返回此错误。  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |当尝试设置任务的完成百分比值无效，则返回此错误。 值必须是介于 0 和 100 （含） 之间。  <br/> |
|ErrorInvalidPermissionSettings  <br/> |此错误指示权限级别不一致的权限设置。  <br/> |
|ErrorInvalidPhoneCallId  <br/> |此错误指示呼叫者标识符无效。  <br/> |
|ErrorInvalidPhoneNumber  <br/> |此错误指示的电话号码不正确或不适合的拨号计划的规则。  <br/> |
|ErrorInvalidPropertyAppend  <br/> | 当您尝试追加到的属性不支持追加，将发生此错误。 <br/><br/>以下是支持追加的唯一属性： <br/> <br/>-收件人集合 (ToRecipients，CcRecipients，BccRecipients)  <br/>-Attendee 集 （RequiredAttendees，OptionalAttendees，资源）  <br/>正文  <br/>-回复  <br/><br/>  此外，当邮件正文追加如果请求中指定的格式不匹配的项存储区中的格式，将发生此错误。  <br/> |
|ErrorInvalidPropertyDelete  <br/> |如果删除操作指定在[UpdateItem 操作](updateitem-operation.md)或[UpdateFolder 操作](updatefolder-operation.md)调用不支持删除操作的属性，将发生此错误。 例如，您无法删除[项目](item.md)对象的[ItemId](itemid.md)元素。  <br/> |
|ErrorInvalidPropertyForExists  <br/> |如果使用者通过[Exists](exists.md)筛选器中的标志属性之一，将发生此错误。 例如，如果[Exists](exists.md)元素中指定的[IsRead](isread.md)或[IsFromMe](isfromme.md)标志，将发生此错误。 请求应改用[IsEqualTo](isequalto.md)元素对于这些与标志因此单个属性的一部分。  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |当您尝试操作的属性不支持对其执行的操作，将发生此错误。  <br/> |
|ErrorInvalidPropertyRequest  <br/> | 如果不可用该项目类型的请求中指定的属性，将发生此错误。 例如，如果[GetItem 操作](getitem-operation.md)中请求时才可用在日历项目的属性返回此错误邮件呼叫或更新[UpdateItem 操作](updateitem-operation.md)中调用的一条消息。 <br/> <br/>  这将发生以下操作： <br/> <br/>- [GetItem 操作](getitem-operation.md) <br/>- [GetFolder 操作](getfolder-operation.md) <br/>- [UpdateItem 操作](updateitem-operation.md) <br/>- [UpdateFolder 操作](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |此错误表明您试图操作的属性不支持对其执行的操作。 例如，如果您试图设置该属性是只读的则返回此错误。  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | 当客户端尝试更新已发送邮件的特定属性时， [UpdateItem 操作](updateitem-operation.md)期间发生此错误。<br/><br/> 例如，无法发送邮件更新以下属性： <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |如果您使用一个推送订阅 id。 调用[GetEvents 操作](getevents-operation.md)或[取消操作](unsubscribe-operation.md)，将发生此错误 若要取消订阅推送订阅，必须响应推送请求取消订阅的响应，或断开连接的 Web 服务并等待超时推送通知。  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | 创建"强制"订阅和指示请求中包含的 URL 无效时，将[Subscribe 操作](subscribe-operation.md)返回此错误。<br/><br/>为 Exchange Web 服务以接受 URL 必须满足以下条件： <br/> <br/>-String 长度\>0 和\<2083年。  <br/>Http 或 https 协议。  <br/>-URL 可以解析 URI Microsoft.NET Framework 类。  <br/> |
|ErrorInvalidRecipients  <br/> |此错误指示邮件的收件人集合或日历项目的与会者集合无效。 例如，当尝试发送项目已没有收件人，则将返回此错误。  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |此错误表明搜索文件夹的 Exchange Web 服务不能代表一个收件人表筛选器。 若要解决此错误，而不请求搜索参数检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |此错误表明搜索文件夹的 Exchange Web 服务不能代表一个收件人表筛选器。 若要解决此错误，而不请求搜索参数检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |此错误表明搜索文件夹的 Exchange Web 服务不能代表一个收件人表筛选器。 若要解决此错误，而不请求搜索参数检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |此错误表明搜索文件夹的 Exchange Web 服务不能代表一个收件人表筛选器。 若要解决此错误，而不请求搜索参数检索文件夹。  <br/> |
|ErrorInvalidReferenceItem  <br/> | 从以下方案中的正向和答复响应对象[CreateItem operation，](createitem-operation.md)将返回此错误：<br/>  <br/>-引用的项标识符不是[邮件](message-ex15websvcsotherref.md)、[日历项目](calendaritem.md)或**邮件**或**日历项目**的后代。  <br/>-引用的项标识符的**日历项目**并对自己组织者尝试到答复或全部答复。  <br/>-邮件是草稿，并且在选择了答复或全部答复。  <br/>-引用项目， [SuppressReadReceipt](suppressreadreceipt.md)，不是**邮件**或**消息**的后代。  <br/> |
|ErrorInvalidRequest  <br/> |SOAP 请求 SOAP 正文中具有 SOAP 操作标头，但执行任何操作时，将发生此错误。 请注意，SOAP Action 标头，则不需要 Exchange Web 服务可以确定要调用从 SOAP 正文中的根元素的本地名称的方法。  <br/> |
|ErrorInvalidRestriction  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |当指定的保留标记有与之关联的操作不正确，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |当尝试对**PolicyTag**属性设置不存在或不可见的标记，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |当尝试**PolicyTag**属性上设置隐式标记，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |指示保留标记 GUID 无效。  <br/> |
|ErrorInvalidRoutingType  <br/> |如果传递[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)元素的路由类型无效，将发生此错误。 通常情况下，传送类型设置为简单邮件传输协议 (SMTP)。  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |如果指定的工期的结束时间不大于开始时间或结束时间不会发生将来，将发生此错误。  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |此错误指示代理请求发送给另一台服务器不能因版本控制不匹配请求提供服务。  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |此错误指示存储区中日历文件夹上的 Exchange 安全描述符已损坏。  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |尝试发送的项目其中[SavedItemFolderId](saveditemfolderid.md)指定请求中但**SaveItemToFolder**属性设置为**false**时，发生此错误。  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |此错误指示标头中传递的令牌格式不正确，并不指在目录中，有效的帐户，或者缺少的主要组**ConnectingSID**。  <br/> |
|ErrorInvalidSharingData  <br/> |此错误指示共享元数据无效。 原因可能是无效的 XML。  <br/> |
|ErrorInvalidSharingMessage  <br/> |此错误指示共享邮件无效。 原因可能是一个缺少的属性。  <br/> |
|ErrorInvalidSid  <br/> |当无效 SID 传递请求中，将发生此错误。  <br/> |
|ErrorInvalidSIPUri  <br/> |此错误指示 SIP 名称、 拨号计划或电话号码是无效的 SIP Uri。  <br/> |
|ErrorInvalidServerVersion  <br/> |此错误指示无效请求的服务器版本已请求中指定。  <br/> |
|ErrorInvalidSmtpAddress  <br/> |无法解析 SMTP 地址时，将发生此错误。  <br/> |
|ErrorInvalidSubfilterType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidSubscription  <br/> |此错误指示订阅不再有效。 这可能是因为客户端访问服务器正在重新启动或订阅已过期。  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |此错误表示的 subscribe 请求包含多个公用文件夹 Id。 订阅可以包含多个文件夹从同一邮箱或一个公用文件夹的 id。  <br/> |
|ErrorInvalidSyncStateData  <br/> |如果传递的[SyncState](syncstate-ex15websvcsotherref.md)数据无效，通过[SyncFolderItems](syncfolderitems.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)返回此错误。 若要解决此错误，您必须重新同步的同步状态的情况下。 请确保如果您是持久化的同步状态 Blob、 意外未截断的 BLOB。  <br/> |
|ErrorInvalidTimeInterval  <br/> |此错误指示指定的时间间隔无效。 开始时间必须大于或等于结束时间。  <br/> |
|ErrorInvalidUserInfo  <br/> |此错误指示权限操作指定了内部不一致的[用户 Id](userid.md) 。 例如，如果指定 （默认值或匿名） 的可分辨的用户 ID，如果您还尝试指定 SID 或主 SMTP 地址或显示名称为此用户返回此错误。  <br/> |
|ErrorInvalidUserOofSettings  <br/> |此错误指示用户外出 (OOF) 设置由于缺少的内部或外部答复均无效。  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |在 Exchange 模拟期间出现此错误。 呼叫者中无效的 UPN 不可访问在目录中的 SOAP 标头中传递。  <br/> |
|ErrorInvalidUserSid  <br/> |当无效 SID 传递请求中，将发生此错误。  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |不使用此响应代码。  <br/> |
|ErrorInvalidValueForProperty  <br/> |此错误表明您要对其进行比较的属性限制中的比较值无效。<br/><br/> 例如， [DateTimeCreated](datetimecreated.md)比较值 > **，则返回 true**会返回此响应代码。 <br/><br/>如果您指定枚举属性在比较中，但您要对其进行比较的值不是有效的枚举值，也会返回此响应代码。  <br/> |
|ErrorInvalidWatermark  <br/> |无效的水印被导致此错误。  <br/> |
|ErrorIPGatewayNotFound  <br/> |此错误指示一个有效的 VoIP 网关不可用。  <br/> |
|ErrorIrresolvableConflict  <br/> |此错误指示冲突解决无法解析属性的更改。 存储区中的项目可能已更改，并且必须更新。 检索更新后的更改密钥，然后重试。  <br/> |
|ErrorItemCorrupt  <br/> |此错误指示对象的状态已损坏，并且无法检索。 当检索项目时，只有某些元素将此状态下，如[正文](body.md)和[MimeContent](mimecontent.md)。 忽略这些元素和重试该操作。  <br/> |
|ErrorItemNotFound  <br/> |未找到项目或没有访问的项目的权限时，将发生此错误。  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |如果项目上的属性请求失败，将发生此错误。 该属性可能存在，但无法检索。  <br/> |
|ErrorItemSave  <br/> |当尝试保存的项目或文件夹失败，将发生此错误。  <br/> |
|ErrorItemSavePropertyError  <br/> |当尝试保存的项目或文件夹失败由于无效的属性值，将发生此错误。 响应代码包含无效属性的路径。  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |不使用此响应代码。  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |不使用此响应代码。  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |此错误指示可用性服务无法以登录以将请求代理到适当的网站或林的网络服务。 此响应通常指示配置错误。  <br/> |
|ErrorMailboxConfiguration  <br/> |此错误表明未正确配置 AD DS 中的邮箱信息。  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |此错误指示请求中的[MailboxDataArray](mailboxdataarray.md)元素为空。 您必须提供至少一个邮箱标识符。  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |超过 100 个条目提供[MailboxDataArray](mailboxdataarray.md)元素中时，将发生此错误。  <br/> |
|ErrorMailboxFailover  <br/> |此错误指示访问的邮箱的尝试失败，因为此邮箱位于故障转移过程。  <br/> |
|ErrorMailboxHoldNotFound  <br/> |指示找不到邮箱保留项。  <br/> |
|ErrorMailboxLogonFailed  <br/> |要获取的日历视图信息的邮箱的连接失败时，将发生此错误。  <br/> |
|ErrorMailboxMoveInProgress  <br/> | 此错误指示邮箱正在被移动到不同的邮箱存储或服务器。 此错误还可以指示邮箱位于另一个服务器或邮箱数据库。  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | 此错误表示某个条件出现以下错误：  <br/><br/>邮箱存储已损坏。  <br/>正在停止-邮箱存储。  <br/>邮箱存储处于脱机状态。  <br/>-尝试访问邮箱存储时发生网络错误。  <br/>邮箱存储过载，无法接受更多的连接。  <br/>已暂停-邮箱存储。  <br/> |
|ErrorMailRecipientNotFound  <br/> |如果[MailboxData](mailboxdata.md)元素信息无法映射到有效邮箱帐户，将发生此错误。  <br/> |
|ErrorMailTipsDisabled  <br/> |此错误指示邮件提示处于禁用状态。  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |如果您试图已创建的托管的文件夹邮箱中存在，将发生此错误。  <br/> |
|ErrorManagedFolderNotFound  <br/> |已请求中指定的文件夹名称不会映射到 AD DS 中的托管的文件夹定义时，将发生此错误。 您只能创建的托管文件夹的 AD DS 中定义的文件夹的实例。 检查名称，然后重试。  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |此错误指示从邮箱中删除的托管的文件夹根目录或文件夹存在同名的托管的文件夹根的同一个父文件夹中。 如果尝试创建根托管文件夹失败，也会发生此问题。  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |此错误指示建议引擎遇到问题，当试图生成建议。  <br/> |
|ErrorMessageDispositionRequired  <br/> | 如果未设置**MessageDisposition**属性，将发生此错误。<br/><br/> 此属性时，需要以下： <br/> <br/>- [CreateItem operation](createitem-operation.md)和[UpdateItem 操作](updateitem-operation.md)创建或更新的项目时[消息](message-ex15websvcsotherref.md)。  <br/>- [CancelCalendarItem](cancelcalendaritem.md)、 [AcceptItem](acceptitem.md)、 [DeclineItem](declineitem.md)或[TentativelyAcceptItem](tentativelyacceptitem.md)响应对象。  <br/> |
|ErrorMessageSizeExceeded  <br/> |此错误指示要发送的邮件超过允许的限制。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |此错误表明找不到指定的域。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |此错误指示邮件跟踪服务无法跟踪消息。  <br/> |
| ErrorMessageTrackingTransientError  <br/> |此错误指示邮件跟踪服务已关闭或忙碌。 此错误代码指示暂时性错误。 客户端可以重新尝试连接到服务器时收到此错误。  <br/> |
|ErrorMimeContentConversionFailed  <br/> |MIME 内容不是有效时发生此错误 iCal [CreateItem 操作](createitem-operation.md)。 对于[GetItem 操作](getitem-operation.md)，该响应表示无法生成 MIME 内容。  <br/> |
|ErrorMimeContentInvalid  <br/> |MIME 内容无效时，将发生此错误。  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |请求中的 MIME 内容为不是有效基 64 字符串时，将发生此错误。  <br/> |
|ErrorMissingArgument  <br/> |此错误指示已请求中缺少必需的参数。 响应消息文本指示要检查的参数。  <br/> |
|ErrorMissingEmailAddress  <br/> |此错误指示在请求中，指定的可分辨的文件夹 ID 但发出请求的帐户没有系统上的邮箱。 在这种情况下，必须提供[DistinguishedFolderId](distinguishedfolderid.md)下的[邮箱](mailbox.md)子元素。  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |此错误指示在请求中，指定的可分辨的文件夹 ID 但发出请求的帐户没有系统上的邮箱。 在这种情况下，必须提供[DistinguishedFolderId](distinguishedfolderid.md)下的[邮箱](mailbox.md)子元素。 从[CreateManagedFolder 操作](createmanagedfolder-operation.md)返回此响应。  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |缺少的[电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md)元素时，将发生此错误。  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |缺少[ReferenceItemId](referenceitemid.md)时，将发生此错误。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |永远不会返回此错误代码。  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |当尝试[CreateAttachment 操作](createattachment-operation.md)请求的**ItemAttachment**元素中包含的项元素，则返回此错误。  <br/> |
|ErrorMissingManagedFolderId  <br/> |Id 属性的策略，该文件夹的属性标记 0x6732 缺少时，将发生此错误。 您应考虑此文件夹已损坏。  <br/> |
|ErrorMissingRecipients  <br/> |此错误表明您尝试不包括收件人发送项目。 请注意，是否您调用[CreateItem operation，](createitem-operation.md)使其发送消息的消息处置时，您将收到以下响应代码： **ErrorInvalidRecipients**。  <br/> |
|ErrorMissingUserIdInformation  <br/> |此错误指示的[UserId](userid.md)尚未完全指定权限集中。  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |此错误表明您指定了请求中的多个[ExchangeImpersonation](exchangeimpersonation.md)元素值。  <br/> |
|ErrorMoveCopyFailed  <br/> |此错误指示移动或复制操作失败。 接受会议请求中的已删除邮件文件夹时，移动[CreateItem operation，](createitem-operation.md)在发生。 此外，如果您拒绝会议请求、 取消日历项目，或从日历中删除会议，它移至已删除邮件文件夹。  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |如果您尝试移动可分辨的文件夹，将发生此错误。  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |尝试访问多个邮箱服务器的请求时，将发生此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |如果[ResolveNames 操作](resolvenames-operation.md)返回多个结果或您指定的模糊名称匹配的目录中的多个对象，将发生此错误。 响应代码响应数据中包括的匹配的名称。  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |此错误指示呼叫者没有系统上的邮箱。 [ResolveNames 操作](resolvenames-operation.md)或[ExpandDL 操作](expanddl-operation.md)是无效的连接没有邮箱的用户。  <br/> |
|ErrorNameResolutionNoResults  <br/> |此错误指示[ResolveNames 操作](resolvenames-operation.md)返回任何结果。  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |Web 服务找不到要处理请求的服务器时，必须返回此错误代码。  <br/> |
|ErrorNoCalendar  <br/> |如果没有邮箱的日历文件夹，将发生此错误。  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |此错误指示请求引用到另一个 Active Directory 站点中的邮箱，但在目标网站中的没有客户端访问服务器配置的 Windows 身份验证，并且因此请求无法代理。  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |此错误指示请求引用到另一个 Active Directory 站点中的邮箱，但在目标网站中的没有客户端访问服务器配置的 SSL 连接，并且因此请求无法代理。  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |此错误表明请求引用到另一个 Active Directory 站点中的邮箱，但在目标网站中的没有客户端访问服务器已经可接受的产品版本，以接收请求，并因此请求无法代理。  <br/> |
|ErrorNoFolderClassOverride  <br/> |如果您设置[FolderClass](folderclass.md)元素创建通用文件夹之外的项目时，将发生此错误。 对于[CalendarFolder](calendarfolder.md)等[TasksFolder](tasksfolder.md)键入文件夹，则暗示文件夹类。 设置为不同的文件夹类型**ErrorObjectTypeChanged**响应中使用[UpdateFolder 操作](updatefolder-operation.md)结果文件夹类。 而是使用泛型文件夹类型，但将文件夹类设置为所需的值。 Exchange Web 服务将创建正确的强类型的文件夹。  <br/> |
|ErrorNoFreeBusyAccess  <br/> |此错误指示呼叫者在问题日历文件夹没有忙/闲查看权限。  <br/> |
|ErrorNonExistentMailbox  <br/> | 在下列情况下将发生此错误： <br/> <br/>-电子邮件地址为空[CreateManagedFolder](createmanagedfolder.md)中。  <br/>-电子邮件地址不引用中采用电子邮件地址或正文中的 SOAP 标头，如 Exchange 模拟呼叫中的请求的有效帐户。  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |当呼叫者传入非主 SMTP 地址时，将发生此错误。 响应包含正确的 SMTP 地址，以使用。  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |此错误指示自定义范围，0x8000 中的 MAPI 属性和更高版本，不能被属性标记引用。 您必须使用 EWS 托管 API [PropertySetId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)属性或 EWS [ExtendedFieldURI](extendedfielduri.md)元素 PropertySetId 属性。  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |不使用此响应代码。  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |如果没有公用文件夹服务器是否可用，或者调用方没有主公用服务器，则必须返回此错误代码。  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |此错误表明，网站响应，并因此请求无法代理请求引用到另一个 Active Directory 站点，但没有任何客户端访问服务器中的邮箱。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |此错误指示调用方尝试向另一个组织内的用户授予其日历或联系人文件夹中的权限，并且在尝试失败。  <br/> |
|ErrorNotDelegate  <br/> |此错误指示用户不是邮箱的代理人。 它是[GetDelegate 操作](getdelegate-operation.md)、 [RemoveDelegate 操作](removedelegate-operation.md)和[UpdateDelegate 操作](updatedelegate-operation.md)时返回代理人的列表中未找到指定的代理用户。  <br/> |
|ErrorNotEnoughMemory  <br/> |此错误指示由于内存不足，无法不完成该操作。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |此错误指示共享邮件不受支持。  <br/> |
|ErrorObjectTypeChanged  <br/> |如果更改的对象类型，将发生此错误。  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |出现的[开始](start.md)或[结束](end-ex15websvcsotherref.md)时间更新，以使计划事件发生之前或更高的相应的上一个或下一个匹配项时，将发生此错误。  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |此错误指示给定发生的时间分配重叠与另一个匹配项的同一个定期项目。 以分钟为单位的给定发生长度大于 Int32.MaxValue 时，也会发生此响应。  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |此错误指示当前操作对公用文件夹根无效。  <br/> |
|ErrorOrganizationNotFederated  <br/> |此错误指示以便申请者无法创建共享的邮件发送给外部用户，或者无法接受从外部用户共享邮件接收未联盟请求者的组织。  <br/> |
|ErrorParentFolderIdRequired  <br/> |不使用此响应代码。  <br/> |
|ErrorParentFolderNotFound  <br/> |找不到父文件夹时，则将发生此错误[CreateFolder 操作](createfolder-operation.md)中。  <br/> |
|ErrorPasswordChangeRequired  <br/> |此错误指示您必须更改密码，然后才能访问此邮箱。 在创建新帐户和管理员指示用户必须更改密码在首次登录时，将发生这种情况。 无法使用 Exchange Web 服务来更新密码。 您必须使用 Microsoft Office Outlook Web App 之类的工具更改您的密码。  <br/> |
|ErrorPasswordExpired  <br/> |此错误指示密码已过期。 您无法使用 Exchange Web 服务更改密码。 您必须使用 Outlook Web App 之类的工具更改您的密码。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |此错误指示请求者尝试在其日历中授予的权限或向外部用户但分配给请求者的共享策略联系人文件夹，则指示请求的权限级别高于允许共享策略。  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |此错误表明未正确的窗体的电话号码。  <br/> |
|ErrorPropertyUpdate  <br/> |此错误指示更新失败由于无效的属性值。 响应消息中包含无效的属性路径。  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorPropertyValidationFailure  <br/> |不使用此响应代码。  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |此错误指示请求引用另一个客户端访问服务器存在的订阅，但代理至该客户端访问服务器请求的尝试失败。  <br/> |
|ErrorProxyCallFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |此错误指示请求引用到另一个 Active Directory 站点中, 邮箱和原始呼叫者位于 3000 多个组的成员。  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |此错误指示尝试满足[GetUserAvailabilityRequest](getuseravailabilityrequest.md)请求时，Exchange Web 服务发送给另一台客户端访问服务器的请求无效。 此响应代码通常指示发生了配置或权限错误，或者，某人未获成功模仿可用性代理请求。  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |此错误指示 Exchange Web 服务代理尝试到另一个客户端访问服务器，以履行、 可用性请求，但请求失败。 此响应可能由网络连接问题导致或请求超时问题。  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |如果 Web 服务无法确定该请求是目标服务器上运行还是将通过代理传送到另一台服务器，则必须返回此错误代码。  <br/> |
|ErrorProxyTokenExpired  <br/> |不使用此响应代码。  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |公用文件夹邮箱找不到 URL 时，将发生此错误。 此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |尝试访问公用文件夹和不成功时，将发生此错误。 此错误是 Exchange 2013Exchange Server 2013 中引入的。  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |在传递给[GetUserAvailability 操作](getuseravailability-operation.md)收件人位于运行早于 Exchange 2007 和检索忙/闲信息的请求的 Exchange Server 的版本的计算机上时，将发生此错误从公用文件夹服务器的收件人失败。  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |在传递给[GetUserAvailability 操作](getuseravailability-operation.md)收件人位于运行早于 Exchange 2007 和检索忙/闲信息的请求的 Exchange Server 的版本的计算机上时，将发生此错误收件人从公用文件夹服务器失败，因为没有关联的公用文件夹服务器的组织单位。  <br/> |
|ErrorPublicFolderSyncException  <br/> |当同步操作成功对主公用文件夹邮箱，但不成功针对辅公用文件夹邮箱时，将发生此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorQueryFilterTooLong  <br/> |此错误表明搜索文件夹限制可能是有效的但不是受支持的 EWS。 Exchange Web 服务限制以包含 255 的筛选器表达式的最大的限制。 如果您尝试绑定到现有搜索文件夹超过 255 的则返回此响应代码。  <br/> |
|ErrorQuotaExceeded  <br/> |超出邮箱配额时，将发生此错误。  <br/> |
|ErrorReadEventsFailed  <br/> |检索事件信息时，发生故障时， [GetEvents 操作](getevents-operation.md)或推送通知将返回此错误。 返回此错误时，将删除订阅。 重新创建基于最后一个已知水印事件同步。  <br/> |
|ErrorReadReceiptNotPending  <br/> |如果尝试禁止已读的回执时发件人未请求邮件上的已读的回执或邮件位于垃圾邮件文件夹， [CreateItem operation，](createitem-operation.md)则返回此错误。  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |当重复周期的结束日期后 9/1/4500 时，将发生此错误。  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |指定的定期指定范围中没有任何匹配项实例时，将发生此错误。  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |此错误指示代理人列表失败后删除代理人，已保存。  <br/> |
|ErrorRequestAborted  <br/> |不使用此响应代码。  <br/> |
|ErrorRequestStreamTooBig  <br/> | 大于 400 KB 请求流时，将发生此错误。  <br/> |
|ErrorRequiredPropertyMissing  <br/> |[CreateAttachment 操作](createattachment-operation.md)请求中缺少必需的属性时，将返回此错误。 在响应中包含缺失属性 URI。  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |此错误指示呼叫者具有指定不[ResolveNames 操作](resolvenames-operation.md)是联系人文件夹的文件夹。  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |此错误指示呼叫者具有指定多个[ResolveNames 操作](resolvenames-operation.md)的联系人文件夹。  <br/> |
|ErrorResponseSchemaValidation  <br/> |不使用此响应代码。  <br/> |
|ErrorRestrictionTooLong  <br/> |如果限制中包含超过 255 个节点，将发生此错误。  <br/> |
|ErrorRestrictionTooComplex  <br/> |由 Exchange Web 服务无法计算限制时，将发生此错误。  <br/> |
|ErrorResultSetTooBig  <br/> |此错误指示给定收件人的日历条目数超过允许的限制为 1000年。 减少窗口，然后重试。  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |找不到[SavedItemFolderId](saveditemfolderid.md)时，将发生此错误。  <br/> |
|ErrorSchemaValidation  <br/> | 无法根据架构验证请求时，将发生此错误。  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |此错误指示已创建搜索文件夹，但从未文件夹上设置搜索条件。 当您访问损坏的搜索文件夹创建的使用其他 API 或客户端仅时发生。 若要解决此错误，请使用[UpdateFolder 操作](updatefolder-operation.md)设置[SearchParameters](searchparameters.md)元素以包括应的文件夹的限制。  <br/> |
|ErrorSendAsDenied  <br/> | 两个以下条件发生时，将发生此错误： <br/> <br/>-用户已被授予 CanActAsOwner 权限，但不授予委派权限的主体的邮箱。  <br/>-相同的用户尝试创建和使用 SendAndSaveCopy 选项的主体的邮箱中发送电子邮件。<br/>  <br/>  结果是 ErrorSendAsDenied 错误，并创建的主体的草稿文件夹中的电子邮件。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |如果请求中缺少**SendMeetingCancellations**属性，要删除的项是日历项目，将[删除项操作](deleteitem-operation.md)返回此错误。  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |如果请求中缺少**SendMeetingInvitationsOrCancellations**属性，要更新的项是日历项目， [UpdateItem 操作](updateitem-operation.md)将返回此错误。  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |如果请求中缺少**SendMeetingInvitations**属性，要创建的项是日历项目， [CreateItem operation，](createitem-operation.md)则返回此错误。  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |此错误指示组织者发送会议请求后，无法更新请求。 若要修改会议，请修改日历项目，而不是会议请求。  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |此错误指示任务发起方发送任务请求后，无法更新该请求。  <br/> |
|ErrorServerBusy  <br/> |服务器正忙时，将发生此错误。  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |此错误指示 Exchange Web 服务尝试代理用户可用性请求到相应的林的收件人，但无法确定将请求发送由于服务发现故障的位置。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |此错误指示的外部 URL 属性尚未设置 Active Directory 数据库中。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |此错误指示同步共享文件夹的尝试失败。 <br/><br/>将发生以下情况，则会返回此错误代码：<br/><br/>找不到共享文件夹-订阅。<br/>未找到-共享文件夹。<br/>未找到-相应的目录用户。<br/>-用户不再存在。<br/>-该约会是无效。<br/>-联系人项目无效。<br/>-没有与远程服务器通信失败。  <br/> |
|ErrorStaleObject  <br/> |当更改密钥不是最新的或未提供，则将发生此错误在[UpdateItem 操作](updateitem-operation.md)或[SendItem 操作](senditem-operation.md)。 调用[GetItem operation，](getitem-operation.md)以检索更新后的更改密钥，然后再次尝试该操作。  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |此错误指示用户不能立即发送更多的请求，因为已达到提交配额。  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |当您尝试使用未创建该订阅的帐户访问订阅时，将发生此错误。 每个订阅只能创建订阅者访问。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |此错误指示无法创建订阅，是否您不是所有者或不具有到邮箱所有者访问。  <br/> |
|ErrorSubscriptionNotFound  <br/> |如果找不到订阅对应于指定的[SubscriptionId (GetEvents)](subscriptionid-getevents.md) ，将发生此错误。 订阅可能已过期、 Exchange Web 服务过程可能具有已重新启动，或传递了无效的订阅。 如果该订阅有效，重新创建带有最新水印订阅。 这被返回由[取消操作](unsubscribe-operation.md)或[GetEvents 操作](getevents-operation.md)响应。  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |必须返回此错误代码，当请求已取消订阅的订阅。  <br/> |
|ErrorSyncFolderNotFound  <br/> |如果找不到指定的父文件夹， [SyncFolderItems 操作](syncfolderitems-operation.md)将返回此错误。  <br/> |
|ErrorTeamMailboxNotFound  <br/> |此错误表明找不到团队邮箱。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |此错误表明找团队邮箱，但其未链接到 SharePoint Server。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |此错误表明找团队邮箱，但到 SharePoint Server 的链接无效。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |不使用此错误代码。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |不使用此错误代码。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |此错误指示给团队邮箱所有者发送通知的尝试成功。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |此错误指示尝试访问团队邮箱时可能发生的常规错误。 尝试在以后提交请求。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorTimeIntervalTooBig  <br/> |此错误指示指定的时间长度大于所允许的限制。 默认情况下，允许的限制为 42。  <br/> |
|ErrorTimeoutExpired  <br/> | 当没有足够的时间来完成处理的请求时，将发生此错误。  <br/> |
|ErrorTimeZone  <br/> |此错误指示所在的时区错误。  <br/> |
|ErrorToFolderNotFound  <br/> |此错误指示目标文件夹不存在。  <br/> |
|ErrorTokenSerializationDenied  <br/> |如果呼叫者尝试执行令牌序列化请求，但没有 ms-Exch-EPI-TokenSerialization 右客户端访问服务器上，将发生此错误。  <br/> |
|ErrorTooManyObjectsOpened  <br/> |已超出内部限制在打开对象时，将发生此错误。  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |此错误指示用户的拨号计划不可用。  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |此错误表明找不到用户。  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |此错误指示可以找到用于拨号计划的有效服务器来处理请求。  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |不使用此响应代码。  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |失败尝试进行从组中删除 IM 联系人时，将发生此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUnsupportedCulture  <br/> |当您尝试将**区域性**属性设置为不是由**System.Globalization.CultureInfo**类可分析的值时，将发生此错误。  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |当呼叫者尝试使用类型对象、 对象数组、 错误，则为 null 的扩展的属性时，将发生此错误。  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |当您尝试检索或设置为[PostItem](postitem.md)、[邮件](message-ex15websvcsotherref.md)或[日历项目](calendaritem.md)的 object 之外的其他项目的 MIME 内容时，将发生此错误。  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |当呼叫者传入是无效的查询的属性时，将发生此错误。 使用计算的属性时会发生该错误。  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |当呼叫者传入排序或分组依据属性是无效的属性时，将发生此错误。 使用计算的属性时会发生该错误。  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |不使用此响应代码。  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |此错误表明搜索文件夹限制可能是有效的但不是受支持的 EWS。  <br/> |
|ErrorUnsupportedRecurrence  <br/> |此错误指示指定的定期不支持的任务。  <br/> |
|ErrorUnsupportedSubFilter  <br/> |不使用此响应代码。  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |此错误指示 Exchange Web 服务发现存储中的属性类型，但它无法生成 XML 用于属性类型。  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |此错误指示的代理人列表失败，代理人已更新后保存。  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |更改说明中列出的单个属性路径与实际的[项目](item.md)或[文件夹](folder.md)对象中设置的单个属性不匹配时，将发生此错误。  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |此错误指示请求者未启用。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |此错误指示请求者尝试在其日历中授予的权限或向外部用户但分配给请求者的共享策略联系人文件夹表示外部用户的域未列在策略。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指示请求者的组织都有一的联盟域，但请求者的组织没有使用一个联盟任何的域 SMTP 代理地址。  <br/> |
|ErrorValueOutOfRange  <br/> |此错误指示日历视图的开始日期或结束日期设置为 1/1/0001 12:00:00 或 12/31/9999 11:59:59 PM。  <br/> |
|ErrorVirusDetected  <br/> |此错误指示在 Exchange 存储的邮件中检测到病毒。  <br/> |
|ErrorVirusMessageDeleted  <br/> |此错误指示 Exchange 存储在邮件中检测到病毒，并将其删除。  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |不使用此响应代码。  <br/> |
|ErrorWebRequestInInvalidState  <br/> |不使用此响应代码。  <br/> |
|ErrorWin32InteropError  <br/> |此错误指示与非托管代码的通信过程中出现了内部错误。  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |不使用此响应代码。  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |不使用此响应代码。  <br/> |
|ErrorWrongServerVersion  <br/> |此错误指示到邮箱服务器的版本相同的服务器可以仅发出请求。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |此错误指示请求由具有不同的服务器版本比的主体的邮箱服务器的代理人。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |永远不会返回此错误代码。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |指定存在重复的 SOAP 标头。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | 指定同步共享文件夹的尝试失败。<br/><br/> 此错误代码必须返回时：<br/><br/>找不到共享文件夹-订阅。  <br/>找不到-共享文件夹。  <br/>-找不到相应目录用户。  <br/>-用户不再存在。  <br/>-该约会是无效。  <br/>-联系人项目无效。  <br/>-出现与远程服务器通信失败。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |指定外部 URL 属性尚未设置 Active Directory 数据库中。 如果尚未设置 Active Directory 数据库中的外部 URL 属性，则必须返回此错误代码。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |指定已获得忙/闲信息的通讯组列表达到最大组成员计数。 已达到最大组成员计数获得忙/闲信息的通讯组列表时，必须返回此错误。  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |指定的数据类型和 ShareFolderId 元素都存在请求中。 如果数据类型和 ShareFolderId 元素都在请求中存在，则必须返回此错误代码。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |指定调用方尝试向中其他组织和尝试失败的用户授予其日历或联系人文件夹中的权限。 呼叫者或时分配给呼叫者的共享策略不允许共享请求的级别或请求的文件夹类型禁用共享策略时，必须返回此错误代码。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |指定请求者尝试在其日历中授予的权限或向外部用户但分配给请求者的共享策略联系人文件夹指定的外部用户的域未列出在策略。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |指定尝试授予对外部用户但分配给请求者的共享策略其日历或联系人文件夹中的权限指定的请求的权限级别较高的请求程序比共享策略允许。  <br/> |
|ErrorOrganizationNotFederated  <br/> |指定以便请求程序无法创建共享的邮件发送给外部用户，或者无法接受从外部用户共享邮件接收未联盟请求者的组织。 如果请求者的组织联盟，则必须返回此错误代码。  <br/> |
|ErrorMailboxFailover  <br/> |指定尝试访问的邮箱失败，因为此邮箱位于故障转移过程。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |指定共享邀请发件人未创建的共享邀请元数据。 如果共享邀请发件人未创建的共享邀请元数据，则必须返回此错误代码。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |指定的邮件跟踪服务无法跟踪消息。  <br/> |
|ErrorMessageTrackingTransientError  <br/> |指定任一邮件跟踪服务已关闭或忙碌。 此错误代码指定的暂时性错误。 客户端可以重新尝试连接到服务器时收到此错误。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |指定找不到指定的域。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指定请求者的组织都有一的联盟域，但请求者的组织没有使用一个联盟任何的域 SMTP 代理地址。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |指定呼叫者请求的其他组织中的用户的忙/闲信息但组织的关系时，没有启用忙/闲。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |指定请求者的组织联盟对象未正确配置。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |指定的共享邮件，不应为呼叫者。  <br/> |
|ErrorInvalidSharingData  <br/> |指定的共享元数据无效。 原因可能是无效的 XML。  <br/> |
|ErrorInvalidSharingMessage  <br/> |指定共享邮件不是有效。 原因可能是一个缺少的属性。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |指定共享邮件不受支持。  <br/> |
|ErrorApplyConversationActionFailed  <br/> |如果操作不能应用于对话中的一个或多个项目，则必须返回此错误。  <br/> |
|ErrorInboxRulesValidationError  <br/> |如果任何规则不验证，则必须返回此错误。  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |尝试管理收件箱规则发生后另一个客户端已访问的收件箱规则时，必须返回此错误。  <br/> |
|ErrorRulesOverQuota  <br/> |已超出用户的规则配额时，必须返回此错误。  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |如果打开第二个订阅连接，必须对第一个订阅连接返回此错误。  <br/> |
|ErrorMissedNotificationEvents  <br/> |会丢失事件通知时，必须返回此错误。  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |当 Active Directory 域服务 (AD DS) 中的重复旧的可分辨的名称时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |此错误指示获取客户端访问令牌的请求无效。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorNoSpeechDetected  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorUMServerUnavailable  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorRecipientNotFound  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorRecognizerNotInstalled  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSpeechGrammarError  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |如果 SOAP 标头中的[ManagementRole](managementrole.md)标头不正确，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesDisabled  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |此错误旨在仅供内部使用。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorWeatherServiceDisabled  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |搜索范围的尝试执行无需使用[查询字符串 （字符串）](querystring-string.md)元素的内容索引搜索时，将返回此错误。 这是适用于**SearchMailboxes**和**FindConversation**操作。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |当存档邮箱搜索不成功，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |当存档邮箱的 URL 不是可供搜索，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |要获取的远程存档邮箱文件夹的操作失败时，将发生此错误。  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |要查找的远程存档邮箱文件夹的操作失败时，将发生此错误。  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |若要获取的远程存档邮箱项目操作失败时，将发生此错误。  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |远程存档邮箱的项目导出操作失败时，将发生此错误。  <br/> |
|ErrorInvalidPhotoSize  <br/> |如果从服务器请求是无效的照片大小，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |意外的照片大小请求**GetUserPhoto**操作请求中时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |**SearchMailboxes**操作请求包含太多邮箱搜索时，将返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |此错误表明没有保留标记找到该用户。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |当发现搜索租户或服务器上禁用，则返回此错误。 此错误是在 Exchange 2013 中引入的。  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |尝试调用来获取日历项目，这不支持与[SeekToConditionPageItemView](seektoconditionpageitemview.md) [FindItem 操作](finditem-operation.md)时，将发生此错误。  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |此错误旨在仅供内部使用。  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |租户标记为删除。  <br/> |
|ErrorInvalidLicense  <br/> |用户不具有有效的许可证。  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |每个文件夹的邮件接收已超出配额。  <br/> |
   
## <a name="remarks"></a>注解

此元素不需要，并且不包含在所有响应。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

