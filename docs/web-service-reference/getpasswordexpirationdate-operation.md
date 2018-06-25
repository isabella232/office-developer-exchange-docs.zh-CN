---
title: GetPasswordExpirationDate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: GetPasswordExpirationDate 操作提供当前用户的电子邮件帐户密码到期日期。
ms.openlocfilehash: c57942c88b09a910e2d529a12ea279bb2da5d693
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754642"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate 操作

**GetPasswordExpirationDate**操作提供当前用户的电子邮件帐户密码到期日期。 
  
此操作是在 Exchange Server 2010 Service Pack 1 (SP1) 中引入的。
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>GetPasswordExpirationDate 操作 SOAP 标头

**GetPasswordExpirationDate**操作可以使用下表中列出的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。 这是适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构。 这是适用于请求。 这是适用于请求。  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate 操作请求示例

### <a name="description"></a>说明

**GetPasswordExpirationDate**操作请求的下面的示例演示如何获取的电子邮件帐户的密码到期日期。 
  
### <a name="code"></a>代码

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>成功 GetPasswordExpirationDate 操作响应

在响应中使用以下元素：
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

