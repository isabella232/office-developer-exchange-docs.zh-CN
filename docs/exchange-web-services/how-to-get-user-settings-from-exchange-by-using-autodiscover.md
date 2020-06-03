---
title: 使用自动发现从 Exchange 获取用户设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6d90c305-4802-4e18-8d52-f60349feaa8d
description: 了解如何使用自动发现从 Exchange 服务器获取用户配置设置。
localization_priority: Priority
ms.openlocfilehash: 5f7ea04e6b04f674d4cb481cf9243d46437d6950
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527997"
---
# <a name="get-user-settings-from-exchange-by-using-autodiscover"></a><span data-ttu-id="73720-103">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="73720-103">Get user settings from Exchange by using Autodiscover</span></span>

<span data-ttu-id="73720-104">了解如何使用自动发现从 Exchange 服务器获取用户配置设置。</span><span class="sxs-lookup"><span data-stu-id="73720-104">Learn how to get user configuration settings from an Exchange server by using Autodiscover.</span></span>
  
<span data-ttu-id="73720-105">自动发现通过仅使用用户的电子邮件地址和密码轻松访问用户配置信息，从而简化了应用程序配置。</span><span class="sxs-lookup"><span data-stu-id="73720-105">Autodiscover simplifies application configuration by providing easy access to user configuration information using only the user's email address and password.</span></span> <span data-ttu-id="73720-106">可通过自动发现（如用户的显示名称或外部 web 服务 URL）使用[许多用户配置设置](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="73720-106">A [number of user configuration settings](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) are available via Autodiscover, such as the user's display name or external web service URL.</span></span> 
  
<span data-ttu-id="73720-107">您可以使用以下一种开发技术从自动发现服务中检索用户设置：</span><span class="sxs-lookup"><span data-stu-id="73720-107">You can use one of the following development technologies to retrieve user settings from the Autodiscover service:</span></span>
  
- <span data-ttu-id="73720-108">[启动 EWS 托管 API 客户端应用程序的入门](get-started-with-ews-managed-api-client-applications.md)</span><span class="sxs-lookup"><span data-stu-id="73720-108">The [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md)</span></span>
    
