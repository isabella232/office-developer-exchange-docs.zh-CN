---
title: MarkAsJunk 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: 查找有关 MarkAsJunk EWS 操作的信息。
ms.openlocfilehash: 25d6b01dfff64c4e45f3382223311219d349c165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468570"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="84e07-103">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="84e07-103">MarkAsJunk operation</span></span>

<span data-ttu-id="84e07-104">查找有关**MarkAsJunk** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="84e07-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="84e07-105">**MarkAsJunk**操作在阻止的电子邮件列表中添加和删除用户，并将电子邮件移动到 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="84e07-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="84e07-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="84e07-107">使用 MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="84e07-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="84e07-108">**MarkAsJunk**操作包含两个布尔选项，用于指示是否应将电子邮件发件人添加到 "阻止的发件人" 列表以及是否应将目标电子邮件移动到默认的 "垃圾邮件" 文件夹或 "收件箱" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="84e07-109">操作由**IsJunk**和**MoveItem**属性的值决定。</span><span class="sxs-lookup"><span data-stu-id="84e07-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="84e07-110">以下是基于**IsJunk**和**MoveItem**属性的值组合的可能操作：</span><span class="sxs-lookup"><span data-stu-id="84e07-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="84e07-111">如果**IsJunk**属性设置为**True**，并且**MoveItem**属性设置为**true**，则目标电子邮件的发件人将添加到 "阻止的发件人" 列表中，并将电子邮件移动到 "垃圾 Dmail" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="84e07-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="84e07-112">如果将**IsJunk**属性设置为**true**，并将**MoveItem**属性设置为**false**，则目标电子邮件的发件人将添加到 "阻止的发件人" 列表中，并且不会从文件夹中移动电子邮件。</span><span class="sxs-lookup"><span data-stu-id="84e07-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="84e07-113">如果将**IsJunk**属性设置为**false**，并将**MoveItem**属性设置为**true**，则目标电子邮件 messageis 的发件人将从阻止的发件人列表中删除，并且电子邮件将移至 "收件箱" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="84e07-114">如果将**IsJunk**属性设置为**false**，并将**MoveItem**属性设置为**false**，则会从阻止的发件人列表中删除目标电子邮件的发件人，并且不会将电子邮件从文件夹中移出。</span><span class="sxs-lookup"><span data-stu-id="84e07-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="84e07-115">阻止的发件人列表的内容不能从 EWS 中检测到。</span><span class="sxs-lookup"><span data-stu-id="84e07-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="84e07-116">如果将发件人添加到 "阻止的发件人" 列表中，则需要保留被阻止的发件人发送的电子邮件的副本，以在将来取消阻止该发件人。</span><span class="sxs-lookup"><span data-stu-id="84e07-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="84e07-117">MarkAsJunk 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="84e07-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="84e07-118">**MarkAsJunk**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="84e07-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="84e07-119">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="84e07-119">**Header name**</span></span>|<span data-ttu-id="84e07-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="84e07-120">**Element**</span></span>|<span data-ttu-id="84e07-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="84e07-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84e07-122">**模拟**</span><span class="sxs-lookup"><span data-stu-id="84e07-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="84e07-123">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="84e07-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="84e07-124">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="84e07-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="84e07-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="84e07-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="84e07-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="84e07-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="84e07-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="84e07-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="84e07-128">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="84e07-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="84e07-129">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="84e07-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="84e07-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="84e07-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="84e07-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="84e07-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="84e07-132">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="84e07-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="84e07-133">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="84e07-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="84e07-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="84e07-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="84e07-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="84e07-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="84e07-136">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="84e07-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="84e07-137">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="84e07-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="84e07-138">MarkAsJunk 操作请求示例：将发件人添加到阻止的发件人列表</span><span class="sxs-lookup"><span data-stu-id="84e07-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="84e07-139">以下示例的**MarkAsJunk**操作请求显示如何将电子邮件的发件人添加到 "阻止的发件人" 列表中并将电子邮件移动到 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="84e07-140">**MarkAsJunk**操作接受唯一的电子邮件标识符，以标识用于引用添加到 "阻止的发件人" 列表中的发件人的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="84e07-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="84e07-141">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="84e07-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="84e07-142">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="84e07-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="84e07-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="84e07-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="84e07-144">ItemIds</span><span class="sxs-lookup"><span data-stu-id="84e07-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="84e07-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="84e07-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="84e07-146">成功的 MarkAsJunk 操作响应</span><span class="sxs-lookup"><span data-stu-id="84e07-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="84e07-147">以下示例显示了对**MarkAsJunk**操作请求的成功响应，以将发件人添加到阻止的发件人列表并将电子邮件移动到 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="84e07-148">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="84e07-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="84e07-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="84e07-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="84e07-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="84e07-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="84e07-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="84e07-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="84e07-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="84e07-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="84e07-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="84e07-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="84e07-154">MarkAsJunk 操作请求示例：从阻止的发件人列表中删除发件人</span><span class="sxs-lookup"><span data-stu-id="84e07-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="84e07-155">以下示例的**MarkAsJunk**操作请求显示如何从阻止的发件人列表中删除电子邮件的发件人，并将电子邮件移动到 "收件箱" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="84e07-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="84e07-156">您需要保留被阻止的发件人发送的电子邮件，以从阻止的发件人列表中删除发件人。</span><span class="sxs-lookup"><span data-stu-id="84e07-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="84e07-157">发件人的电子邮件地址与发件人发送的电子邮件相关联。</span><span class="sxs-lookup"><span data-stu-id="84e07-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="84e07-158">如果参考电子邮件不再存在于用户的邮箱中，则从阻止的发件人列表中删除发件人将不会成功。</span><span class="sxs-lookup"><span data-stu-id="84e07-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="84e07-159">用于将电子邮件与其发件人相关联的项目标识符必须与 Exchange 邮箱中存在的项目相关联。</span><span class="sxs-lookup"><span data-stu-id="84e07-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="84e07-160">我们建议您创建一个隐藏文件夹来存储由以前被阻止的发件人发送的项目，以便可以从客户端应用程序取消阻止这些发件人。</span><span class="sxs-lookup"><span data-stu-id="84e07-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="84e07-161">如果已从 Exchange 邮箱中删除某个项目，则管理员必须使用 Exchange 管理控制台访问阻止的发件人列表，以从列表中删除发件人。</span><span class="sxs-lookup"><span data-stu-id="84e07-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="84e07-162">有关如何使用 Exchange 管理控制台取消阻止用户的信息，请参阅[如何在 Office 365 中配置安全发件人和阻止的发件人设置](https://support.microsoft.com/kb/2545137)。</span><span class="sxs-lookup"><span data-stu-id="84e07-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](https://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="84e07-163">从阻止的发件人列表中删除发件人的成功响应与将发件人添加到阻止的发件人列表的响应相同。</span><span class="sxs-lookup"><span data-stu-id="84e07-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="84e07-164">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="84e07-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="84e07-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="84e07-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="84e07-166">ItemIds</span><span class="sxs-lookup"><span data-stu-id="84e07-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="84e07-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="84e07-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="84e07-168">MarkAsJunk 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="84e07-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="84e07-169">下面的示例演示对**MarkAsJunk**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="84e07-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="84e07-170">这是在由项目标识符指定的电子邮件不再存在于邮箱中时，对向阻止的发件人列表添加或删除发件人的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="84e07-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="84e07-171">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="84e07-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="84e07-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="84e07-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="84e07-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="84e07-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="84e07-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="84e07-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="84e07-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="84e07-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="84e07-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="84e07-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="84e07-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="84e07-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="84e07-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84e07-178">See also</span></span>

- [<span data-ttu-id="84e07-179">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="84e07-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="84e07-180">[GetItem 操作](getitem-operation.md)GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="84e07-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="84e07-181">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="84e07-181">FindItem operation</span></span>](finditem-operation.md)
    

