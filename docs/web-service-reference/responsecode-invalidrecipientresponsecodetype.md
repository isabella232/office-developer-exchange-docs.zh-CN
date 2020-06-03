---
title: ResponseCode （InvalidRecipientResponseCodeType）
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
description: ResponseCode 元素提供有关收件人无效的原因的信息。
ms.openlocfilehash: d78de64de7725007ec51a55dad13d1cc892a25e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529719"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode （InvalidRecipientResponseCodeType）

**ResponseCode**元素提供有关收件人无效的原因的信息。 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

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
|OtherError  <br/> |指示错误不是由另一个错误响应代码指定的。  <br/> |
|RecipientOrganizationNotFederated  <br/> |表示共享关系对收件人的 SMTP 电子邮件地址中指定的组织不可用。  <br/> |
|CannotObtainTokenFromSTS  <br/> |指示从令牌服务器获取安全令牌时出现问题。  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |指示系统管理员已设置阻止与指定收件人共享的系统策略。  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |指示指定的收件人所使用的安全令牌服务是未知的。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

