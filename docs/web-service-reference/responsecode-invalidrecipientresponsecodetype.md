---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: ResponseCode 元素提供了有关收件人无效的原因的信息。
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

**ResponseCode**元素提供了有关收件人无效的原因的信息。 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |包含无效的收件人和收件人无效的原因有关的信息的 SMTP 地址。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**ResponseCode**元素的可能值。 
  
|**代码**|**说明**|
|:-----|:-----|
|OtherError  <br/> |指示错误不由其他错误响应代码指定。  <br/> |
|RecipientOrganizationNotFederated  <br/> |指示，共享关系都无法与组织中收件人的 SMTP 电子邮件地址指定。  <br/> |
|CannotObtainTokenFromSTS  <br/> |指示出现从令牌服务器获取安全令牌问题。  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |指示系统管理员已将阻止与指定的收件人共享系统策略设置。  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |指示由指定的收件人的安全令牌服务未知。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

