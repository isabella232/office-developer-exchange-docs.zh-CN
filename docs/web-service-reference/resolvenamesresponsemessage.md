---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: ResolveNamesResponseMessage 元素包含 ResolveNames 操作请求的状态和结果。
ms.openlocfilehash: a7debc5f5056ad7a33ebfaf2b0d5d914acdb2397
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523473"
---
# <a name="resolvenamesresponsemessage"></a>ResolveNamesResponseMessage

**ResolveNamesResponseMessage 元素** 包含 [ResolveNames](resolvenames-operation.md)操作请求的状态和结果。 
  
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
|**ResponseClass** <br/> | 描述 [ResolveNames 操作响应](resolvenames-operation.md) 的状态。 <br/><br/>以下值对此属性有效：  <br/><br/>- 成功  <br/>- 警告  <br/>- 错误  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass 属性

|**值**|**说明**|
|:-----|:-----|
|**Success** <br/> |描述已实现的请求。 当请求的名称是明确的且响应包含单个收件人时，将发生这种情况。  <br/> |
|**警告** <br/> | 描述未处理的请求。 如果在请求中的项目正在处理并且后续项目无法处理时发生错误，则可能会返回警告。 <br/><br/>以下是警告来源的示例：  <br/><br/>- Exchange在批处理期间脱机。  <br/>- Active Directory 域服务 (AD DS) 脱机。  <br/>- 移动邮箱。  <br/>- MDB (邮箱) 脱机。  <br/>- 密码已过期。  <br/>- 超出配额。  <br/>- 请求的名称不明确，响应包含多个收件人。  <br/> |
|**错误** <br/> | 描述无法实现的请求。 <br/><br/>以下是错误源的示例：  <br/><br/>- 无法解析请求的名称。  <br/>- 属性或元素无效。  <br/>- 属性或元素在范围内。  <br/>- 标记未知。  <br/>- 属性或元素无效上下文中定义。  <br/>- 发生任何客户端的未经授权访问尝试。  <br/>- 响应有效的客户端调用时发生服务器端故障。  <br/>  <br/>有关错误的信息可在 [ResponseCode](responsecode.md) 和 [MessageText](messagetext.md) 元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的错误信息。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用且保留以供将来使用。 它包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[ResolutionSet](resolutionset.md) <br/> |包含一组用于不明确名称的解决方法。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Web 服务请求Exchange消息。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
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

