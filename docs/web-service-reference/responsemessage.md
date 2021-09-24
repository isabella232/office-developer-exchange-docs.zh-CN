---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: ResponseMessage 元素提供有关请求中单个实体的响应状态的描述性信息。
ms.openlocfilehash: 21db84698b693fc97c67285c8ca89da028b4e59b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516369"
---
# <a name="responsemessage"></a>ResponseMessage

**ResponseMessage** 元素提供有关请求中单个实体的响应状态的描述性信息。 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 表示响应的状态。 <br/><br/>以下值对此属性有效：  <br/><br/>- 成功  <br/>- 警告  <br/>- 错误  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|成功  <br/> |描述已实现的请求。  <br/> |
|警告  <br/> | 描述未处理的请求。 如果在请求中的项目正在处理并且后续项目无法处理时发生错误，则可能会返回警告。 <br/><br/>以下是警告的一些可能原因：  <br/><br/>- Exchange存储在批处理期间处于脱机状态。  <br/>- Active Directory 目录服务脱机。  <br/>- 移动邮箱。  <br/>- 邮件数据库 (MDB) 处于脱机状态。  <br/>- 密码已过期。  <br/>- 超出配额。  <br/> |
|错误  <br/> | 描述无法实现的请求。 <br/><br/>以下是导致出错的一些可能原因：  <br/><br/>- 无效的属性或元素  <br/>- 属性或元素范围外  <br/>- 未知标记  <br/>- 上下文中无效属性或元素  <br/>- 任何客户端的未授权访问尝试  <br/>- 响应有效的客户端调用的服务器端故障  <br/> <br/> 有关错误的信息可在 [ResponseCode](responsecode.md) 和 [MessageText](messagetext.md) 元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供一个错误代码，用于标识请求遇到的特定错误。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用且保留以供将来使用。 它包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |包含单个邮箱用户的忙/闲信息。 <br/> <br/> 下面是此元素的 XPath 2.0 表达式： <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |包含请求的会议建议的响应信息和建议数据。  <br/><br/> 下面是此元素的 XPath 2.0 表达式：<br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含用户的响应结果和 OOF 设置。  <br/><br/> 下面是此元素的 XPath 2.0 表达式：  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[SetUserOofSettingsResponse](setuseroofsettingsresponse.md) <br/> |包含尝试的 [SetUserOofSettingsRequest 邮件](setuseroofsettingsrequest.md) 的结果。 <br/> <br/> 下面是此元素的 XPath 2.0 表达式：  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>注解

**ResponseMessageType** 类型通用于所有 Exchange Web 服务响应。 **ResponseMessageType** 类型由以下复杂类型扩展： 
  
- **ApplyConversationActionResponseMessageType**
    
- **AttachmentInfoResponseMessageType**
    
- **DeleteAttachmentResponseMessageType**
    
- **DeleteItemResponseMessageType**
    
- **ExpandDLResponseMessageType**
    
- **FindFolderResponseMessageType**
    
- **FindItemResponseMessageType**
    
- **FolderInfoResponseMessageType**
    
- **GetEventsResponseMessageType**
    
- **ItemInfoResponseMessageType**
    
- **ResolveNamesResponseMessageType**
    
- **SubscribeResponseMessageType**
    
- **SendNotificationResponseMessageType**
    
- **SyncFolderHierarchyResponseMessageType**
    
- **SyncFolderItemsResponseMessageType**
    
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
### <a name="version-differences"></a>版本差异

**ApplyConversationActionResponseMessage** 和 **DeleteItemResponseMessageType** 类型在 Exchange 内部版本 15.00.0986.00 中引入。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)
- [GetUserOofSettings 操作](getuseroofsettings-operation.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

