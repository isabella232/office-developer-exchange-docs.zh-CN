---
title: 日历和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: 了解日历、 日历文件夹和项目、 约会和 Exchange 中的会议。
ms.openlocfilehash: bb9702118ff1db66862a5788c2d8f58dd55c4d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752702"
---
# <a name="calendars-and-ews-in-exchange"></a>日历和 Exchange 中的 EWS

了解日历、 日历文件夹和项目、 约会和 Exchange 中的会议。
  
您可能已经熟悉许多像 Outlook 的电子邮件客户端使您能够跟踪约会、 安排会议、 检查用户的可用性、 邀请与会者，并更改或取消会议中的日历功能。
  
Exchange 中的日历相关的功能是有点不同于如 Outlook 客户端中看到的内容。 而不是在 Exchange 中显示的信息，EWS 使您能够执行某些操作，如创建、 存储、 发送，或更改信息。 若要使用 EWS 使用日历，您需要熟悉如信息存储、 时间、 定期，和邮件流的概念。 更具体地说，您需要熟悉以下：
  
- 日历文件夹、 日历项和日历视图
    
- 会议请求、 响应、 日程安排，与会者、 资源、 聊天室和可用性
    
- 持续时间、 时区和会议和约会的开始和结束时间
    
- 定期系列、 定期模式、 例外和单实例约会和会议
    
幸运的是，EWS 和 EWS 托管 API 提供了一组丰富的操作和方法，使您能够执行各种与日历相关的任务。 例如，使用 EWS 托管 API，可以创建会议并发送邀请与会者几行代码，如下面的示例中所示。
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## <a name="calendar-folders-and-calendar-items"></a>日历文件夹和日历项目
<a name="bk_CalendarFolder"> </a>

日历文件夹包含日历项。 日历文件夹具有**IPF[文件夹类](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)。约会**，并且可以包括仅由[ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS 托管 API 属性，其相关联的[约会类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或 EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素定义的项目。 
  
日历文件夹中的项目是有点不同于邮箱中的其他文件夹中的项目，因为定期系列和定期系列的例外发生次数不是实际的项目中邮箱，而不内部存储为定期附件主控形状。 因此，为了检索给定的日期范围内的所有约会，您需要使用日历视图。 若要了解有关检索约会和日历视图的详细信息，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="meetings-and-appointments"></a>会议和约会
<a name="bk_meetings"> </a>

会议和约会的基本区别是，会议具有与会者，并且不约会。 内部 Exchange 使用相同的对象的会议和约会。 使用 EWS 托管 API[约会类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 EWS[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素以使用会议和约会。 
  
约会和会议可以是单个实例或[定期系列](recurrence-patterns-and-ews.md)，一部分但约会不包括与会者、 聊天室或资源，因为它们不需要发送一条消息。
  
会议包括发送和响应请求和更新，因为它们涉及多个只需访问日历文件夹中的项目。 它们还具有关联的工作流。 当与会者可用，并且还会涉及预留会议室，或资源如投影仪或其他设备必须安排会议。
  
会议工作流通常包括以下步骤：
  
1. 创建会议并将其填充开始和结束时间、 位置和邮件正文等信息。
    
2. 创建的潜在与会者、 资源和会议室列表。
    
3. 检查与会者的可用性状态。 
    
4. 会议请求发送给与会者。
    
5. 与会者的答复其目的参加会议的会议。 与会者可能还建议会议的新时间。
    
6. 会议可以取消此事件或更新，这通常会触发新邮件发送给与会者。
    
## <a name="calendars-and-time"></a>日历和时间
<a name="bk_Time"> </a>

或缺日历时间相关功能。 约会和会议已开始和结束时间、 持续时间，以及其他与时间有关的属性，如频率一条消息是创建、 发送和接收的时间。 可以从基于开始和结束时间的日历文件夹中检索现有约会和会议。 定期系列有起始和结束。 会议中给定时区，即在全球经济越来越重要发生。
  
时间内部存储在 Exchange 服务器以协调世界时 (UTC) 上。 Exchange 将其转换为基于客户端设置本地时区。 [DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)属性范围限定到计算机的本地时区。 
  
## <a name="recurring-series"></a>定期系列
<a name="bk_recurrence"> </a>

一系列定期约会或会议组成定期主控形状、 匹配项，一套和 （可选） 的一组例外项。 重复信息存储在定期主项目。 [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS 元素是与出现系列的例外关联，或者您可以使用[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/dd635978%28v=EXCHG.80%29.aspx) EWS 托管 API 方法以获取定期主控形状。 使用的一系列实例，您可以找到的元素和系列相关联的信息。 
  
请注意，定期属性存在于上的所有日历项目，但他们会仅在定期主项目上填充。 除了系列中所有匹配项的索引，定期主具有修改和删除匹配项和一系列定期模式参考 （例如、 每日、 每周、 每月或年）。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [使用 Exchange 2013 中的 EWS 中创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 EWS 在 Exchange 中创建全天事件](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [删除约会，并在 Exchange 使用 EWS 取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [要在 Exchange 使用 EWS 获取会议室列表](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [要在 Exchange 使用 EWS 获取忙/闲信息](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [建议在 Exchange 使用 EWS 的新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [在 Exchange 处理批次中的日历项目](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

