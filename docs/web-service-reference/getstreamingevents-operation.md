---
title: GetStreamingEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: 8da95423-72bc-4034-90a8-162eedcd059b
description: 查找有关 GetStreamingEvents EWS 操作的信息。
ms.openlocfilehash: 27744ec40d7c7cb551f35ed5f6fcb726f23d4865
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530167"
---
# <a name="getstreamingevents-operation"></a>GetStreamingEvents 操作

查找有关**GetStreamingEvents** EWS 操作的信息。 
  
流式订阅客户端使用**GetStreamingEvents**操作从客户端访问服务器中请求通知。 **GetStreamingEvents**响应返回自上次通知以来在邮箱中发生的项和事件的数组。 
  
## <a name="getstreamingevents-request-example"></a>GetStreamingEvents 请求示例

### <a name="description"></a>Description

下面的**GetStreamingEvents**操作示例演示如何请求与订阅标识符标识的订阅相关联的事件和项目。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
  xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Body>
    <GetStreamingEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <ConnectionTimeout>30</ConnectionTimeout>
    </GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getstreamingevents-request-elements"></a>GetStreamingEvents 请求元素

请求中使用以下元素：
  
- [GetStreamingEvents](getstreamingevents.md)
    
- [SubscriptionId （GetStreamingEvents）](subscriptionid-getstreamingevents.md)
    
- [ConnectionTimeout](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a>成功的 GetStreamingEvents 响应示例

### <a name="description"></a>Description

下面的**GetStreamingEvents**响应示例显示收到新电子邮件时发送给客户端的通知。 它包括针对以下事件的通知： CreatedEvent、NewMail 和 ModifiedEvent。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <ServerVersionInfo xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
</soap:Header>
<soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:CreatedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:CreatedEvent>
            <t:NewMailEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:ModifiedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:FolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgEJAAAA" ChangeKey="AQAAAA==" />
              <t:UnreadCount>1</t:UnreadCount>
            </t:ModifiedEvent>
          </m:Notification>
        </m:Notifications>
      </m:GetStreamingEventsResponseMessage>
    </m:ResponseMessages>
  </m:GetStreamingEventsResponse>
</soap:Body>
```

### <a name="getstreamingevents-response-elements"></a>GetStreamingEvents 响应元素

响应中使用以下元素：
  
- [GetStreamingEventsResponse](getstreamingeventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md)
    
- [NotesFolderPermissionLevel](notesfolderpermissionlevel.md)
    
- [通知](notification-ex15websvcsotherref.md)
    
- [SubscriptionId （GetStreamingEvents）](subscriptionid-getstreamingevents.md)
    
若要查找**GetStreamingEvents**操作的响应邮件的其他选项，请浏览架构层次结构。 从[通知](notification-ex15websvcsotherref.md)元素开始。 
  
## <a name="getstreamingevents-error-response-example"></a>GetStreamingEvents 错误响应示例

### <a name="description"></a>Description

下面的示例演示对**GetStreamingEvents**请求的错误响应。 
  
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
    <GetStreamingEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetStreamingEventsResponseMessage ResponseClass="Error">
        <m:MessageText></m:MessageText>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        <m:ResponseCode>ErrorInvalidSubscription</m:ResponseCode>
        <m:ConnectionStatus>Closed</m:ConnectionStatus>
      </m:ResponseMessages>
    </GetStreamingEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a>备注

在处理**GetStreamingEvents**请求时，客户端访问服务器将执行以下步骤： 
  
1. 将请求的[SubscriptionId （GetStreamingEvents）](subscriptionid-getstreamingevents.md)确认为在客户端访问服务器上承载的有效订阅。 如果不是，则**GetStreamingEvents**调用将失败。 
    
2. 对请求的经过身份验证的用户的 SMTP 地址进行验证，以获得模拟权限。 如果不是，则**GetStreamingEvents**请求将失败。 
    
3. 将查询订阅队列中等待发送到客户端的事件。 如果队列不为空，则会从队列中提取队列中的前50个事件并将其编码到通知中。
    
4. 如果队列中未找到任何事件，则会生成[StatusEvent](statusevent.md)并将其编码到通知响应中。 
    
5. 通知响应将返回到客户端。
    
6. 通知中包含的事件将从订阅队列中删除，并且客户端访问服务器-订阅的本地最后的水印将设置为返回的最后一个事件的水印。
    
7. 订阅的超时计时器将重置。
    
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)

