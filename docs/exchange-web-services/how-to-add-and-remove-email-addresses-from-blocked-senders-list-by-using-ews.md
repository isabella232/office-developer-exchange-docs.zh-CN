---
title: 添加并在 Exchange 使用 EWS 从阻止发件人列表中删除电子邮件地址
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: 了解如何使用 EWS 托管 API 或 EWS 添加到的电子邮件地址和删除阻止的发件人列表。
ms.openlocfilehash: c03ed585ebd62802000179d8c837786ba5f9aab4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752725"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a><span data-ttu-id="54e43-103">添加并在 Exchange 使用 EWS 从阻止发件人列表中删除电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="54e43-103">Add and remove email addresses from the Blocked Senders List by using EWS in Exchange</span></span>

<span data-ttu-id="54e43-104">了解如何使用 EWS 托管 API 或 EWS 添加到的电子邮件地址和删除阻止的发件人列表。</span><span class="sxs-lookup"><span data-stu-id="54e43-104">Find out how to use the EWS Managed API or EWS to add email addresses to and remove them from the Blocked Senders List.</span></span>
  
<span data-ttu-id="54e43-105">用户的垃圾邮件选项中的阻止发件人列表提供了一种方法将从指定发件人的所有电子邮件都移动到垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="54e43-105">The Blocked Senders List in a user's Junk Email options provides a way to move all email messages from specified senders to the Junk Email folder.</span></span> <span data-ttu-id="54e43-106">您可以让您的 EWS 托管 API 或 EWS 应用程序添加到的电子邮件地址或删除被阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="54e43-106">You can enable your EWS Managed API or EWS application to add email addresses to or remove them from the Blocked Senders List.</span></span>
  
<span data-ttu-id="54e43-107">请注意之前可以添加到的电子邮件地址或从阻止的发件人列表中删除它中的电子邮件地址的邮件必须存在用户的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="54e43-107">Note that a message from the email address must exist in the user's mailbox before you can add the email address to or remove it from the Blocked Senders List.</span></span> <span data-ttu-id="54e43-108">[ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法和[MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS 操作使用一项 Id。</span><span class="sxs-lookup"><span data-stu-id="54e43-108">The [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API method and the [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS operation use a collection of item IDs.</span></span> <span data-ttu-id="54e43-109">项目集合中的 Id 指示应为其更改的垃圾邮件状态的邮箱中的邮件。</span><span class="sxs-lookup"><span data-stu-id="54e43-109">The item IDs in the collection indicate messages in the mailbox for which the junk mail status should be changed.</span></span> 
  
