---
title: 确定要模拟的帐户
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: 了解您的服务应用程序如何使用 EWS 来标识要模拟的用户。
localization_priority: Priority
ms.openlocfilehash: 7159707abe96632aba2ed70dc0057417e087349f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527990"
---
# <a name="identify-the-account-to-impersonate"></a>确定要模拟的帐户

了解您的服务应用程序如何使用 EWS 来标识要模拟的用户。
  
您的服务应用程序通过使用以下三个标识符之一来标识要模拟的用户帐户：
  
- 主 SMTP 地址。
    
- 用户主体名称（UPN）。
    
- 安全标识符（SID）。
    
您使用的标识符取决于您的应用程序提供的信息。
  
## <a name="identifying-the-user-account-to-impersonate"></a>标识要模拟的用户帐户

您的应用程序可以使用 EWS 托管 API 或 EWS SOAP 请求来标识正在模拟的用户帐户。 EWS 托管 API 使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性来标识模拟的用户。 EWS 使用[ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)元素，如以下 XML 片段所示。 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

以下各节显示了如何使用其中一个标识符。 有关在操作中显示模拟标识符的示例，请参阅[使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)。
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a>使用 SMTP 电子邮件地址标识用户帐户

SMTP 电子邮件地址是与用户帐户相关联的主电子邮件地址。
  
在 EWS 托管 API 应用程序中，您可以指定 SMTP 电子邮件地址和[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

在 EWS SOAP 请求中， [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)元素包含用户帐户的电子邮件地址。 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a>使用 UPN 标识用户帐户

UPN 包含用户帐户位置的完全限定的域名（FQDN）。 这不一定是用户的邮箱域。 必须在 Active Directory 域服务（AD DS）中的用户帐户上正确设置**UserPrincipalName**属性，才能成功实现用户查找。 
  
在 EWS 托管 API 应用程序中，您可以指定 UPN 以及[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

在 EWS SOAP 请求中， [PrincipalName 元素（ConnectingSIDType 复杂类型）（EWS）](../web-service-reference/principalname.md)元素包含用户帐户的 UPN。 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a>使用 SID 标识用户帐户

SID 是要以安全描述符定义语言（SDDL）形式模拟的帐户的标识符。
  
在 EWS 托管 API 应用程序中，您可以指定 SID 以及[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

在 EWS SOAP 请求中， [sid](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)元素包含用户帐户的 sid。 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a>另请参阅


- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [ExchangeService 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

