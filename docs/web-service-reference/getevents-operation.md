---
title: GetEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: GetEvents 操作由拉取订阅客户端用于从客户端访问服务器请求通知。 GetEvents 操作响应返回自上次通知以来邮箱中发生的项目和事件的数组。
ms.openlocfilehash: 72d99a654921794115d56d28327a39a21c9ea378
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511598"
---
# <a name="getevents-operation"></a>GetEvents 操作

**GetEvents** 操作由拉取订阅客户端用于从客户端访问服务器请求通知。 **GetEvents** 操作响应返回自上次通知以来邮箱中发生的项目和事件的数组。 
  
> [!IMPORTANT]
> **DeleteUserConfiguration** 操作将触发事件通知系统的移动事件。 用户配置对象将移动到垃圾站。 
  
## <a name="notes"></a>注意

对"日历"项的更改可能会导致生成多个事件。 这些事件是在邮箱中创建的临时项目、作为常规日历操作一部分更改的忙/闲数据存储项目或同时更改这两者的结果。 项目类"IPM"的事件。Web 服务客户端应忽略 SchedulePlus.FreeBusy.BinaryData"。 这些临时项目创建后将被删除;因此，如果尝试检索这些项目，将返回一个错误，指出未找到该项目。
  
## <a name="getevents-request-example"></a>GetEvents 请求示例

### <a name="description"></a>Description

以下示例演示如何请求与订阅标识符和水印标识的订阅关联的事件和项目。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>GetEvents 请求元素

请求中会使用下列元素：
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="successful-getevents-response-example"></a>成功的 GetEvents 响应示例

### <a name="description"></a>Description

以下响应示例显示自上一个通知请求发送到服务器后存在两封新邮件的通知。
  
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
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

> [!NOTE]
> 已缩短项和文件夹标识符以保持可读性。 
  
### <a name="getevents-response-elements"></a>GetEvents 响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetEventsResponse](geteventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetEventsResponseMessage](geteventsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [通知](notification-ex15websvcsotherref.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [PreviousWatermark](previouswatermark.md)
    
- [MoreEvents](moreevents.md)
    
- [NewMailEvent](newmailevent.md)
    
- [Watermark](watermark.md)
    
- [TimeStamp](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
若要查找 **GetEvents** 操作的响应消息的其他选项，请浏览架构层次结构。 从 [Notification 元素](notification-ex15websvcsotherref.md) 开始。 
  
## <a name="getevents-error-response-example"></a>GetEvents 错误响应示例

### <a name="description"></a>Description

以下示例显示对 **GetEvents** 请求的错误响应。 
  
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
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a>注解

处理 **GetEvents** 请求时，客户端访问服务器将执行以下步骤： 
  
1. 请求的 SubscriptionID 已确认为托管在客户端访问服务器上的有效订阅。 如果不是 **，GetEvents** 调用将失败。 
    
2. 请求的已验证用户的 SMTP 地址与创建订阅的用户的 SMTP 地址进行比较。 如果它们不匹配 **，GetEvents 请求** 将失败。 
    
3. 查询订阅队列，了解正在等待发送到客户端的事件。 如果队列不为空，则队列中前 50 个事件从队列中提取并编码为通知。
    
4. 如果在队列中未找到任何事件，则生成 StatusEvent，并编码为通知响应。
    
5. 通知响应将返回到客户端。
    
6. 通知中包含的事件将从订阅队列中删除，并且订阅的客户端访问服务器本地最后一个水印设置为返回的最后一个事件水印。
    
7. 重置订阅的超时计时器。
    
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)


[使用拉取订阅](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