- <span data-ttu-id="73720-109">[SOAP 自动发现 web 服务](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73720-109">The [SOAP Autodiscover web service](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)</span></span>
    
- <span data-ttu-id="73720-110">[POX 自动发现 web 服务](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73720-110">The [POX Autodiscover web service](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)</span></span>
    
<span data-ttu-id="73720-111">EWS 托管 API 提供了用于检索用户设置的基于对象的接口。</span><span class="sxs-lookup"><span data-stu-id="73720-111">The EWS Managed API provides an object-based interface for retrieving user settings.</span></span> <span data-ttu-id="73720-112">如果客户端应用程序使用托管代码，建议使用 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="73720-112">If your client application uses managed code, we recommend that you use the EWS Managed API.</span></span> <span data-ttu-id="73720-113">如果您使用 EWS 托管 API，请确定您所需的设置是否在[WebServices](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx)枚举中可用。</span><span class="sxs-lookup"><span data-stu-id="73720-113">If you are using the EWS Managed API, determine whether the settings that you need are available in the [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx) enumeration.</span></span> <span data-ttu-id="73720-114">如果不是，则可能需要使用 SOAP 或 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="73720-114">If they aren't, you might want to use the SOAP or POX Autodiscover services.</span></span> 
  
<span data-ttu-id="73720-115">如果使用的是 web 服务，我们建议使用 SOAP 自动发现服务，因为它支持的功能集比 POX 自动发现服务更丰富。</span><span class="sxs-lookup"><span data-stu-id="73720-115">If you are using a web service, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span> <span data-ttu-id="73720-116">如果 SOAP 自动发现服务不可用，则 POX 自动发现服务是一个很理想的替代方法。</span><span class="sxs-lookup"><span data-stu-id="73720-116">If the SOAP Autodiscover service isn't available, the POX Autodiscover service is a good alternative.</span></span>
  
## <a name="set-up-to-get-user-settings"></a><span data-ttu-id="73720-117">设置以获取用户设置</span><span class="sxs-lookup"><span data-stu-id="73720-117">Set up to get user settings</span></span>
<span data-ttu-id="73720-118"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="73720-118"><a name="bk_Prereq"> </a></span></span>

<span data-ttu-id="73720-119">在使用自动发现服务获取用户设置之前，请确保您有权访问以下内容：</span><span class="sxs-lookup"><span data-stu-id="73720-119">Before you get user settings by using the Autodiscover service, make sure that you have access to the following:</span></span>
  
- <span data-ttu-id="73720-120">如果使用 EWS 托管 API 或基于 POX 的自动发现服务，则 Exchange Online、Exchange Online 作为 Office 365 的一部分，或者运行 Exchange 2007 SP1 的 Exchange 版本的服务器。</span><span class="sxs-lookup"><span data-stu-id="73720-120">If you are using the EWS Managed API or the POX-based Autodiscover service, Exchange Online, Exchange Online as part of Office 365, or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> 
    
- <span data-ttu-id="73720-121">如果使用基于 SOAP 的自动发现服务，则 Exchange Online 或从 Exchange 2010 开始的 Exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="73720-121">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
> [!NOTE]
> <span data-ttu-id="73720-122">如果使用 EWS 托管 API，在某些情况下将需要[提供证书验证回调方法](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="73720-122">If you are using the EWS Managed API, you will need to [provide a certificate validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) in some circumstances.</span></span> <span data-ttu-id="73720-123">您可能还需要具有一些生成的代理库的证书验证回调方法，例如由 Visual Studio 创建的代理库。</span><span class="sxs-lookup"><span data-stu-id="73720-123">You might also need a certificate validation callback method with some generated proxy libraries, such as those created by Visual Studio.</span></span> 
  
## <a name="get-user-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="73720-124">使用 EWS 托管 API 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="73720-124">Get user settings by using the EWS Managed API</span></span>
<span data-ttu-id="73720-125"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="73720-125"><a name="bk_Managed"> </a></span></span>

<span data-ttu-id="73720-126">您可以使用[GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx)方法检索用户的配置信息，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="73720-126">You can use the [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) method to retrieve configuration information for a user, as shown in the following example.</span></span> <span data-ttu-id="73720-127">在此示例中，您可以指定要返回的用户设置的数组（从[UserSettingName](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx)枚举中提供的设置），并且该方法将遵循来自 Exchange 服务器的重定向响应。</span><span class="sxs-lookup"><span data-stu-id="73720-127">In this example, you can specify an array of user settings to return (from those available in the [UserSettingName](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) enumeration), and the method will follow redirection responses from the Exchange server.</span></span> 
  
```cs
using System;
using System.Net;
using Microsoft.Exchange.WebServices.Autodiscover;
public static GetUserSettingsResponse GetUserSettings(
    AutodiscoverService service,
    string emailAddress,
    int maxHops,
    params UserSettingName[] settings)
{
    Uri url = null;
    GetUserSettingsResponse response = null;
    for (int attempt = 0; attempt < maxHops; attempt++)
    {
        service.Url = url;
        service.EnableScpLookup = (attempt < 2);
        response = service.GetUserSettings(emailAddress, settings);
        if (response.ErrorCode == AutodiscoverErrorCode.RedirectAddress)
        {
            url = new Uri(response.RedirectTarget);
        }
        else if (response.ErrorCode == AutodiscoverErrorCode.RedirectUrl)
        {
            url = new Uri(response.RedirectTarget);
        }
        else
        {
            return response;
        }
    }
    throw new Exception("No suitable Autodiscover endpoint was found.");
}
```

<span data-ttu-id="73720-128">您可以分析返回的集合，以访问用户设置数组中的每个键/值对。</span><span class="sxs-lookup"><span data-stu-id="73720-128">You can parse the collection returned to access each key/value pair in the user settings array.</span></span> <span data-ttu-id="73720-129">下面的示例演示如何分析每个返回的元素并显示每个键/值对的名称和值。</span><span class="sxs-lookup"><span data-stu-id="73720-129">The following example shows how to parse through each returned element and display the name and value of each key/value pair.</span></span>
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
// userresponse is a GetUserSettingsResonse object.
foreach (KeyValuePair<UserSettingName, Object> usersetting in userresponse.Settings)
{
    Console.WriteLine(usersetting.Key.ToString() + ": " + usersetting.Value);
}
```

<span data-ttu-id="73720-130">或者，您可以获取特定设置的值。</span><span class="sxs-lookup"><span data-stu-id="73720-130">Alternatively, you can obtain the value of a specific setting.</span></span> <span data-ttu-id="73720-131">在下面的示例中，将显示**UserDisplayName**设置。</span><span class="sxs-lookup"><span data-stu-id="73720-131">In the following example, the **UserDisplayName** setting is to be displayed.</span></span> 
  
```cs
// Display a specific setting, such as UserDisplayName.
Console.WriteLine(userresponse.Settings[UserSettingName.UserDisplayName]);
```

## <a name="get-user-settings-by-using-soap-autodiscover"></a><span data-ttu-id="73720-132">使用 SOAP 自动发现获取用户设置</span><span class="sxs-lookup"><span data-stu-id="73720-132">Get user settings by using SOAP Autodiscover</span></span>
<span data-ttu-id="73720-133"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="73720-133"><a name="bk_SOAP"> </a></span></span>

<span data-ttu-id="73720-134">如果您不使用 EWS 托管 API，我们建议使用 SOAP 自动发现 web 服务。</span><span class="sxs-lookup"><span data-stu-id="73720-134">If you're not using the EWS Managed API, we recommend that you use the SOAP Autodiscover web service.</span></span> <span data-ttu-id="73720-135">仅当 SOAP 自动发现 web 服务失败或不可用时，才使用 POX 自动发现 web 服务。</span><span class="sxs-lookup"><span data-stu-id="73720-135">Only use the POX Autodiscover web service if the SOAP Autodiscover web service fails or is not available.</span></span> 
  
<span data-ttu-id="73720-136">若要获取用户设置，请使用[GetUserSettings 操作（SOAP）](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="73720-136">To get user settings, use the [GetUserSettings operation (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx).</span></span> <span data-ttu-id="73720-137">请求的设置将作为[UserSetting 元素](https://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx)返回。</span><span class="sxs-lookup"><span data-stu-id="73720-137">The requested settings are returned as [UserSetting elements](https://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="73720-138">下面的示例演示了从服务器获取用户设置的 SOAP 自动发现请求。</span><span class="sxs-lookup"><span data-stu-id="73720-138">The following example shows a SOAP Autodiscover request to get user settings from the server.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>mara@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>PublicFolderServer</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>ExternalMailboxServer</a:Setting>
          <a:Setting>EcpDeliveryReportUrlFragment</a:Setting>
          <a:Setting>EcpPublishingUrlFragment</a:Setting>
          <a:Setting>EcpTextMessagingUrlFragment</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
          <a:Setting>GroupingInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="73720-139">下面的示例演示了服务器在分析来自客户端的请求后返回的 SOAP 响应。</span><span class="sxs-lookup"><span data-stu-id="73720-139">The following example shows the SOAP response that is returned by the server after it parses the request from the client.</span></span> <span data-ttu-id="73720-140">响应仅包含所请求的设置（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="73720-140">The response contains only the settings that are requested, if they exist.</span></span>
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>Mara Whitley</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=mara</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>649d50b8-a1ce-4bac-8ace-2321   e463f701</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>15.01.0160.004</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007, Exchange2007_SP1, Exchange2010, Exchange2010_SP1, Exchange2010_SP2, Exchange2013</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>dc.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group 
                  (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=mail.contoso.com/cn=Contoso Private MDB</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>PublicFolderServer</Name>
                <Value>public.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpDeliveryReportUrlFragment</Name>
                <Value>PersonalSettings/DeliveryReport.aspx?exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpTextMessagingUrlFragment</Name>
                <Value>?p=sms/textmessaging.slab&amp;amp;exsvurl=1</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpPublishingUrlFragment</Name>
                <Value>customize/calendarpublishing.slab?exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://mail.contoso.com/EWS/Exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>GroupingInformation</Name>
                <Value>CONTOSO-1</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope
```

## <a name="get-user-settings-by-using-pox-autodiscover"></a><span data-ttu-id="73720-141">使用 POX 自动发现获取用户设置</span><span class="sxs-lookup"><span data-stu-id="73720-141">Get user settings by using POX Autodiscover</span></span>
<span data-ttu-id="73720-142"><a name="bk_POX"> </a></span><span class="sxs-lookup"><span data-stu-id="73720-142"><a name="bk_POX"> </a></span></span>

<span data-ttu-id="73720-143">[！注意] 尽管我们建议使用 SOAP 自动发现 web 服务，但在 SOAP 不可用时，POX 自动发现 web 服务是一个不错的备份选项。</span><span class="sxs-lookup"><span data-stu-id="73720-143">Although we recommend that you use the SOAP Autodiscover web service, the POX Autodiscover web service is a good backup option for those times when SOAP isn't available.</span></span> <span data-ttu-id="73720-144">例如，Exchange 2007 不支持 SOAP 自动发现 web 服务，因此，如果您针对的是 Exchange 2007，则必须使用 POX 自动发现 web 服务。</span><span class="sxs-lookup"><span data-stu-id="73720-144">For example, Exchange 2007 does not support the SOAP Autodiscover web service, so if you are targeting Exchange 2007, you have to use the POX Autodiscover web service.</span></span> <span data-ttu-id="73720-145">与 SOAP 自动发现 web 服务不同，POX 自动发现服务不允许您请求特定设置。</span><span class="sxs-lookup"><span data-stu-id="73720-145">Unlike the SOAP Autodiscover web service, the POX Autodiscover service does not allow you to request specific settings.</span></span> <span data-ttu-id="73720-146">相反，服务器会将可用设置的完整列表作为[Protocol 元素](https://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx)的子元素返回。</span><span class="sxs-lookup"><span data-stu-id="73720-146">Instead, the server returns a full list of available settings as child elements of the [Protocol element](https://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="73720-147">以下示例显示了从服务器获取用户设置的 POX 自动发现请求。</span><span class="sxs-lookup"><span data-stu-id="73720-147">The following example shows a POX Autodiscover request to get user settings from the server.</span></span> <span data-ttu-id="73720-148">以下 XML 通过 HTTP POST 发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="73720-148">The following XML is sent to the server via an HTTP POST.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>mara@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="73720-149">下面的示例展示了服务器返回的 POX 响应。</span><span class="sxs-lookup"><span data-stu-id="73720-149">The following example shows the POX response that is returned by the server.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>Mara Whitley</DisplayName>
      <LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=f5eeabead90d4b6fb51d6379474692cd-Mara</LegacyDN>
      <AutoDiscoverSMTPAddress>mara@contoso.com</AutoDiscoverSMTPAddress>
      <DeploymentId>50817eff-b925-4578-a0db-13bfc635e7a5</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <MicrosoftOnline>False</MicrosoftOnline>
      <Protocol>
        <Type>EXCH</Type>
        <Server>5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</Server>
        <ServerDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</ServerDN>
        <ServerVersion>73C08204</ServerVersion>
        <MdbDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com/cn=Microsoft Private MDB</MdbDN>
        <PublicFolderServer>public.contoso.com</PublicFolderServer>
        <AD>dc.contoso.com</AD>
        <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
        <EwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EwsUrl>
        <EmwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EmwsUrl>
        <EcpUrl>https://mail.contoso.com/ecp/</EcpUrl>
        <EcpUrl-um>?rfr=olk&amp;amp;p=customize/voicemail.aspx&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-um>
        <EcpUrl-aggr>?rfr=olk&amp;amp;p=personalsettings/EmailSubscriptions.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-aggr>
        <EcpUrl-mt>PersonalSettings/DeliveryReport.aspx?rfr=olk&amp;amp;exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-mt>
        <EcpUrl-ret>?rfr=olk&amp;amp;p=organize/retentionpolicytags.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-ret>
        <EcpUrl-sms>?rfr=olk&amp;amp;p=sms/textmessaging.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-sms>
        <EcpUrl-publish>customize/calendarpublishing.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-publish>
        <EcpUrl-photo>PersonalSettings/EditAccount.aspx?rfr=olk&amp;amp;chgPhoto=1&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-photo>
        <EcpUrl-tm>?rfr=olk&amp;amp;ftr=TeamMailbox&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tm>
        <EcpUrl-tmCreating>?rfr=olk&amp;amp;ftr=TeamMailboxCreating&amp;amp;SPUrl=&amp;lt;SPUrl&amp;gt;&amp;amp;Title=&amp;lt;Title&amp;gt;&amp;amp;SPTMAppUrl=&amp;lt;SPTMAppUrl&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmCreating>
        <EcpUrl-tmEditing>?rfr=olk&amp;amp;ftr=TeamMailboxEditing&amp;amp;Id=&amp;lt;Id&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmEditing>
        <EcpUrl-extinstall>Extension/InstalledExtensions.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-extinstall>
        <OOFUrl>https://mail.contoso.com/EWS/Exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/EWS/UM2007Legacy.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/c21c7bc2-53b3-4ddc-ad89-1219b486c37c/</OABUrl>
        <ServerExclusiveConnect>off</ServerExclusiveConnect>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>mail.contoso.com</Server>
        <SSL>Off</SSL>
        <AuthPackage>Ntlm</AuthPackage>
        <ServerExclusiveConnect>on</ServerExclusiveConnect>
        <CertPrincipalName>None</CertPrincipalName>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Basic, Fba">https://mail.contoso.com/owa/</OWAUrl>
          <Protocol>
            <Type>EXCH</Type>
            <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
          </Protocol>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="next-steps"></a><span data-ttu-id="73720-150">后续步骤</span><span class="sxs-lookup"><span data-stu-id="73720-150">Next steps</span></span>
<span data-ttu-id="73720-151"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="73720-151"><a name="bk_Next"> </a></span></span>

<span data-ttu-id="73720-152">从服务器检索到用户所需的配置详细信息后，即可与 Exchange 进行通信，以执行应用程序需要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="73720-152">After you've retrieved the necessary configuration details for your user from the server, you are ready to communicate with Exchange to do the things your application needs to do.</span></span> <span data-ttu-id="73720-153">下一步操作取决于与 Exchange 通信的方式和要实现的目标。</span><span class="sxs-lookup"><span data-stu-id="73720-153">What you do next depends on how you communicate with Exchange and what you want to accomplish.</span></span> <span data-ttu-id="73720-154">如果需要进行一些灵感，并且使用 EWS，则可能需要浏览[Exchange 101 代码示例](https://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)以了解一些想法。</span><span class="sxs-lookup"><span data-stu-id="73720-154">If you need some inspiration, and you're using EWS, you might explore the [Exchange 101 code samples](https://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c) for some ideas.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73720-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73720-155">See also</span></span>


- [<span data-ttu-id="73720-156">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="73720-156">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="73720-157">Exchange Web Services (EWS) 托管 API</span><span class="sxs-lookup"><span data-stu-id="73720-157">Exchange Web Services (EWS) Managed API</span></span>](https://msdn.microsoft.com/library/exchange/jj220535%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="73720-158">Exchange 的 SOAP 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="73720-158">SOAP Autodiscover web service reference for Exchange</span></span>](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- [<span data-ttu-id="73720-159">Exchange 的 POX 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="73720-159">POX Autodiscover web service reference for Exchange</span></span>](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    

