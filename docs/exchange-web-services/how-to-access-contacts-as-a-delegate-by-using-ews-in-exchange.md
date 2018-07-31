---
title: 作为代理人在 Exchange 使用 EWS 访问联系人
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: 了解如何通过在 Exchange 使用 EWS 托管 API 或 EWS 访问作为代理人的联系人。
ms.openlocfilehash: 47540082f7e60645cae60fe2347e50e17cd226dd
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353719"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="8cbed-103">作为代理人在 Exchange 使用 EWS 访问联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="8cbed-104">了解如何通过在 Exchange 使用 EWS 托管 API 或 EWS 访问作为代理人的联系人。</span><span class="sxs-lookup"><span data-stu-id="8cbed-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8cbed-105">您可以使用 EWS 托管 API 或 EWS 向邮箱所有者的联系人文件夹的用户访问。</span><span class="sxs-lookup"><span data-stu-id="8cbed-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="8cbed-106">委托然后可以创建联系人代表邮箱所有者，和检索、 更新和删除联系人从邮箱所有者的联系人文件夹，具体取决于他们的权限。</span><span class="sxs-lookup"><span data-stu-id="8cbed-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="8cbed-107">作为代理人，您使用相同的方法和操作访问用于访问自己联系人文件夹邮箱所有者的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="8cbed-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="8cbed-108">主要区别是，您必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)可查找或创建联系人项目，，然后确定项目 ID 后，您可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)以获取、 更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="8cbed-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="8cbed-109">**表 1。EWS 托管 API 方法和用于访问作为代理人的联系人的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="8cbed-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="8cbed-110">**如果您希望...**</span><span class="sxs-lookup"><span data-stu-id="8cbed-110">**If you want to…**</span></span>|<span data-ttu-id="8cbed-111">**使用此 EWS 托管 API 方法...**</span><span class="sxs-lookup"><span data-stu-id="8cbed-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="8cbed-112">**使用此 EWS 操作...**</span><span class="sxs-lookup"><span data-stu-id="8cbed-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cbed-113">作为代理人创建联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-114">[Item.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx)其中的[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="8cbed-114">[Item.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="8cbed-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="8cbed-116">作为代理人创建多个联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)其中的**文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="8cbed-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="8cbed-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="8cbed-119">作为代理人解决联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)其中的[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="8cbed-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="8cbed-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="8cbed-122">搜索或查找联系人作为代理人</span><span class="sxs-lookup"><span data-stu-id="8cbed-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-123">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)其中的**文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="8cbed-123">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="8cbed-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="8cbed-125">作为代理人获取联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="8cbed-126">Contact.Bind</span><span class="sxs-lookup"><span data-stu-id="8cbed-126">Contact.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8cbed-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="8cbed-127">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="8cbed-128">作为代理人更新联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-129">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)跟[Contact.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-129">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="8cbed-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="8cbed-131">作为代理人删除联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="8cbed-132">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)跟[Contact.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-132">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="8cbed-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="8cbed-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="8cbed-134">在本文中的代码示例，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="8cbed-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="8cbed-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-135"></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="8cbed-136">必备组件的任务</span><span class="sxs-lookup"><span data-stu-id="8cbed-136">Prerequisite tasks</span></span>

<span data-ttu-id="8cbed-137">用户可以访问邮箱所有者的联系人文件夹作为代理人之前，用户必须[添加为具有权限代理](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="8cbed-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="8cbed-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-138"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="8cbed-139">使用 EWS 托管 API 创建作为代理人的联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="8cbed-140">EWS 托管 API 可使用的代理用户的服务对象创建邮箱所有者的联系人。</span><span class="sxs-lookup"><span data-stu-id="8cbed-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="8cbed-141">本示例演示如何使用[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="8cbed-141">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="8cbed-142">此示例假定该**服务**的代理是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和委托已被授予邮箱所有者的联系人文件夹的相应权限。</span><span class="sxs-lookup"><span data-stu-id="8cbed-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="8cbed-143">注意当您保存项目时，[保存](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法调用必须确定邮箱所有者的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="8cbed-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="8cbed-144">如果未指定邮箱所有者的联系人文件夹，则会议请求中获取保存到代理的联系人文件夹并不邮箱所有者的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="8cbed-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="8cbed-145">您可以在两种方式中的**保存**方法调用中包含邮箱所有者的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="8cbed-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="8cbed-146">我们建议您通过使用[WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)和邮箱所有者的 SMTP 地址实例[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="8cbed-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="8cbed-147">但是，您还可以[将绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)到联系人文件夹首先，然后使用**保存**方法调用中的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="8cbed-147">However, you can also [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="8cbed-148">请注意，但是，这将创建的额外的 EWS 调用。</span><span class="sxs-lookup"><span data-stu-id="8cbed-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="8cbed-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-149"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="8cbed-150">使用 EWS 创建作为代理人的联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="8cbed-151">EWS，可以使用的代理用户的服务对象为邮箱所有者创建联系人项目。</span><span class="sxs-lookup"><span data-stu-id="8cbed-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="8cbed-152">本示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建联系人。</span><span class="sxs-lookup"><span data-stu-id="8cbed-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="8cbed-153">这也是 EWS 托管 API 时您使用**Save**方法向[联系人](#bk_createewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="8cbed-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="8cbed-154">服务器响应包含**NoError**，这表明已成功创建联系人[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="8cbed-154">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="8cbed-155">响应还包含新创建的联系人的项 ID。</span><span class="sxs-lookup"><span data-stu-id="8cbed-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="8cbed-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-156"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="8cbed-157">作为代理人的联系人解决使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="8cbed-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="8cbed-158">查找联系人基于可能模糊名称或术语，您必须以便您可以指定邮箱所有者的联系人文件夹使用[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)方法，其中包括[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数之一。</span><span class="sxs-lookup"><span data-stu-id="8cbed-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="8cbed-159">**ResolveNames**方法调用返回一个响应，id 后，您可以[获取、 更新或删除该联系人](#bk_getewsma)使用的 ID 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;并不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="8cbed-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="8cbed-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-160"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="8cbed-161">通过使用 EWS 解决作为代理人的联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="8cbed-162">EWS 使您可以使用的代理用户的服务对象以解析邮箱所有者的联系人文件夹中的部分名称。</span><span class="sxs-lookup"><span data-stu-id="8cbed-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="8cbed-163">本示例演示如何使用[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作在包含单词"johnson"的邮箱所有者的联系人文件夹中查找会议。</span><span class="sxs-lookup"><span data-stu-id="8cbed-163">This example shows how to use the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="8cbed-164">这也是 EWS 托管 API 时您使用**ResolveName**方法[解析联系人](#bk_resolveewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="8cbed-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="8cbed-165">服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明的操作成功完成，找到仅具有一个[ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx)消息的**ResolveNames**请求结果或**ErrorNameResolutionMultipleResults**找到多个结果-如果这是基于该联系人[创建一个联系人作为代理人使用 EWS 托管 API](#bk_createewsma)的第三个代码示例中显示的内容。</span><span class="sxs-lookup"><span data-stu-id="8cbed-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="8cbed-166">响应还包含[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的每个结果。</span><span class="sxs-lookup"><span data-stu-id="8cbed-166">The response also contains the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="8cbed-167">为便于阅读缩短了**ItemId**元素的值。</span><span class="sxs-lookup"><span data-stu-id="8cbed-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="8cbed-168">既然您已经**ItemId**模糊名称匹配的联系人，您可以[获取、 更新或删除作为使用 EWS 代理人的联系人项目](#bk_getews)使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;并不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="8cbed-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="8cbed-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-169"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="8cbed-170">获取、 更新或删除联系人项目作为代理人使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="8cbed-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="8cbed-171">EWS 托管 API 可用于获取、 更新或删除您执行这些操作，您不使用代理访问时的相同方式中的联系人。</span><span class="sxs-lookup"><span data-stu-id="8cbed-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="8cbed-172">唯一的区别是服务对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="8cbed-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="8cbed-173">唯一的**绑定**方法调用中包含的项 ID 标识邮箱所有者的联系人文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="8cbed-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="8cbed-174">**表 2。EWS 托管 API 方法处理作为代理人的联系人**</span><span class="sxs-lookup"><span data-stu-id="8cbed-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="8cbed-175">**任务**</span><span class="sxs-lookup"><span data-stu-id="8cbed-175">**Task**</span></span>|<span data-ttu-id="8cbed-176">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="8cbed-176">**EWS Managed API method**</span></span>|<span data-ttu-id="8cbed-177">**代码示例：**</span><span class="sxs-lookup"><span data-stu-id="8cbed-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cbed-178">获取联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="8cbed-179">绑定</span><span class="sxs-lookup"><span data-stu-id="8cbed-179">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8cbed-180">使用 EWS 托管 API 获取项</span><span class="sxs-lookup"><span data-stu-id="8cbed-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="8cbed-181">更新联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-181">Update a contact</span></span>  <br/> |<span data-ttu-id="8cbed-182">[更新](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-182">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="8cbed-183">使用 EWS 托管 API 更新项</span><span class="sxs-lookup"><span data-stu-id="8cbed-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="8cbed-184">删除联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="8cbed-185">[删除](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-185">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="8cbed-186">使用 EWS 托管 API 删除项</span><span class="sxs-lookup"><span data-stu-id="8cbed-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="8cbed-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="8cbed-187"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="8cbed-188">获取、 更新或使用 EWS 删除作为代理人的联系人项目</span><span class="sxs-lookup"><span data-stu-id="8cbed-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="8cbed-189">您可以使用 EWS 获取、 更新或删除会议或约会联系人与您执行这些操作，您不使用代理访问时相同的方式。</span><span class="sxs-lookup"><span data-stu-id="8cbed-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="8cbed-190">唯一的区别是服务对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="8cbed-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="8cbed-191">唯一[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)请求中包含的项 ID 标识邮箱所有者的联系人文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="8cbed-191">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="8cbed-192">**表 3。使用作为代理人的联系人的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="8cbed-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="8cbed-193">**任务**</span><span class="sxs-lookup"><span data-stu-id="8cbed-193">**Task**</span></span>|<span data-ttu-id="8cbed-194">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="8cbed-194">**EWS operation**</span></span>|<span data-ttu-id="8cbed-195">**示例**</span><span class="sxs-lookup"><span data-stu-id="8cbed-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cbed-196">获取联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="8cbed-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="8cbed-197">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="8cbed-198">使用 EWS 获取项</span><span class="sxs-lookup"><span data-stu-id="8cbed-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="8cbed-199">更新联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-199">Update a contact</span></span>  <br/> |<span data-ttu-id="8cbed-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cbed-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="8cbed-201">使用 EWS 更新项</span><span class="sxs-lookup"><span data-stu-id="8cbed-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="8cbed-202">删除联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="8cbed-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="8cbed-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="8cbed-204">使用 EWS 删除项</span><span class="sxs-lookup"><span data-stu-id="8cbed-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cbed-205">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8cbed-205">See also</span></span>

- [<span data-ttu-id="8cbed-206">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="8cbed-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="8cbed-207">添加和删除代理人，在 Exchange 使用 EWS</span><span class="sxs-lookup"><span data-stu-id="8cbed-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="8cbed-208">在 Exchange 使用 EWS 设置另一个用户的文件夹权限</span><span class="sxs-lookup"><span data-stu-id="8cbed-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="8cbed-209">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="8cbed-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="8cbed-210">模糊名称解析使用 EWS 在 Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8cbed-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

