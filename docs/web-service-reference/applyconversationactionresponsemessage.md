---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: ApplyConversationActionResponseMessage 元素包含 ApplyConversationAction 操作请求的状态和结果。
ms.openlocfilehash: 81378c822a473d969035f46f34ffca8939d7059d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522045"
---
# <a name="applyconversationactionresponsemessage"></a>ApplyConversationActionResponseMessage

**ApplyConversationActionResponseMessage 元素** 包含 [ApplyConversationAction](applyconversationaction-operation.md)操作请求的状态和结果。  
  
- [ApplyConversationActionResponse](applyconversationactionresponse.md)
- [ResponseMessages](responsemessages.md)
- [ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 **ApplyConversationActionResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述响应的状态。<br/><br/>以下值对此属性有效：<ul><li>成功</li><li>警告</li><li>错误</li></ul> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|**Success** <br/> |描述已实现的请求。  <br/> |
|**警告** <br/> | 描述未处理的请求。 如果在请求中的项目正在处理并且后续项目无法处理时发生错误，则可能会返回警告。<br/><br/>以下是警告来源的示例：<ul><li>该Exchange存储在批处理期间处于脱机状态。</li><li>Active Directory 域服务 (AD DS) 处于脱机状态。</li><li>邮箱已移动。</li><li>邮件数据库 (MDB) 处于脱机状态。</li><li>密码已过期。</li><li>已超出配额。</li></ul> |
|**错误** <br/> | 描述无法实现的请求。<br/><br/>以下是错误源的示例：  <ul><li>无效的属性或元素</li><li>范围外的属性或元素</li><li>未知标记  </li><li>在上下文中无效属性或元素</li><li>任何客户端的未授权访问尝试</li><li>响应有效客户端调用的服务器端故障</li></ul>有关错误的信息可在 [ResponseCode](responsecode.md) 和 [MessageText](messagetext.md) 元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供一个错误代码，用于标识请求遇到的特定错误。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。 此元素包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Web 服务请求Exchange消息。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
### <a name="version-differences"></a>版本差异

在从内部版本 15.00.0986.00 开始的版本 Exchange 中 **，ApplyConversationActionResponseMessage** 元素的类型为 **ApplyConversationActionResponseMessageType**。 在以前的版本中，元素的类型为 **ResponseMessageType**。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ApplyConversationAction 操作](applyconversationaction-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

