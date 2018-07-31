---
title: 使用 Exchange 模拟添加约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: 了解如何使用模拟 EWS 的 EWS 托管 API 在 Exchange 将约会添加到用户的日历。
ms.openlocfilehash: ab10a7d65a5603a84e12d918dd54198927d88b8a
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353453"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a><span data-ttu-id="c9c6d-103">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="c9c6d-103">Add appointments by using Exchange impersonation</span></span>

<span data-ttu-id="c9c6d-104">了解如何使用模拟 EWS 的 EWS 托管 API 在 Exchange 将约会添加到用户的日历。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-104">Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.</span></span>
  
<span data-ttu-id="c9c6d-105">您可以创建的服务应用程序将直接插入 Exchange 日历约会，使用具有**AppplicationImpersonation**[启用角色](how-to-configure-impersonation.md)的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-105">You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **AppplicationImpersonation**[role enabled](how-to-configure-impersonation.md).</span></span> <span data-ttu-id="c9c6d-106">使用模拟时，将应用程序充当用户;是，如果用户使用如 Outlook 客户端到日历添加约会。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-106">When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.</span></span> 
  
<span data-ttu-id="c9c6d-107">当您使用模拟时，请记住以下原则：</span><span class="sxs-lookup"><span data-stu-id="c9c6d-107">When you are using impersonation, keep in mind the following:</span></span>
  
- <span data-ttu-id="c9c6d-108">[ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)对象必须绑定到的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-108">Your [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account.</span></span> <span data-ttu-id="c9c6d-109">同一**ExchangeService**对象可用于通过更改您想要模拟的每个帐户的[ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)属性模拟多个帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-109">You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.</span></span> 
    
- <span data-ttu-id="c9c6d-110">您将保存到模拟的帐户的任何项目仅使用一次。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-110">Any item that you save to an impersonated account can only be used once.</span></span> <span data-ttu-id="c9c6d-111">如果您想要保存多个帐户相同的约会，例如，必须创建每个帐户[约会](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-111">If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.</span></span> 
    
## <a name="prerequisites"></a><span data-ttu-id="c9c6d-112">先决条件</span><span class="sxs-lookup"><span data-stu-id="c9c6d-112">Prerequisites</span></span>

<span data-ttu-id="c9c6d-113">您的应用程序需要用于连接到 Exchange 服务器才能使用模拟的帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-113">Your application needs an account to use to connect to the Exchange server before it can use impersonation.</span></span> <span data-ttu-id="c9c6d-114">我们建议您的应用程序授予它将访问的帐户的应用程序模拟角色使用的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-114">We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing.</span></span> <span data-ttu-id="c9c6d-115">有关详细信息，请参阅[Configure 模拟](how-to-configure-impersonation.md)</span><span class="sxs-lookup"><span data-stu-id="c9c6d-115">For more information, see [Configure impersonation](how-to-configure-impersonation.md)</span></span>
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a><span data-ttu-id="c9c6d-116">将约会添加模拟使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="c9c6d-116">Add appointments by using impersonation with the EWS Managed API</span></span>

<span data-ttu-id="c9c6d-117">下面的示例将约会或会议添加到一个或多个 Exchange 帐户的日历。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-117">The following example adds an appointment or meeting to the calendar of one or more Exchange accounts.</span></span> <span data-ttu-id="c9c6d-118">该方法采用三个参数。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-118">The method takes three parameters.</span></span>
  
-  <span data-ttu-id="c9c6d-119">_服务_— **ExchangeService**对象的 Exchange 服务器上绑定到服务应用程序的帐户。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-119">_service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.</span></span> 
    
-  <span data-ttu-id="c9c6d-120">_emailAddresses_ — 一个[System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx)对象，该对象包含列表的 SMTP 电子邮件地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-120">_emailAddresses_ — A [System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.</span></span> 
    
