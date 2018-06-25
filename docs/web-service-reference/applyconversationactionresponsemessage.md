---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: ApplyConversationActionResponseMessage 元素包含状态和 ApplyConversationAction 操作请求的结果。
ms.openlocfilehash: d8c5571cfc9c2ea6aaf09cb26a0e47e4abfc3f40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753240"
---
# <a name="applyconversationactionresponsemessage"></a>ApplyConversationActionResponseMessage

**ApplyConversationActionResponseMessage**元素包含状态和[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的结果。  
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 介绍响应的状态。<br/><br/>下面是此属性有效值：<ul><li>成功</li><li>警告</li><li>错误</li></ul> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|**成功** <br/> |介绍的已完成的请求。  <br/> |
|**Warning** <br/> | 介绍了未处理的请求。 如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。<br/><br/>以下是源的警告的示例：<ul><li>在 Exchange 存储过程批次中处于脱机状态。</li><li>Active Directory 域服务 (AD DS) 处于脱机状态。</li><li>邮箱移动。</li><li>邮件数据库 (MDB) 处于脱机状态。</li><li>密码已过期。</li><li>已超出配额。</li></ul> |
|**Error** <br/> | 描述无法满足请求。<br/><br/>错误的来源的示例如下：  <ul><li>无效的属性或元素</li><li>超出范围元素或属性</li><li>未知的标记  </li><li>属性或上下文中无效的元素</li><li>由任何客户端的未经授权的访问尝试</li><li>服务器端失败响应有效的客户端调用</li></ul>[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供的响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供标识的特定错误的请求时遇到的错误代码。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。 此元素包含一个值为 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含为 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
### <a name="version-differences"></a>版本差异

在版本的 Exchange 开头生成 15.00.0986.00， **ApplyConversationActionResponseMessage**元素是类型**ApplyConversationActionResponseMessageType**。 在早期版本，该元素是类型**ResponseMessageType**。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ApplyConversationAction 操作](applyconversationaction-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

