---
title: 在 Exchange 中使用 EWS 以代理的形式访问联系人
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 以代理的形式访问联系人。
ms.openlocfilehash: 06faf7dd7459b14792abbea21761e909c8eb9fb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455343"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="01921-103">在 Exchange 中使用 EWS 以代理的形式访问联系人</span><span class="sxs-lookup"><span data-stu-id="01921-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="01921-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 以代理的形式访问联系人。</span><span class="sxs-lookup"><span data-stu-id="01921-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="01921-105">您可以使用 EWS 托管 API 或 EWS 授予用户对邮箱所有者的 "联系人" 文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="01921-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="01921-106">然后，代理可以代表邮箱所有者创建联系人，并检索、更新和删除邮箱所有者的 "联系人" 文件夹中的联系人，具体取决于他们的权限。</span><span class="sxs-lookup"><span data-stu-id="01921-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="01921-107">作为代理，您可以使用相同的方法和操作来访问邮箱所有者的 "联系人" 文件夹，用于访问自己的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="01921-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="01921-108">主要区别在于，必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)来查找或创建联系人项目，然后在确定项目 ID 之后，可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="01921-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="01921-109">**表1。用于将联系人作为代理访问的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="01921-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="01921-110">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="01921-110">**If you want to…**</span></span>|<span data-ttu-id="01921-111">**使用此 EWS 托管 API 方法 .。。**</span><span class="sxs-lookup"><span data-stu-id="01921-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="01921-112">**使用此 EWS 操作 .。。**</span><span class="sxs-lookup"><span data-stu-id="01921-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01921-113">创建联系人作为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="01921-114">[项。保存](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "联系人" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的位置</span><span class="sxs-lookup"><span data-stu-id="01921-114">[Item.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="01921-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="01921-116">将多个联系人创建为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="01921-117">**FolderId**参数提供对邮箱所有者的 "联系人" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[CreateItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="01921-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="01921-119">将联系人解析为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="01921-120">[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "联系人" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[ResolveName ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-120">[ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="01921-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="01921-122">搜索或查找联系人为代理</span><span class="sxs-lookup"><span data-stu-id="01921-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="01921-123">**FolderId**参数提供对邮箱所有者的 "联系人" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[FindItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-123">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="01921-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="01921-125">获取作为代理的联系人</span><span class="sxs-lookup"><span data-stu-id="01921-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="01921-126">Contact。绑定</span><span class="sxs-lookup"><span data-stu-id="01921-126">Contact.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="01921-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="01921-127">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="01921-128">将联系人更新为代理</span><span class="sxs-lookup"><span data-stu-id="01921-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="01921-129">[联系我们](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)，后跟[contact。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-129">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="01921-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="01921-131">将联系人删除为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="01921-132">[联系人。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)请先绑定，后跟[联系人。删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-132">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="01921-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="01921-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="01921-134">在本文的代码示例中，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="01921-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="01921-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-135"><a name="bk_prereq"> </a></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="01921-136">先决条件任务</span><span class="sxs-lookup"><span data-stu-id="01921-136">Prerequisite tasks</span></span>

<span data-ttu-id="01921-137">在用户可以将邮箱所有者的 "联系人" 文件夹作为代理进行访问之前，必须将该用户[添加为具有](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的 "联系人" 文件夹权限的代理。</span><span class="sxs-lookup"><span data-stu-id="01921-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="01921-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-138"><a name="bk_createewsma"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="01921-139">使用 EWS 托管 API 将联系人创建为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="01921-140">使用 EWS 托管 API，您可以使用代理用户的服务对象为邮箱所有者创建联系人。</span><span class="sxs-lookup"><span data-stu-id="01921-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="01921-141">本示例演示如何使用[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="01921-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="01921-142">本示例假定**服务**是委派的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且已为委派授予对邮箱所有者的 "联系人" 文件夹的适当权限。</span><span class="sxs-lookup"><span data-stu-id="01921-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
```cs
 public static void DelegateAccessCreateContact(ExchangeService service)
{
    // Create the contact.
    Contact contact = new Contact(service);
    // Specify the name and how the contact should be filed.
    contact.GivenName = "Brian";
    contact.MiddleName = "David";
    contact.Surname = "Johnson";
    contact.FileAsMapping = FileAsMapping.SurnameCommaGivenName;
    // Specify the company name.
    contact.CompanyName = "Contoso";
    // Specify the business, home, and car phone numbers.
    contact.PhoneNumbers[PhoneNumberKey.BusinessPhone] = "425-555-0110";
    contact.PhoneNumbers[PhoneNumberKey.HomePhone] = "425-555-0120";
    contact.PhoneNumbers[PhoneNumberKey.CarPhone] = "425-555-0130";
    // Specify two email addresses.
    contact.EmailAddresses[EmailAddressKey.EmailAddress1] = 
        new EmailAddress("brian_1@contoso.com");
    contact.EmailAddresses[EmailAddressKey.EmailAddress2] = 
        new EmailAddress("brian_2@contoso.com");
    // Save the contact in the mailbox owner's Contacts folder.
    // This method call results in a CreateItem call to EWS. 
    // The contact identifier contains the context for the mailbox owner's 
    // Contact folder. Any additional actions take on this contact will 
    // be performed in the mailbox owner's mailbox. 
    contact.Save(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    // Verify that the contact was created.
    // This method call results in a GetItem call to EWS
    // to load the display name property on the contact. 
    contact.Load(new PropertySet (ContactSchema.DisplayName));
    Console.WriteLine("\nContact created: " + contact.DisplayName + "\n");
}
```

<span data-ttu-id="01921-143">请注意，保存项目时， [save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法调用必须标识邮箱所有者的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="01921-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="01921-144">如果未指定邮箱所有者的 "联系人" 文件夹，则会将会议请求保存到代理的 "联系人" 文件夹中，而不是邮箱所有者的 "联系人" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="01921-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="01921-145">您可以通过两种方式将邮箱所有者的 "联系人" 文件夹包含在**Save**方法调用中。</span><span class="sxs-lookup"><span data-stu-id="01921-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="01921-146">建议使用[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)和邮箱所有者的 SMTP 地址实例化[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="01921-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="01921-147">但是，您还可以先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)到 "联系人" 文件夹，然后在**Save**方法调用中使用该文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="01921-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="01921-148">但请注意，这会导致额外的 EWS 调用。</span><span class="sxs-lookup"><span data-stu-id="01921-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="01921-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-149"><a name="bk_createews"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="01921-150">使用 EWS 将联系人创建为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="01921-151">EWS 使您可以使用委派用户的服务对象为邮箱所有者创建联系人项目。</span><span class="sxs-lookup"><span data-stu-id="01921-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="01921-152">本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作来创建联系人。</span><span class="sxs-lookup"><span data-stu-id="01921-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="01921-153">这也是当您使用**Save**方法[创建联系人](#bk_createewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="01921-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Contact>
          <t:FileAsMapping>LastCommaFirst</t:FileAsMapping>
          <t:GivenName>Brian</t:GivenName>
          <t:MiddleName>David</t:MiddleName>
          <t:CompanyName>Contoso</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">brian_1@contoso.com</t:Entry>
            <t:Entry Key="EmailAddress2">brian_2@contoso.com</t:Entry>
          </t:EmailAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">425-555-0110</t:Entry>
            <t:Entry Key="HomePhone">425-555-0120</t:Entry>
            <t:Entry Key="CarPhone">425-555-0130</t:Entry>
          </t:PhoneNumbers>
          <t:Surname>Johnson</t:Surname>
        </t:Contact>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="01921-154">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功创建该联系人。</span><span class="sxs-lookup"><span data-stu-id="01921-154">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="01921-155">该响应还包含新创建的联系人的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="01921-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="01921-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-156"><a name="bk_resolveewsma"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="01921-157">使用 EWS 托管 API 将联系人解析为代理</span><span class="sxs-lookup"><span data-stu-id="01921-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="01921-158">若要基于可能不明确的名称或术语查找联系人，必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)方法之一，以便您可以指定邮箱所有者的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="01921-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
```cs
private static void DelegateAccessResolveContacts(ExchangeService service)
{
    // Create a list to store folders to search.
    List<FolderId> folders = new List<FolderId>();
   
    // Add the mailbox owner's folder to the list.
    folders.Add(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    
    // Resolve the ambiguous name "Johnson".
    // This method call results in a ResolveNames call to EWS.
    NameResolutionCollection resolvedNames = service.ResolveName(
        "johnson", folders, ResolveNameSearchLocation.ContactsOnly, true);
    // Output the list of candidate email addresses and contact names.
    foreach (NameResolution nameRes in resolvedNames)
    {
        Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
        Console.WriteLine("Contact ID: " + nameRes.Mailbox.Id);
    }
}
```

<span data-ttu-id="01921-159">在**ResolveNames**方法调用返回带有 id 的响应后，您可以使用 id 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来[获取、更新或删除联系人](#bk_getewsma)， &mdash; 无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="01921-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="01921-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-160"><a name="bk_resolveews"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="01921-161">使用 EWS 将联系人解析为代理人</span><span class="sxs-lookup"><span data-stu-id="01921-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="01921-162">EWS 使您可以使用委派用户的服务对象来解析邮箱所有者的 "联系人" 文件夹中的部分名称。</span><span class="sxs-lookup"><span data-stu-id="01921-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="01921-163">本示例演示如何使用[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作查找邮箱所有者的 "联系人" 文件夹中包含 "johnson" 一词的会议。</span><span class="sxs-lookup"><span data-stu-id="01921-163">This example shows how to use the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="01921-164">这也是在使用**ResolveName**方法[解析联系人](#bk_resolveewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="01921-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ResolveNames ReturnFullContactData="true"
                    SearchScope="Contacts">
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
      <m:UnresolvedEntry>johnson</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="01921-165">服务器响应**ResolveNames**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**的[ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx)消息，该消息指示操作已成功完成且仅找到一个结果，或者如果发现多个结果，则为**ErrorNameResolutionMultipleResults** 。如果找到多个结果，则基于该联系人的第三个代码示例中显示的是[使用 EWS 托管 API 创建一个联系人作为代理人](#bk_createewsma)。</span><span class="sxs-lookup"><span data-stu-id="01921-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="01921-166">该响应还包含每个结果的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="01921-166">The response also contains the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="01921-167">为了提高可读性， **ItemId**元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="01921-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Warning">
          <m:MessageText>Multiple results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionMultipleResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:ResolutionSet TotalItemsInView="2"
                           IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_1@contoso.com</t:Name>
                <t:EmailAddress>brian_1@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_2@contoso.com</t:Name>
                <t:EmailAddress>brian_2@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="01921-168">现在，您已拥有与不明确名称匹配的联系人的**ItemId** ，您可以通过使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来[获取、更新或删除联系人项目作为代理](#bk_getews)， &mdash; 而无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="01921-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="01921-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-169"><a name="bk_getewsma"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="01921-170">使用 EWS 托管 API 获取、更新或删除联系人项目作为代理</span><span class="sxs-lookup"><span data-stu-id="01921-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="01921-171">您可以使用 EWS 托管 API 来获取、更新或删除联系人，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="01921-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="01921-172">唯一的区别是，服务对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="01921-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="01921-173">**Bind**方法调用中包含的项目 ID 在邮箱所有者的 "联系人" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="01921-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="01921-174">**表2。使用联系人作为代理的 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="01921-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="01921-175">**任务**</span><span class="sxs-lookup"><span data-stu-id="01921-175">**Task**</span></span>|<span data-ttu-id="01921-176">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="01921-176">**EWS Managed API method**</span></span>|<span data-ttu-id="01921-177">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="01921-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01921-178">获取联系人</span><span class="sxs-lookup"><span data-stu-id="01921-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="01921-179">绑定</span><span class="sxs-lookup"><span data-stu-id="01921-179">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="01921-180">使用 EWS 托管 API 获取项</span><span class="sxs-lookup"><span data-stu-id="01921-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="01921-181">更新联系人</span><span class="sxs-lookup"><span data-stu-id="01921-181">Update a contact</span></span>  <br/> |<span data-ttu-id="01921-182">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-182">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="01921-183">使用 EWS 托管 API 更新项</span><span class="sxs-lookup"><span data-stu-id="01921-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="01921-184">删除联系人</span><span class="sxs-lookup"><span data-stu-id="01921-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="01921-185">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-185">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="01921-186">使用 EWS 托管 API 删除项目</span><span class="sxs-lookup"><span data-stu-id="01921-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="01921-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="01921-187"><a name="bk_getews"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="01921-188">使用 EWS 获取、更新或删除联系人项目作为代理</span><span class="sxs-lookup"><span data-stu-id="01921-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="01921-189">您可以使用 EWS 获取、更新或删除会议或约会联系人，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="01921-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="01921-190">唯一的区别是，服务对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="01921-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="01921-191">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)请求中包含的项目 ID 在邮箱所有者的 "联系人" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="01921-191">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="01921-192">**表3。用于将联系人作为代理使用的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="01921-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="01921-193">**任务**</span><span class="sxs-lookup"><span data-stu-id="01921-193">**Task**</span></span>|<span data-ttu-id="01921-194">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="01921-194">**EWS operation**</span></span>|<span data-ttu-id="01921-195">**示例**</span><span class="sxs-lookup"><span data-stu-id="01921-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01921-196">获取联系人</span><span class="sxs-lookup"><span data-stu-id="01921-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="01921-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="01921-197">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="01921-198">使用 EWS 获取项</span><span class="sxs-lookup"><span data-stu-id="01921-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="01921-199">更新联系人</span><span class="sxs-lookup"><span data-stu-id="01921-199">Update a contact</span></span>  <br/> |<span data-ttu-id="01921-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01921-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="01921-201">使用 EWS 更新项</span><span class="sxs-lookup"><span data-stu-id="01921-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="01921-202">删除联系人</span><span class="sxs-lookup"><span data-stu-id="01921-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="01921-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="01921-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="01921-204">使用 EWS 删除项</span><span class="sxs-lookup"><span data-stu-id="01921-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01921-205">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01921-205">See also</span></span>

- [<span data-ttu-id="01921-206">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="01921-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="01921-207">使用 Exchange 中的 EWS 添加和删除委派</span><span class="sxs-lookup"><span data-stu-id="01921-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="01921-208">使用 Exchange 中的 EWS 为另一个用户设置文件夹权限</span><span class="sxs-lookup"><span data-stu-id="01921-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="01921-209">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="01921-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="01921-210">使用 Exchange 2013 中的 EWS 解析不明确的名称</span><span class="sxs-lookup"><span data-stu-id="01921-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

