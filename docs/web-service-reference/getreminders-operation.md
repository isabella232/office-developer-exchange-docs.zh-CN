---
title: GetReminders 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: 查找有关 GetReminders EWS 操作的信息。
ms.openlocfilehash: dcbe20c674d7524a7776d374fa6964899abf472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458304"
---
# <a name="getreminders-operation"></a><span data-ttu-id="e1e5a-103">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="e1e5a-103">GetReminders operation</span></span>

<span data-ttu-id="e1e5a-104">查找有关**GetReminders** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="e1e5a-105">**GetReminders** Exchange Web 服务（EWS）操作检索日历和任务项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="e1e5a-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="e1e5a-107">使用 GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="e1e5a-107">Using the GetReminders operation</span></span>

<span data-ttu-id="e1e5a-108">**GetReminders**操作将根据请求中传递的元素值，在用户的邮箱中获取当前和将来的日历和任务项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="e1e5a-109">该操作可以检索当前和将来的所有日历项目以及具有提醒集的任务。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="e1e5a-110">私有日历项目包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="e1e5a-111">没有提醒的任务不会包含在响应中，也不会包含提醒或后续标志的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="e1e5a-112">若要检索所有当前提醒，建议将[ReminderType](remindertype.md)设置为 "**所有**"，并将 "[结束](endtime-remindermessagedatatype.md)" 设置为 "当前时间"。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="e1e5a-113">如果请求中包含[BeginTime](begintime.md)和**EndTime**元素，则该响应包括在**BeginTime**和**EndTime**之间发生提醒之间发生的任何日历和任务项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="e1e5a-114">下表介绍了在包含**BeginTime**和**EndTime**元素时**ReminderType**元素的行为。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="e1e5a-115">ReminderType \* \* 元素值 \* \*</span><span class="sxs-lookup"><span data-stu-id="e1e5a-115">\*\*\*\*ReminderType\*\* element value\*\*</span></span>|<span data-ttu-id="e1e5a-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1e5a-117">所有</span><span class="sxs-lookup"><span data-stu-id="e1e5a-117">All</span></span>  <br/> |<span data-ttu-id="e1e5a-118">在**BeginTime**和**EndTime**之间发生的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="e1e5a-119">Current</span><span class="sxs-lookup"><span data-stu-id="e1e5a-119">Current</span></span>  <br/> |<span data-ttu-id="e1e5a-120">**全部**提醒，以及早于请求的时间窗口的提醒（如果事件仍在进行）以及所有约会（无论期限是什么）。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="e1e5a-121">Old</span><span class="sxs-lookup"><span data-stu-id="e1e5a-121">Old</span></span>  <br/> |<span data-ttu-id="e1e5a-122">除所有尚未完成的事件、减去所有约会之外的**全部**、负事件返回的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="e1e5a-123">必须将**BeginTime**和**EndTime**元素设置为使用**旧**值。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="e1e5a-124">GetReminders 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="e1e5a-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="e1e5a-125">**GetReminders**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e1e5a-126">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-126">**Header name**</span></span>|<span data-ttu-id="e1e5a-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-127">**Element**</span></span>|<span data-ttu-id="e1e5a-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1e5a-129">**模拟**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="e1e5a-130">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="e1e5a-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="e1e5a-131">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="e1e5a-132">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e1e5a-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="e1e5a-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="e1e5a-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="e1e5a-135">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="e1e5a-136">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e1e5a-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e1e5a-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e1e5a-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e1e5a-139">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e1e5a-140">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e1e5a-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e1e5a-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e1e5a-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e1e5a-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e1e5a-143">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e1e5a-144">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="e1e5a-145">GetReminders 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="e1e5a-145">GetReminders operation request example</span></span>

<span data-ttu-id="e1e5a-146">以下示例的**GetReminders**操作请求显示如何检索**BeginTime**和**EndTime**之间发生的前五个日历项目。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
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
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e1e5a-147">示例请求 SOAP body 包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1e5a-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1e5a-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="e1e5a-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="e1e5a-149">EndTime</span><span class="sxs-lookup"><span data-stu-id="e1e5a-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="e1e5a-150">ReminderType</span><span class="sxs-lookup"><span data-stu-id="e1e5a-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="e1e5a-151">SOAP 正文还可以包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1e5a-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="e1e5a-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="e1e5a-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="e1e5a-153">MaxItems</span><span class="sxs-lookup"><span data-stu-id="e1e5a-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="e1e5a-154">成功的 GetReminders 操作响应</span><span class="sxs-lookup"><span data-stu-id="e1e5a-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="e1e5a-155">下面的示例演示对**GetReminders**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="e1e5a-156">响应包含 "团队会议" 日历项目的提醒和 "任务以发送会议笔记" 任务的提醒。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1e5a-157">为了保持可读性，标识符已被缩短。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-157">Identifiers have been shortened to preserve readability.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e1e5a-158">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1e5a-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1e5a-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="e1e5a-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="e1e5a-160">提醒</span><span class="sxs-lookup"><span data-stu-id="e1e5a-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="e1e5a-161">提醒</span><span class="sxs-lookup"><span data-stu-id="e1e5a-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="e1e5a-162">主题</span><span class="sxs-lookup"><span data-stu-id="e1e5a-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="e1e5a-163">Location</span><span class="sxs-lookup"><span data-stu-id="e1e5a-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="e1e5a-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="e1e5a-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="e1e5a-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="e1e5a-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="e1e5a-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="e1e5a-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="e1e5a-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="e1e5a-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e1e5a-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="e1e5a-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="e1e5a-169">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="e1e5a-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="e1e5a-170">UID</span><span class="sxs-lookup"><span data-stu-id="e1e5a-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="e1e5a-171">GetReminders 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="e1e5a-171">GetReminders operation error response example</span></span>

<span data-ttu-id="e1e5a-172">下面的示例演示对**GetReminders**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="e1e5a-173">这是对结束日期早于开始日期的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e1e5a-174">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1e5a-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1e5a-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="e1e5a-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="e1e5a-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="e1e5a-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e1e5a-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e1e5a-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e1e5a-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e1e5a-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e1e5a-179">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="e1e5a-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1e5a-180">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1e5a-180">See also</span></span>


- [<span data-ttu-id="e1e5a-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="e1e5a-181">PerformReminderAction</span></span>](performreminderaction.md)
    

