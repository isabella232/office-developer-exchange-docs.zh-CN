---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: ResolveNamesResponseMessage 元素包含 ResolveNames 操作请求的状态和结果。
ms.openlocfilehash: 12f32008dbbc603fca7adf26057f1f1904d3cfb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455595"
---
# <a name="resolvenamesresponsemessage"></a>ResolveNamesResponseMessage

**ResolveNamesResponseMessage**元素包含[ResolveNames 操作](resolvenames-operation.md)请求的状态和结果。 
  
- [ResolveNamesResponse](resolvenamesresponse.md) 
- [ResponseMessages](responsemessages.md)
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 **ResolveNamesResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述[ResolveNames 操作](resolvenames-operation.md)响应的状态。 <br/><br/>以下值对此属性有效：  <br/><br/>-成功  <br/>-警告  <br/>-错误  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass 属性

|**值**|**说明**|
|:-----|:-----|
|**Success** <br/> |描述已完成的请求。 当请求的名称明确且响应包含单个收件人时，会出现这种情况。  <br/> |
|**警告** <br/> | 介绍未处理的请求。 如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。 <br/><br/>以下是警告源的示例：  <br/><br/>-Exchange 存储在批处理过程中脱机。  <br/>-Active Directory 域服务（AD DS）脱机。  <br/>-移动邮箱。  <br/>-邮箱数据库（MDB）脱机。  <br/>-密码已过期。  <br/>-超出配额。  <br/>-请求的名称不明确，响应中包含多个收件人。  <br/> |
|**Error** <br/> | 介绍无法满足的请求。 <br/><br/>以下是错误源的示例：  <br/><br/>-无法解析请求的名称。  <br/>-属性或元素无效。  <br/>-属性或元素超出范围。  <br/>-标记未知。  <br/>-上下文中的属性或元素无效。  <br/>-发生任何客户端的未经授权的访问尝试。  <br/>-响应有效的客户端调用时发生服务器端故障。  <br/>  <br/>有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的错误消息。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，并保留以供将来使用。 它包含值0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[ResolutionSet](resolutionset.md) <br/> |包含一个不明确名称的分辨率数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ResolveNames](resolvenames.md)
- [ResolveNamesResponse](resolvenamesresponse.md)
- [ResolveNames 操作](resolvenames-operation.md)

