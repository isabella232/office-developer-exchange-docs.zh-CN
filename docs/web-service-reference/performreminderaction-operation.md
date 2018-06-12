---
title: PerformReminderAction 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: 查找信息 PerformReminderAction EWS 操作。
ms.openlocfilehash: 778fbb508413721f58cfcf9143a5296874e6cd1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826722"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="327df-103">PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="327df-103">PerformReminderAction operation</span></span>

<span data-ttu-id="327df-104">查找有关**PerformReminderAction** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="327df-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="327df-105">**PerformReminderAction** Exchange Web Services (EWS) 操作启动提醒上的消除或暂停操作。</span><span class="sxs-lookup"><span data-stu-id="327df-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="327df-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="327df-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="327df-107">使用 PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="327df-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="327df-108">您可以使用**PerformReminderAction**操作关闭或 snooze （延迟） 提醒[GetReminders](getreminders-operation.md)操作返回。</span><span class="sxs-lookup"><span data-stu-id="327df-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="327df-109">Snooze 提醒、 设置为**Snooze**， [ActionType](actiontype-reminderactiontype.md)和[NewReminderTime](newremindertime.md)将值设置为时间晚于当前[ReminderTime](remindertime.md)，否则**NewReminderTime** ，则忽略该服务器。</span><span class="sxs-lookup"><span data-stu-id="327df-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="327df-110">如果提醒为的定期会议，并且与以前的下一个匹配项提醒是**NewReminderTime**提醒采取**Snooze**操作，有效地消除的提醒。</span><span class="sxs-lookup"><span data-stu-id="327df-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="327df-111">若要消除提醒， **Dismiss**到设置**ActionType** 。</span><span class="sxs-lookup"><span data-stu-id="327df-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="327df-112">在服务器处理请求，服务器将项目的[IsReminderSet](isreminderset.md)值从**True**更改为**False**。</span><span class="sxs-lookup"><span data-stu-id="327df-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="327df-113">PerformReminderAction 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="327df-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="327df-114">**PerformReminderAction**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="327df-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="327df-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="327df-115">**Header name**</span></span>|<span data-ttu-id="327df-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="327df-116">**Element**</span></span>|<span data-ttu-id="327df-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="327df-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="327df-118">**模拟**</span><span class="sxs-lookup"><span data-stu-id="327df-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="327df-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="327df-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="327df-120">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="327df-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="327df-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="327df-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="327df-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="327df-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="327df-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="327df-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="327df-124">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="327df-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="327df-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="327df-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="327df-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="327df-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="327df-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="327df-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="327df-128">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="327df-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="327df-129">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="327df-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="327df-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="327df-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="327df-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="327df-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="327df-132">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="327df-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="327df-133">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="327df-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="327df-134">PerformReminderAction 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="327df-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="327df-135">**PerformReminderAction**操作请求的下面的示例演示如何 snooze 当前提醒和设置新的提醒时间。</span><span class="sxs-lookup"><span data-stu-id="327df-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="327df-136">请注意，您需要包含[ItemId](itemid.md) **更改密钥**和**NewReminderTime**必须设置为高于**ReminderTime** [GetReminders](getreminders-operation.md)操作返回的时间。</span><span class="sxs-lookup"><span data-stu-id="327df-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
> <span data-ttu-id="327df-137">已缩短**ItemId**值，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="327df-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="327df-138">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="327df-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="327df-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="327df-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="327df-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="327df-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="327df-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="327df-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="327df-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="327df-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="327df-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="327df-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="327df-144">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="327df-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="327df-145">成功 PerformReminderAction 操作响应</span><span class="sxs-lookup"><span data-stu-id="327df-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="327df-146">下面的示例演示对**PerformReminderAction**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="327df-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="327df-147">**UpdatedItemIds**元素包含的更新的日历项目**ItemIds** 。</span><span class="sxs-lookup"><span data-stu-id="327df-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="327df-148">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="327df-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="327df-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="327df-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="327df-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="327df-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="327df-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="327df-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="327df-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="327df-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="327df-153">PerformReminderAction 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="327df-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="327df-154">下面的示例演示**PerformReminderAction**操作请求的响应，当在服务器上没有更改。</span><span class="sxs-lookup"><span data-stu-id="327df-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="327df-155">这是在其中发送请求，但返回没有**UpdatedItemIds** ，这意味着没有提醒已更改的响应。</span><span class="sxs-lookup"><span data-stu-id="327df-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
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
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="327df-156">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="327df-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="327df-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="327df-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="327df-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="327df-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="327df-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="327df-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="327df-160">是通用的 EWS 的额外的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="327df-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="327df-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="327df-161">See also</span></span>


- [<span data-ttu-id="327df-162">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="327df-162">GetReminders operation</span></span>](getreminders-operation.md)
    

