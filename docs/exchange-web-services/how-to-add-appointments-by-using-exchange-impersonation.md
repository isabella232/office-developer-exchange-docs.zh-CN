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
# <a name="add-appointments-by-using-exchange-impersonation"></a><span data-ttu-id="1afc6-103">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="1afc6-103">Add appointments by using Exchange impersonation</span></span>

<span data-ttu-id="1afc6-104">了解如何将模拟与 Exchange 中的 EWS 托管 API 或 EWS 结合使用，以向用户的日历中添加约会。</span><span class="sxs-lookup"><span data-stu-id="1afc6-104">Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.</span></span>
  
<span data-ttu-id="1afc6-105">您可以创建一个服务应用程序，通过使用已启用**ApplicationImpersonation** [角色](how-to-configure-impersonation.md)的服务帐户，将约会直接插入到 Exchange 日历中。</span><span class="sxs-lookup"><span data-stu-id="1afc6-105">You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **ApplicationImpersonation** [role enabled](how-to-configure-impersonation.md).</span></span> <span data-ttu-id="1afc6-106">使用模拟时，应用程序将充当用户;就像用户使用客户端（如 Outlook）将约会添加到日历一样。</span><span class="sxs-lookup"><span data-stu-id="1afc6-106">When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.</span></span> 
  
<span data-ttu-id="1afc6-107">使用模拟时，请记住以下几点：</span><span class="sxs-lookup"><span data-stu-id="1afc6-107">When you are using impersonation, keep in mind the following:</span></span>
  
