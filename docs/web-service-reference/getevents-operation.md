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
description: GetEvents 操作使用拉订阅客户端请求通知从客户端访问服务器。 GetEvents 操作响应返回的数组项和发生的事件的邮箱中上次通知。
ms.openlocfilehash: 1a23a9d570a4554e54becb7927f25dff89888c74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754531"
---
# <a name="getevents-operation"></a>GetEvents 操作

**GetEvents**操作使用拉订阅客户端请求通知从客户端访问服务器。 **GetEvents**操作响应返回的数组项和发生的事件的邮箱中上次通知。 
  
> [!IMPORTANT]
> **DeleteUserConfiguration**操作将触发事件通知系统移动的事件。 用户配置对象将移至转储程序。 
  
## <a name="remarks"></a>注解

对日历项目的更改可能会导致生成的多个事件。 这些事件是正在更改为正常的日历操作中，或两者的一部分的忙/闲数据存储项在邮箱中创建的临时项目的结果。 项目的事件类"IPM。Web 服务客户端应忽略 SchedulePlus.FreeBusy.BinaryData"。 在创建; 后删除临时项目因此，如果尝试检索这些项，将返回错误，指出找不到该项目。
  
## <a name="getevents-request-example"></a>GetEvents 请求示例

### <a name="description"></a>说明

下面的示例演示如何请求的事件和订阅的订阅标识符和水印标识与关联的项目。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>GetEvents 请求元素

请求中使用以下元素：
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [水印](watermark.md)
    
## <a name="successful-getevents-response-example"></a>成功 GetEvents 响应示例

### <a name="description"></a>说明

下面的示例响应的显示存在两个新邮件通知自从最后一个通知请求发送到服务器。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

> [!NOTE]
> 项目和文件夹标识符具有已缩短要保留可读性。 
  
### <a name="getevents-response-elements"></a>GetEvents 响应元素

在响应中使用以下元素：
  
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
    
- [水印](watermark.md)
    
- [时间戳](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
若要查找的响应消息**GetEvents**操作的其他选项，浏览的架构层次结构。 启动[通知](notification-ex15websvcsotherref.md)元素。 
  
## <a name="getevents-error-response-example"></a>GetEvents 错误响应示例

### <a name="description"></a>说明

下面的示例演示对**GetEvents**请求错误响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

当处理**GetEvents**请求，客户端访问服务器将执行以下步骤： 
  
1. 确认请求的 SubscriptionID 是有效的订阅的客户端访问服务器上承载。 如果不存在，则**GetEvents**调用将失败。 
    
2. 创建订阅的用户的 SMTP 地址进行比较的请求身份验证的用户的 SMTP 地址。 如果不匹配， **GetEvents**请求失败。 
    
3. 订阅队列中等待要发送给客户端的事件查询。 如果不为空队列，从队列的前 50 个事件是从队列中拉取和编码到通知。
    
4. 如果在队列中不发现的任何事件，StatusEvent 生成，且编码到通知响应。
    
5. 通知响应将返回到客户端。
    
6. 从订阅队列中删除包含在的通知的事件和客户端访问服务器本地最后一个水印订阅设置为返回的最后一个事件水印。
    
7. 订阅超时计时器重置。
    
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[取消操作](unsubscribe-operation.md)


[使用请求订阅](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

