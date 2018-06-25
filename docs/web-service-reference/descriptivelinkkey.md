---
title: DescriptiveLinkKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DescriptiveLinkKey
api_type:
- schema
ms.assetid: f7f36749-00f3-4915-b17c-e3caa0af6e67
description: DescriptiveLinkKey 元素是当前未使用，并且保留以供将来使用。 它包含的值为 0。
ms.openlocfilehash: c917f401c0954a68ddce1226b522d54c87502462
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753852"
---
# <a name="descriptivelinkkey"></a>DescriptiveLinkKey

**DescriptiveLinkKey**元素是当前未使用，并且保留以供将来使用。 它包含的值为 0。 
  
```XML
<DescriptiveLinkKey/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | 提供有关的响应状态的描述性信息。  <br/><br/>以下是一些可能的 XPath 表达式到此元素：<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>`/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>`/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |包含状态和单个**删除项**请求的结果。  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |包含状态和单个**SendItem**请求的结果。  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |包含状态和单个**DeleteFolder**请求的结果。  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含状态和单个**DeleteAttachment**请求的结果。  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |包含状态和单个**取消订阅**请求的结果。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含状态和单个**CreateFolder**请求的结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含状态和单个**GetFolder**请求的结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含状态和单个**UpdateFolder**请求的结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含状态和单个**MoveFolder**请求的结果。  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含状态和单个**CopyFolder**请求的结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含状态和单个**CreateManagedFolder**请求的结果。  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含状态和单个**FindFolder**请求的结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含状态和单个**CreateItem**请求的结果。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含状态和单个**GetItem**请求的结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含状态和单个**UpdateItem**请求的结果。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含状态和单个**MoveItem**请求的结果。  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含状态和单个**CopyItem**请求的结果。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含状态和单个**CreateAttachment**请求的结果。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含状态和单个**GetAttachment**请求的结果。  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含状态和单个**FindItem**请求的结果。  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含状态和**ResolveNames**请求的结果。  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含状态和单个**ExpandDL**请求的结果。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含状态和单个**Subscribe**请求的结果。  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含状态和单个**GetEvents**请求的结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含状态和单个**SendNotification**请求的结果。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含状态和**SyncFolderHierarchy**请求的结果。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含状态和**SyncFolderItems**请求的结果。  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含状态和**ConvertId**请求的结果。  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |包含状态和**AddDelegate**请求的结果。  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |包含状态和**GetServerTimeZones**请求的结果。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含状态和**GetSharingFolder**请求的结果。  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |定义**GetSharingFolder**请求的响应。  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |包含状态和**GetSharingMetadata**请求的结果。  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |定义**GetSharingMetadata**请求的响应。  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |包含状态和**RefreshSharingFolder**请求的结果。  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |定义**RefreshSharingFolder**请求的响应。  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |包含状态和**FindConversation**响应的结果。  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |包含状态和单个**EmptyFolder**请求的结果。  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |包含状态和**UpdateInboxRules**请求的结果。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含状态和**UploadItemsResponse**请求的结果。  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |包含**GetInboxRules**请求的响应。  <br/> |
|GetServiceConfigurationResponse  <br/> |包含**GetServiceConfiguration**请求的响应。  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要的文本值。 此元素是只读的。
  
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

- [Exchange 的 EWS 引用](ews-reference-for-exchange.md) 
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