- <span data-ttu-id="1afc6-108">您的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)对象必须绑定到服务帐户。</span><span class="sxs-lookup"><span data-stu-id="1afc6-108">Your [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account.</span></span> <span data-ttu-id="1afc6-109">您可以使用相同的**ExchangeService**对象，通过更改要模拟的每个帐户的[ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性来模拟多个帐户。</span><span class="sxs-lookup"><span data-stu-id="1afc6-109">You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.</span></span> 
    
- <span data-ttu-id="1afc6-110">您保存到模拟帐户中的任何项目都只能使用一次。</span><span class="sxs-lookup"><span data-stu-id="1afc6-110">Any item that you save to an impersonated account can only be used once.</span></span> <span data-ttu-id="1afc6-111">例如，如果要在多个帐户中保存相同的约会，则必须为每个帐户创建一个[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-111">If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.</span></span> 
    
## <a name="prerequisites"></a><span data-ttu-id="1afc6-112">先决条件</span><span class="sxs-lookup"><span data-stu-id="1afc6-112">Prerequisites</span></span>

<span data-ttu-id="1afc6-113">您的应用程序需要一个帐户，用于连接到 Exchange 服务器，然后才能使用模拟。</span><span class="sxs-lookup"><span data-stu-id="1afc6-113">Your application needs an account to use to connect to the Exchange server before it can use impersonation.</span></span> <span data-ttu-id="1afc6-114">建议您对已为其将访问的帐户授予应用程序模拟角色的应用程序使用服务帐户。</span><span class="sxs-lookup"><span data-stu-id="1afc6-114">We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing.</span></span> <span data-ttu-id="1afc6-115">有关详细信息，请参阅[配置模拟](how-to-configure-impersonation.md)</span><span class="sxs-lookup"><span data-stu-id="1afc6-115">For more information, see [Configure impersonation](how-to-configure-impersonation.md)</span></span>
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a><span data-ttu-id="1afc6-116">通过在 EWS 托管 API 中使用模拟来添加约会</span><span class="sxs-lookup"><span data-stu-id="1afc6-116">Add appointments by using impersonation with the EWS Managed API</span></span>

<span data-ttu-id="1afc6-117">下面的示例将约会或会议添加到一个或多个 Exchange 帐户的日历中。</span><span class="sxs-lookup"><span data-stu-id="1afc6-117">The following example adds an appointment or meeting to the calendar of one or more Exchange accounts.</span></span> <span data-ttu-id="1afc6-118">该方法采用三个参数。</span><span class="sxs-lookup"><span data-stu-id="1afc6-118">The method takes three parameters.</span></span>
  
-  <span data-ttu-id="1afc6-119">_服务_—绑定到 Exchange 服务器上的服务应用程序帐户的**ExchangeService**对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-119">_service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.</span></span> 
    
-  <span data-ttu-id="1afc6-120">_emailAddresses_ —包含 SMTP 电子邮件地址字符串列表的[system.object](https://msdn.microsoft.com/library/6sh2ey19.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-120">_emailAddresses_ — A [System.List](https://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.</span></span> 
    
-  <span data-ttu-id="1afc6-121">_factory_ —实现**IAppointmentFactory**接口的对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-121">_factory_ — An object that implements the **IAppointmentFactory** interface.</span></span> <span data-ttu-id="1afc6-122">此接口有一个方法， **GetAppointment** ，该方法将**ExchangeService**对象作为参数，并返回一个**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-122">This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object.</span></span> <span data-ttu-id="1afc6-123">**IAppointmentFactory**接口定义[IAppointmentFactory 接口](#bk_IAppointmentFactory)。</span><span class="sxs-lookup"><span data-stu-id="1afc6-123">The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).</span></span>
    
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

<span data-ttu-id="1afc6-124">保存约会时，代码会进行检查以确定是否有任何与会者已添加到[RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx)属性中。</span><span class="sxs-lookup"><span data-stu-id="1afc6-124">When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property.</span></span> <span data-ttu-id="1afc6-125">如果有，则使用[SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用[Save](https://msdn.microsoft.com/library/dd635394.aspx)方法，以便与会者接收会议请求;否则，使用[SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用**Save**方法，以便将约会保存到模拟用户的日历中，并将[IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx)属性设置为**false**。</span><span class="sxs-lookup"><span data-stu-id="1afc6-125">If they have, the [Appointment.Save](https://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.</span></span>
  
### <a name="iappointmentfactory-interface"></a><span data-ttu-id="1afc6-126">IAppointmentFactory 接口</span><span class="sxs-lookup"><span data-stu-id="1afc6-126">IAppointmentFactory interface</span></span>
<span data-ttu-id="1afc6-127"><a name="bk_IAppointmentFactory"> </a></span><span class="sxs-lookup"><span data-stu-id="1afc6-127"><a name="bk_IAppointmentFactory"> </a></span></span>

<span data-ttu-id="1afc6-128">由于每次您需要在模拟用户的日历上保存约会时都需要一个新的**约会**对象，因此**IAppointmentFactory**接口会对用于填充每个**约会**对象的对象进行抽象化。</span><span class="sxs-lookup"><span data-stu-id="1afc6-128">Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object.</span></span> <span data-ttu-id="1afc6-129">此版本是一个简单的接口，它只包含一个方法**GetAppointment**，该方法将**ExchangeService**对象作为参数，并返回绑定到该**ExchangeService**对象的新的**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="1afc6-129">This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.</span></span> 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

<span data-ttu-id="1afc6-130">下面的**AppointmentFactory**类示例显示了**IAppointmentFactory**接口的实现，该接口返回从现在起三天内发生的简单约会。</span><span class="sxs-lookup"><span data-stu-id="1afc6-130">The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now.</span></span> <span data-ttu-id="1afc6-131">如果取消注释 `appointment.RequiredAttendees.Add` 该行， **GetAppointment**方法将返回一个会议，并且该行中指定的电子邮件地址将接收一个会议请求，并将被列为组织的模拟用户。</span><span class="sxs-lookup"><span data-stu-id="1afc6-131">If you uncomment the  `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.</span></span> 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a><span data-ttu-id="1afc6-132">通过使用模拟和 EWS 添加约会</span><span class="sxs-lookup"><span data-stu-id="1afc6-132">Add appointments by using impersonation with EWS</span></span>

<span data-ttu-id="1afc6-133">EWS 使您的应用程序可以使用模拟来代表日历的所有者将项目添加到日历中。</span><span class="sxs-lookup"><span data-stu-id="1afc6-133">EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner.</span></span> <span data-ttu-id="1afc6-134">本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作将约会添加到模拟帐户的日历中。</span><span class="sxs-lookup"><span data-stu-id="1afc6-134">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.</span></span> 
  
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

<span data-ttu-id="1afc6-135">请注意，除了在 SOAP 头中添加**ExchangeImpersonation**元素以指定我们模拟的帐户之外，这也是用于创建约会而不使用模拟的相同 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="1afc6-135">Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.</span></span> 
  
<span data-ttu-id="1afc6-136">下面的示例演示由**CreateItem**操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="1afc6-136">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1afc6-137">为提高可读性，将缩短**ItemId**和**ChangeKey**属性。</span><span class="sxs-lookup"><span data-stu-id="1afc6-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="1afc6-138">同样，当您在不使用模拟的情况下使用**CreateItem**操作时，将返回相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="1afc6-138">Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1afc6-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1afc6-139">See also</span></span>


- [<span data-ttu-id="1afc6-140">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1afc6-140">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="1afc6-141">ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="1afc6-141">ApplicationImpersonation role</span></span>](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="1afc6-142">配置模拟</span><span class="sxs-lookup"><span data-stu-id="1afc6-142">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="1afc6-143">确定要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="1afc6-143">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="1afc6-144">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="1afc6-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="1afc6-145">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="1afc6-145">CreateItem operation (calendar item)</span></span>](../web-service-reference/createitem-operation-calendar-item.md)
    
- [<span data-ttu-id="1afc6-146">ExchangeService 属性</span><span class="sxs-lookup"><span data-stu-id="1afc6-146">ExchangeService.ImpersonatedUserId property</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

