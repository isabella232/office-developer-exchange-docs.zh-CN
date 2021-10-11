---
title: ResponseCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 4b84d670-74c9-4d6d-84e7-f0a9f76f0d93
description: ResponseCode 元素提供有关请求的状态信息。
ms.openlocfilehash: fc328ffde3a21add77ce6870a87bc7092f3f46ab
ms.sourcegitcommit: f13a3a4a61fa23ca6414b7c96ddf087adbe3dc9e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2021
ms.locfileid: "60262216"
---
# <a name="responsecode"></a>ResponseCode

**ResponseCode** 元素提供有关请求的状态信息。 
  
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
|[ResponseMessage](responsemessage.md) <br/> | 提供有关响应状态的描述性信息。<br/><br/>  以下是此元素的可能 XPath 表达式：<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |包含单个 [DeleteItem](deleteitem-operation.md) 操作请求的状态和结果。  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |包含单个 [SendItem](senditem-operation.md) 操作请求的状态和结果。  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |包含单个 [DeleteFolder](deletefolder-operation.md) 操作请求的状态和结果。  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含单个 [DeleteAttachment](deleteattachment-operation.md) 操作请求的状态和结果。  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |包含单个 Unsubscribe 操作请求的状态 [和](unsubscribe-operation.md) 结果。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含单个 [CreateFolder](createfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含单个 [GetFolder](getfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含单个 [UpdateFolder](updatefolder-operation.md) 操作请求的状态和结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含单个 [MoveFolder](movefolder-operation.md) 操作请求的状态和结果。  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含单个 [CopyFolder](copyfolder-operation.md)操作请求的状态和结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含单个 [CreateManagedFolder 操作请求的状态和](createmanagedfolder-operation.md) 结果。  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含单个 [FindFolder](findfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含单个 [CreateItem](createitem-operation.md) 操作请求的状态和结果。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含单个 [GetItem](getitem-operation.md) 操作请求的状态和结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含单个 [UpdateItem](updateitem-operation.md) 操作请求的状态和结果。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含单个 [MoveItem](moveitem-operation.md) 操作请求的状态和结果。  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含单个 [CopyItem](copyitem-operation.md) 操作请求的状态和结果。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含单个 [CreateAttachment](createattachment-operation.md) 操作请求的状态和结果。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含单个 [GetAttachment](getattachment-operation.md) 操作请求的状态和结果。  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含单个 [FindItem](finditem-operation.md) 操作请求的状态和结果。  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含 [ResolveNames](resolvenames-operation.md) 操作请求的状态和结果。  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含单个 [ExpandDL](expanddl-operation.md) 操作请求的状态和结果。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含单个 Subscribe 操作请求的状态 [和](subscribe-operation.md) 结果。  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含单个 [GetEvents](getevents-operation.md) 操作请求的状态和结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含单个 SendNotification 操作请求的状态和结果。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含 [SyncFolderHierarchy](syncfolderhierarchy-operation.md) 操作请求的状态和结果。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含 [SyncFolderItems](syncfolderitems-operation.md) 操作请求的状态和结果。  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含 ConvertId 操作请求 [的状态和](convertid-operation.md) 结果。  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |包含 [AddDelegate](adddelegate-operation.md) 操作请求的状态和结果。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含 [GetDelegate](getdelegate-operation.md) 操作请求的状态和结果。  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |包含 [RemoveDelegate](removedelegate-operation.md) 操作请求的状态和结果。  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |包含 [UpdateDelegate](updatedelegate-operation.md) 操作请求的状态和结果。  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |包含 [GetServerTimeZones](getservertimezones-operation.md) 操作请求的状态和结果。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含 [GetSharingFolder 操作请求的状态和](getsharingfolder-operation.md) 结果。  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |定义对 [GetSharingFolder 操作请求](getsharingfolder-operation.md) 的响应。  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |包含 [GetSharingMetadata 操作请求的状态和](getsharingmetadata-operation.md) 结果。  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |包含 [RefreshSharingFolder 操作请求的状态和](refreshsharingfolder-operation.md) 结果。  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |定义对 [RefreshSharingFolder 操作请求](refreshsharingfolder-operation.md) 的响应。  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |包含 [FindConversation](findconversation-operation.md) 操作响应的状态和结果。  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |包含 [ApplyConversationAction](applyconversationaction-operation.md) 操作请求的状态和结果。  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |包含单个 [EmptyFolder](emptyfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |包含 [UpdateInboxRules 操作请求的状态和](updateinboxrules-operation.md) 结果。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含 [UploadItems](uploaditems-operation.md) 操作请求的状态和结果。  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |包含对 [GetInboxRules 操作](getinboxrules-operation.md) **** 请求的响应。  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |包含对 [GetServiceConfiguration 操作请求](getserviceconfiguration-operation.md) 的响应。  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
## <a name="text-value"></a>文本值

如果此元素已使用，则文本值是必需的。 下表描述了此元素返回的值。
  
|值|说明|
|:-----|:-----|
|NoError  <br/> |请求未发生错误。  <br/> |
|ErrorAccessDenied  <br/> |当呼叫帐户没有权限执行所请求的操作时，将发生此错误。  <br/> |
|ErrorAccessModeSpecified  <br/> |此错误仅供内部使用。 不返回此错误。  <br/> |
|ErrorAccountDisabled  <br/> |当禁用了有关帐户时，将发生此错误。  <br/> |
|ErrorAddDelegatesFailed  <br/> |当无法保存具有已添加的委托的列表时，将发生此错误。  <br/> |
|ErrorAddressSpaceNotFound  <br/> |在 Active Directory 数据库中找不到跨林可用性的地址空间记录或域名系统 (DNS) 域名时，将发生此错误。  <br/> |
|ErrorADOperation  <br/> |当操作因 Active Directory 域服务与 AD DS 服务器之间的通信问题 (发生) 。  <br/> |
|ErrorADSessionFilter  <br/> |当 **ResolveNames** 操作请求指定名称时，将返回此错误无效。  <br/> |
|ErrorADUnavailable  <br/> |此错误发生在 AD DS 不可用时。 请稍后重试请求。  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |此错误指示未指定 **AffectedTaskOccurrences** 属性。 当 [DeleteItem](deleteitem.md) 元素用于删除至少一个作为任务的项目时，无论该任务是否是定期任务，必须指定 **AffectedTaskOccurrences** 属性，以便 **DeleteItem** 可以确定是删除当前事件还是删除整个系列。  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |指示创建存档文件夹路径时出错。  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |指示未启用存档邮箱。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |指示存档邮箱服务发现失败。  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |指定已尝试创建包含 10 多个嵌套附件的项目。 此值在 sp2 Exchange Server 2010 Service Pack 2 (中引入) 。  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |如果试图创建大小超过 Int32.MaxValue 的附件（以字节为单位）时 [，CreateAttachment](createattachment.md) 元素将返回此错误。  <br/> 如果尝试检索大小超过 Int32.MaxValue 的现有附件（以字节为单位）时 [，GetAttachment](getattachment.md) 元素将返回此错误。  <br/> |
|ErrorAutoDiscoverFailed  <br/> |此错误指示 Exchange Web 服务尝试确定运行 Exchange 2010 的跨林计算机的位置，该计算机使用自动发现服务安装了客户端访问服务器角色，但调用自动发现服务失败。  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |此错误指示 AD DS 中缺少本地林的可用性配置信息。  <br/> |
|ErrorBatchProcessingStopped  <br/> | 此错误指示处理项目时发生异常，并且后续项目可能会发生异常。 请求可以包含多个项目;例如，GetItem 操作请求可能包含多个标识符。 通常，项目一次处理一个。 如果在处理项目时发生异常，并且后续项目可能会发生该异常，将不会处理后续项目。  <br/><br/>  以下是将停止处理以下项目的错误示例：<br/>  <br/>- ErrorAccessDenied  <br/>- ErrorAccountDisabled  <br/>- ErrorADUnavailable  <br/>- ErrorADOperation  <br/>- ErrorConnectionFailed  <br/>- ErrorMailboxStoreUnavailable  <br/>- ErrorMailboxMoveInProgress  <br/>- ErrorPasswordChangeRequired  <br/>- ErrorPasswordExpired  <br/>- ErrorQuotaExceeded  <br/>- ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |当尝试移动或复制定期日历项目的一个匹配项时，将发生此错误。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | 当尝试更新位于"已删除邮件"文件夹中的日历项目，以及根据 **SendMeetingInvitationsOrCancellations** 属性的值发送会议更新或取消时，将发生此错误。 <br/><br/>以下是该属性可能的值：  <br/><br/>- SendToAllAndSaveCopy  <br/>- SendToChangedAndSaveCopy  <br/>- SendOnlyToAll  <br/>- SendOnlyToChanged  <br/>  <br/>但是，只有在此属性的值设置为 SendToNone 时，才允许此类更新。  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |当调用 UpdateItem、GetItem、DeleteItem、MoveItem、CopyItem 或 SendItem 操作，并且指定的 ID 不是任何定期日历项目的事件 ID 时，将发生此错误。  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |当调用 UpdateItem、GetItem、DeleteItem、MoveItem、CopyItem或 **SendItem** 操作，并且指定的 ID 不是任何定期主项目的 ID 时，将发生此错误。      <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |当日历项目持续时间超过允许的最大值（当前为 5 年）时，在 **CreateItem** 或 **UpdateItem** 操作期间发生此错误。  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |当日历的"结束时间"设置为同一时间或"开始时间"之后，将发生此错误。  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |当使用 [CalendarView](calendarview.md)元素的 **FindItem** 操作指定的文件夹不是日历文件夹类型时，将发生此错误。  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |此响应代码未使用。  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |当 Day、WeekendDay 和 Weekday 的无效值用于定义时间更改模式时，在 **CreateItem** 或 **UpdateItem** 操作期间发生此错误。  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |此错误发生在 **CreateItem** 或 **UpdateItem** 操作期间，当使用 Day、WeekDay 和 WeekendDay 的无效值指定每周重复周期时。  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |当日历项目定期二进制大型对象或 BLOB 存储中 (BLOB) 的状态无效Exchange发生此错误。  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |此响应代码未使用。  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |当无法创建指定的定期时，将发生此错误。  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |当遇到无效时区时，将发生此错误。  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |此错误 指示日历项目已取消。  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |此错误指示日历项目已取消。  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |此错误指示日历项目已取消。  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |此错误指示日历项目已取消。  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |此错误指示 [AcceptItem](acceptitem.md) 元素对于委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |此错误指示 [DeclineItem](declineitem.md) 元素对于委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |此错误指示 [RemoveItem](removeitem.md) 元素对于委派方案中的会议取消无效。  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |此错误指示 [TentativelyAcceptItem](tentativelyacceptitem.md) 元素对于委派方案中的日历项目或会议请求无效。  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |此错误指示对 (项) CancelItem 事件无效操作。 只有会议组织者可以取消会议。  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |此错误指示 [AcceptItem](acceptitem.md) 对于组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |此错误指示 [DeclineItem](declineitem.md) 对组织者的日历项目无效。  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |此错误指示 [RemoveItem](removeitem.md) 对于组织者的日历项目无效。 若要从日历中删除会议，组织者必须使用 CancelCalendarItem。  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |此错误指示 [TentativelyAcceptItem](tentativelyacceptitem.md) 对组织者的日历项目无效。  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |此错误指示会议请求已过期，无法更新。  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |此错误指示事件索引不指向当前定期周期内的事件。 例如，如果定期模式定义一组三个会议事件，并且您尝试访问第五次会议，则此响应代码将生成。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |此错误指示通过定期主 ID 和 (索引对已删除事件进行的任何操作) 无效。  <br/> |
|ErrorCalendarOutOfRange  <br/> |当属性值在范围外时，会针对日历项目或任务定期属性的 CreateItem 和 UpdateItem 操作报告此错误。 例如，指定一个月的第十五周将导致此响应代码。  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |当 [CalendarView](calendarview.md) 元素的 Start 到 End 范围超过允许的最大值（当前为 2 年）时，将发生此错误。  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |此错误指示请求的帐户不是目录数据库中的有效帐户。  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |指示已尝试存档日历联系人任务文件夹。  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |指示已尝试在公用文件夹中存档项目。  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |指示已尝试存档存档邮箱中的项目。  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |此错误发生在创建日历项目且 **SavedItemFolderId** 属性引用非日历文件夹时。  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |此错误发生在创建联系人且 **SavedItemFolderId** 属性引用非联系人文件夹时。  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |此错误指示无法在除邮件文件夹外的文件夹（如日历、联系人、任务、便笺等）中创建发布项目。  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |创建任务且 **SavedItemFolderId** 属性引用非任务文件夹时，将发生此错误。  <br/> |
|ErrorCannotDeleteObject  <br/> |当无法删除要删除的项目或文件夹时，将发生此错误。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |[DeleteItem 操作](deleteitem-operation.md)在无法删除定期任务的当前事件时返回此错误。 只有在 **AffectedTaskOccurrences** 属性已设置为 SpecifiedOccurrenceOnly 时，才能发生这种情况。  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |指示已尝试禁用强制扩展。  <br/> |
|ErrorCannotEmptyFolder  <br/> |当服务器无法清空文件夹时，必须返回此错误。  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |指示无法检索源文件夹路径。  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |指定服务器无法检索"选项"Outlook Web App URL。  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |如果 **GetAttachment** 操作无法检索文件附件的正文，则返回此错误。  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |此错误指示呼叫者尝试设置非日历文件夹的日历权限。  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |此错误指示呼叫者尝试对日历文件夹设置非日历权限。  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |此错误指示您无法在权限集内设置未知权限。  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |指示已尝试将搜索文件夹指定为源文件夹。  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |当为需要项目标识符的请求提供文件夹标识符时，将发生此错误。  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |当为需要文件夹标识符的请求提供项目标识符时，将发生此错误。  <br/> |
|ErrorChangeKeyRequired  <br/> |此响应代码已被 **ErrorChangeKeyRequiredForWriteOperations 取代** <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |当项目的更改键缺失或过时时，将返回此错误。 <br/><br/>对于 SendItem、UpdateItem 和 UpdateFolder 操作，调用方必须传递项的正确和当前更改键。 请注意，即使将冲突解决设置为始终覆盖，UpdateItem 也如此。  <br/> |
|ErrorClientDisconnected  <br/> |指定客户端已断开连接。  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |此错误仅供内部使用。  <br/> |
|ErrorClientIntentNotFound  <br/> |此错误仅供内部使用。  <br/> |
|ErrorConnectionFailed  <br/> |当 Web 服务Exchange邮箱时，将发生此错误。  <br/> |
|ErrorConnectionFailedTransientError  <br/> |当 Web 服务Exchange邮箱时，将发生此错误。 此错误代码指示暂时性错误。 收到此错误时，客户端可以重试连接到服务器。 <br/> |
|ErrorContainsFilterWrongType  <br/> |此错误指示检查到 Contains 筛选器的属性不是字符串类型。  <br/> |
|ErrorContentConversionFailed  <br/> |当 Web 服务无法检索所请求Exchange的 MIME 内容时 **，GetItem** 操作将返回此错误。 <br/><br/>当 Web 服务无法从提供的 MIME Exchange创建项目时 **，CreateItem** 操作将返回此错误。 通常，这表示项目属性已损坏或截断。  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |此错误发生在使用 QueryString 选项提出搜索请求并且未为目标邮箱启用内容索引时。  <br/> |
|ErrorCorruptData  <br/> |当数据已损坏且无法处理时，将发生此错误。  <br/> |
|ErrorCreateItemAccessDenied  <br/> |当调用方无权创建项目时，将发生此错误。  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |当创建 CreateManagedFolder 操作请求中指定的一个或多个托管文件夹失败时，将发生此错误。 搜索每个文件夹以确定已创建的文件夹以及不存在的文件夹。  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |当调用帐户没有创建子文件夹所需的权限时，将发生此错误。  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |当尝试将项目或文件夹从一个邮箱移动到另一个邮箱时，将发生此错误。 如果源邮箱和目标邮箱不同，则您将收到此错误。  <br/> |
|ErrorCrossSiteRequest  <br/> |此错误指示不允许该请求，因为应处理请求的客户端访问服务器位于不同的站点中。  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |此错误可能发生在下列情况下：<br/>  <br/>- 尝试访问或写入项目上的属性，并且该属性值过大。<br/>- 请求 XML 中经过 base64 编码的 MIME 内容长度超过此限制。<br/>- 现有项目正文的正文大小超过此限制。<br/>- 使用者尝试设置 HTML 或文本正文，如果追加 (，则其长度或组合) 超出限制。 |
|ErrorDataSourceOperation  <br/> |当基础数据提供程序无法完成操作时，将发生此错误。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |当指定用户已存在于委派列表中时 **，AddDelegate** 操作中将发生此错误。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |当要添加的指定用户是邮箱的所有者时 **，AddDelegate** 操作中会出现此错误。  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |如果本地 FreeBusy 邮件上没有委派信息，或者没有 Active Directory 公共代理 (在 AD DS) 中没有"公共代理"或没有"代表发送"条目，则 **GetDelegate** 操作中会出现此错误。  <br/> |
|ErrorDelegateNoUser  <br/> |当指定的用户无法映射到 AD DS 中的用户时，将发生此错误。  <br/> |
|ErrorDelegateValidationFailed  <br/> |当添加的委派用户被添加时 **，AddDelegate** 操作无效。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |当尝试删除可分辨文件夹时，将发生此错误。  <br/> |
|ErrorDeleteItemsFailed  <br/> |此响应代码未使用。  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |此错误仅供内部使用。  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |此错误指示为操作无效可分辨用户 ID。 Request 中不应存在 **DistinguishedUserType。**  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |此错误指示请求通讯组列表成员在通讯组列表中不存在。  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |当 **CreateManagedFolder** 操作请求的 [FolderNames](foldernames.md)元素中指定了重复的文件夹名称时，将发生此错误。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |此错误指示存在重复的 SOAP 标头。  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |此错误指示在权限集内找到了重复的用户 ID，"默认"或"匿名"设置多次，或者存在重复的 SID 或收件人。  <br/> |
|ErrorEmailAddressMismatch  <br/> |当请求尝试创建/更新搜索文件夹的搜索参数时，将发生此错误。 例如，当在邮箱中创建搜索文件夹，但搜索文件夹被定向到另一个邮箱中查找时，可能会发生这种情况。  <br/> |
|ErrorEventNotFound  <br/> |在返回事件之前删除与水印关联的事件时，将发生此错误。 返回此错误时，订阅也会被删除。  <br/> |
|ErrorExceededConnectionCount  <br/> |此错误 -i表明针对服务器的并发请求多于用户策略允许的并发请求数。  <br/> |
|ErrorExceededSubscriptionCount  <br/> |此错误指示已超出用户的限制策略最大订阅计数。  <br/> |
|ErrorExceededFindCountLimit  <br/> |此错误指示搜索操作调用已超过可返回的项目总数。  <br/> |
|ErrorExpiredSubscription  <br/> |如果由于订阅已过期而将 [GetEvents](getevents-operation.md) 操作调用为订阅，则会发生此错误。  <br/> |
|ErrorExtensionNotFound  <br/> |指示未找到扩展。  <br/> |
|ErrorFolderCorrupt  <br/> |如果文件夹已损坏且无法保存，则会发生此错误。  <br/> |
|ErrorFolderExists  <br/> |如果试图创建的文件夹与同一父文件夹中的另一个文件夹同名，则会发生此错误。 不允许重复的文件夹名称。  <br/> |
|ErrorFolderNotFound  <br/> |此错误指示指定的文件夹 ID 与有效的文件夹不对应，或者代理无权访问该文件夹。  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |此错误指示无法检索请求的属性。 这并不表示属性不存在，但属性因某种原因损坏，因此检索失败。  <br/> |
|ErrorFolderSave  <br/> |此错误指示由于状态无效，无法创建或更新文件夹。  <br/> |
|ErrorFolderSaveFailed  <br/> |此错误指示由于状态无效，无法创建或更新文件夹。  <br/> |
|ErrorFolderSavePropertyError  <br/> |此错误指示由于属性值无效，无法创建或更新文件夹。 响应代码列出了导致该问题的属性。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |此错误指示为获取通讯组列表的忙/闲信息已达到最大组成员计数。  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |如果由于中间故障而无法检索忙/闲信息，则返回此错误。  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |此响应代码未使用。  <br/> |
|ErrorImContactLimitReached  <br/> |当由于已达到最大联系人数 (即时消息) 联系人时，将返回此错误。 此错误是在 2013 年 Exchange Server引入的。  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |当尝试添加组时，将返回此错误显示名称现有组已具有相同的组显示名称。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorImGroupLimitReached  <br/> |当由于已达到最大组数而无法添加新的 IM 组时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorImpersonateUserDenied  <br/> |当调用方没有适当的权限来模拟特定用户时，Exchange模拟的服务器到服务器授权案例中返回错误。 此错误映射到 ms-Exch-MAPS-May-Impersonate 扩展 Active Directory 权限。  <br/> |
|ErrorImpersonationDenied  <br/> |当调用方没有适当的权限通过其请求所针对的客户端访问服务器进行模拟时，此错误在 Exchange Impersonation 的服务器到服务器授权中返回。 这会映射到 ms-Exch-MAPS-Impersonation 扩展 Active Directory 右侧。  <br/> |
|ErrorImpersonationFailed  <br/> |此错误指示尝试执行服务器到服务器身份验证时出现意外错误。 此响应代码通常指示运行 Exchange Web Services 应用程序池 的服务帐户配置不正确、Exchange Web 服务无法与目录对话，或者未正确配置林之间的信任。  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |此错误指示请求对当前 Exchange Server有效，但对于指定的请求服务器版本无效。  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |此错误指示 [UpdateItem](updateitem.md) 或 [UpdateFolder](updatefolder.md) 元素中的每个更改说明只能列出一个要更新的属性。  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |当请求包含要解决的与会者过多时，将发生此错误。 默认情况下，要解析的最大与会者数为 100。  <br/> |
|ErrorInsufficientResources  <br/> |当邮箱服务器过载时，将发生此错误。 请稍后重试请求。  <br/> |
|ErrorInternalServerError  <br/> |此错误指示Exchange Web 服务遇到无法恢复的错误，并且不存在与发生的错误相关联的更具体的响应代码。  <br/> |
|ErrorInternalServerTransientError  <br/> |此错误指示发生了内部服务器错误，您应稍后重试请求。  <br/> |
|ErrorInvalidAccessLevel  <br/> |此错误指示呼叫者对忙/闲数据具有的访问级别无效。  <br/> |
|ErrorInvalidArgument  <br/> |此错误指示由传递给 [GetMessageTrackingReport](getmessagetrackingreport-operation.md)操作的所有无效参数导致的一个错误。<br/><br/> 此错误在下列情况下返回： <br/><br/>- 在  _sending-as_ 参数中指定的用户不存在于目录中。 <br/>- 在  _sending-as_ 参数中指定的用户在目录中不是唯一的。 <br/>-  _发送者地址_ 为空。<br/>-  _发送者_ 地址不是有效的电子邮件地址。  <br/> |
|ErrorInvalidAttachmentId  <br/> |当找不到与指定 ID 对应的附件时 [，GetAttachment](getattachment-operation.md) 操作或 [DeleteAttachment](deleteattachment-operation.md) 操作将返回此错误。  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |此错误发生在尝试使用复杂附件表限制绑定到现有搜索文件夹时。 ExchangeWeb 服务仅支持针对附件表的简单包含筛选器。 如果您尝试绑定到具有更复杂的附件表限制的现有搜索文件夹 (子筛选器) ，Exchange Web 服务将无法呈现该筛选器的 XML 并返回此响应代码。 <br/><br/>请注意，你仍然可以对文件夹调用 GetFolder 操作，但不请求 [SearchParameters](searchparameters.md) 元素。  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |此错误发生在尝试使用复杂附件表限制绑定到现有搜索文件夹时。 ExchangeWeb 服务仅支持针对附件表的简单包含筛选器。 <br/><br/>如果您尝试绑定到具有更复杂的附件表限制的现有搜索文件夹，Exchange Web 服务无法呈现该筛选器的 XML。 在这种情况下，附件子筛选器包含文本筛选器，但它不会查看附件显示名称。<br/><br/> 请注意，你仍然可以对文件夹调用 GetFolder 操作，但不请求 [SearchParameters](searchparameters.md) 元素。  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | 此错误指示请求者的授权过程失败。  <br/> |
|ErrorInvalidChangeKey  <br/> |当使用者使用无法分析的更改键传递文件夹或项目标识符时，将发生此错误。 例如，这可能是无效的 base64 内容或空字符串。  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |此错误指示尝试解析调用方的标识时出现内部错误。  <br/> |
|ErrorInvalidCompleteDate  <br/> |当尝试将任务的 [CompleteDate](completedate.md) 元素值设置为将来的某个时间时，将返回此错误。 当任务转换为客户端访问服务器的本地时间时，不能将任务的 [CompleteDate](completedate.md) 设置为比客户端访问服务器上本地时间晚的值。  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |此错误指示为联系人提供了无效的电子邮件地址。  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |此错误指示为电子邮件条目提供了无效的电子邮件索引值。  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |当用于将请求代理到其他目录服务林的凭据身份验证失败时，将发生此错误。  <br/> |
|ErrorInvalidDelegatePermission  <br/> |此错误指示指定的文件夹权限无效。  <br/> |
|ErrorInvalidDelegateUserId  <br/> |此错误指示指定的委派用户 ID 无效。  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |当呼叫者未指定 UPN Exchange电子邮件地址或用户 SID 时，此错误在模拟期间发生。 如果调用方指定了其中一个或多个值且值为空，也会发生这种情况。  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |当传递到 [Excludes](excludes.md) 元素限制的位掩码无法解析时，将发生此错误。  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidExtendedProperty  <br/> | 发生以下事件时，将发生此错误： <br/> <br/>- 调用方尝试使用 Web 服务不支持的扩展Exchange属性。  <br/>- 调用方传递扩展属性的无效属性值组合。 如果未传递任何属性，也会发生这种情况。 仅允许某些组合。  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |当扩展属性的值部分与该属性的类型不匹配时，将发生此错误。 <br/><br/>例如，将 PropertyType="String" 的扩展属性设置为整数数组将导致此错误。 任何不可强制转换为为扩展属性指定的类型的字符串表示形式都表示此错误。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |此错误指示共享邀请发件人未创建共享邀请元数据。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |此错误指示共享消息不适合呼叫者。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |此错误指示请求者的组织联合对象配置不正确。  <br/> |
|ErrorInvalidFolderId  <br/> |如果文件夹 ID 已损坏，则会发生此错误。  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |此错误指示指定的文件夹类型对于当前操作无效。 例如，不能在公用文件夹中创建搜索文件夹。  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | 当用户指定了以下项之一时，小数分页会出现此错误： <br/> <br/>- 大于分母的分子  <br/>- 小于零的分子  <br/>- 小于或等于零的分母  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |此错误指示请求中同时存在 [DataType](datatype.md) 和 ShareFolderId 元素。  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |此错误发生在 [调用 GetUserAvailability 操作](getuseravailability-operation.md) 时 [，FreeBusyViewType](freebusyviewtype.md) 为 None。  <br/> |
|ErrorInvalidId  <br/> |此错误指示 ID 和/或更改密钥格式不正确。  <br/> |
|ErrorInvalidIdEmpty  <br/> |当调用方指定一个 **空的 Id** 属性时，将发生此错误。  <br/> |
|ErrorInvalidLikeRequest  <br/> |当项目无法被喜欢时，将发生此错误。 从内部Exchange号 15.00.0913.09 开始的版本包含此值。  <br/> |
|ErrorInvalidIdMalformed  <br/> |当调用方指定的 **Id** 属性格式不正确时，将发生此错误。  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |此错误指示为具有 Exchange 2007 SP1 或更高版本的请求指定了使用 Exchange 2007 格式的文件夹或项目 ID。 您不能在 Exchange 2007 SP1 或更高版本Exchange 2007 IDS。 您必须使用 [ConvertId 操作首先](convertid-operation.md) 转换它们。  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |当调用方指定的 **Id** 属性太长时，将发生此错误。  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |只要将非项目附件 ID 的 ID 传递给需要附件 ID 的 Web 服务方法，就会返回此错误。  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |如果邮箱中的联系人已损坏，则会发生此错误。  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |当调用方指定的 **Id** 属性太长时，将发生此错误。  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |当项目的附件层次结构超过最大 255 层深度时，将返回此错误。  <br/> |
|ErrorInvalidIdXml  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidImContactId  <br/> |当指定的 IM 联系人标识符不代表有效标识符时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |当指定的 IM 通讯组 SMTP 地址标识符不表示有效标识符时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidImGroupId  <br/> |当指定的 IM 组标识符不表示有效标识符时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |如果索引分页的偏移量为负数，则会发生此错误。  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |指示项目对于 **ArchiveItem** 操作无效。  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |如果试图对会议请求或日历项目外的项目类型使用 AcceptItem 响应对象，或者试图接受"已删除邮件"文件夹中的日历项目事件，则会发生此错误。  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |当尝试对日历项目外的项目类型使用 CancelItem 响应对象时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | 尝试创建不受支持类型的项目附件时，将返回此错误。  <br/><br/>  项目附件支持的项目类型包括以下对象：  <br/><br/>- [Item](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [任务](task.md) <br/>- [联系人](contact.md) <br/> <br/> 例如，如果您尝试创建 [MeetingMessage](meetingmessage.md) 附件，则会遇到此响应代码。  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | 如果请求包含不受支持的项目类型，则 [从 CreateItem](createitem-operation.md) 操作返回此错误。 <br/><br/>支持的项目包括以下对象：<br/>  <br/>- [Item](item.md) <br/>- [消息](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [任务](task.md) <br/>- [联系人](contact.md) <br/><br/>  某些类型的创建是作为执行其他一些措施的副作用。 例如，向与会者发送日历项目时，会创建会议消息;它们未显式创建。  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |当尝试对会议请求或日历项目外的项目类型使用 DeclineItem 响应对象，或者试图拒绝"已删除邮件"文件夹中的日历项目出现时，将发生此错误。  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |此错误指示 [ExpandDL 操作](expanddl-operation.md) 仅对专用通讯组列表有效。  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |如果请求指定的项目不是会议取消项目，则从 RemoveItem 响应对象返回此错误。  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |如果请求指定的项目不是邮件项目，则 [从 SendItem](senditem-operation.md) 操作返回此错误。  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |当尝试对会议请求或日历项目外的项目类型使用 [TentativelyAcceptItem](tentativelyacceptitem.md) 时，或者试图暂时接受"已删除邮件"文件夹中的日历项目事件时，将发生此错误。  <br/> |
|ErrorInvalidLogonType  <br/> |此错误仅供内部使用。 不返回此错误。  <br/> |
|ErrorInvalidMailbox  <br/> |此错误指示 [CreateItem 操作](createitem-operation.md) 或 [UpdateItem 操作](updateitem-operation.md) 在创建或更新个人通讯组列表时失败。  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |当托管文件夹的结构已损坏且无法呈现时，将发生此错误。  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |当在托管文件夹上设置的配额小于零（表示托管文件夹已损坏）时，将发生此错误。  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |当托管文件夹上设置的大小小于零时，将发生此错误，这表明托管文件夹已损坏。  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |提供合并的忙/闲内部值无效时，将发生此错误。 默认最小值为 5 分钟。 默认最大值为 1440 分钟。  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |当名称对于 ResolveNames 操作无效时 [，将发生此错误](resolvenames-operation.md)。 例如，零长度字符串、单个空格、逗号和短划线都是无效名称。  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |此错误指示客户端访问服务器上网络服务帐户中的错误。  <br/> |
|ErrorInvalidOofParameter  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidOperation  <br/> | 这是在请求的操作无效时使用的一般错误。 <br/><br/>例如，您无法执行以下操作： <br/> <br/>- 对公用文件夹使用 [FindFolder](findfolder-operation.md) 操作执行"深度"遍历。  <br/>- 移动或复制公用文件夹根目录。  <br/>- 使用除"硬"删除以外的任何模式删除关联项。  <br/>- 移动或复制关联的项。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |此错误指示呼叫者为另一个组织中用户请求忙/闲信息，但组织关系未启用忙/闲。  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |当使用者为要返回的最大行传递零或负值时，将发生此错误。  <br/> |
|ErrorInvalidParentFolder  <br/> |当使用者为操作传递无效的父文件夹时，将发生此错误。 例如，如果您尝试在搜索文件夹中创建文件夹，则返回此错误。  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |尝试将任务完成百分比设置为无效值时，将返回此错误。 该值必须介于 0 和 100 之间， (100) 。  <br/> |
|ErrorInvalidPermissionSettings  <br/> |此错误指示权限级别与权限设置不一致。  <br/> |
|ErrorInvalidPhoneCallId  <br/> |此错误指示调用方标识符无效。  <br/> |
|ErrorInvalidPhoneNumber  <br/> |此错误指示电话号码不正确或不符合拨号计划规则。  <br/> |
|ErrorInvalidPropertyAppend  <br/> | 如果试图追加的属性不支持追加，则会发生此错误。 <br/><br/>以下是支持追加的唯一属性： <br/> <br/>- 收件人集合 (ToRecipients、CcRecipients、BccRecipients)   <br/>- Attendee 集合 (RequiredAttendees、OptionalAttendees、Resources)   <br/>- 正文  <br/>- ReplyTo  <br/><br/>  此外，如果请求中指定的格式与存储区中项目的格式不匹配，则附加邮件正文时会出现此错误。  <br/> |
|ErrorInvalidPropertyDelete  <br/> |如果对不支持删除操作的属性在 [UpdateItem](updateitem-operation.md) 操作或 [UpdateFolder](updatefolder-operation.md) 操作调用中指定了删除操作，则会发生此错误。 例如，不能删除 Item[对象的 ItemId](itemid.md) [元素。](item.md)  <br/> |
|ErrorInvalidPropertyForExists  <br/> |如果使用者在 Exists 筛选器中传递其中一个标志属性，则 [会发生](exists.md) 此错误。 例如，如果在[Exists](exists.md)元素中指定了[IsRead](isread.md)或[IsFromMe](isfromme.md)标志，则会发生此错误。 请求应改为对它们使用 [IsEqualTo](isequalto.md) 元素，因为它们是标志，因此是单个属性的一部分。  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |如果试图操作的属性不支持对该属性执行的操作，则会发生此错误。  <br/> |
|ErrorInvalidPropertyRequest  <br/> | 如果请求中指定的属性对项目类型不可用，则会发生此错误。 例如，如果在邮件的 [GetItem](getitem-operation.md) 操作调用中请求了仅在日历项目上可用的属性，或在邮件的 [UpdateItem](updateitem-operation.md) 操作调用中进行了更新，则返回此错误。 <br/> <br/>  此操作发生在以下操作中： <br/> <br/>- [GetItem 操作](getitem-operation.md) <br/>- [GetFolder 操作](getfolder-operation.md) <br/>- [UpdateItem 操作](updateitem-operation.md) <br/>- [UpdateFolder 操作](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |此错误指示您尝试操作的属性不支持对该属性执行的操作。 例如，如果您尝试设置的属性是只读的，则返回此错误。  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | 当客户端尝试更新已发送的邮件的某些属性时，在 [UpdateItem](updateitem-operation.md) 操作期间会发生此错误。<br/><br/> 例如，无法在已发送的邮件上更新以下属性： <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |如果使用推送订阅 ID 调用 [GetEvents](getevents-operation.md) 操作或 [Unsubscribe](unsubscribe-operation.md) 操作，则会发生此错误。 若要取消订阅推送订阅，必须使用取消订阅响应响应推送请求，或者断开 Web 服务连接并等待推送通知退出。  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | 当订阅操作创建"推送[](subscribe-operation.md)"订阅时，将返回此错误，并指示请求中包含的 URL 无效。<br/><br/>Web 服务必须满足以下Exchange Web 服务接受 URL： <br/> <br/>- 字符串长度 \> 0 和 \< 2083.  <br/> - 协议为 http 或 https。  <br/>- URL 可以通过 URI Microsoft .NET Framework分析。  <br/> |
|ErrorInvalidRecipients  <br/> |此错误指示邮件上的收件人集合或日历项目上的与会者集合无效。 例如，当尝试发送没有收件人的项目时，将返回此错误。  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |此错误指示搜索文件夹具有 Web 服务无法表示的收件人Exchange筛选器。 若要绕绕此错误，无需请求搜索参数即可检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |此错误指示搜索文件夹具有 Web 服务无法表示的收件人Exchange筛选器。 若要绕绕此错误，无需请求搜索参数即可检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |此错误指示搜索文件夹具有 Web 服务无法表示的收件人Exchange筛选器。 若要绕绕此错误，无需请求搜索参数即可检索文件夹。  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |此错误指示搜索文件夹具有 Web 服务无法表示的收件人Exchange筛选器。 若要绕绕此错误，无需请求搜索参数即可检索文件夹。  <br/> |
|ErrorInvalidReferenceItem  <br/> | 在下列情况下，此错误从 Forward 和 Reply 响应对象的 [CreateItem](createitem-operation.md) 操作返回：<br/>  <br/>- 引用的项目标识符不是 [Message](message-ex15websvcsotherref.md) [、CalendarItem](calendaritem.md)或 **Message** 或 **CalendarItem** 的后代。  <br/>- 引用项标识符用于 **CalendarItem，** 组织者尝试向自己回复或全部答复。  <br/>- 邮件为草稿，选择"答复"或"全部答复"。  <br/>- [SuppressReadReceipt](suppressreadreceipt.md)的引用项不是 **Message** 或 Message 的 **后代**。  <br/> |
|ErrorInvalidRequest  <br/> |当 SOAP 请求具有 SOAP 操作标头，但 SOAP 正文中没有任何内容时，将发生此错误。 请注意，SOAP 操作标头不是必需的，Exchange Web 服务可以确定从 SOAP 正文中根元素的本地名称调用的方法。  <br/> |
|ErrorInvalidRestriction  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |当指定的保留标记有一个与之关联的错误操作时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |当尝试在 **PolicyTag** 属性上设置不存在或不可见的标记时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |尝试在 **PolicyTag** 属性上设置隐式标记时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |指示保留标记 GUID 无效。  <br/> |
|ErrorInvalidRoutingType  <br/> |如果为 [EmailAddressType ](routingtype-emailaddresstype.md) 元素的 RoutingType 传递的 (类型无效，) 此错误。 通常，路由类型设置为简单邮件传输协议 (SMTP) 。  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |如果指定的持续时间结束时间不大于开始时间，或者如果将来不发生结束时间，则会发生此错误。  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |此错误指示由于版本不匹配，发送到其他服务器的代理请求无法为请求提供服务。  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |此错误指示存储区Exchange日历文件夹上的安全描述符已损坏。  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |此错误发生在尝试发送一个项目，其中 [SavedItemFolderId](saveditemfolderid.md) 在请求中指定，但 **SaveItemToFolder** 属性设置为 **false**。  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |此错误指示标头中传递的令牌格式不正确、未引用目录中的有效帐户或缺少主组 **ConnectingSID**。  <br/> |
|ErrorInvalidSharingData  <br/> |此错误指示共享元数据无效。 这可能会导致 XML 无效。  <br/> |
|ErrorInvalidSharingMessage  <br/> |此错误指示共享消息无效。 这由缺少属性导致。  <br/> |
|ErrorInvalidSid  <br/> |在请求中传递无效 SID 时，将发生此错误。  <br/> |
|ErrorInvalidSIPUri  <br/> |此错误指示 SIP 名称、拨号计划或电话号码无效的 SIP URI。  <br/> |
|ErrorInvalidServerVersion  <br/> |此错误指示请求中指定了无效的请求服务器版本。  <br/> |
|ErrorInvalidSmtpAddress  <br/> |无法分析 SMTP 地址时，将发生此错误。  <br/> |
|ErrorInvalidSubfilterType  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidSubscription  <br/> |此错误指示订阅不再有效。 这可能是因为客户端访问服务器正在重新启动或订阅已过期。  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |此错误指示订阅请求包含多个公用文件夹 ID。 订阅可以包含来自同一邮箱的多个文件夹或一个公用文件夹 ID。  <br/> |
|ErrorInvalidSyncStateData  <br/> |如果传递的[SyncState](syncstate-ex15websvcsotherref.md)数据无效[，SyncFolderItems](syncfolderitems.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)将返回此错误。 若要修复此错误，必须在没有同步状态的情况下重新同步。 确保保持同步状态 BLOB 时不会意外截断 BLOB。  <br/> |
|ErrorInvalidTimeInterval  <br/> |此错误指示指定的时间间隔无效。 开始时间必须大于或等于结束时间。  <br/> |
|ErrorInvalidUserInfo  <br/> |此错误指示为权限操作指定了内部不一致的[UserId。](userid.md) 例如，如果为可分辨用户 ID (Default 或 Anonymous) ，如果您还尝试为此用户指定 SID、主 SMTP 地址或 显示名称，则返回此错误。  <br/> |
|ErrorInvalidUserOofSettings  <br/> |此错误指示用户"外出Office (OOF) 由于缺少内部或外部答复而无效。  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |此错误发生在模拟Exchange过程中。 在 SOAP 标头中传递的调用者在 SOAP 标头中传递的无效 UPN 不可在目录中访问。  <br/> |
|ErrorInvalidUserSid  <br/> |在请求中传递无效 SID 时，将发生此错误。  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |此响应代码未使用。  <br/> |
|ErrorInvalidValueForProperty  <br/> |此错误指示限制中的比较值对于要进行比较的属性无效。<br/><br/> 例如[，DateTimeCreated](datetimecreated.md)true 的比较  >  值将返回此响应代码。 <br/><br/>如果在比较中指定了枚举属性，但要与之比较的值不是该枚举的有效值，也会返回此响应代码。  <br/> |
|ErrorInvalid使用Mark  <br/> |此错误由无效水印引起。  <br/> |
|ErrorIPGatewayNotFound  <br/> |此错误指示有效的 VoIP 网关不可用。  <br/> |
|ErrorIrresolvableConflict  <br/> |此错误指示冲突解决无法解析属性的更改。 存储中的项目可能已更改，必须进行更新。 检索更新后的更改密钥，然后重试。  <br/> |
|ErrorItemCorrupt  <br/> |此错误指示对象的状态已损坏，无法检索。 检索项目时，只有某些元素将在此状态中，如 [Body](body.md) 和 [MimeContent](mimecontent.md)。 省略这些元素，然后重试该操作。  <br/> |
|ErrorItemNotFound  <br/> |如果未找到项目或您无权访问该项目，则会发生此错误。  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |如果项目的属性请求失败，则会发生此错误。 属性可能存在，但无法检索。  <br/> |
|ErrorItemSave  <br/> |当尝试保存项目或文件夹失败时，将发生此错误。  <br/> |
|ErrorItemSavePropertyError  <br/> |当尝试保存项目或文件夹因无效属性值而失败时，将发生此错误。 响应代码包括无效属性的路径。  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |此响应代码未使用。  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |此响应代码未使用。  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |此错误指示可用性服务无法作为网络服务登录以将请求代理到相应的站点或林。 此响应通常指示配置错误。  <br/> |
|ErrorMailboxConfiguration  <br/> |此错误指示 AD DS 中的邮箱信息配置不正确。  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |此错误指示请求中的 [MailboxDataArray](mailboxdataarray.md) 元素为空。 必须至少提供一个邮箱标识符。  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |当 [MailboxDataArray](mailboxdataarray.md) 元素中提供 100 多个条目时，将发生此错误。  <br/> |
|ErrorMailboxFailover  <br/> |此错误指示访问邮箱的尝试失败，因为该邮箱在故障转移过程中。  <br/> |
|ErrorMailboxHoldNotFound  <br/> |指示未找到邮箱保留。  <br/> |
|ErrorMailboxLogonFailed  <br/> |当与邮箱的连接获取日历视图信息失败时，将发生此错误。  <br/> |
|ErrorMailboxMoveInProgress  <br/> | 此错误指示邮箱正在移动到其他邮箱存储或服务器。 此错误还可以指示邮箱位于其他服务器或邮箱数据库中。  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | 此错误指示发生了下列错误情况之一：  <br/><br/>- 邮箱存储已损坏。  <br/>- 正在停止邮箱存储。  <br/>- 邮箱存储处于脱机状态。  <br/>- 尝试访问邮箱存储时发生网络错误。  <br/>- 邮箱存储过载，不能再接受任何其他连接。  <br/>- 邮箱存储已暂停。  <br/> |
|ErrorMailRecipientNotFound  <br/> |如果 [MailboxData](mailboxdata.md) 元素信息无法映射到有效的邮箱帐户，则会发生此错误。  <br/> |
|ErrorMailTipsDisabled  <br/> |此错误指示禁用邮件提示。  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |如果您尝试创建的托管文件夹已存在于邮箱中，则会发生此错误。  <br/> |
|ErrorManagedFolderNotFound  <br/> |当请求中指定的文件夹名称未映射到 AD DS 中的托管文件夹定义时，将发生此错误。 只能为 AD DS 中定义的文件夹创建托管文件夹的实例。 请检查名称并重试。  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |此错误指示托管文件夹根目录从邮箱中删除，或文件夹位于同一父文件夹中，该父文件夹中具有托管文件夹根目录的名称。 如果创建根托管文件夹的尝试失败，也会发生这种情况。  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |此错误指示建议引擎在尝试生成建议时遇到问题。  <br/> |
|ErrorMessageDispositionRequired  <br/> | 如果未设置 **MessageDisposition** 属性，则会发生此错误。<br/><br/> 以下各项需要此属性： <br/> <br/>-[创建或更新的项目时](createitem-operation.md)[，CreateItem 操作和 UpdateItem](updateitem-operation.md) [操作是消息](message-ex15websvcsotherref.md)。  <br/>- [CancelCalendarItem、AcceptItem、DeclineItem](cancelcalendaritem.md)或[TentativelyAcceptItem](tentativelyacceptitem.md)响应对象。 [](acceptitem.md) [](declineitem.md)  <br/> |
|ErrorMessageSizeExceeded  <br/> |此错误指示您尝试发送的邮件超出了允许的限制。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |此错误指示找不到给定的域。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |此错误指示邮件跟踪服务无法跟踪邮件。  <br/> |
| ErrorMessageTrackingTransientError  <br/> |此错误指示邮件跟踪服务是关闭还是繁忙。 此错误代码指示暂时性错误。 收到此错误时，客户端可以重试连接到服务器。  <br/> |
|ErrorMimeContentConversionFailed  <br/> |当 MIME 内容不是 CreateItem 操作的有效 iCal 时， [将发生此错误](createitem-operation.md)。 对于 [GetItem 操作](getitem-operation.md)，此响应指示无法生成 MIME 内容。  <br/> |
|ErrorMimeContentInvalid  <br/> |当 MIME 内容无效时，将发生此错误。  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |当请求中的 MIME 内容不是有效的 base 64 字符串时，将发生此错误。  <br/> |
|ErrorMissingArgument  <br/> |此错误指示请求中缺少必需的参数。 响应消息文本指示要检查的参数。  <br/> |
|ErrorMissingEmailAddress  <br/> |此错误指示在请求中指定了可分辨文件夹 ID，但提出请求的帐户在系统中没有邮箱。 在这种情况下，您必须在[DistinguishedFolderId](distinguishedfolderid.md)下提供[Mailbox](mailbox.md)子元素。  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |此错误指示在请求中指定了可分辨文件夹 ID，但提出请求的帐户在系统中没有邮箱。 在这种情况下，您必须在[DistinguishedFolderId](distinguishedfolderid.md)下提供[Mailbox](mailbox.md)子元素。 此响应从 [CreateManagedFolder](createmanagedfolder-operation.md)操作 返回。  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |如果缺少 [NonEmptyStringType (EmailAddress ](emailaddress-nonemptystringtype.md)) ，则会发生此错误。  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |如果缺少 [ReferenceItemId，则会发生](referenceitemid.md) 此错误。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |绝不会返回此错误代码。  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |当尝试在 [CreateAttachment](createattachment-operation.md)操作请求的 **ItemAttachment** 元素中不包含 item 元素时，将返回此错误。  <br/> |
|ErrorMissingManagedFolderId  <br/> |当缺少文件夹的策略 IDs 属性、0x6732标记时，将发生此错误。 你应该认为该文件夹已损坏。  <br/> |
|ErrorMissingRecipients  <br/> |此错误指示您尝试发送项目，但不包括收件人。 请注意，如果使用导致邮件发送的邮件处置调用 [CreateItem](createitem-operation.md) 操作，则得到以下响应代码 **：ErrorInvalidRecipients**。  <br/> |
|ErrorMissingUserIdInformation  <br/> |此错误指示权限集尚未完全指定[UserId。](userid.md)  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |此错误指示在请求中指定了多个 [ExchangeImpersonation](exchangeimpersonation.md) 元素值。  <br/> |
|ErrorMoveCopyFailed  <br/> |此错误指示移动或复制操作失败。 当您接受"已删除邮件"文件夹中的会议请求时，将发生 [CreateItem](createitem-operation.md) 操作中的移动。 此外，如果拒绝会议请求、取消日历项目或者从日历中删除会议，会议将移动到"已删除邮件"文件夹。  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |如果尝试移动可分辨文件夹，则会发生此错误。  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |当请求尝试访问多个邮箱服务器时，将发生此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |如果 [ResolveNames](resolvenames-operation.md) 操作返回多个结果或您指定的不明确名称与目录中多个对象匹配，则会发生此错误。 响应代码在响应数据中包含匹配的名称。  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |此错误指示呼叫者在系统上没有邮箱。 [ResolveNames 操作](resolvenames-operation.md)或[ExpandDL 操作](expanddl-operation.md)对于在没有邮箱的情况下连接用户无效。  <br/> |
|ErrorNameResolutionNoResults  <br/> |此错误指示 [ResolveNames 操作未](resolvenames-operation.md) 返回任何结果。  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |当 Web 服务找不到服务器来处理请求时，必须返回此错误代码。  <br/> |
|ErrorNoCalendar  <br/> |如果邮箱没有"日历"文件夹，则会发生此错误。  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但目标站点中未将客户端访问服务器配置为 Windows 身份验证，因此无法代理该请求。  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但目标站点中未针对 SSL 连接配置客户端访问服务器，因此无法代理该请求。  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但目标站点中没有任何客户端访问服务器可接受产品版本来接收请求，因此无法代理该请求。  <br/> |
|ErrorNoFolderClassOverride  <br/> |如果在创建非泛型文件夹的项目时设置 [FolderClass](folderclass.md) 元素，则会发生此错误。 对于类型文件夹（如 [CalendarFolder](calendarfolder.md) 和 [TasksFolder），](tasksfolder.md)文件夹类是隐含的。 使用 [UpdateFolder](updatefolder-operation.md) 操作将文件夹类设置为其他文件夹类型会导致 **ErrorObjectTypeChanged** 响应。 请改为使用泛型文件夹类型，但将文件夹类设置为您需要的值。 ExchangeWeb 服务将创建正确的强类型文件夹。  <br/> |
|ErrorNoFreeBusyAccess  <br/> |此错误指示呼叫者对"日历"文件夹没有忙/闲查看权限。  <br/> |
|ErrorNonExistentMailbox  <br/> | 此错误在下列情况下发生： <br/> <br/>- 电子邮件地址在 [CreateManagedFolder 中为空](createmanagedfolder.md)。  <br/>- 电子邮件地址不引用在正文或 SOAP 标头中采用电子邮件地址的请求（如在 Exchange 调用中）中的有效帐户。  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |当呼叫者传递非主 SMTP 地址时，将发生此错误。 该响应包括要使用的正确 SMTP 地址。  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |此错误指示不能通过属性标记引用自定义区域（0x8000或更大）中的 MAPI 属性。 您必须将 EWS 托管 API [PropertySetId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)属性或 EWS [ExtendedFieldURI](extendedfielduri.md) 元素与 PropertySetId 属性一同使用。  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |此响应代码未使用。  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |如果没有公用文件夹服务器或调用方没有主公用服务器，则必须返回此错误代码。  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，但该站点中没有客户端访问服务器响应，因此无法代理该请求。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |此错误指示呼叫者尝试将日历或联系人文件夹中的权限授予另一个组织中用户，但尝试失败。  <br/> |
|ErrorNotDelegate  <br/> |此错误指示用户不是邮箱的代理。 当在委派列表中找不到指定的委派用户时 [，GetDelegate](getdelegate-operation.md)操作 [、RemoveDelegate](removedelegate-operation.md)操作和 [UpdateDelegate](updatedelegate-operation.md) 操作将返回它。  <br/> |
|ErrorNotEnoughMemory  <br/> |此错误指示由于内存不足无法完成操作。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |此错误指示不支持共享消息。  <br/> |
|ErrorObjectTypeChanged  <br/> |如果已更改，则对象类型错误。  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |当更新事件的开始时间或结束[](start.md)时间，[](end-ex15websvcsotherref.md)以便计划发生时间早于或晚于相应的上一次或下一次发生时，将发生此错误。  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |此错误指示给定事件的时间分配与同一定期项目的另一个事件重叠。 当给定事件的长度（以分钟数表示）大于 Int32.MaxValue 时，也会发生此响应。  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |此错误指示当前操作无效文件夹根目录。  <br/> |
|ErrorOrganizationNotFederated  <br/> |此错误指示请求者的组织未联合，因此请求者无法创建要发送给外部用户的共享邮件，或不接受从外部用户接收的共享邮件。  <br/> |
|ErrorParentFolderIdRequired  <br/> |此响应代码未使用。  <br/> |
|ErrorParentFolderNotFound  <br/> |当找不到父文件夹时 [，此错误发生在 CreateFolder](createfolder-operation.md) 操作中。  <br/> |
|ErrorPasswordChangeRequired  <br/> |此错误指示您必须先更改密码，然后才能访问此邮箱。 如果已创建一个新帐户，并且管理员指示用户必须在首次登录时更改密码，则会发生此情况。 不能使用 Web 服务更新Exchange密码。 必须使用 Web App 等Microsoft Office Outlook更改密码。  <br/> |
|ErrorPasswordExpired  <br/> |此错误指示密码已过期。 不能使用 Web 服务更改Exchange密码。 必须使用工具（如Outlook Web App更改密码。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |此错误指示请求者尝试将其日历或联系人文件夹中的权限授予外部用户，但分配给请求者共享策略指示请求的权限级别高于共享策略允许的权限级别。  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |此错误指示电话号码格式不正确。  <br/> |
|ErrorPropertyUpdate  <br/> |此错误指示更新因属性值无效而失败。 响应消息包括无效的属性路径。  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorPropertyValidationFailure  <br/> |此响应代码未使用。  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |此错误指示请求引用了存在于另一个客户端访问服务器上，但尝试将请求代理到该客户端访问服务器失败。  <br/> |
|ErrorProxyCallFailed  <br/> |此响应代码未使用。  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |此错误指示请求引用了另一个 Active Directory 站点中的邮箱，并且原始呼叫者是 3，000 多个组的成员。  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |此错误指示尝试Exchange [GetUserAvailabilityRequest](getuseravailabilityrequest.md)请求时向另一个客户端访问服务器发送的 Web 服务的请求无效。 此响应代码通常指示发生了配置或权限错误，或者有人尝试模仿可用性代理请求失败。  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |此错误指示 Web Exchange尝试将可用性请求代理到另一个客户端访问服务器以实施，但请求失败。 此响应可能是由网络连接问题或请求超时问题导致的。  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |如果 Web 服务无法确定请求是在目标服务器上运行，还是将被代理到其他服务器，则必须返回此错误代码。  <br/> |
|ErrorProxyTokenExpired  <br/> |此响应代码未使用。  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |当找不到公用文件夹邮箱 URL 时，将发生此错误。 此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |当尝试访问公用文件夹并且尝试失败时，将发生此错误。 此错误在 Exchange 2013Exchange Server 2013 中引入。  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |当传递给[GetUserAvailability](getuseravailability-operation.md)操作的收件人位于运行 Exchange Server 版本早于 Exchange 2007 的计算机上，并且从公用文件夹服务器检索收件人的忙/闲信息的请求失败时，将发生此错误。  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |当传递给[GetUserAvailability](getuseravailability-operation.md)操作的收件人位于运行 Exchange Server 版本早于 Exchange 2007 的计算机上，并且从公用文件夹服务器检索收件人的忙/闲信息请求失败，因为组织单位没有关联的公用文件夹服务器，则会发生此错误。  <br/> |
|ErrorPublicFolderSyncException  <br/> |当同步操作对主公用文件夹邮箱成功，但辅助公用文件夹邮箱失败时，会发生此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorQueryFilterTooLong  <br/> |此错误指示搜索文件夹限制可能有效，但不受 EWS 支持。 ExchangeWeb 服务限制最多包含 255 个筛选器表达式。 如果尝试绑定到超过 255 的现有搜索文件夹，将返回此响应代码。  <br/> |
|ErrorQuotaExceeded  <br/> |超出邮箱配额时发生此错误。  <br/> |
|ErrorReadEventsFailed  <br/> |当检索事件信息时发生故障时 [，GetEvents](getevents-operation.md) 操作或推送通知将返回此错误。 返回此错误时，订阅将被删除。 基于上一个已知水印重新创建事件同步。  <br/> |
|ErrorReadReceiptNotPending  <br/> |如果尝试在邮件发件人未请求邮件上的已读回执时禁止显示已读回执，或者邮件位于"垃圾邮件"文件夹中， [则 CreateItem](createitem-operation.md) 操作将返回此错误。  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |当重复周期的结束日期在 9/1/4500 之后时，将发生此错误。  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |当指定的定期周期没有指定范围内的任何实例时，将发生此错误。  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |此错误指示删除委托后无法保存委派列表。  <br/> |
|ErrorRequestAborted  <br/> |此响应代码未使用。  <br/> |
|ErrorRequestStreamTooBig  <br/> | 当请求流大于 400 KB 时，将发生此错误。  <br/> |
|ErrorRequiredPropertyMissing  <br/> |当 [CreateAttachment](createattachment-operation.md) 操作请求中缺少必需属性时，将返回此错误。 响应中包含缺少的属性 URI。  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |此错误指示呼叫者向 [ResolveNames](resolvenames-operation.md)操作指定了非联系人文件夹的文件夹。  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |此错误指示呼叫者向 [ResolveNames](resolvenames-operation.md)操作指定了多个联系人文件夹。  <br/> |
|ErrorResponseSchemaValidation  <br/> |此响应代码未使用。  <br/> |
|ErrorRestrictionTooLong  <br/> |如果限制包含的节点数超过 255 个，则会发生此错误。  <br/> |
|ErrorRestrictionTooComplex  <br/> |当 Web 服务无法评估限制时，Exchange此错误。  <br/> |
|ErrorResultSetTooBig  <br/> |此错误指示给定收件人的日历条目数超过了允许的 1000 个限制。 请减小窗口，然后重试。  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |当未找到 [SavedItemFolderId 时，将](saveditemfolderid.md) 发生此错误。  <br/> |
|ErrorSchemaValidation  <br/> | 如果无法根据架构验证请求，则会发生此错误。  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |此错误指示已创建搜索文件夹，但从未在文件夹上设置搜索条件。 这仅在访问使用另一个 API 或客户端创建的损坏的搜索文件夹时发生。 若要修复此错误，请使用 [UpdateFolder](updatefolder-operation.md) 操作将 [SearchParameters](searchparameters.md) 元素设置为包含应位于文件夹上的限制。  <br/> |
|ErrorSendAsDenied  <br/> | 出现以下两个条件时，将发生此错误： <br/> <br/>- 已授予用户 CanActAsOwner 权限，但不向用户授予主体邮箱的委派权限。  <br/>- 同一用户尝试使用 SendAndSaveCopy 选项在主体邮箱中创建和发送电子邮件。<br/>  <br/>  结果为 ErrorSendAsDenied 错误，并创建主体的"草稿"文件夹中的电子邮件。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |如果请求中缺少 **SendMeetingCancellations** 属性，并且要删除的项目是日历项目，则 [DeleteItem](deleteitem-operation.md)操作将返回此错误。  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |如果请求中缺少 **SendMeetingInvitationsOrCancellations** 属性，并且要更新的项目是日历项目，则 [UpdateItem](updateitem-operation.md)操作将返回此错误。  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |如果请求中缺少 **SendMeetingInvitations** 属性，并且要创建的项目是日历项目，则 [CreateItem](createitem-operation.md)操作将返回此错误。  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |此错误指示在组织者发送会议请求后，无法更新请求。 若要修改会议，请修改日历项目，而不是会议请求。  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |此错误指示在任务发起人发送任务请求后，无法更新该请求。  <br/> |
|ErrorServerBusy  <br/> |当服务器繁忙时，将发生此错误。  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |此错误指示Exchange Web 服务尝试将用户可用性请求代理到收件人的适当林，但由于服务发现失败，它无法确定将请求发送到何处。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |此错误指示尚未在 Active Directory 数据库中设置外部 URL 属性。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |此错误指示同步共享文件夹的尝试失败。 <br/><br/>发生以下情况时，将返回此错误代码：<br/><br/>- 找不到共享文件夹的订阅。<br/>- 未找到共享文件夹。<br/>- 未找到相应的目录用户。<br/>- 用户不再存在。<br/>- 约会无效。<br/>- 联系人项目无效。<br/>- 与远程服务器通信失败。  <br/> |
|ErrorStaleObject  <br/> |如果更改键不是最新的或未提供，则此错误发生在 [UpdateItem](updateitem-operation.md) 操作或 [SendItem](senditem-operation.md) 操作中。 调用 [GetItem 操作](getitem-operation.md) 以检索更新后的更改密钥，然后再次尝试该操作。  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |此错误 指示用户无法立即发送更多请求，因为已达到提交配额。  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |此错误发生在尝试使用未创建该订阅的帐户访问订阅时。 每个订阅都只能由订阅的创建者访问。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |此错误指示如果您不是所有者或没有邮箱的所有者访问权限，则您无法创建订阅。  <br/> |
|ErrorSubscriptionNotFound  <br/> |如果找不到与 [GetEvents ](subscriptionid-getevents.md) (SubscriptionId) 发生此错误。 订阅可能已过期，Exchange Web 服务进程可能重新启动，或者传递了无效的订阅。 如果订阅有效，请重新创建具有最新水印的订阅。 这由 Unsubscribe [操作或](unsubscribe-operation.md) [GetEvents 操作响应](getevents-operation.md) 返回。  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |当对已取消订阅的订阅提出请求时，必须返回此错误代码。  <br/> |
|ErrorSyncFolderNotFound  <br/> |如果找不到指定的父文件夹 [，SyncFolderItems](syncfolderitems-operation.md) 操作将返回此错误。  <br/> |
|ErrorTeamMailboxNotFound  <br/> |此错误指示未找到团队邮箱。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |此错误指示已找到团队邮箱，但它未链接到 SharePoint 服务器。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |此错误指示已找到团队邮箱，但指向 SharePoint 服务器的链接无效。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |此错误代码未使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |此错误代码未使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |此错误指示尝试向团队邮箱所有者发送通知失败。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |此错误指示尝试访问团队邮箱时可能会发生的常规错误。 请尝试稍后提交请求。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorTimeIntervalTooBig  <br/> |此错误指示指定的时间窗口大于允许的限制。 默认情况下，允许的限制是 42。  <br/> |
|ErrorTimeoutExpired  <br/> | 当没有足够的时间完成对请求的处理时，将发生此错误。  <br/> |
|ErrorTimeZone  <br/> |此错误指示存在时区错误。  <br/> |
|ErrorToFolderNotFound  <br/> |此错误指示目标文件夹不存在。  <br/> |
|ErrorTokenSerializationDenied  <br/> |如果调用方尝试执行令牌序列化请求，但客户端访问服务器上没有 ms-Exch-CALLER-TokenSerialization 权限，则会发生此错误。  <br/> |
|ErrorTooManyObjectsOpened  <br/> |当超出打开对象的内部限制时，将发生此错误。  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |此错误指示用户的拨号计划不可用。  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |此错误指示找不到用户。  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |此错误指示可以找到拨号计划的有效服务器来处理请求。  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |此响应代码未使用。  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |如果尝试从组中删除 IM 联系人失败，则会发生此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorUnsupportedCulture  <br/> |当您尝试将 **Culture** 属性设置为 **System.Globalization.CultureInfo** 类无法分析的值时，将发生此错误。  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |当调用方尝试使用类型对象、对象数组、错误或 null 的扩展属性时，将发生此错误。  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |当您尝试检索或设置[PostItem、Message](postitem.md)或[CalendarItem](calendaritem.md)对象外的项目的 MIME[](message-ex15websvcsotherref.md)内容时，将发生此错误。  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |当调用方传递的属性对查询无效时，将发生此错误。 使用计算属性时可能发生此情况。  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |当调用方传递的属性对按属性排序或分组无效时，将发生此错误。 使用计算属性时可能发生此情况。  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |此响应代码未使用。  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |此错误指示搜索文件夹限制可能有效，但不受 EWS 支持。  <br/> |
|ErrorUnsupportedRecurrence  <br/> |此错误指示任务不支持指定的定期。  <br/> |
|ErrorUnsupportedSubFilter  <br/> |此响应代码未使用。  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |此错误指示 Web Exchange在存储区中发现了属性类型，但它无法生成属性类型的 XML。  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |此错误指示在更新委托后无法保存委派列表。  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |当更改说明中列出的单个属性路径与在实际 [Item](item.md) 或 Folder 对象中设置的单个属性不匹配时， [将发生](folder.md) 此错误。  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |此错误指示请求程序未启用。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |此错误指示请求者尝试将其日历或联系人文件夹中的权限授予外部用户，但分配给请求者共享策略指示该策略中未列出外部用户的域。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指示请求者的组织具有一组联盟域，但请求者的组织没有任何具有其中一个联盟域的 SMTP 代理地址。  <br/> |
|ErrorValueOutOfRange  <br/> |此错误指示日历视图开始日期或结束日期设置为 1/1/0001 12：00：00 AM 或 12/31/9999 11：59：59 PM。  <br/> |
|ErrorVirusDetected  <br/> |此错误指示邮件Exchange邮件中检测到病毒。  <br/> |
|ErrorVirusMessageDeleted  <br/> |此错误指示该Exchange在邮件中检测到病毒并将其删除。  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |此响应代码未使用。  <br/> |
|ErrorWebRequestInInvalidState  <br/> |此响应代码未使用。  <br/> |
|ErrorWin32InteropError  <br/> |此错误指示与非托管代码通信期间出现内部故障。  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |此响应代码未使用。  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |此响应代码未使用。  <br/> |
|ErrorWrongServerVersion  <br/> |此错误指示只能向与邮箱服务器版本相同的服务器提出请求。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |此错误指示请求是由服务器版本与主体邮箱服务器不同的代理提出的。  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |绝不会返回此错误代码。  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |指定存在重复的 SOAP 标头。  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | 指定同步共享文件夹的尝试失败。<br/><br/> 在出现此错误代码时，必须返回此错误代码：<br/><br/>- 找不到共享文件夹的订阅。  <br/>- 未找到共享文件夹。  <br/>- 未找到相应的目录用户。  <br/>- 用户不再存在。  <br/>- 约会无效。  <br/>- 联系人项目无效。  <br/>- 与远程服务器通信失败。  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |指定尚未在 Active Directory 数据库中设置外部 URL 属性。 如果尚未在 Active Directory 数据库中设置外部 URL 属性，则必须返回此错误代码。  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |指定已达到获取通讯组列表的忙/闲信息的最大组成员计数。 当已达到获取通讯组列表的忙/闲信息时，必须返回此错误。  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |指定请求中同时存在 DataType 和 ShareFolderId 元素。 如果请求中同时存在 DataType 和 ShareFolderId 元素，则必须返回此错误代码。  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |指定呼叫者尝试将日历或联系人文件夹中的权限授予另一个组织中用户，但尝试失败。 当为呼叫者禁用共享策略时，或者分配给呼叫者的共享策略不允许对请求的级别或请求的文件夹类型进行共享时，必须返回此错误代码。  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |指定请求者尝试将其日历或联系人文件夹中的权限授予外部用户，但分配给请求者共享策略指定外部用户的域未列在策略中。  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |指定请求者尝试将日历或联系人文件夹中的权限授予外部用户，但分配给请求者共享策略指定请求的权限级别高于共享策略允许的权限级别。  <br/> |
|ErrorOrganizationNotFederated  <br/> |指定请求者的组织未联合，因此请求者无法创建要发送给外部用户的共享邮件，或不接受从外部用户接收的共享邮件。 如果请求者的组织未联合，则必须返回此错误代码。  <br/> |
|ErrorMailboxFailover  <br/> |指定由于邮箱在故障转移过程中，尝试访问邮箱失败。  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |指定共享邀请发件人未创建共享邀请元数据。 如果共享邀请发件人没有创建共享邀请元数据，则必须返回此错误代码。  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |指定邮件跟踪服务无法跟踪邮件。  <br/> |
|ErrorMessageTrackingTransientError  <br/> |指定邮件跟踪服务是关闭还是繁忙。 此错误代码指定暂时性错误。 收到此错误时，客户端可以重试连接到服务器。  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |指定找不到给定域。  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |指定请求者的组织具有一组联盟域，但请求者的组织没有任何具有其中一个联盟域的 SMTP 代理地址。  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |指定呼叫者为另一个组织中用户请求忙/闲信息，但组织关系未启用忙/闲。  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |指定请求者的组织联合对象未正确配置。  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |指定共享消息不供呼叫者使用。  <br/> |
|ErrorInvalidSharingData  <br/> |指定共享元数据无效。 这可能会导致 XML 无效。  <br/> |
|ErrorInvalidSharingMessage  <br/> |指定共享邮件是无效。 这由缺少属性导致。  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |指定不支持共享邮件。  <br/> |
|ErrorApplyConversationActionFailed  <br/> |如果操作不能应用于对话中的一个或多个项目，则必须返回此错误。  <br/> |
|ErrorInboxRulesValidationError  <br/> |如果任何规则未验证，则必须返回此错误。  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |当尝试管理收件箱规则时，在另一个客户端访问收件箱规则后，必须返回此错误。  <br/> |
|ErrorRulesOverQuota  <br/> |当超过用户的规则配额时，必须返回此错误。  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |如果打开了第二个订阅连接，则必须将此错误返回到第一个订阅连接。  <br/> |
|ErrorMissedNotificationEvents  <br/> |如果错过事件通知，则必须返回此错误。  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |当 Active Directory 域服务中的旧版可分辨名称与 AD DS (重复时，将) 。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |此错误指示请求获取客户端访问令牌的请求无效。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorNoSpeechDetected  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorUMServerUnavailable  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorRecipientNotFound  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorRecognizerNotInstalled  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorSpeechGrammarError  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |如果 SOAP 标头中的 [ManagementRole](managementrole.md) 标头不正确，则返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorLocationServicesDisabled  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |此错误仅供内部使用。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorWeatherServiceDisabled  <br/> |此错误仅供内部使用。  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |当在未对内容索引搜索使用 [QueryString ](querystring-string.md) (String) 的情况下执行范围搜索尝试时，将返回此错误。 这适用于 **SearchMailboxes 和** **FindConversation** 操作。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |存档邮箱搜索不成功时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |当存档邮箱的 URL 不可发现时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |当获取远程存档邮箱文件夹的操作失败时，将发生此错误。  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |当查找远程存档邮箱文件夹的操作失败时，将发生此错误。  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |此错误发生在获取远程存档邮箱项目的操作失败时。  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |导出远程存档邮箱项目的操作失败时发生此错误。  <br/> |
|ErrorInvalidPhotoSize  <br/> |如果从服务器请求了无效的照片大小，则返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |在 **GetUserPhoto** 操作请求中请求意外的照片大小时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |当 **SearchMailboxes** 操作请求包含太多邮箱进行搜索时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |此错误指示未找到此用户的保留标记。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |在租户或服务器上禁用发现搜索时，将返回此错误。 此错误是在 2013 Exchange引入的。  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |此错误发生在尝试使用[SeekToConditionPageItemView](seektoconditionpageitemview.md)调用[FindItem](finditem-operation.md)操作以提取日历项目时，此操作不受支持。  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |此错误仅供内部使用。  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |此错误仅供内部使用。  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |租户标记为删除。  <br/> |
|ErrorInvalidLicense  <br/> |用户没有有效的许可证。  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |已超出每个文件夹的邮件接收配额。  <br/> |
   
## <a name="remarks"></a>备注

此元素不是必需的，并不包含在所有响应中。 
  
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

