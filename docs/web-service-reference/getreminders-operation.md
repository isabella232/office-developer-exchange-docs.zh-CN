---
title: GetReminders 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: 查找信息 GetReminders EWS 操作。
ms.openlocfilehash: 803dabf51b94dbd8fb01f2709a42ff59a597bfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754669"
---
# <a name="getreminders-operation"></a>GetReminders 操作

查找有关**GetReminders** EWS 操作的信息。 
  
**GetReminders** Exchange Web Services (EWS) 操作中检索日历和任务的项目的提醒。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-getreminders-operation"></a>使用 GetReminders 操作

**GetReminders**操作当前和将来的日历和任务项目的提醒获取用户的邮箱，具体取决于请求中传递的元素值中。 操作可以检索所有当前和将来的日历项目以及设置的提醒的任务。 个人日历项目都包含在响应中。 无提醒任务不包含在响应，也不与提醒的电子邮件或后续标志。 
  
若要检索所有当前提醒，我们建议设置到**所有** [ReminderType](remindertype.md)和[EndTime](endtime-remindermessagedatatype.md)到当前时间。 
  
如果[BeginTime](begintime.md)和**EndTime**元素都包含在请求中，响应包括任何日历提醒和之间发生的任务项目已发生之间的**BeginTime**和**结束时间**的提醒。
  
包含**BeginTime**和**EndTime**元素时下, 表介绍**ReminderType**元素的行为。 
  
|ReminderType * * 元素值 * *|**说明**|
|:-----|:-----|
|所有  <br/> |**BeginTime**和**EndTime**之间发生的提醒。  <br/> |
|当前  <br/> |返回**所有**，提醒加上提醒的早于请求的时间窗口是否仍正在进行，了事件以及无论期限的所有约会。  <br/> |
|旧  <br/> |返回**所有**，减去尚未完成，减去所有约会的事件的提醒。 必须将**BeginTime**和**EndTime**元素设置为使用**旧**值。  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>GetReminders 操作 SOAP 标头

**GetReminders**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。 适用于请求此标头。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。 适用于请求此标头。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 适用于请求此标头。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 适用于响应此标头。  <br/> |
   
## <a name="getreminders-operation-request-example"></a>GetReminders 操作请求示例

**GetReminders**操作请求的下面的示例演示如何检索**BeginTime**和**EndTime**之间发生的第五个日历项目。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

示例请求 SOAP 正文包含以下元素：
  
- [GetReminders](getreminders.md)
    
- [结束时间](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
SOAP 正文还可以包含以下元素：
  
- [BeginTime](begintime.md)
    
- [MaxItems](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>成功 GetReminders 操作响应

下面的示例演示对**GetReminders**操作请求成功响应。 则响应中包含"团队会议"日历项目的提醒和提醒"任务发送会议笔记"任务。 
  
> [!NOTE]
> 标识符具有已缩短要保留可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Team meeting</Subject>
          <Location />
          <ReminderTime>2014-04-15T21:00:00Z</ReminderTime>
          <StartDate>2014-04-15T21:00:00Z</StartDate>
          <EndDate>2014-04-15T21:30:00Z</EndDate>
          <ItemId Id="vQAAAA=="
                  ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV4" />
          <RecurringMasterItemId Id="K7u5AAA=" ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV0" />
          <ReminderGroup>Calendar</ReminderGroup>
          <UID>6CF2FA62</UID>
        </Reminder>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Task to send meeting notes</Subject>
          <Location />
          <ReminderTime>2014-04-16T14:00:00Z</ReminderTime>
          <StartDate>0001-01-02T00:00:00Z</StartDate>
          <EndDate>0001-01-02T00:00:00Z</EndDate>
          <ItemId Id="vAAAAA=="
                  ChangeKey="EwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAIDg==" />
          <ReminderGroup>Task</ReminderGroup>
          <UID>vAAAAA==</UID>
        </Reminder>
      </Reminders>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

响应 SOAP 正文中包含以下元素：
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Reminders](reminders.md)
    
- [提醒](reminder.md)
    
- [Subject](subject.md)
    
- [位置](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [ReminderGroup](remindergroup.md)
    
- [UID](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>GetReminders 操作错误响应示例

下面的示例演示对**GetReminders**操作请求错误响应。 这是对在其中的结束日期已早于开始日期的请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅


- [PerformReminderAction](performreminderaction.md)
    

