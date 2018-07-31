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
# <a name="identify-the-account-to-impersonate"></a><span data-ttu-id="887fd-103">识别要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="887fd-103">Identify the account to impersonate</span></span>

<span data-ttu-id="887fd-104">了解服务应用程序如何使用 EWS 来确定要模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="887fd-104">Learn how your service application uses EWS to identify the user to impersonate.</span></span>
  
<span data-ttu-id="887fd-105">服务应用程序标识的用户帐户模拟使用以下三个标识符之一：</span><span class="sxs-lookup"><span data-stu-id="887fd-105">Your service application identifies the user account to impersonate by using one of the following three identifiers:</span></span>
  
- <span data-ttu-id="887fd-106">主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="887fd-106">The primary SMTP address.</span></span>
    
- <span data-ttu-id="887fd-107">用户主体名称 (UPN)。</span><span class="sxs-lookup"><span data-stu-id="887fd-107">The user principle name (UPN).</span></span>
    
- <span data-ttu-id="887fd-108">安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="887fd-108">The security identifier (SID).</span></span>
    
<span data-ttu-id="887fd-109">您使用的标识符取决于，当然，在信息应用程序具有可用。</span><span class="sxs-lookup"><span data-stu-id="887fd-109">The identifier that you use depends, of course, on the information that your application has available.</span></span>
  
## <a name="identifying-the-user-account-to-impersonate"></a><span data-ttu-id="887fd-110">标识要模拟的用户帐户</span><span class="sxs-lookup"><span data-stu-id="887fd-110">Identifying the user account to impersonate</span></span>

<span data-ttu-id="887fd-111">您的应用程序可以使用 EWS 托管 API 或 EWS SOAP 请求来标识模拟的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="887fd-111">Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating.</span></span> <span data-ttu-id="887fd-112">EWS 托管 API 使用的[ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性标识模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="887fd-112">The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user.</span></span> <span data-ttu-id="887fd-113">EWS 使用[ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)元素，如以下 XML 片段中所示。</span><span class="sxs-lookup"><span data-stu-id="887fd-113">EWS uses the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment.</span></span> 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

<span data-ttu-id="887fd-114">以下各节显示如何使用的一个标识符。</span><span class="sxs-lookup"><span data-stu-id="887fd-114">Each of the following sections shows how to use one of the identifiers.</span></span> <span data-ttu-id="887fd-115">在操作中显示模拟标识符的示例，请参阅[添加使用 Exchange 模拟的约会](how-to-add-appointments-by-using-exchange-impersonation.md)。</span><span class="sxs-lookup"><span data-stu-id="887fd-115">For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).</span></span>
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a><span data-ttu-id="887fd-116">用于标识的用户帐户的 SMTP 电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="887fd-116">Use the SMTP email address to identify the user account</span></span>

<span data-ttu-id="887fd-117">SMTP 电子邮件地址是相关联的用户帐户的主电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="887fd-117">The SMTP email address is the primary email address that is associated with a user account.</span></span>
  
<span data-ttu-id="887fd-118">EWS 托管 API 应用程序，在您指定的 SMTP 电子邮件地址以及[ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="887fd-118">In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

<span data-ttu-id="887fd-119">在 EWS SOAP 请求中， [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)元素包含用户帐户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="887fd-119">In an EWS SOAP request, the [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a><span data-ttu-id="887fd-120">使用 UPN 标识的用户帐户</span><span class="sxs-lookup"><span data-stu-id="887fd-120">Use the UPN to identify the user account</span></span>

<span data-ttu-id="887fd-121">UPN 包含的用户帐户的位置的完全限定的域名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="887fd-121">The UPN contains the fully qualified domain name (FQDN) for the location of the user account.</span></span> <span data-ttu-id="887fd-122">这不一定是用户的邮箱域。</span><span class="sxs-lookup"><span data-stu-id="887fd-122">This is not necessarily the user's mailbox domain.</span></span> <span data-ttu-id="887fd-123">**UserPrincipleName**属性必须正确设置 Active Directory 域服务 (AD DS) 中的用户帐户的用户查找成功。</span><span class="sxs-lookup"><span data-stu-id="887fd-123">The **UserPrincipleName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed.</span></span> 
  
<span data-ttu-id="887fd-124">EWS 托管 API 应用程序，在您指定的 UPN [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="887fd-124">In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipleName, "alias@billing.contoso.com");
```

<span data-ttu-id="887fd-125">在 EWS SOAP 请求中， [PrincipalName 元素 （ConnectingSIDType 复杂类型） (EWS)](../web-service-reference/principalname.md)元素包含用户帐户的 UPN。</span><span class="sxs-lookup"><span data-stu-id="887fd-125">In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) element contains the UPN for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a><span data-ttu-id="887fd-126">使用 SID 标识的用户帐户</span><span class="sxs-lookup"><span data-stu-id="887fd-126">Use the SID to identify the user account</span></span>

<span data-ttu-id="887fd-127">SID 是用于模拟安全描述符定义语言 (SDDL) 窗体中的帐户的标识符。</span><span class="sxs-lookup"><span data-stu-id="887fd-127">The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.</span></span>
  
<span data-ttu-id="887fd-128">EWS 托管 API 应用程序，在您指定的 SID [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)枚举值。</span><span class="sxs-lookup"><span data-stu-id="887fd-128">In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

<span data-ttu-id="887fd-129">在 EWS SOAP 请求中， [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)元素包含用户帐户的 SID。</span><span class="sxs-lookup"><span data-stu-id="887fd-129">In an EWS SOAP request, the [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a><span data-ttu-id="887fd-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="887fd-130">See also</span></span>


- [<span data-ttu-id="887fd-131">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="887fd-131">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="887fd-132">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="887fd-132">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [<span data-ttu-id="887fd-133">ExchangeService 类</span><span class="sxs-lookup"><span data-stu-id="887fd-133">ExchangeService class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [<span data-ttu-id="887fd-134">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="887fd-134">ExchangeImpersonation</span></span>](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

