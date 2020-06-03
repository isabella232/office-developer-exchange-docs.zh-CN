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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462288"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="9a316-103">PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="9a316-103">PerformReminderAction operation</span></span>

<span data-ttu-id="9a316-104">查找有关**PerformReminderAction** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="9a316-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="9a316-105">**PerformReminderAction** Exchange Web 服务（EWS）操作对提醒启动取消或推迟操作。</span><span class="sxs-lookup"><span data-stu-id="9a316-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="9a316-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="9a316-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="9a316-107">使用 PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="9a316-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="9a316-108">您可以使用**PerformReminderAction**操作消除或推迟（延迟） [GetReminders](getreminders-operation.md)操作返回的提醒。</span><span class="sxs-lookup"><span data-stu-id="9a316-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="9a316-109">若要暂停提醒，请将[ActionType](actiontype-reminderactiontype.md)设置为 "**暂停**"，并将 " [NewReminderTime](newremindertime.md) " 值设置为晚于当前[ReminderTime](remindertime.md)的时间，否则服务器将忽略**NewReminderTime** 。</span><span class="sxs-lookup"><span data-stu-id="9a316-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="9a316-110">如果提醒针对的是定期会议，并且在提醒中对该提醒执行了**暂停**操作，而该提醒的**NewReminderTime**已超过了下一次出现的提醒，则将有效地消除提醒。</span><span class="sxs-lookup"><span data-stu-id="9a316-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="9a316-111">若要消除提醒，请将**ActionType**设置为 "**消除**"。</span><span class="sxs-lookup"><span data-stu-id="9a316-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="9a316-112">当服务器处理请求时，服务器会将项目的[IsReminderSet](isreminderset.md)值从**True**更改为**False**。</span><span class="sxs-lookup"><span data-stu-id="9a316-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="9a316-113">PerformReminderAction 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="9a316-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="9a316-114">**PerformReminderAction**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="9a316-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="9a316-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="9a316-115">**Header name**</span></span>|<span data-ttu-id="9a316-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9a316-116">**Element**</span></span>|<span data-ttu-id="9a316-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9a316-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a316-118">**模拟**</span><span class="sxs-lookup"><span data-stu-id="9a316-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="9a316-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="9a316-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="9a316-120">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="9a316-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="9a316-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="9a316-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9a316-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="9a316-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="9a316-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="9a316-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="9a316-124">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="9a316-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="9a316-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="9a316-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9a316-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="9a316-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="9a316-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9a316-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9a316-128">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="9a316-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="9a316-129">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="9a316-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9a316-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="9a316-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="9a316-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9a316-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9a316-132">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="9a316-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="9a316-133">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="9a316-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="9a316-134">PerformReminderAction 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="9a316-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="9a316-135">以下示例的**PerformReminderAction**操作请求显示如何推迟当前提醒并设置新的提醒时间。</span><span class="sxs-lookup"><span data-stu-id="9a316-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="9a316-136">请注意，您需要包含[ItemId](itemid.md)的**ChangeKey** ，并且**NewReminderTime**必须设置为晚于[GetReminders](getreminders-operation.md)操作返回的**ReminderTime**的时间。</span><span class="sxs-lookup"><span data-stu-id="9a316-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
> <span data-ttu-id="9a316-137">为了保持可读性， **ItemId**值已缩短。</span><span class="sxs-lookup"><span data-stu-id="9a316-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="9a316-138">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9a316-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9a316-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="9a316-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="9a316-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="9a316-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="9a316-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="9a316-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="9a316-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="9a316-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="9a316-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="9a316-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="9a316-144">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="9a316-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="9a316-145">成功的 PerformReminderAction 操作响应</span><span class="sxs-lookup"><span data-stu-id="9a316-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="9a316-146">下面的示例演示对**PerformReminderAction**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="9a316-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="9a316-147">**UpdatedItemIds**元素包含更新的日历项目的**ItemIds** 。</span><span class="sxs-lookup"><span data-stu-id="9a316-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
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

<span data-ttu-id="9a316-148">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9a316-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9a316-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="9a316-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="9a316-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9a316-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9a316-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="9a316-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="9a316-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="9a316-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="9a316-153">PerformReminderAction 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="9a316-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="9a316-154">下面的示例演示在服务器上未进行任何更改时对**PerformReminderAction**操作请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9a316-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="9a316-155">这是发送请求的响应，但未返回任何**UpdatedItemIds** ，这意味着未更改任何提醒。</span><span class="sxs-lookup"><span data-stu-id="9a316-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
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

<span data-ttu-id="9a316-156">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9a316-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9a316-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="9a316-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="9a316-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9a316-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9a316-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="9a316-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="9a316-160">有关对 EWS 通用的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="9a316-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a316-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a316-161">See also</span></span>


- [<span data-ttu-id="9a316-162">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="9a316-162">GetReminders operation</span></span>](getreminders-operation.md)
    

