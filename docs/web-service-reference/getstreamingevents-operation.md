---
title: GetStreamingEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: 8da95423-72bc-4034-90a8-162eedcd059b
description: 查找有关 GetStreamingEvents EWS 操作的信息。
ms.openlocfilehash: 794407c2224e606be4f32cc610eff9f95e65a83b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523060"
---
# <a name="getstreamingevents-operation"></a>GetStreamingEvents 操作

查找有关 **GetStreamingEvents** EWS 操作的信息。 
  
**GetStreamingEvents** 操作由流式订阅客户端用于从客户端访问服务器请求通知。 **GetStreamingEvents** 响应返回自上次通知以来邮箱中发生的项目和事件的数组。 
  
## <a name="getstreamingevents-request-example"></a>GetStreamingEvents 请求示例

### <a name="description"></a>Description

下面的 **GetStreamingEvents** 操作示例演示如何请求与订阅标识符标识的订阅关联的事件和项目。 
  
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

请求中会使用下列元素：
  
- [GetStreamingEvents](getstreamingevents.md)
    
- [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md)
    
- [ConnectionTimeout](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a>成功的 GetStreamingEvents 响应示例

### <a name="description"></a>Description

**GetStreamingEvents** 响应的以下示例显示收到新电子邮件时发送给客户端的通知。 它包含以下事件的通知：CreatedEvent、NewMail 和 ModifiedEvent。 
  
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

响应中会使用下列元素：
  
- [GetStreamingEventsResponse](getstreamingeventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md)
    
- [NotesFolderPermissionLevel](notesfolderpermissionlevel.md)
    
- [通知](notification-ex15websvcsotherref.md)
    
- [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md)
    
若要查找 **GetStreamingEvents** 操作的响应消息的其他选项，请浏览架构层次结构。 从 [Notification 元素](notification-ex15websvcsotherref.md) 开始。 
  
## <a name="getstreamingevents-error-response-example"></a>GetStreamingEvents 错误响应示例

### <a name="description"></a>Description

以下示例显示对 **GetStreamingEvents** 请求的错误响应。 
  
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

## <a name="remarks"></a>注解

处理 **GetStreamingEvents** 请求时，客户端访问服务器将执行以下步骤： 
  
1. 请求 [ (GetStreamingEvents ](subscriptionid-getstreamingevents.md)) 的 SubscriptionId 已确认为托管在客户端访问服务器上的有效订阅。 如果不是 **，GetStreamingEvents 调用** 将失败。 
    
2. 验证请求的已验证用户的 SMTP 地址具有模拟权限。 如果没有 **，GetStreamingEvents 请求** 将失败。 
    
3. 查询订阅队列，了解正在等待发送到客户端的事件。 如果队列不为空，则队列中前 50 个事件从队列中提取并编码为通知。
    
4. 如果在队列中未找到任何事件，则 [生成 StatusEvent，](statusevent.md) 并编码为通知响应。 
    
5. 通知响应将返回到客户端。
    
6. 通知中包含的事件将从订阅队列中删除，并且订阅的客户端访问服务器本地最后一个水印设置为返回的最后一个事件水印。
    
7. 重置订阅的超时计时器。
    
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)

