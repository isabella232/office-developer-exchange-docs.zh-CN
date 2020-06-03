---
title: 使用 Exchange 中的 EWS 获取服务配置信息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: 了解如何从 Exchange 中的 EWS 获取 UM、策略微移、邮件提示和保护规则的服务配置信息。
ms.openlocfilehash: 7546d9524f1e004eda2bdc55687fb44beafa44af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528004"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="0ff46-103">使用 Exchange 中的 EWS 获取服务配置信息</span><span class="sxs-lookup"><span data-stu-id="0ff46-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="0ff46-104">了解如何从 Exchange 中的 EWS 获取 UM、策略微移、邮件提示和保护规则的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ff46-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="0ff46-105">您的 EWS 应用程序是否适用于统一消息（UM）、策略微移、邮件提示或保护规则？</span><span class="sxs-lookup"><span data-stu-id="0ff46-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="0ff46-106">如果是这样，应用程序将需要调用[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)以获取所需的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ff46-106">If so, your application will need to call the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="0ff46-107">**GetServiceConfiguration**操作返回特定于这些 EWS 功能中的每个功能的配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ff46-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0ff46-108">EWS 托管 API 无法实现此功能。</span><span class="sxs-lookup"><span data-stu-id="0ff46-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="0ff46-109">**表1。GetServiceConfiguration 操作返回的配置信息**</span><span class="sxs-lookup"><span data-stu-id="0ff46-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="0ff46-110">EWS 功能</span><span class="sxs-lookup"><span data-stu-id="0ff46-110">EWS feature</span></span>|<span data-ttu-id="0ff46-111">GetServiceConfiguration 操作返回 .。。</span><span class="sxs-lookup"><span data-stu-id="0ff46-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ff46-112">UM</span><span class="sxs-lookup"><span data-stu-id="0ff46-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="0ff46-113">一个指示是否启用 UM 的值。</span><span class="sxs-lookup"><span data-stu-id="0ff46-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="0ff46-114">一个指示是否启用 "在电话上播放" 的值。</span><span class="sxs-lookup"><span data-stu-id="0ff46-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="0ff46-115">"在电话上播放" 拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="0ff46-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="0ff46-116">策略微移</span><span class="sxs-lookup"><span data-stu-id="0ff46-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="0ff46-117">在客户端中显示的策略微移。</span><span class="sxs-lookup"><span data-stu-id="0ff46-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="0ff46-118">邮件提示</span><span class="sxs-lookup"><span data-stu-id="0ff46-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="0ff46-119">一个值，指示是否启用邮件提示。</span><span class="sxs-lookup"><span data-stu-id="0ff46-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="0ff46-120">每个请求的最大收件人数。</span><span class="sxs-lookup"><span data-stu-id="0ff46-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="0ff46-121">最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="0ff46-121">The maximum message size.</span></span></li><li><span data-ttu-id="0ff46-122">大型访问群体阈值。</span><span class="sxs-lookup"><span data-stu-id="0ff46-122">The large audience threshold.</span></span></li><li><span data-ttu-id="0ff46-123">一个值，指示是否显示外部收件人的数量。</span><span class="sxs-lookup"><span data-stu-id="0ff46-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="0ff46-124">内部域的列表。</span><span class="sxs-lookup"><span data-stu-id="0ff46-124">A list of internal domains.</span></span></li><li><span data-ttu-id="0ff46-125">一个指示是否启用策略提示的值。</span><span class="sxs-lookup"><span data-stu-id="0ff46-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="0ff46-126">大型听众帽阈值，用于指示是否将您的邮件视为具有大量收件人。</span><span class="sxs-lookup"><span data-stu-id="0ff46-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="0ff46-127">保护规则</span><span class="sxs-lookup"><span data-stu-id="0ff46-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="0ff46-128">客户端的保护规则设置。</span><span class="sxs-lookup"><span data-stu-id="0ff46-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="0ff46-129">组织内部的域的列表。</span><span class="sxs-lookup"><span data-stu-id="0ff46-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="0ff46-130">代码示例：使用 EWS 获取邮件提示的服务配置信息</span><span class="sxs-lookup"><span data-stu-id="0ff46-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="0ff46-131">下面的代码示例使用[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)来请求邮件提示的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ff46-131">The following code example uses the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="0ff46-132">您可以通过使用不同的值添加更多[ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx)元素来请求其他服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ff46-132">You can request additional service configuration information by adding more [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
    "               xmlns:xs=\"http://www.w3.org/2001/XMLSchema\">\n" +
    "  <soap:Header>\n" +
    "    <t:RequestServerVersion Version=\"Exchange2013\" />\n" +
    "  </soap:Header>\n" +
    "  <soap:Body>\n" +
    "    <m:GetServiceConfiguration>\n" +
    "      <m:ActingAs>\n" +
    "        <t:EmailAddress>user1@contoso.com</t:EmailAddress>\n" +
    "        <t:RoutingType>SMTP</t:RoutingType>\n" +
    "      </m:ActingAs>\n" +
    "      <m:RequestedConfiguration>\n" +
    "        <m:ConfigurationName>MailTips</m:ConfigurationName>\n" +
    "      </m:RequestedConfiguration>\n" +
    "    </m:GetServiceConfiguration>\n" +
    "  </soap:Body>\n" +
    "</soap:Envelope>";
  // Encoded GetServiceConfiguration operation request.
  byte[] payload = System.Text.Encoding.UTF8.GetBytes(getServiceConfigurationRequest);
  try
  {
    HttpWebRequest request = (HttpWebRequest)WebRequest.Create(service.Url);
    request.AllowAutoRedirect = false;
    request.Credentials = creds;
    request.Method = "POST";
    request.ContentType = "text/xml";
    Stream requestStream = request.GetRequestStream();
    requestStream.Write(payload, 0, payload.Length);
    requestStream.Close();
    HttpWebResponse response = (HttpWebResponse)request.GetResponse();
    if (response.StatusCode == HttpStatusCode.OK)
    {
      Stream responseStream = response.GetResponseStream();
      StreamReader reader = new StreamReader(responseStream);
      string responseFromServer = reader.ReadToEnd();
      Console.WriteLine("You will need to parse this response to get the configuration information:\n\n" + responseFromServer);
      reader.Close();
      responseStream.Close();
    }
    else
      throw new WebException(response.StatusDescription);
          
  }
  catch (WebException e)
  {
    Console.WriteLine(e.Message);
  }
}

```

## <a name="next-steps"></a><span data-ttu-id="0ff46-133">后续步骤</span><span class="sxs-lookup"><span data-stu-id="0ff46-133">Next steps</span></span>

<span data-ttu-id="0ff46-134">请求服务配置信息后，使用工作[类型类](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx)加载响应 XML，以便您可以对其进行分析。</span><span class="sxs-lookup"><span data-stu-id="0ff46-134">After you request service configuration information, use the [XmlDocument class](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="0ff46-135">然后，根据您的方案，您可以执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="0ff46-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="0ff46-136">使用[GetMailTips 操作](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx)可获取要向用户显示的客户端应用程序的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="0ff46-136">Use the [GetMailTips operation](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="0ff46-137">如果启用了 UM，请[了解如何通过电话播放邮箱项目](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0ff46-137">If UM is enabled, [learn about how to play mailbox items](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0ff46-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ff46-138">See also</span></span>

- [<span data-ttu-id="0ff46-139">Exchange 中 EWS 的配置选项</span><span class="sxs-lookup"><span data-stu-id="0ff46-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="0ff46-140">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="0ff46-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="0ff46-141">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="0ff46-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

