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
# <a name="identify-the-account-to-impersonate"></a><span data-ttu-id="40efc-103">确定要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="40efc-103">Identify the account to impersonate</span></span>

<span data-ttu-id="40efc-104">了解您的服务应用程序如何使用 EWS 来标识要模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="40efc-104">Learn how your service application uses EWS to identify the user to impersonate.</span></span>
  
<span data-ttu-id="40efc-105">您的服务应用程序通过使用以下三个标识符之一来标识要模拟的用户帐户：</span><span class="sxs-lookup"><span data-stu-id="40efc-105">Your service application identifies the user account to impersonate by using one of the following three identifiers:</span></span>
  
- <span data-ttu-id="40efc-106">主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="40efc-106">The primary SMTP address.</span></span>
    
- <span data-ttu-id="40efc-107">用户主体名称（UPN）。</span><span class="sxs-lookup"><span data-stu-id="40efc-107">The user principal name (UPN).</span></span>
    
- <span data-ttu-id="40efc-108">安全标识符（SID）。</span><span class="sxs-lookup"><span data-stu-id="40efc-108">The security identifier (SID).</span></span>
    
<span data-ttu-id="40efc-109">您使用的标识符取决于您的应用程序提供的信息。</span><span class="sxs-lookup"><span data-stu-id="40efc-109">The identifier that you use depends, of course, on the information that your application has available.</span></span>
  
## <a name="identifying-the-user-account-to-impersonate"></a><span data-ttu-id="40efc-110">标识要模拟的用户帐户</span><span class="sxs-lookup"><span data-stu-id="40efc-110">Identifying the user account to impersonate</span></span>

<span data-ttu-id="40efc-111">您的应用程序可以使用 EWS 托管 API 或 EWS SOAP 请求来标识正在模拟的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="40efc-111">Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating.</span></span> <span data-ttu-id="40efc-112">EWS 托管 API 使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性来标识模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="40efc-112">The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user.</span></span> <span data-ttu-id="40efc-113">EWS 使用[ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)元素，如以下 XML 片段所示。</span><span class="sxs-lookup"><span data-stu-id="40efc-113">EWS uses the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment.</span></span> 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

<span data-ttu-id="40efc-114">以下各节显示了如何使用其中一个标识符。</span><span class="sxs-lookup"><span data-stu-id="40efc-114">Each of the following sections shows how to use one of the identifiers.</span></span> <span data-ttu-id="40efc-115">有关在操作中显示模拟标识符的示例，请参阅[使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)。</span><span class="sxs-lookup"><span data-stu-id="40efc-115">For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).</span></span>
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a><span data-ttu-id="40efc-116">使用 SMTP 电子邮件地址标识用户帐户</span><span class="sxs-lookup"><span data-stu-id="40efc-116">Use the SMTP email address to identify the user account</span></span>

<span data-ttu-id="40efc-117">SMTP 电子邮件地址是与用户帐户相关联的主电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="40efc-117">The SMTP email address is the primary email address that is associated with a user account.</span></span>
  
<span data-ttu-id="40efc-118">在 EWS 托管 API 应用程序中，您可以指定 SMTP 电子邮件地址和[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="40efc-118">In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

<span data-ttu-id="40efc-119">在 EWS SOAP 请求中， [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)元素包含用户帐户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="40efc-119">In an EWS SOAP request, the [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a><span data-ttu-id="40efc-120">使用 UPN 标识用户帐户</span><span class="sxs-lookup"><span data-stu-id="40efc-120">Use the UPN to identify the user account</span></span>

<span data-ttu-id="40efc-121">UPN 包含用户帐户位置的完全限定的域名（FQDN）。</span><span class="sxs-lookup"><span data-stu-id="40efc-121">The UPN contains the fully qualified domain name (FQDN) for the location of the user account.</span></span> <span data-ttu-id="40efc-122">这不一定是用户的邮箱域。</span><span class="sxs-lookup"><span data-stu-id="40efc-122">This is not necessarily the user's mailbox domain.</span></span> <span data-ttu-id="40efc-123">必须在 Active Directory 域服务（AD DS）中的用户帐户上正确设置**UserPrincipalName**属性，才能成功实现用户查找。</span><span class="sxs-lookup"><span data-stu-id="40efc-123">The **UserPrincipalName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed.</span></span> 
  
<span data-ttu-id="40efc-124">在 EWS 托管 API 应用程序中，您可以指定 UPN 以及[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="40efc-124">In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

<span data-ttu-id="40efc-125">在 EWS SOAP 请求中， [PrincipalName 元素（ConnectingSIDType 复杂类型）（EWS）](../web-service-reference/principalname.md)元素包含用户帐户的 UPN。</span><span class="sxs-lookup"><span data-stu-id="40efc-125">In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) element contains the UPN for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a><span data-ttu-id="40efc-126">使用 SID 标识用户帐户</span><span class="sxs-lookup"><span data-stu-id="40efc-126">Use the SID to identify the user account</span></span>

<span data-ttu-id="40efc-127">SID 是要以安全描述符定义语言（SDDL）形式模拟的帐户的标识符。</span><span class="sxs-lookup"><span data-stu-id="40efc-127">The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.</span></span>
  
<span data-ttu-id="40efc-128">在 EWS 托管 API 应用程序中，您可以指定 SID 以及[ConnectingIdType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="40efc-128">In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

<span data-ttu-id="40efc-129">在 EWS SOAP 请求中， [sid](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)元素包含用户帐户的 sid。</span><span class="sxs-lookup"><span data-stu-id="40efc-129">In an EWS SOAP request, the [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a><span data-ttu-id="40efc-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40efc-130">See also</span></span>


- [<span data-ttu-id="40efc-131">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="40efc-131">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="40efc-132">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="40efc-132">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [<span data-ttu-id="40efc-133">ExchangeService 类</span><span class="sxs-lookup"><span data-stu-id="40efc-133">ExchangeService class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [<span data-ttu-id="40efc-134">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="40efc-134">ExchangeImpersonation</span></span>](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

