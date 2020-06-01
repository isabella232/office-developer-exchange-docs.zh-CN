---
title: PerformReminderAction 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: 查找有关 PerformReminderAction EWS 操作的信息。
ms.openlocfilehash: 4c069d541e9a42167c447a50c405399958d3608d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462288"
---
# <a name="performreminderaction-operation"></a>PerformReminderAction 操作

查找有关**PerformReminderAction** EWS 操作的信息。 
  
**PerformReminderAction** Exchange Web 服务（EWS）操作对提醒启动取消或推迟操作。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-performreminderaction-operation"></a>使用 PerformReminderAction 操作

您可以使用**PerformReminderAction**操作消除或推迟（延迟） [GetReminders](getreminders-operation.md)操作返回的提醒。 若要暂停提醒，请将[ActionType](actiontype-reminderactiontype.md)设置为 "**暂停**"，并将 " [NewReminderTime](newremindertime.md) " 值设置为晚于当前[ReminderTime](remindertime.md)的时间，否则服务器将忽略**NewReminderTime** 。 如果提醒针对的是定期会议，并且在提醒中对该提醒执行了**暂停**操作，而该提醒的**NewReminderTime**已超过了下一次出现的提醒，则将有效地消除提醒。 
  
若要消除提醒，请将**ActionType**设置为 "**消除**"。 当服务器处理请求时，服务器会将项目的[IsReminderSet](isreminderset.md)值从**True**更改为**False**。
  
### <a name="performreminderaction-operation-soap-headers"></a>PerformReminderAction 操作 SOAP 标头

**PerformReminderAction**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 此标头适用于响应。  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>PerformReminderAction 操作请求示例

以下示例的**PerformReminderAction**操作请求显示如何推迟当前提醒并设置新的提醒时间。 请注意，您需要包含[ItemId](itemid.md)的**ChangeKey** ，并且**NewReminderTime**必须设置为晚于[GetReminders](getreminders-operation.md)操作返回的**ReminderTime**的时间。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:PerformReminderAction>
      <m:ReminderItemActions>
        <t:ReminderItemAction>
          <t:ActionType>Snooze</t:ActionType>
          <t:ItemId Id="vwAAAA=="
           ChangeKey="DwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAUDA=="/>
          <t:NewReminderTime>2014-04-16T17:00:00Z</t:NewReminderTime>
        </t:ReminderItemAction>
      </m:ReminderItemActions>
    </m:PerformReminderAction>
  </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> 为了保持可读性， **ItemId**值已缩短。 
  
请求 SOAP 正文包含以下元素：
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>成功的 PerformReminderAction 操作响应

下面的示例演示对**PerformReminderAction**操作请求的成功响应。 **UpdatedItemIds**元素包含更新的日历项目的**ItemIds** 。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>PerformReminderAction 操作错误响应示例

下面的示例演示在服务器上未进行任何更改时对**PerformReminderAction**操作请求的响应。 这是发送请求的响应，但未返回任何**UpdatedItemIds** ，这意味着未更改任何提醒。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
有关对 EWS 通用的其他错误代码，请参阅[ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅


- [GetReminders 操作](getreminders-operation.md)
    

