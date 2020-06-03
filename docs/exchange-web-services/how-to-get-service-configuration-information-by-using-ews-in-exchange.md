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
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 获取服务配置信息

了解如何从 Exchange 中的 EWS 获取 UM、策略微移、邮件提示和保护规则的服务配置信息。
  
您的 EWS 应用程序是否适用于统一消息（UM）、策略微移、邮件提示或保护规则？ 如果是这样，应用程序将需要调用[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)以获取所需的服务配置信息。 **GetServiceConfiguration**操作返回特定于这些 EWS 功能中的每个功能的配置信息。 
  
> [!NOTE]
> EWS 托管 API 无法实现此功能。 
  
**表1。GetServiceConfiguration 操作返回的配置信息**

|EWS 功能|GetServiceConfiguration 操作返回 .。。|
|:-----|:-----|
|UM  <br/> | <ul><li>一个指示是否启用 UM 的值。</li><li>一个指示是否启用 "在电话上播放" 的值。</li><li>"在电话上播放" 拨号字符串。</li></ul> |
|策略微移  <br/> | <ul><li>在客户端中显示的策略微移。</li></ul> |
|邮件提示  <br/> | <ul><li>一个值，指示是否启用邮件提示。</li><li>每个请求的最大收件人数。</li><li>最大邮件大小。</li><li>大型访问群体阈值。</li><li>一个值，指示是否显示外部收件人的数量。</li><li>内部域的列表。</li><li>一个指示是否启用策略提示的值。</li><li>大型听众帽阈值，用于指示是否将您的邮件视为具有大量收件人。  </li></ul>|
|保护规则  <br/> | <ul><li>客户端的保护规则设置。</li><li>组织内部的域的列表。  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>代码示例：使用 EWS 获取邮件提示的服务配置信息

下面的代码示例使用[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)来请求邮件提示的服务配置信息。 您可以通过使用不同的值添加更多[ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx)元素来请求其他服务配置信息。 
  
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

## <a name="next-steps"></a>后续步骤

请求服务配置信息后，使用工作[类型类](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx)加载响应 XML，以便您可以对其进行分析。 然后，根据您的方案，您可以执行以下操作之一： 
  
- 使用[GetMailTips 操作](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx)可获取要向用户显示的客户端应用程序的邮件提示。 
    
- 如果启用了 UM，请[了解如何通过电话播放邮箱项目](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx)。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 中 EWS 的配置选项](configuration-options-for-ews-in-exchange.md)    
- [设置 EWS 应用程序](setting-up-your-ews-application.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

