---
title: 使用 EWS 获取服务配置Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: 了解如何从 EXCHANGE 中的 EWS 获取 UM 的服务配置信息、策略微机制、邮件提示和保护Exchange。
ms.openlocfilehash: 30d4058104726c79f473a88a09398689675b988d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513169"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>使用 EWS 获取服务配置Exchange

了解如何从 EXCHANGE 中的 EWS 获取 UM 的服务配置信息、策略微机制、邮件提示和保护Exchange。
  
您的 EWS 应用程序是否与统一消息 (UM) 策略、邮件提示或保护规则一起运行？ 如果是这样，应用程序将需要调用 [GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) 操作，获取所需的服务配置信息。 **GetServiceConfiguration** 操作返回特定于其中每个 EWS 功能的配置信息。 
  
> [!NOTE]
> EWS 托管 API 无法实现此功能。 
  
**表 1.GetServiceConfiguration 操作返回的配置信息**

|EWS 功能|GetServiceConfiguration 操作返回...|
|:-----|:-----|
|UM  <br/> | <ul><li>一个值，指示是否已启用 UM。</li><li>指示是否启用在电话上播放的值。</li><li>在电话拨号串上播放。</li></ul> |
|策略不活动  <br/> | <ul><li>在客户端中显示的策略微微。</li></ul> |
|邮件提示  <br/> | <ul><li>一个值，该值指示是否已启用邮件提示。</li><li>每个请求的最大收件人数。</li><li>最大邮件大小。</li><li>大型受众阈值。</li><li>一个值，该值指示是否显示外部收件人的数量。</li><li>内部域的列表。</li><li>指示是否启用策略提示的值。</li><li>用于指示邮件是否被视为具有大量收件人的大型受众上限阈值。  </li></ul>|
|保护规则  <br/> | <ul><li>为客户端设置保护规则。</li><li>组织内部的域列表。  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>代码示例：使用 EWS 获取邮件提示的服务配置信息

以下代码示例使用 [GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) 请求邮件提示的服务配置信息。 可以通过添加更多具有不同的值的 [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) 元素来请求其他服务配置信息。 
  
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

## <a name="next-steps"></a>后续步骤

请求服务配置信息后，使用 [XmlDocument 类](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) 加载响应 XML，以便分析它。 然后，根据你的方案，你可以执行以下操作之一： 
  
- 使用 [GetMailTips 操作](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) 获取客户端应用程序向用户显示的邮件提示。 
    
- 如果启用了 UM， [请了解如何在电话上播放](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) 邮箱项目。 
    
## <a name="see-also"></a>另请参阅

- [EWS 在Exchange](configuration-options-for-ews-in-exchange.md)    
- [设置 EWS 应用程序](setting-up-your-ews-application.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