<span data-ttu-id="54e43-110">您可以使用[Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979784%28v=exchg.150%29.aspx)和[Set-mailboxjunkemailconfiguration](http://technet.microsoft.com/en-us/library/dd979780%28v=exchg.150%29.aspx) Exchange Management Shell cmdlet 直接访问阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="54e43-110">You can use the [Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979784%28v=exchg.150%29.aspx) and [Set-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979780%28v=exchg.150%29.aspx) Exchange Management Shell cmdlets to access the Blocked Senders List directly.</span></span> 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a><span data-ttu-id="54e43-111">添加到的电子邮件地址或删除它从阻止的发件人列表使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="54e43-111">Add an email address to or remove it from the Blocked Senders List by using the EWS Managed API</span></span>
<span data-ttu-id="54e43-112"><a name="bk_AddRemoveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="54e43-112"></span></span>

<span data-ttu-id="54e43-113">若要添加到阻止的发件人列表的电子邮件的发件人，请使用**MarkAsJunk**方法，并将**isJunk**参数设置为**true**。</span><span class="sxs-lookup"><span data-stu-id="54e43-113">To add the sender of an email message to the Blocked Senders List, use the **MarkAsJunk** method and set the **isJunk** parameter to **true**.</span></span> <span data-ttu-id="54e43-114">若要从阻止的发件人列表中删除电子邮件的发件人，请将**isJunk**参数设置为**false**。</span><span class="sxs-lookup"><span data-stu-id="54e43-114">To remove the sender of an email message from the Blocked Senders List, set the **isJunk** parameter to **false**.</span></span>
  
<span data-ttu-id="54e43-115">下面的示例演示如何使用**MarkAsJunk**方法可更改垃圾邮件的状态。</span><span class="sxs-lookup"><span data-stu-id="54e43-115">The following example shows how to use the **MarkAsJunk** method to change the junk status of a message.</span></span> 
  
```cs
private static void MarkMessageAsJunk(ExchangeService service, ItemId messageId, bool isJunk, bool moveItem)
{
    List<ItemId> junkItemIds = new List<ItemId>();
    junkItemIds.Add(messageId);
    ServiceResponseCollection<MarkAsJunkResponse> responseCollection = null;
    try
    {
        // If isJunk is true, the sender of the email message is added to 
        // the Blocked Senders List. If isJunk is false, the sender is removed
        // from the list (if present).
        responseCollection = service.MarkAsJunk(junkItemIds, isJunk, moveItem);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error marking item as junk: {0}", ex.ErrorCode);
        return;
    }
    foreach (MarkAsJunkResponse response in responseCollection)
    {
        if (response.Result == ServiceResult.Success)
        {
            Console.WriteLine("Successfully marked message as {0}junk.", isJunk ? "": "NOT ");
            if (moveItem)
            {
                Console.WriteLine("New item ID: {0}", response.MovedItemId.ToString());
            }
        }
        else
        {
            Console.WriteLine("[{0}]: {1}", response.Result.ToString(),
                response.ErrorCode.ToString());
        }
    }
}
```

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a><span data-ttu-id="54e43-116">添加到的电子邮件地址或使用 EWS 将其删除阻止的发件人列表</span><span class="sxs-lookup"><span data-stu-id="54e43-116">Add an email address to or remove it from the Blocked Senders List by using EWS</span></span>
<span data-ttu-id="54e43-117"><a name="bk_AddRemoveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="54e43-117"></span></span>

<span data-ttu-id="54e43-118">以下 EWS SOAP 请求标记为垃圾邮件通过**IsJunk**属性设置为**true**的[MarkAsJunk](http://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx)元素中的项目。</span><span class="sxs-lookup"><span data-stu-id="54e43-118">The following EWS SOAP request marks an item as junk by setting the **IsJunk** attribute on the [MarkAsJunk](http://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) element to **true**.</span></span> <span data-ttu-id="54e43-119">它还会将邮件移到垃圾邮件文件夹通过**MoveItem**属性设置为**true**的**MarkAsJunk**元素。</span><span class="sxs-lookup"><span data-stu-id="54e43-119">It also moves the message to the Junk Email folder by setting the **MoveItem** attribute on the **MarkAsJunk** element to **true**.</span></span>
  
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
        <t:ItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAENAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEuAAA=" 
            ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAADi" />
      </m:ItemIds>
    </m:MarkAsJunk>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="54e43-120">以下 EWS SOAP 响应显示成功响应。</span><span class="sxs-lookup"><span data-stu-id="54e43-120">The following EWS SOAP response shows the successful response.</span></span> <span data-ttu-id="54e43-121">在响应中的[MovedItemId](http://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx)元素包含项目的项 ID 后移动。</span><span class="sxs-lookup"><span data-stu-id="54e43-121">The [MovedItemId](http://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) element in the response contains the item ID for the item after it was moved.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:MovedItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEbAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59DIAAA="
              ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59E+" />
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="54e43-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="54e43-122">See also</span></span>

- [<span data-ttu-id="54e43-123">Inbox management and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="54e43-123">Inbox management and EWS in Exchange</span></span>](inbox-management-and-ews-in-exchange.md)   
- [<span data-ttu-id="54e43-124">ExchangeService.MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="54e43-124">ExchangeService.MarkAsJunk</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="54e43-125">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="54e43-125">MarkAsJunk operation</span></span>](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [<span data-ttu-id="54e43-126">Get MailboxJunkEmailConfiguration</span><span class="sxs-lookup"><span data-stu-id="54e43-126">Get-MailboxJunkEmailConfiguration</span></span>](http://technet.microsoft.com/en-us/library/dd979784%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="54e43-127">Set-mailboxjunkemailconfiguration</span><span class="sxs-lookup"><span data-stu-id="54e43-127">Set-MailboxJunkEmailConfiguration</span></span>](http://technet.microsoft.com/en-us/library/dd979780%28v=exchg.150%29.aspx) 
- [<span data-ttu-id="54e43-128">Exchange 命令行管理程序</span><span class="sxs-lookup"><span data-stu-id="54e43-128">Exchange Management Shell</span></span>](../management/exchange-management-shell.md)
    

