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
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>要在 Exchange 使用 EWS 获取服务配置信息

了解如何在 Exchange 从 EWS 获取 UM、 策略微移、 邮件提示和保护规则的服务配置信息。
  
EWS 应用程序工作与统一消息 (UM)、 策略微移、 邮件提示或保护规则？ 如果是这样，您的应用程序需要呼叫[GetServiceConfiguration 操作](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)来获取它需要的服务配置信息。 **GetServiceConfiguration**操作返回特定于每个这些 EWS 功能的配置信息。 
  
> [!NOTE]
> EWS 托管 API 无法实现此功能。 
  
**表 1。GetServiceConfiguration 操作返回的配置信息**

|EWS 功能|返回 GetServiceConfiguration 操作...|
|:-----|:-----|
|UM  <br/> | <ul><li>一个值，指示是否已启用 UM。</li><li>一个值，指示是否已启用在电话上的播放。</li><li>电话拨号串上播放。</li></ul> |
|策略微移  <br/> | <ul><li>显示您的客户端中的微移策略。</li></ul> |
|邮件提示  <br/> | <ul><li>一个值，指示是否启用邮件提示。</li><li>最大收件人每次请求数。</li><li>最大邮件大小。</li><li>大型受众阈值。</li><li>一个值，指示是否显示外部收件人的数量。</li><li>内部域的列表。</li><li>一个值，指示是否启用策略提示。</li><li>用于指示您的邮件是否被视为有大量的收件人的大型受众帽阈值。  </li></ul>|
|保护规则  <br/> | <ul><li>您的客户端的保护规则安装程序。</li><li>在组织内部的域的列表。  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>代码示例： 使用 EWS 获取服务配置邮件提示信息

下面的代码示例使用邮件提示[GetServiceConfiguration 操作](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)请求服务配置信息。 您可以通过添加使用不同的值的详细[配置名](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx)元素请求额外的服务配置信息。 
  
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

请求服务配置信息后，使用[XmlDocument 类](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx)，以便您可以分析加载 XML 的响应。 然后，具体取决于您的情况，您可以执行下列选项之一： 
  
- 使用[GetMailTips 操作](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx)获取客户端应用程序向用户显示的邮件提示。 
    
- 如果启用 UM，则通过电话的[了解有关如何播放邮箱项目](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx)。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 的配置选项](configuration-options-for-ews-in-exchange.md)    
- [EWS 应用程序设置](setting-up-your-ews-application.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

