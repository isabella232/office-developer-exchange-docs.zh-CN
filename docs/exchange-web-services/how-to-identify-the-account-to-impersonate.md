---
title: 识别要模拟的帐户
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: 了解服务应用程序如何使用 EWS 来确定要模拟的用户。
ms.openlocfilehash: 01c6ee797359c38c8539257003a2f110fdf253cf
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354293"
---
# <a name="identify-the-account-to-impersonate"></a>识别要模拟的帐户

了解服务应用程序如何使用 EWS 来确定要模拟的用户。
  
服务应用程序标识的用户帐户模拟使用以下三个标识符之一：
  
- 主 SMTP 地址。
    
- 用户主体名称 (UPN)。
    
- 安全标识符 (SID)。
    
您使用的标识符取决于，当然，在信息应用程序具有可用。
  
## <a name="identifying-the-user-account-to-impersonate"></a>标识要模拟的用户帐户

您的应用程序可以使用 EWS 托管 API 或 EWS SOAP 请求来标识模拟的用户帐户。 EWS 托管 API 使用的[ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性标识模拟的用户。 EWS 使用[ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)元素，如以下 XML 片段中所示。 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

以下各节显示如何使用的一个标识符。 在操作中显示模拟标识符的示例，请参阅[添加使用 Exchange 模拟的约会](how-to-add-appointments-by-using-exchange-impersonation.md)。
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a>用于标识的用户帐户的 SMTP 电子邮件地址

SMTP 电子邮件地址是相关联的用户帐户的主电子邮件地址。
  
EWS 托管 API 应用程序，在您指定的 SMTP 电子邮件地址以及[ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

在 EWS SOAP 请求中， [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)元素包含用户帐户的电子邮件地址。 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a>使用 UPN 标识的用户帐户

UPN 包含的用户帐户的位置的完全限定的域名 (FQDN)。 这不一定是用户的邮箱域。 **UserPrincipleName**属性必须正确设置 Active Directory 域服务 (AD DS) 中的用户帐户的用户查找成功。 
  
EWS 托管 API 应用程序，在您指定的 UPN [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipleName, "alias@billing.contoso.com");
```

在 EWS SOAP 请求中， [PrincipalName 元素 （ConnectingSIDType 复杂类型） (EWS)](../web-service-reference/principalname.md)元素包含用户帐户的 UPN。 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a>使用 SID 标识的用户帐户

SID 是用于模拟安全描述符定义语言 (SDDL) 窗体中的帐户的标识符。
  
EWS 托管 API 应用程序，在您指定的 SID [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

在 EWS SOAP 请求中， [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)元素包含用户帐户的 SID。 
  
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
    
- [ExchangeService 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

