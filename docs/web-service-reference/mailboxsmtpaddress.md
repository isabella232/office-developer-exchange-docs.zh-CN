---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: MailboxSmtpAddress 元素表示要检索或更新其收件箱规则的用户的 SMTP 地址;或要检索其密码到期日期。
ms.openlocfilehash: 86a39c416b9674e1f48f0a75508c003ad9d620f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511129"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

**MailboxSmtpAddress** 元素表示要检索或更新其收件箱规则的用户的 SMTP 地址;或要检索其密码到期日期。 
  
```XML
<MailboxSmtpAddress/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetInboxRules](getinboxrules.md) <br/> |定义一个请求，请求获取服务器存储中邮箱的收件箱规则。  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |定义获取电子邮件帐户的密码到期日期的请求。  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |定义更新服务器存储中邮箱中的收件箱规则的请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

**MailboxSmtpAddress** 元素是可选元素。 如果 **省略 MailboxSmtpAddress** 元素，则使用已登录用户的地址。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetInboxRules 操作](getinboxrules-operation.md)
- [GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)
- [UpdateInboxRules 操作](updateinboxrules-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

