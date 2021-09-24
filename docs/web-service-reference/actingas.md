---
title: ActingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: ActingAs 元素标识呼叫者发送者的身份。
ms.openlocfilehash: a470a7571e5f1b2ecc85014157d3fc4de291389e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540339"
---
# <a name="actingas"></a>ActingAs

**ActingAs** 元素标识呼叫者发送者的身份。 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |定义用于邮箱路由。默认值为 SMTP。此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetServiceConfiguration](getserviceconfiguration.md) <br/> |定义 **GetServiceConfiguration** 请求。  <br/> |
   
## <a name="remarks"></a>说明

此元素为可选。 如果此元素不存在，则假定经过身份验证的用户是发件人。 **必须包含 ActingAs** 元素以请求发送方提示。 如果 **ActingAs** 元素缺失、不包含路由类型、不包含电子邮件地址、包含无效的电子邮件地址、未解析为 Active Directory 域服务 (AD DS) 中的用户或解析为 AD DS 中的多个用户，则响应中可能会返回 **ErrorInvalidArgument** 错误。 
  
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