-  <span data-ttu-id="c9c6d-121">_中心_— 实现**IAppointmentFactory**接口的对象。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-121">_factory_ — An object that implements the **IAppointmentFactory** interface.</span></span> <span data-ttu-id="c9c6d-122">此接口具有一种方法， **GetAppointment**采用**ExchangeService**对象作为参数并返回**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-122">This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object.</span></span> <span data-ttu-id="c9c6d-123">**IAppointmentFactory**接口定义[IAppointmentFactory 接口](#bk_IAppointmentFactory)。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-123">The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).</span></span>
    
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

<span data-ttu-id="c9c6d-124">将保存约会时，该代码将检查以确定是否已添加的任何与会者到[RequiredAttendees](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-124">When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property.</span></span> <span data-ttu-id="c9c6d-125">如果拥有，以便与会者接收会议要求; 使用[SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值调用[Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx)方法否则， **Appointment.Save**方法调用[SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx)枚举值，以便将约会保存到模拟的用户的日历[Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx)属性设置为**false**。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-125">If they have, the [Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.</span></span>
  
### <a name="iappointmentfactory-interface"></a><span data-ttu-id="c9c6d-126">IAppointmentFactory 接口</span><span class="sxs-lookup"><span data-stu-id="c9c6d-126">IAppointmentFactory interface</span></span>
<span data-ttu-id="c9c6d-127"><a name="bk_IAppointmentFactory"> </a></span><span class="sxs-lookup"><span data-stu-id="c9c6d-127"></span></span>

<span data-ttu-id="c9c6d-128">因为您想要保存在模拟的用户的日历的约会每次需要新的**约会**对象， **IAppointmentFactory**界面使抽象化用于填充每个**约会**对象的对象。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-128">Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object.</span></span> <span data-ttu-id="c9c6d-129">此版本是一个简单的界面，只包含一个方法， **GetAppointment**，它采用**ExchangeService**对象作为参数并返回一个绑定到该**ExchangeService**对象的新**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-129">This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.</span></span> 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

<span data-ttu-id="c9c6d-130">下面的**AppointmentFactory**类示例演示返回一个简单的约会的**IAppointmentFactory**接口的实现从现在发生三天。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-130">The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now.</span></span> <span data-ttu-id="c9c6d-131">如果您取消注释`appointment.RequiredAttendees.Add`行，则**GetAppointment**方法将返回会议并指定是否在行将收到与模拟用户列为组织者的会议请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-131">If you uncomment the  `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.</span></span> 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a><span data-ttu-id="c9c6d-132">通过使用 EWS 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="c9c6d-132">Add appointments by using impersonation with EWS</span></span>

<span data-ttu-id="c9c6d-133">EWS 允许您应用程序使用模拟将项目添加到代表日历的日历所有者。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-133">EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner.</span></span> <span data-ttu-id="c9c6d-134">本示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作添加模拟的帐户的日历约会。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-134">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.</span></span> 
  
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

<span data-ttu-id="c9c6d-135">请注意， **ExchangeImpersonation**元素中指定的帐户，我们模拟的 SOAP 标头的增加之外，这是用来创建约会，无需使用模拟了相同的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-135">Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.</span></span> 
  
<span data-ttu-id="c9c6d-136">下面的示例显示了响应由**CreateItem**操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-136">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c9c6d-137">为便于阅读缩短**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="c9c6d-138">同样，这是您使用**CreateItem** operation，而使用模拟时返回相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="c9c6d-138">Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9c6d-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9c6d-139">See also</span></span>


- [<span data-ttu-id="c9c6d-140">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c9c6d-140">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c9c6d-141">ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="c9c6d-141">ApplicationImpersonation role</span></span>](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="c9c6d-142">配置模拟</span><span class="sxs-lookup"><span data-stu-id="c9c6d-142">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="c9c6d-143">识别要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="c9c6d-143">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="c9c6d-144">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="c9c6d-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="c9c6d-145">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="c9c6d-145">CreateItem operation (calendar item)</span></span>](../web-service-reference/createitem-operation-calendar-item.md)
    
- [<span data-ttu-id="c9c6d-146">ExchangeService.ImpersonatedUserId 属性</span><span class="sxs-lookup"><span data-stu-id="c9c6d-146">ExchangeService.ImpersonatedUserId property</span></span>](https://docs.microsoft.com/en-us/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

