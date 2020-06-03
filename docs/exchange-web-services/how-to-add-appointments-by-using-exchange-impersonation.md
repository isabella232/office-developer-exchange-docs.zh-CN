---
title: 使用 Exchange 模拟添加约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: 了解如何将模拟与 Exchange 中的 EWS 托管 API 或 EWS 结合使用，以向用户的日历中添加约会。
localization_priority: Priority
ms.openlocfilehash: b1473d72113f8cc07d05364a4d87fedf23c7351d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455329"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a>使用 Exchange 模拟添加约会

了解如何将模拟与 Exchange 中的 EWS 托管 API 或 EWS 结合使用，以向用户的日历中添加约会。
  
您可以创建一个服务应用程序，通过使用已启用**ApplicationImpersonation** [角色](how-to-configure-impersonation.md)的服务帐户，将约会直接插入到 Exchange 日历中。 使用模拟时，应用程序将充当用户;就像用户使用客户端（如 Outlook）将约会添加到日历一样。 
  
使用模拟时，请记住以下几点：
  
- 您的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)对象必须绑定到服务帐户。 您可以使用相同的**ExchangeService**对象，通过更改要模拟的每个帐户的[ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性来模拟多个帐户。 
    
- 您保存到模拟帐户中的任何项目都只能使用一次。 例如，如果要在多个帐户中保存相同的约会，则必须为每个帐户创建一个[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx)对象。 
    
## <a name="prerequisites"></a>先决条件

您的应用程序需要一个帐户，用于连接到 Exchange 服务器，然后才能使用模拟。 建议您对已为其将访问的帐户授予应用程序模拟角色的应用程序使用服务帐户。 有关详细信息，请参阅[配置模拟](how-to-configure-impersonation.md)
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>通过在 EWS 托管 API 中使用模拟来添加约会

下面的示例将约会或会议添加到一个或多个 Exchange 帐户的日历中。 该方法采用三个参数。
  
-  _服务_—绑定到 Exchange 服务器上的服务应用程序帐户的**ExchangeService**对象。 
    
-  _emailAddresses_ —包含 SMTP 电子邮件地址字符串列表的[system.object](https://msdn.microsoft.com/library/6sh2ey19.aspx)对象。 
    
-  _factory_ —实现**IAppointmentFactory**接口的对象。 此接口有一个方法， **GetAppointment** ，该方法将**ExchangeService**对象作为参数，并返回一个**约会**对象。 **IAppointmentFactory**接口定义[IAppointmentFactory 接口](#bk_IAppointmentFactory)。
    
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

保存约会时，代码会进行检查以确定是否有任何与会者已添加到[RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx)属性中。 如果有，则使用[SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用[Save](https://msdn.microsoft.com/library/dd635394.aspx)方法，以便与会者接收会议请求;否则，使用[SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用**Save**方法，以便将约会保存到模拟用户的日历中，并将[IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx)属性设置为**false**。
  
### <a name="iappointmentfactory-interface"></a>IAppointmentFactory 接口
<a name="bk_IAppointmentFactory"> </a>

由于每次您需要在模拟用户的日历上保存约会时都需要一个新的**约会**对象，因此**IAppointmentFactory**接口会对用于填充每个**约会**对象的对象进行抽象化。 此版本是一个简单的接口，它只包含一个方法**GetAppointment**，该方法将**ExchangeService**对象作为参数，并返回绑定到该**ExchangeService**对象的新的**约会**对象。 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

下面的**AppointmentFactory**类示例显示了**IAppointmentFactory**接口的实现，该接口返回从现在起三天内发生的简单约会。 如果取消注释 `appointment.RequiredAttendees.Add` 该行， **GetAppointment**方法将返回一个会议，并且该行中指定的电子邮件地址将接收一个会议请求，并将被列为组织的模拟用户。 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a>通过使用模拟和 EWS 添加约会

EWS 使您的应用程序可以使用模拟来代表日历的所有者将项目添加到日历中。 本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作将约会添加到模拟帐户的日历中。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

请注意，除了在 SOAP 头中添加**ExchangeImpersonation**元素以指定我们模拟的帐户之外，这也是用于创建约会而不使用模拟的相同 XML 请求。 
  
下面的示例演示由**CreateItem**操作返回的响应 XML。 
  
> [!NOTE]
> 为提高可读性，将缩短**ItemId**和**ChangeKey**属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

同样，当您在不使用模拟的情况下使用**CreateItem**操作时，将返回相同的 XML。 
  
## <a name="see-also"></a>另请参阅


- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [ApplicationImpersonation 角色](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [配置模拟](how-to-configure-impersonation.md)
    
- [确定要模拟的帐户](how-to-identify-the-account-to-impersonate.md)
    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [CreateItem 操作（日历项目）](../web-service-reference/createitem-operation-calendar-item.md)
    
- [ExchangeService 属性](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

