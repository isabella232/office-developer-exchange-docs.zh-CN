---
title: 要在 Exchange 使用 EWS 获取服务配置信息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: 了解如何在 Exchange 从 EWS 获取 UM、 策略微移、 邮件提示和保护规则的服务配置信息。
ms.openlocfilehash: e84a563bb094a2fe03e08f8e1a81b2b054d45850
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752777"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="0cdd5-103">要在 Exchange 使用 EWS 获取服务配置信息</span><span class="sxs-lookup"><span data-stu-id="0cdd5-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="0cdd5-104">了解如何在 Exchange 从 EWS 获取 UM、 策略微移、 邮件提示和保护规则的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="0cdd5-105">EWS 应用程序工作与统一消息 (UM)、 策略微移、 邮件提示或保护规则？</span><span class="sxs-lookup"><span data-stu-id="0cdd5-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="0cdd5-106">如果是这样，您的应用程序需要呼叫[GetServiceConfiguration 操作](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)来获取它需要的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-106">If so, your application will need to call the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="0cdd5-107">**GetServiceConfiguration**操作返回特定于每个这些 EWS 功能的配置信息。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0cdd5-108">EWS 托管 API 无法实现此功能。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="0cdd5-109">**表 1。GetServiceConfiguration 操作返回的配置信息**</span><span class="sxs-lookup"><span data-stu-id="0cdd5-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="0cdd5-110">EWS 功能</span><span class="sxs-lookup"><span data-stu-id="0cdd5-110">EWS feature</span></span>|<span data-ttu-id="0cdd5-111">返回 GetServiceConfiguration 操作...</span><span class="sxs-lookup"><span data-stu-id="0cdd5-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cdd5-112">UM</span><span class="sxs-lookup"><span data-stu-id="0cdd5-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="0cdd5-113">一个值，指示是否已启用 UM。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="0cdd5-114">一个值，指示是否已启用在电话上的播放。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="0cdd5-115">电话拨号串上播放。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="0cdd5-116">策略微移</span><span class="sxs-lookup"><span data-stu-id="0cdd5-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="0cdd5-117">显示您的客户端中的微移策略。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="0cdd5-118">邮件提示</span><span class="sxs-lookup"><span data-stu-id="0cdd5-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="0cdd5-119">一个值，指示是否启用邮件提示。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="0cdd5-120">最大收件人每次请求数。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="0cdd5-121">最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-121">The maximum message size.</span></span></li><li><span data-ttu-id="0cdd5-122">大型受众阈值。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-122">The large audience threshold.</span></span></li><li><span data-ttu-id="0cdd5-123">一个值，指示是否显示外部收件人的数量。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="0cdd5-124">内部域的列表。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-124">A list of internal domains.</span></span></li><li><span data-ttu-id="0cdd5-125">一个值，指示是否启用策略提示。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="0cdd5-126">用于指示您的邮件是否被视为有大量的收件人的大型受众帽阈值。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="0cdd5-127">保护规则</span><span class="sxs-lookup"><span data-stu-id="0cdd5-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="0cdd5-128">您的客户端的保护规则安装程序。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="0cdd5-129">在组织内部的域的列表。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="0cdd5-130">代码示例： 使用 EWS 获取服务配置邮件提示信息</span><span class="sxs-lookup"><span data-stu-id="0cdd5-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="0cdd5-131">下面的代码示例使用邮件提示[GetServiceConfiguration 操作](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)请求服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-131">The following code example uses the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="0cdd5-132">您可以通过添加使用不同的值的详细[配置名](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx)元素请求额外的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-132">You can request additional service configuration information by adding more [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
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

## <a name="next-steps"></a><span data-ttu-id="0cdd5-133">后续步骤</span><span class="sxs-lookup"><span data-stu-id="0cdd5-133">Next steps</span></span>

<span data-ttu-id="0cdd5-134">请求服务配置信息后，使用[XmlDocument 类](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx)，以便您可以分析加载 XML 的响应。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-134">After you request service configuration information, use the [XmlDocument class](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="0cdd5-135">然后，具体取决于您的情况，您可以执行下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="0cdd5-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="0cdd5-136">使用[GetMailTips 操作](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx)获取客户端应用程序向用户显示的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-136">Use the [GetMailTips operation](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="0cdd5-137">如果启用 UM，则通过电话的[了解有关如何播放邮箱项目](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0cdd5-137">If UM is enabled, [learn about how to play mailbox items](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0cdd5-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cdd5-138">See also</span></span>

- [<span data-ttu-id="0cdd5-139">Exchange 中的 EWS 的配置选项</span><span class="sxs-lookup"><span data-stu-id="0cdd5-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="0cdd5-140">EWS 应用程序设置</span><span class="sxs-lookup"><span data-stu-id="0cdd5-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="0cdd5-141">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="0cdd5-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

