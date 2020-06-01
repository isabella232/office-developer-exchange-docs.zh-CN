---
title: GetEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: 请求订阅客户端使用 GetEvents 操作从客户端访问服务器中请求通知。 GetEvents 操作响应返回自上次通知以来在邮箱中发生的项和事件的数组。
ms.openlocfilehash: 9258fd003c242911866aa7abbca5eba2b9582223
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462512"
---
# <a name="getevents-operation"></a>GetEvents 操作

请求订阅客户端使用**GetEvents**操作从客户端访问服务器中请求通知。 **GetEvents**操作响应返回自上次通知以来在邮箱中发生的项和事件的数组。 
  
> [!IMPORTANT]
> **DeleteUserConfiguration**操作将触发事件通知系统的移动事件。 用户配置对象将被移动到转储程序。 
  
## <a name="remarks"></a>备注

对日历项目所做的更改可能会导致生成多个事件。 这些事件是在邮箱、忙/闲数据存储项目被更改为常规日历操作的一部分或同时在这两者中创建的临时项目的结果。 项目类 "IPM." 的事件。Web 服务客户端应忽略 FreeBusy。 SchedulePlus。 这些临时项目在创建后将被删除;因此，如果尝试检索这些项，则将返回错误，指出找不到该项目。
  
## <a name="getevents-request-example"></a>GetEvents 请求示例

### <a name="description"></a>说明

下面的示例演示如何请求与订阅标识符和水印标识的订阅相关联的事件和项目。
  
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

请求中使用以下元素：
  
- [GetEvents](getevents.md)
    
- [SubscriptionId （GetEvents）](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="successful-getevents-response-example"></a>成功的 GetEvents 响应示例

### <a name="description"></a>说明

下面的响应示例显示通知，自上次通知请求发送到服务器后，存在两封新邮件。
  
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
> 项目和文件夹标识符已缩短，以保持可读性。 
  
### <a name="getevents-response-elements"></a>GetEvents 响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetEventsResponse](geteventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetEventsResponseMessage](geteventsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [通知](notification-ex15websvcsotherref.md)
    
- [SubscriptionId （GetEvents）](subscriptionid-getevents.md)
    
- [PreviousWatermark](previouswatermark.md)
    
- [MoreEvents](moreevents.md)
    
- [NewMailEvent](newmailevent.md)
    
- [Watermark](watermark.md)
    
- [TimeStamp](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
若要查找**GetEvents**操作的响应邮件的其他选项，请浏览架构层次结构。 从[通知](notification-ex15websvcsotherref.md)元素开始。 
  
## <a name="getevents-error-response-example"></a>GetEvents 错误响应示例

### <a name="description"></a>说明

下面的示例演示对**GetEvents**请求的错误响应。 
  
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

## <a name="remarks"></a>备注

在处理**GetEvents**请求时，客户端访问服务器将执行以下步骤： 
  
1. 将请求的 SubscriptionID 确认为在客户端访问服务器上承载的有效订阅。 如果不是，则**GetEvents**调用将失败。 
    
2. 将请求的已通过身份验证的用户的 SMTP 地址与创建订阅的用户的 SMTP 地址进行比较。 如果不匹配， **GetEvents**请求将失败。 
    
3. 将查询订阅队列中等待发送到客户端的事件。 如果队列不为空，则会从队列中提取队列中的前50个事件并将其编码到通知中。
    
4. 如果队列中未找到任何事件，则会生成 StatusEvent 并将其编码到通知响应中。
    
5. 通知响应将返回到客户端。
    
6. 通知中包含的事件将从订阅队列中删除，并且订阅的客户端访问服务器本地最后的水印将设置为返回的最后一个事件的水印。
    
7. 订阅的超时计时器将重置。
    
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)


[使用请求订阅](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

