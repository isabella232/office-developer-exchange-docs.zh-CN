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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754669"
---
# <a name="getreminders-operation"></a><span data-ttu-id="26e16-103">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="26e16-103">GetReminders operation</span></span>

<span data-ttu-id="26e16-104">查找有关**GetReminders** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="26e16-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="26e16-105">**GetReminders** Exchange Web Services (EWS) 操作中检索日历和任务的项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="26e16-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="26e16-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="26e16-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="26e16-107">使用 GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="26e16-107">Using the GetReminders operation</span></span>

<span data-ttu-id="26e16-108">**GetReminders**操作当前和将来的日历和任务项目的提醒获取用户的邮箱，具体取决于请求中传递的元素值中。</span><span class="sxs-lookup"><span data-stu-id="26e16-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="26e16-109">操作可以检索所有当前和将来的日历项目以及设置的提醒的任务。</span><span class="sxs-lookup"><span data-stu-id="26e16-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="26e16-110">个人日历项目都包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="26e16-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="26e16-111">无提醒任务不包含在响应，也不与提醒的电子邮件或后续标志。</span><span class="sxs-lookup"><span data-stu-id="26e16-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="26e16-112">若要检索所有当前提醒，我们建议设置到**所有** [ReminderType](remindertype.md)和[EndTime](endtime-remindermessagedatatype.md)到当前时间。</span><span class="sxs-lookup"><span data-stu-id="26e16-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="26e16-113">如果[BeginTime](begintime.md)和**EndTime**元素都包含在请求中，响应包括任何日历提醒和之间发生的任务项目已发生之间的**BeginTime**和**结束时间**的提醒。</span><span class="sxs-lookup"><span data-stu-id="26e16-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="26e16-114">包含**BeginTime**和**EndTime**元素时下, 表介绍**ReminderType**元素的行为。</span><span class="sxs-lookup"><span data-stu-id="26e16-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="26e16-115">ReminderType * * 元素值 * *</span><span class="sxs-lookup"><span data-stu-id="26e16-115">****ReminderType** element value**</span></span>|<span data-ttu-id="26e16-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="26e16-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26e16-117">所有</span><span class="sxs-lookup"><span data-stu-id="26e16-117">All</span></span>  <br/> |<span data-ttu-id="26e16-118">**BeginTime**和**EndTime**之间发生的提醒。</span><span class="sxs-lookup"><span data-stu-id="26e16-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="26e16-119">当前</span><span class="sxs-lookup"><span data-stu-id="26e16-119">Current</span></span>  <br/> |<span data-ttu-id="26e16-120">返回**所有**，提醒加上提醒的早于请求的时间窗口是否仍正在进行，了事件以及无论期限的所有约会。</span><span class="sxs-lookup"><span data-stu-id="26e16-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="26e16-121">旧</span><span class="sxs-lookup"><span data-stu-id="26e16-121">Old</span></span>  <br/> |<span data-ttu-id="26e16-122">返回**所有**，减去尚未完成，减去所有约会的事件的提醒。</span><span class="sxs-lookup"><span data-stu-id="26e16-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="26e16-123">必须将**BeginTime**和**EndTime**元素设置为使用**旧**值。</span><span class="sxs-lookup"><span data-stu-id="26e16-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="26e16-124">GetReminders 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="26e16-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="26e16-125">**GetReminders**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="26e16-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="26e16-126">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="26e16-126">**Header name**</span></span>|<span data-ttu-id="26e16-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="26e16-127">**Element**</span></span>|<span data-ttu-id="26e16-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="26e16-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26e16-129">**模拟**</span><span class="sxs-lookup"><span data-stu-id="26e16-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="26e16-130">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="26e16-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="26e16-131">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="26e16-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="26e16-132">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="26e16-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="26e16-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="26e16-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="26e16-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="26e16-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="26e16-135">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="26e16-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="26e16-136">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="26e16-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="26e16-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="26e16-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="26e16-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="26e16-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="26e16-139">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="26e16-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="26e16-140">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="26e16-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="26e16-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="26e16-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="26e16-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="26e16-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="26e16-143">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="26e16-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="26e16-144">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="26e16-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="26e16-145">GetReminders 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="26e16-145">GetReminders operation request example</span></span>

<span data-ttu-id="26e16-146">**GetReminders**操作请求的下面的示例演示如何检索**BeginTime**和**EndTime**之间发生的第五个日历项目。</span><span class="sxs-lookup"><span data-stu-id="26e16-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
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

<span data-ttu-id="26e16-147">示例请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="26e16-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="26e16-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="26e16-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="26e16-149">结束时间</span><span class="sxs-lookup"><span data-stu-id="26e16-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="26e16-150">ReminderType</span><span class="sxs-lookup"><span data-stu-id="26e16-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="26e16-151">SOAP 正文还可以包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="26e16-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="26e16-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="26e16-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="26e16-153">MaxItems</span><span class="sxs-lookup"><span data-stu-id="26e16-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="26e16-154">成功 GetReminders 操作响应</span><span class="sxs-lookup"><span data-stu-id="26e16-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="26e16-155">下面的示例演示对**GetReminders**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="26e16-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="26e16-156">则响应中包含"团队会议"日历项目的提醒和提醒"任务发送会议笔记"任务。</span><span class="sxs-lookup"><span data-stu-id="26e16-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26e16-157">标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="26e16-157">Identifiers have been shortened to preserve readability.</span></span> 
  
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

<span data-ttu-id="26e16-158">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="26e16-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="26e16-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="26e16-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="26e16-160">Reminders</span><span class="sxs-lookup"><span data-stu-id="26e16-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="26e16-161">提醒</span><span class="sxs-lookup"><span data-stu-id="26e16-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="26e16-162">Subject</span><span class="sxs-lookup"><span data-stu-id="26e16-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="26e16-163">位置</span><span class="sxs-lookup"><span data-stu-id="26e16-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="26e16-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="26e16-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="26e16-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="26e16-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="26e16-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="26e16-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="26e16-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="26e16-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="26e16-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="26e16-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="26e16-169">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="26e16-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="26e16-170">UID</span><span class="sxs-lookup"><span data-stu-id="26e16-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="26e16-171">GetReminders 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="26e16-171">GetReminders operation error response example</span></span>

<span data-ttu-id="26e16-172">下面的示例演示对**GetReminders**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="26e16-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="26e16-173">这是对在其中的结束日期已早于开始日期的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="26e16-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
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

<span data-ttu-id="26e16-174">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="26e16-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="26e16-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="26e16-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="26e16-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="26e16-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="26e16-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="26e16-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="26e16-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="26e16-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="26e16-179">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="26e16-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26e16-180">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26e16-180">See also</span></span>


- [<span data-ttu-id="26e16-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="26e16-181">PerformReminderAction</span></span>](performreminderaction.md)
    

