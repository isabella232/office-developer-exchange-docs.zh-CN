---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: 查找信息 MarkAsJunk EWS 操作。
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826353"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="c2f42-103">MarkAsJunk Operation</span><span class="sxs-lookup"><span data-stu-id="c2f42-103">MarkAsJunk operation</span></span>

<span data-ttu-id="c2f42-104">查找有关**MarkAsJunk** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="c2f42-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="c2f42-105">**MarkAsJunk**操作添加和用户从列表中删除阻止的电子邮件并将电子邮件移动到垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="c2f42-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="c2f42-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="c2f42-107">使用 MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="c2f42-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="c2f42-108">**MarkAsJunk**操作包含两个布尔选项，以指示是否应将电子邮件发件人添加到阻止发件人列表以及是否应该将目标电子邮件移动到默认垃圾邮件文件夹或收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="c2f42-109">操作**IsJunk**和**MoveItem**属性的值由决定。</span><span class="sxs-lookup"><span data-stu-id="c2f42-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="c2f42-110">以下是可能的操作基于**IsJunk**和**MoveItem**属性的值组合：</span><span class="sxs-lookup"><span data-stu-id="c2f42-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="c2f42-111">如果**IsJunk**属性设置为**true**，并且**MoveItem**属性设置为**true**，则目标电子邮件的发件人添加到阻止发件人列表和电子邮件移动到垃圾 Dmail 文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="c2f42-112">如果**IsJunk**属性设置为**true**，并且**MoveItem**属性设置为**false**，目标电子邮件的发件人添加到阻止发件人列表和电子邮件也不会移动从文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="c2f42-113">如果**IsJunk**属性设置为**false**，且**MoveItem**属性设置为**true**，从阻止发件人列表中删除目标电子邮件 messageis 发件人和电子邮件移动到收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="c2f42-114">如果**IsJunk**属性设置为**false**，并且**MoveItem**属性设置为**false**，从阻止发件人列表中删除的目标电子邮件发件人和电子邮件也不会移动从文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="c2f42-115">阻止发件人列表的内容不从 EWS 可供搜索。</span><span class="sxs-lookup"><span data-stu-id="c2f42-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="c2f42-116">如果发件人添加到阻止发件人列表中，您需要保留一份阻止发件人发送将来取消阻止发件人的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c2f42-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="c2f42-117">MarkAsJunk 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="c2f42-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="c2f42-118">**MarkAsJunk**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c2f42-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c2f42-119">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="c2f42-119">**Header name**</span></span>|<span data-ttu-id="c2f42-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2f42-120">**Element**</span></span>|<span data-ttu-id="c2f42-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2f42-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c2f42-122">**模拟**</span><span class="sxs-lookup"><span data-stu-id="c2f42-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c2f42-123">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c2f42-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c2f42-124">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="c2f42-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c2f42-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="c2f42-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c2f42-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c2f42-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c2f42-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c2f42-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c2f42-128">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="c2f42-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c2f42-129">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="c2f42-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c2f42-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c2f42-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c2f42-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c2f42-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c2f42-132">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="c2f42-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c2f42-133">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="c2f42-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c2f42-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c2f42-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c2f42-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c2f42-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c2f42-136">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="c2f42-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c2f42-137">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="c2f42-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="c2f42-138">MarkAsJunk 操作请求示例： 将发件人添加到阻止发件人列表</span><span class="sxs-lookup"><span data-stu-id="c2f42-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="c2f42-139">**MarkAsJunk**操作请求的下面的示例演示如何将电子邮件发件人添加到阻止发件人列表并将电子邮件移动到垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="c2f42-140">**MarkAsJunk**操作接受标识用于引用添加到阻止发件人列表中的发件人的电子邮件的唯一电子邮件消息标识符。</span><span class="sxs-lookup"><span data-stu-id="c2f42-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c2f42-141">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c2f42-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="c2f42-142">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c2f42-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c2f42-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="c2f42-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="c2f42-144">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c2f42-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="c2f42-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="c2f42-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="c2f42-146">成功 MarkAsJunk 操作响应</span><span class="sxs-lookup"><span data-stu-id="c2f42-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="c2f42-147">下面的示例演示对**MarkAsJunk**操作请求将发件人添加到阻止发件人列表并将电子邮件移动到垃圾邮件文件夹的成功响应。</span><span class="sxs-lookup"><span data-stu-id="c2f42-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

<span data-ttu-id="c2f42-148">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c2f42-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c2f42-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="c2f42-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="c2f42-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2f42-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c2f42-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2f42-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="c2f42-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c2f42-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c2f42-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="c2f42-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="c2f42-154">MarkAsJunk 操作请求示例： 从阻止发件人列表中删除发件人</span><span class="sxs-lookup"><span data-stu-id="c2f42-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="c2f42-155">**MarkAsJunk**操作请求的下面的示例演示如何从阻止发件人列表中删除电子邮件的发件人，并将电子邮件移动到收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="c2f42-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="c2f42-156">您需要保留从阻止发件人列表中删除发件人被阻止发件人发送一封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c2f42-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="c2f42-157">与电子邮件已发送发件人的发件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c2f42-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="c2f42-158">如果引用电子邮件不再存在用户的邮箱中，不会成功从阻止发件人列表中删除发件人。</span><span class="sxs-lookup"><span data-stu-id="c2f42-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="c2f42-159">用于将电子邮件的发件人为相关联的项标识符必须与 Exchange 邮箱中存在的项相关联。</span><span class="sxs-lookup"><span data-stu-id="c2f42-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="c2f42-160">我们建议您创建一个隐藏的文件夹，用于存储项目，以便可以从客户端应用程序的阻止发件人发送的以前阻止发件人。</span><span class="sxs-lookup"><span data-stu-id="c2f42-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="c2f42-161">中的项已从 Exchange 邮箱，管理员必须使用 Exchange 管理控制台访问要从列表中删除发件人的阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="c2f42-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="c2f42-162">有关如何使用 Exchange 管理控制台取消阻止用户的信息，请参阅[如何配置的安全发件人和阻止发件人在 Office 365 中的设置](http://support.microsoft.com/kb/2545137)。</span><span class="sxs-lookup"><span data-stu-id="c2f42-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](http://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="c2f42-163">将发件人添加到阻止发件人列表的响应相同的阻止发件人列表中移除发件人的成功响应。</span><span class="sxs-lookup"><span data-stu-id="c2f42-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="c2f42-164">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c2f42-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c2f42-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="c2f42-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="c2f42-166">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c2f42-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="c2f42-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="c2f42-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="c2f42-168">MarkAsJunk 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="c2f42-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="c2f42-169">下面的示例演示对**MarkAsJunk**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="c2f42-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="c2f42-170">这是要添加或移除阻止发件人列表发件人时指定的项标识符的电子邮件不再存在的邮箱中请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c2f42-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="c2f42-171">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c2f42-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c2f42-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="c2f42-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="c2f42-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2f42-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c2f42-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2f42-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="c2f42-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="c2f42-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c2f42-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c2f42-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c2f42-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c2f42-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="c2f42-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2f42-178">See also</span></span>

- [<span data-ttu-id="c2f42-179">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="c2f42-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="c2f42-180">[GetItem 操作](getitem-operation.md)GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="c2f42-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="c2f42-181">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="c2f42-181">FindItem operation</span></span>](finditem-operation.md)
    

