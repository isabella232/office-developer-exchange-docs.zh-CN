---
title: 使用 Exchange 模拟添加约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: 了解如何使用模拟 EWS 的 EWS 托管 API 在 Exchange 将约会添加到用户的日历。
ms.openlocfilehash: fe737658b88aca66d8b4c2860245db000888ba17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752765"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a>使用 Exchange 模拟添加约会

了解如何使用模拟 EWS 的 EWS 托管 API 在 Exchange 将约会添加到用户的日历。
  
您可以创建的服务应用程序将直接插入 Exchange 日历约会，使用具有**AppplicationImpersonation**[启用角色](how-to-configure-impersonation.md)的服务帐户。 使用模拟时，将应用程序充当用户;是，如果用户使用如 Outlook 客户端到日历添加约会。 
  
当您使用模拟时，请记住以下原则：
  
- [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)对象必须绑定到的服务帐户。 同一**ExchangeService**对象可用于通过更改您想要模拟的每个帐户的[ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性模拟多个帐户。 
    
- 您将保存到模拟的帐户的任何项目仅使用一次。 如果您想要保存多个帐户相同的约会，例如，必须创建每个帐户[约会](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx)对象。 
    
## <a name="prerequisites"></a>先决条件

您的应用程序需要用于连接到 Exchange 服务器才能使用模拟的帐户。 我们建议您的应用程序授予它将访问的帐户的应用程序模拟角色使用的服务帐户。 有关详细信息，请参阅[Configure 模拟](how-to-configure-impersonation.md)
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>将约会添加模拟使用 EWS 托管 API

下面的示例将约会或会议添加到一个或多个 Exchange 帐户的日历。 该方法采用三个参数。
  
-  _服务_— **ExchangeService**对象的 Exchange 服务器上绑定到服务应用程序的帐户。 
    
-  _emailAddresses_ — 一个[System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx)对象，该对象包含列表的 SMTP 电子邮件地址的字符串。 
    
-  _中心_— 实现**IAppointmentFactory**接口的对象。 此接口具有一种方法， **GetAppointment**采用**ExchangeService**对象作为参数并返回**约会**对象。 **IAppointmentFactory**接口定义[IAppointmentFactory 接口](#bk_IAppointmentFactory)。
    
```cs
private static void CreateAppointments(ExchangeService service, List<string> emailAddresses, IAppointmentFactory factory)
{
  // Loop through the list of email addresses to add the appointment.
  foreach (var emailAddress in emailAddresses)
  {
    Console.WriteLine(string.Format("  Placing appointment in calendar for {0}.", emailAddress));
    // Set the email address of the account to get the appointment.
    service.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, emailAddress);
    // Get the appointment to add.
    Appointment appointment = factory.GetAppointment(service);
    // Save the appointment.
    try
    {
      if (appointment.RequiredAttendees.Count > 0)
      {
        // The appointment has attendees so send them the meeting request.
        appointment.Save(SendInvitationsMode.SendToAllAndSaveCopy);
      }
      else
      {
        // The appointment does not have attendees, so just save to calendar.
        appointment.Save(SendInvitationsMode.SendToNone);
      }
    }
    catch (ServiceResponseException ex)
    {
      Console.WriteLine(string.Format("Could not create appointment for {0}", emailAddress));
      Console.WriteLine(ex.Message);
    }
  }
}
```

将保存约会时，该代码将检查以确定是否已添加的任何与会者到[RequiredAttendees](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx)属性。 如果拥有，以便与会者接收会议要求; 使用[SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用[Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx)方法否则， **Appointment.Save**方法调用[SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值，以便将约会保存到模拟的用户的日历[Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx)属性设置为**false**。
  
### <a name="iappointmentfactory-interface"></a>IAppointmentFactory 接口
<a name="bk_IAppointmentFactory"> </a>

因为您想要保存在模拟的用户的日历的约会每次需要新的**约会**对象， **IAppointmentFactory**界面使抽象化用于填充每个**约会**对象的对象。 此版本是一个简单的界面，只包含一个方法， **GetAppointment**，它采用**ExchangeService**对象作为参数并返回一个绑定到该**ExchangeService**对象的新**约会**对象。 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

下面的**AppointmentFactory**类示例演示返回一个简单的约会的**IAppointmentFactory**接口的实现从现在发生三天。 如果您取消注释`appointment.RequiredAttendees.Add`行，则**GetAppointment**方法将返回会议并指定是否在行将收到与模拟用户列为组织者的会议请求的电子邮件地址。 
  
```cs
class AppointmentFactory : IAppointmentFactory
{
  public Appointment GetAppointment(ExchangeService service)
  {
    // First create the appointment to add.
    Appointment appointment = new Appointment(service);
    // Set the properties on the appointment.
    appointment.Subject = "Tennis lesson";
    appointment.Body = "Focus on backhand this week.";
    appointment.Start = DateTime.Now.AddDays(3);
    appointment.End = appointment.Start.AddHours(1);
    appointment.Location = "Tennis club";
    // appointment.RequiredAttendees.Add(new Attendee("sonyaf@contoso1000.onmicrosoft.com"));
    return appointment;
  }
}

```

## <a name="add-appointments-by-using-impersonation-with-ews"></a>通过使用 EWS 模拟添加约会

EWS 允许您应用程序使用模拟将项目添加到代表日历的日历所有者。 本示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作添加模拟的帐户的日历约会。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

请注意， **ExchangeImpersonation**元素中指定的帐户，我们模拟的 SOAP 标头的增加之外，这是用来创建约会，无需使用模拟了相同的 XML 请求。 
  
下面的示例显示了响应由**CreateItem**操作返回的 XML。 
  
> [!NOTE]
> 为便于阅读缩短**ItemId**和**更改密钥**属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

同样，这是您使用**CreateItem** operation，而使用模拟时返回相同的 XML。 
  
## <a name="see-also"></a>另请参阅


- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [ApplicationImpersonation 角色](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)
    
- [配置模拟](how-to-configure-impersonation.md)
    
- [确定要模拟的帐户](how-to-identify-the-account-to-impersonate.md)
    
- [使用 Exchange 2013 中的 EWS 中创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [CreateItem operation，（日历项）](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)
    
- [ExchangeService.ImpersonatedUserId 属性](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx.aspx)
    

