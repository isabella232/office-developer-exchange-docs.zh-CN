---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: MailboxSmtpAddress 元素均表示要检索或更新; 其收件箱规则的用户的 SMTP 地址或者是要检索其密码到期日期。
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826303"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

**MailboxSmtpAddress**元素均表示要检索或更新; 其收件箱规则的用户的 SMTP 地址或者是要检索其密码到期日期。 
  
```XML
<MailboxSmtpAddress/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetInboxRules](getinboxrules.md) <br/> |定义一个请求以获取对邮箱服务器存储区中的收件箱规则。  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |定义一个请求以获取的电子邮件帐户的密码到期日期。  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |定义更新中的邮箱服务器存储区中的收件箱规则的请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

**MailboxSmtpAddress**元素是一个可选的元素。 如果省略**MailboxSmtpAddress**元素，则使用登录用户的地址。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetInboxRules 操作](getinboxrules-operation.md)
- [GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)
- [UpdateInboxRules 操作](updateinboxrules-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

