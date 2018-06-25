---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: GetServiceConfiguration 元素定义 GetServiceConfiguration 请求。
ms.openlocfilehash: 7ff7124ff062f21a02fc69b86b7cc7367ba3fcb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825666"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

**GetServiceConfiguration**元素定义 GetServiceConfiguration 请求。 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 **GetServiceConfigurationType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |标识用户呼叫者发送为。 此元素是可选的。 如果此元素不存在，则假定为经过身份验证的用户为发件人。 **ActingAs**元素必须包含针对请求发件人提示。 如果**ActingAs**元素缺少，不包括路由类型，不包括电子邮件地址、 包含无效的电子邮件地址，不能解决 Active Directory 域中的用户，可以在响应中返回 ErrorInvalidArgument 错误服务 (AD DS)，或将解析为 AD DS 中的多个用户。  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |包含请求的服务配置。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

