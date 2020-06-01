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
ms.openlocfilehash: 4184092cf98161e4c2f74446cef5439722ae71a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457891"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate 操作

**GetPasswordExpirationDate**操作提供当前用户的电子邮件帐户密码到期日期。 
  
此操作是在 Exchange Server 2010 Service Pack 1 （SP1）中引入的。
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>GetPasswordExpirationDate 操作 SOAP 标头

**GetPasswordExpirationDate**操作可以使用下表中列出的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。 这适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构。 这适用于请求。 这适用于请求。  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate 操作请求示例

### <a name="description"></a>说明

以下示例的**GetPasswordExpirationDate**操作请求显示如何获取电子邮件帐户的密码到期日期。 
  
### <a name="code"></a>代码

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>成功的 GetPasswordExpirationDate 操作响应

响应中使用以下元素：
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

