---
title: GetPasswordExpirationDate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: GetPasswordExpirationDate 操作为当前用户提供电子邮件帐户密码到期日期。
ms.openlocfilehash: 07928fd3e6fca410a292d6cd74f1240d8e81c42f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524236"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate 操作

**GetPasswordExpirationDate** 操作为当前用户提供电子邮件帐户密码到期日期。 
  
此操作是在 sp1 Exchange Server 2010 Service Pack 1 (中) 。
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>GetPasswordExpirationDate 操作 SOAP 标头

**GetPasswordExpirationDate** 操作可以使用下表中列出的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的区域性，如 RFC 3066"语言标识标记"中的定义。 这适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构。 这适用于请求。 这适用于请求。  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate 操作请求示例

### <a name="description"></a>Description

**GetPasswordExpirationDate** 操作请求的以下示例显示如何获取电子邮件帐户的密码到期日期。 
  
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

### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>成功的 GetPasswordExpirationDate 操作响应

响应中会使用下列元素：
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

