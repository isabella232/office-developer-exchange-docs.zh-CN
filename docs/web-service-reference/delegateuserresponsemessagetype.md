---
title: DelegateUserResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DelegateUserResponseMessageType
api_type:
- schema
ms.assetid: 3dc9552c-1e2d-40ac-a137-827883c2bb88
description: DelegateUserResponseMessageType 元素包含单个委派用户的响应消息。
ms.openlocfilehash: 7318c80d72022384ca4f0352ec85f68aeede8e22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545466"
---
# <a name="delegateuserresponsemessagetype"></a>DelegateUserResponseMessageType

**DelegateUserResponseMessageType** 元素包含单个委派用户的响应消息。 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

**DelegateUserResponseMessageType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供一个错误代码，用于标识请求遇到的特定错误。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用且保留以供将来使用。 它包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[DelegateUser](delegateuser.md) <br/> |标识在委派管理响应中返回的单个代理。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages (ArrayOfDelegateUserResponseMessageType)](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |包含 Web 服务委派Exchange请求的响应消息。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于在安装了客户端访问服务器角色Exchange Server运行的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [AddDelegate 操作](adddelegate-operation.md)  
- [GetDelegate 操作](getdelegate-operation.md) 
- [UpdateDelegate 操作](updatedelegate-operation.md)  
- [RemoveDelegate 操作](removedelegate-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

