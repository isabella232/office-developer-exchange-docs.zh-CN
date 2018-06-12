---
title: ResponseMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 2071bed8-ea66-4627-aa4f-a1d9a025cf3d
description: ResponseMessages 元素包含 Exchange Web 服务请求的响应消息。
ms.openlocfilehash: dc56476447cceac4eca56c171b148ac1ed177cb3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827203"
---
# <a name="responsemessages"></a>ResponseMessages

**ResponseMessages**元素包含 Exchange Web 服务请求的响应消息。 
  
```XML
<ResponseMessages>
   <CreateItemResponseMessage/>
</ResponseMessages>
```

```xml
<ResponseMessages>
   <DeleteItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <EmptyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UploadItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExportItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ResolveNamesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExpandDLResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetServerTimeZonesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetStreamingEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UnsubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendNotificationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderHierarchyResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateManagedFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ConvertIdResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingMetadataResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <RefreshSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomListsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRemindersResponse/>
</ResponseMessages
```

```xml 
<ResponseMessages>
   <PerformReminderActionResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ApplyConversationActionResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetPasswordExpirationDateResponse />
</ResponseMessages>
```


**ArrayOfResponseMessagesType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含状态和单个 CopyFolder 请求的结果。  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含状态和单个 CopyItem 请求的结果。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含状态和单个 CreateAttachment 请求的结果。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含状态和单个 CreateFolder 请求的结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含状态和单个 CreateItem 请求的结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含状态和单个 CreateManagedFolder 请求的结果。  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含状态和单个 DeleteAttachment 请求的结果。  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |包含状态和单个 DeleteFolder 请求的结果。  <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |包含状态和单个删除项请求的结果。  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |包含状态和单个[EmptyFolder](emptyfolder.md)请求的结果。  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含状态和单个 ExpandDL 请求的结果。  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含状态和单个 FindFolder 请求的结果。  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含状态和单个 FindItem 请求的结果。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含状态和单个 GetAttachment 请求的结果。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含状态和单个 UploadItems 请求的结果。  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |包含状态和单个 ExportItems 请求的结果。  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含状态和单个 GetEvents 请求的结果。  <br/> |
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |包含状态和单个 GetStreamingEvents 请求的结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含状态和单个 GetFolder 请求的结果。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含状态和单个 GetItem 请求的结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含状态和单个 MoveFolder 请求的结果。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含状态和单个 MoveItem 请求的结果。  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含状态和 ResolveNames 请求的结果。  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |包含状态和单个 SendItem 请求的结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含状态和单个 SendNotification 请求的结果。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含状态和单个 Subscribe 请求的结果。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含状态和 SyncFolderHierarchy 请求的结果。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含状态和 SyncFolderItems 请求的结果。  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |包含状态和单个取消订阅请求的结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含状态和单个 UpdateFolder 请求的结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含状态和单个 UpdateItem 请求的结果。  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含状态和 ConvertId 请求的结果。  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |包含状态和 GetSharingMetadata 请求的结果。  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |包含状态和 RefreshSharingFolder 请求的结果。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含状态和 GetSharingFolder 请求的结果。  <br/> |
|[CreateUserConfigurationResponseMessage](createuserconfigurationresponsemessage.md) <br/> |包含状态和 CreateUserConfiguration 请求的结果。  <br/> |
|[DeleteUserConfigurationResponseMessage](deleteuserconfigurationresponsemessage.md) <br/> |包含状态和 DeleteUserConfiguration 请求的结果。  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |包含状态和 GetUserConfiguration 请求的结果。  <br/> |
|[UpdateUserConfigurationResponseMessage](updateuserconfigurationresponsemessage.md) <br/> |包含状态和 UpdateUserConfiguration 请求的结果。  <br/> |
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |包含状态和 GetRoomLists 请求的结果。  <br/> |
|[GetRoomsResponse](getroomsresponse.md) <br/> |包含状态和 GetRooms 请求的结果。  <br/> |
|[GetRemindersResponse](getremindersresponse.md) <br/> |包含状态和 GetReminders 请求的结果。  <br/> |
|[PerformReminderActionResponse](performreminderactionresponse.md) <br/> |包含状态和 PerformReminderAction 请求的结果。  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |包含状态和单个 GetServerTimeZones 请求的结果。  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |包含状态和[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的结果。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyFolderResponse](copyfolderresponse.md) <br/> |定义 CopyFolder 请求的响应。  <br/> |
|[CopyItemResponse](copyitemresponse.md) <br/> |定义 CopyItem 请求的响应。  <br/> |
|[CreateAttachmentResponse](createattachmentresponse.md) <br/> |定义 CreateAttachment 请求的响应。  <br/> |
|[CreateFolderResponse](createfolderresponse.md) <br/> |定义 CreateFolder 请求的响应。  <br/> |
|[CreateItemResponse](createitemresponse.md) <br/> |定义 CreateItem 请求的响应。  <br/> |
|[CreateManagedFolderResponse](createmanagedfolderresponse.md) <br/> |定义 CreateManagedFolder 请求的响应。  <br/> |
|[DeleteAttachmentResponse](deleteattachmentresponse.md) <br/> |定义 DeleteAttachment 请求的响应。  <br/> |
|[DeleteFolderResponse](deletefolderresponse.md) <br/> |定义 DeleteFolder 请求的响应。  <br/> |
|[DeleteItemResponse](deleteitemresponse.md) <br/> |定义删除项请求的响应。  <br/> |
|[EmptyFolderResponse](emptyfolderresponse.md) <br/> |定义 EmptyFolder 请求的响应。  <br/> |
|[ExpandDLResponse](expanddlresponse.md) <br/> |定义 ExpandDL 请求的响应。  <br/> |
|[ExportItemsResponse](exportitemsresponse.md) <br/> |代表对单个 ExportItems 请求响应。  <br/> |
|[FindFolderResponse](findfolderresponse.md) <br/> |定义 FindFolder 请求的响应。  <br/> |
|[FindItemResponse](finditemresponse.md) <br/> |定义 FindItem 请求的响应。  <br/> |
|[GetAttachmentResponse](getattachmentresponse.md) <br/> |定义 GetAttachment 请求的响应。  <br/> |
|[GetEventsResponse](geteventsresponse.md) <br/> |定义 GetEvents 请求的响应。  <br/> |
|[GetStreamingEventsResponse](getstreamingeventsresponse.md) <br/> |定义 GetStreamingEvents 请求的响应。  <br/> |
|[GetFolderResponse](getfolderresponse.md) <br/> |定义 GetFolder 请求的响应。  <br/> |
|[GetItemResponse](getitemresponse.md) <br/> |定义 GetItem 请求的响应。  <br/> |
|[MoveFolderResponse](movefolderresponse.md) <br/> |定义 MoveFolder 请求的响应。  <br/> |
|[MoveItemResponse](moveitemresponse.md) <br/> |定义 MoveItem 请求的响应。  <br/> |
|[ResolveNamesResponse](resolvenamesresponse.md) <br/> |定义 ResolveNames 请求的响应。  <br/> |
|[SendItemResponse](senditemresponse.md) <br/> |定义 SendItem 请求的响应。  <br/> |
|[SendNotificationResult](sendnotificationresult.md) <br/> |定义 SendNotification 请求的响应。  <br/> |
|[SubscribeResponse](subscriberesponse.md) <br/> |定义的 Subscribe 请求的响应。  <br/> |
|[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) <br/> |定义 SyncFolderHierarchy 请求的响应。  <br/> |
|[SyncFolderItemsResponse](syncfolderitemsresponse.md) <br/> |定义 SyncFolderItems 请求的响应。  <br/> |
|[UnsubscribeResponse](unsubscriberesponse.md) <br/> |定义取消订阅请求的响应。  <br/> |
|[UpdateFolderResponse](updatefolderresponse.md) <br/> |定义 UpdateFolder 请求的响应。  <br/> |
|[UpdateItemResponse](updateitemresponse.md) <br/> |定义 UpdateItem 请求的响应。  <br/> |
|[ConvertIdResponse](convertidresponse.md) <br/> |包含 ConvertId 请求的响应。  <br/> |
|[GetServerTimeZonesResponse](getservertimezonesresponse.md) <br/> |定义 GetServerTimeZones 请求的响应。  <br/> |
|[CreateUserConfigurationResponse](createuserconfigurationresponse.md) <br/> |定义 CreateUserConfiuration 请求的响应。  <br/> |
|[DeleteUserConfigurationResponse](deleteuserconfigurationresponse.md) <br/> |定义 DeleteUserConfiguration 请求的响应。  <br/> |
|[GetUserConfigurationResponse](getuserconfigurationresponse.md) <br/> |定义 GetUserConfiguration 请求的响应。  <br/> |
|[UpdateUserConfigurationResponse](updateuserconfigurationresponse.md) <br/> |定义 UpdateUserConfiguration 请求的响应。  <br/> |
|[ApplyConversationActionResponse](applyconversationactionresponse.md) <br/> |定义[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的响应。  <br/> |
|[GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md) <br/> |定义[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)操作请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExportItems 操作](exportitems-operation.md) 
- [UploadItems 操作](uploaditems-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

