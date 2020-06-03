---
title: Calendars and EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: 了解 Exchange 中的日历、日历文件夹和项目、约会和会议。
localization_priority: Priority
ms.openlocfilehash: 3312ebb4deeb6645ccd7048564d61c3db5ea4b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456197"
---
# <a name="calendars-and-ews-in-exchange"></a>Calendars and EWS in Exchange

了解 Exchange 中的日历、日历文件夹和项目、约会和会议。
  
您可能已经熟悉电子邮件客户端（如 Outlook）中的许多日历功能，这使您能够跟踪约会、安排会议、检查人员的可用性、邀请与会者以及更改或取消会议。
  
Exchange 中日历相关的功能与在客户端（如 Outlook）中看到的功能稍有不同。 通过 Exchange 中的 EWS，可以执行创建、存储、发送或更改信息等操作，而不是显示信息。 若要使用 EWS 处理日历，您需要熟悉诸如信息存储、时间、定期和邮件流等概念。 更具体地说，您需要熟悉以下内容：
  
- 日历文件夹、日历项目和日历视图
    
- 会议请求、响应、日程安排、与会者、资源、会议室和可用性
    
- 会议和约会的持续时间、时区以及开始和结束时间
    
- 定期系列、定期模式、异常和单个实例约会和会议
    
幸运的是，EWS 和 EWS 托管 API 提供了一组丰富的操作和方法，使您能够执行大量与日历相关的任务。 例如，使用 EWS 托管 API，您可以创建会议并只向与会者发送邀请，只需几行代码，如下面的示例所示。
  
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

"日历" 文件夹包含日历项目。 "日历" 文件夹的[folder 类](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)为**IPF。约会**，并且可以仅包括由[ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS 托管 API 属性（与[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或 EWS [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素相关联）定义的项目。 
  
"日历" 文件夹中的项目与邮箱中的其他文件夹中的项目略有不同，因为定期系列中的事件和定期系列的例外不是邮箱中的实际项目，而是作为定期母版的附件在内部存储。 因此，为了检索给定日期范围内的所有约会，您需要使用日历视图。 若要了解有关检索约会和日历视图的详细信息，请参阅[使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="meetings-and-appointments"></a>会议和约会
<a name="bk_meetings"> </a>

会议和约会之间的基本区别在于会议具有与会者，而约会则不是。 在内部，Exchange 对会议和约会使用相同的对象。 您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素来处理会议和约会。 
  
约会和会议既可以是单个实例，也可以是[定期系列](recurrence-patterns-and-ews.md)的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。
  
由于会议包括发送和响应请求和更新，因此他们不仅仅涉及访问 "日历" 文件夹中的项目。 它们还具有关联的工作流。 会议必须在与会者可用时安排日程，还可以涉及保留会议室或诸如投影仪或其他设备等资源。
  
会议工作流通常涉及以下步骤：
  
1. 创建一个会议并使用诸如开始和结束时间、位置和邮件正文的信息填充。
    
2. 将创建一个预期的与会者、资源和聊天室的列表。
    
3. 检查与会者的可用性状态。 
    
4. 向与会者发送会议请求。
    
5. 与会者回复会议时，他们想要参加会议。 与会者还可能为会议建议新时间。
    
6. 可以取消或更新会议，这通常会触发要发送给与会者的新邮件。
    
## <a name="calendars-and-time"></a>日历和时间
<a name="bk_Time"> </a>

与时间相关的功能是日历不可或缺的。 约会和会议具有开始和结束时间、持续时间和其他与时间相关的属性，例如创建、发送和接收邮件的时间。 可以基于开始时间和结束时间从 "日历" 文件夹中检索现有约会和会议。 定期系列具有开头和结尾。 和会议在给定时区内发生，这在全球经济中越来越重要。
  
时间以协调世界时（UTC）的形式存储在 Exchange 服务器内部。 Exchange 将根据客户端设置将它们转换为本地时区。 [DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)属性的作用范围限定为计算机的本地时区。 
  
## <a name="recurring-series"></a>定期系列
<a name="bk_recurrence"> </a>

定期的约会或会议系列由一个定期的主控形状、一组发生项以及一组异常项组成。 定期信息存储在定期主项目上。 [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) ews 元素与系列中的匹配项和异常相关联，也可以使用[BINDTORECURRINGMASTER](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) EWS 托管 API 方法来获取定期母版。 使用系列的实例，可以查找与系列关联的所有元素和信息。 
  
请注意，所有日历项目上都存在定期属性，但它们只是在定期的主项目上进行填充。 除了一个系列中的所有匹配项的索引，该定期主控形状具有对修改和删除的匹配项以及系列的定期模式（例如，每天、每周、每月或每年）的引用。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 Exchange 中的 EWS 创建全天事件](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取会议室列表](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取忙/闲信息](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [在 Exchange 中批量处理日历项目](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

