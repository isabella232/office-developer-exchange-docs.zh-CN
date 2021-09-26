---
title: Subscribe 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: Subscribe 操作用于订阅客户端应用程序以推送通知或拉取通知。 必须注意，请求消息和响应的结构因事件通知的类型不同而不同。
ms.openlocfilehash: 546f7ab252c7d3a201130cd48e2b30ca52d00088
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544533"
---
# <a name="subscribe-operation"></a>Subscribe 操作

Subscribe 操作用于订阅客户端应用程序以推送通知或拉取通知。 必须注意，请求消息和响应的结构因事件通知的类型不同而不同。 
  
## <a name="pull-subscription-subscribe-request-example"></a>拉取订阅订阅请求示例

### <a name="description"></a>说明

以下代码示例演示如何订阅拉取事件通知订阅。 订阅会通知客户端应用程序新邮件是否添加到收件箱，以及是否从收件箱中删除了项目。 如果客户端在十分钟内未请求有关事件的信息，订阅将退出。 如果订阅过期，必须建立新订阅以继续请求通知。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PullSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox"/>
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
        </t:EventTypes>
        <t:Timeout>10</t:Timeout>
      </PullSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-request-elements"></a>拉取订阅订阅请求元素

请求中会使用下列元素：
  
- [Subscribe](subscribe.md)
    
- [PullSubscriptionRequest](pullsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [Timeout](timeout.md)
    
若要查找 Subscribe 操作的请求消息的其他选项，请浏览架构层次结构。 从 [PullSubscriptionRequest 元素](pullsubscriptionrequest.md) 开始。 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a>成功拉取订阅订阅响应示例

### <a name="description"></a>说明

以下示例显示了成功的拉取订阅响应。 该响应包含订阅标识符和用于获取与订阅关联的事件数组水印。 订阅标识符还用于取消订阅客户端。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>39ea5d0f-f062-455e-a1e9-89c0304390f4</m:SubscriptionId>
          <m:Watermark>AAAAAHgGAAAAAAAAAQ==</m:Watermark>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-response-elements"></a>拉取订阅订阅响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a>拉取订阅订阅错误响应示例

### <a name="description"></a>说明

以下示例显示了对 Subscribe 请求的错误响应。 此错误是由尝试使用委派访问订阅通知导致的。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>Subscriptions are not supported for delegate user access.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionDelegateAccessNotSupported</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-error-response-elements"></a>拉取订阅错误响应元素

错误响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a>推送订阅请求示例

### <a name="description"></a>说明

以下代码示例演示如何订阅推送通知订阅。 该请求标识要监视的文件夹、要监视的事件类型、状态通知的频率以及侦听推送通知的客户端 Web 服务的 URL。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="https://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="https://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

在发送推送通知订阅请求之前，必须设置客户端 Web 服务;否则，第一个通知将不会发送到有效的终结点，并且推送通知将失败。 有关详细信息，请参阅推送通知 [示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)。
  
在重新 [订阅 (将) GetEvents ](subscriptionid-getevents.md) 对象的新 SubscriptionId。 使用上一订阅水印在上一订阅结束时重新订阅。 
  
### <a name="push-subscription-request-elements"></a>推送订阅请求元素

请求中会使用下列元素：
  
- [Subscribe](subscribe.md)
    
- [PushSubscriptionRequest](pushsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [StatusFrequency](statusfrequency.md)
    
- [Url ](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a>成功的推送订阅响应示例

### <a name="description"></a>说明

以下示例显示了成功的推送订阅响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <SubscribeResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <SubscriptionId>83826921-afdf-48be-b469-628cc02b5f49</SubscriptionId>
          <Watermark>AQAAAOpvG0LURVdOhQkPOWZLPcI8EgAAAAAAAAE=</Watermark>
        </SubscribeResponseMessage>
      </ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="push-subscription-response-elements"></a>推送订阅响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="see-also"></a>另请参阅



[Unsubscribe 操作](unsubscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)


[使用拉取订阅](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[推送通知示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

