---
title: 模糊名称解析使用 EWS 在 Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: 了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务 (AD DS) 或用户的邮箱中的联系人文件夹中获取可能的匹配项来解析模糊名称。
ms.openlocfilehash: 05a88043083a27d2e6d445cd71e5f3919c5a775d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752873"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a><span data-ttu-id="192e0-103">模糊名称解析使用 EWS 在 Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="192e0-103">Resolve ambiguous names by using EWS in Exchange 2013</span></span>

<span data-ttu-id="192e0-104">了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务 (AD DS) 或用户的邮箱中的联系人文件夹中获取可能的匹配项来解析模糊名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-104">Learn how to use the EWS Managed API or EWS to resolve ambiguous names by getting possible matches from Active Directory Domain Services (AD DS) or a contacts folder in your user's mailbox.</span></span>
  
<span data-ttu-id="192e0-105">您的组织中的用户参加培训课程的员工提供手写的名称和地址列表。</span><span class="sxs-lookup"><span data-stu-id="192e0-105">A user in your organization is given a hand-written list of names and addresses for employees that attended a training session.</span></span> <span data-ttu-id="192e0-106">所需的某些其他信息的电子邮件发送给人员在列表中，但他们不能读取每个人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="192e0-106">They want to send an email with some additional information to people on the list, but they can't read everyone's email address.</span></span> <span data-ttu-id="192e0-107">如果您想要解决此问题，供您的应用程序中的用户，可以帮助 EWS。</span><span class="sxs-lookup"><span data-stu-id="192e0-107">If you want to solve this problem for your users in your application, EWS can help.</span></span> <span data-ttu-id="192e0-108">您可以使用[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作返回的文本，如最后一个名称的一部分的选定内容的潜在匹配项的列表。</span><span class="sxs-lookup"><span data-stu-id="192e0-108">You can use the [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API method or the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to return a list of potential matches for a selection of text, such as part of a last name.</span></span> <span data-ttu-id="192e0-109">返回的项可以是公共用户邮箱、 通讯组和联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-109">The returned items can be public user mailboxes, distribution groups, and contacts.</span></span> 
  
<span data-ttu-id="192e0-110">请注意，Exchange 保存与前缀的路由类型，如 smtp 或 sip，多值数组中的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="192e0-110">Note that Exchange saves email addresses with prefixed routing types, such as smtp or sip, in a multivalue array.</span></span> <span data-ttu-id="192e0-111">无法解析的名称，例如"sip: User1"的开头添加路由类型时， **ResolveName**方法和**ResolveNames**操作执行针对该数组的每个值的部分匹配。</span><span class="sxs-lookup"><span data-stu-id="192e0-111">The **ResolveName** method and the **ResolveNames** operation perform a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1".</span></span> <span data-ttu-id="192e0-112">如果不指定传送类型，该方法或操作将默认为 smtp、 匹配到主 smtp 地址属性，以及不搜索多值数组。</span><span class="sxs-lookup"><span data-stu-id="192e0-112">If you don't specify a routing type, the method or operation will default to smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> <span data-ttu-id="192e0-113">例如，如果您搜索 User1，不包括 sip 前缀，您将不接收 sip:User1@Contoso.com 结果是，即使这是有效的邮箱。</span><span class="sxs-lookup"><span data-stu-id="192e0-113">For example, if you search for User1 and do not include the sip prefix, you will not receive sip:User1@Contoso.com as a result, even if that is a valid mailbox.</span></span> 
  
<span data-ttu-id="192e0-114">您只能在单个请求中指定一个模糊名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-114">You can only specify one ambiguous name in a single request.</span></span> <span data-ttu-id="192e0-115">如果您有一组不明确的名称解析，您将需要循环访问列表，并调用该方法或为每个项的操作。</span><span class="sxs-lookup"><span data-stu-id="192e0-115">If you have a list of ambiguous names to resolve, you will need to loop through the list and call the method or operation for each entry.</span></span> <span data-ttu-id="192e0-116">从用户的联系人文件夹的候选人将具有一个非空项目 ID 值，该值可然后用于[Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)方法调用或[GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)操作请求中检索的其他信息。</span><span class="sxs-lookup"><span data-stu-id="192e0-116">Candidates from a user's Contacts folder will have a non-null item ID value, which can then be used in a [Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) method call or [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request to retrieve additional information.</span></span> <span data-ttu-id="192e0-117">如果候选通讯组，可以使用[ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS 操作来获取成员的列表。</span><span class="sxs-lookup"><span data-stu-id="192e0-117">If the candidate is a distribution group, you can use the [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS operation to get the list of members.</span></span> <span data-ttu-id="192e0-118">如果_returnContactDetails_参数或**ReturnFullContactData** EWS 属性设置为 true，通过**ResolveName**方法返回 Active Directory 条目或**ResolveNames**操作将包含其他属性用于描述联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-118">If the  _returnContactDetails_ parameter or the **ReturnFullContactData** EWS attribute is set to true, Active Directory entries returned via a **ResolveName** method or **ResolveNames** operation will include additional properties that describe the contact.</span></span> <span data-ttu-id="192e0-119">_ReturnContactDetails_参数或**ReturnFullContactData**属性不影响联系人返回的数据和联系人组。</span><span class="sxs-lookup"><span data-stu-id="192e0-119">The  _returnContactDetails_ parameter or the **ReturnFullContactData** attribute does not affect the data that is returned for contacts and contact groups.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a><span data-ttu-id="192e0-120">模糊名称解析使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="192e0-120">Resolve ambiguous names by using EWS Managed API</span></span>
<span data-ttu-id="192e0-121"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="192e0-121"></span></span>

<span data-ttu-id="192e0-122">可以使用[ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)方法查找与传递的模糊名称匹配的候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-122">You can use the [ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) method to find candidates that match the ambiguous name you pass.</span></span> <span data-ttu-id="192e0-123">可以使用**ResolveName**方法的重载的候选项搜索五个不同的方式。</span><span class="sxs-lookup"><span data-stu-id="192e0-123">You can use overloads of the **ResolveName** method to search for candidates in five different ways.</span></span> 
  
<span data-ttu-id="192e0-124">**表 1。重载的 ResolveName 方法**</span><span class="sxs-lookup"><span data-stu-id="192e0-124">**Table 1. Overloaded ResolveName methods**</span></span>

|<span data-ttu-id="192e0-125">**方法**</span><span class="sxs-lookup"><span data-stu-id="192e0-125">**Method**</span></span>|<span data-ttu-id="192e0-126">**工作原理**</span><span class="sxs-lookup"><span data-stu-id="192e0-126">**How it works**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="192e0-127">ResolveName(String)</span><span class="sxs-lookup"><span data-stu-id="192e0-127">ResolveName(String)</span></span>](http://msdn.microsoft.com/en-us/library/dd635548%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="192e0-128">在用户的联系人文件夹和全局地址列表 (GAL) 中查找联系人 — 该顺序。</span><span class="sxs-lookup"><span data-stu-id="192e0-128">Finds contacts in the user's Contacts folder and the Global Address List (GAL) — in that order.</span></span> <span data-ttu-id="192e0-129">字符串变量是您试图解析的不明确名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-129">The string variable is the ambiguous name you are trying to resolve.</span></span>  <br/> |
|[<span data-ttu-id="192e0-130">ResolveName （字符串，ResolveNameSearchLocation，布尔值）</span><span class="sxs-lookup"><span data-stu-id="192e0-130">ResolveName(String, ResolveNameSearchLocation, Boolean)</span></span>](http://msdn.microsoft.com/en-us/library/dd634595%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="192e0-131">在默认联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-131">Finds contacts in the default Contacts folder and/or the Global Address List (GAL).</span></span> <span data-ttu-id="192e0-132">字符串值不明确的名称，搜索位置指定联系人文件夹和/或 GAL，并且布尔值，该值指示是否返回完整的联系信息。</span><span class="sxs-lookup"><span data-stu-id="192e0-132">The string value is the ambiguous name, the search location specifies the Contacts folder and/or the GAL, and the Boolean value indicates whether to return the full contact information.</span></span>  <br/> |
|[<span data-ttu-id="192e0-133">ResolveName (字符串，ResolveNameSearchLocation，Boolean、 属性集)</span><span class="sxs-lookup"><span data-stu-id="192e0-133">ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](http://msdn.microsoft.com/en-us/library/hh532803%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="192e0-134">在默认联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-134">Finds contacts in the default Contacts folder and/or Global Address List (GAL).</span></span> <span data-ttu-id="192e0-135">此方法可设置所返回的属性。</span><span class="sxs-lookup"><span data-stu-id="192e0-135">This method enables you to set the properties that are returned.</span></span>  <br/> |
|[<span data-ttu-id="192e0-136">ResolveName (String、 IEnumerable\<文件夹 Id\>，ResolveNameSearchLocation、 Boolean)</span><span class="sxs-lookup"><span data-stu-id="192e0-136">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)</span></span>](http://msdn.microsoft.com/en-us/library/dd636014%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="192e0-137">在指定的联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-137">Finds contacts in specified contact folders and/or the Global Address List (GAL).</span></span> <span data-ttu-id="192e0-138">您可以使用此方法将传递的搜索文件夹集合。</span><span class="sxs-lookup"><span data-stu-id="192e0-138">You can use this method to pass a collection of folders to search.</span></span> <span data-ttu-id="192e0-139">这使您可以查找联系人文件夹之外的默认联系人文件夹中。</span><span class="sxs-lookup"><span data-stu-id="192e0-139">This enables you to look in contact folders other than the default Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="192e0-140">ResolveName (String、 IEnumerable\<文件夹 Id\>，ResolveNameSearchLocation、 Boolean、 属性集)</span><span class="sxs-lookup"><span data-stu-id="192e0-140">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](http://msdn.microsoft.com/en-us/library/hh532581%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="192e0-141">在全局地址列表 (GAL) 和/或特定的联系人文件夹中查找联系人。</span><span class="sxs-lookup"><span data-stu-id="192e0-141">Finds contacts in the Global Address List (GAL) and/or in specific contact folders.</span></span> <span data-ttu-id="192e0-142">此方法可设置所返回的属性。</span><span class="sxs-lookup"><span data-stu-id="192e0-142">This method enables you to set the properties that are returned.</span></span>  <br/> |
   
<span data-ttu-id="192e0-143">让我们开始一个简单示例。</span><span class="sxs-lookup"><span data-stu-id="192e0-143">Let's start with a simple example.</span></span> <span data-ttu-id="192e0-144">下面的示例演示如何解决"dan"的文本字符串和输出找到的每个应聘者的姓名和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="192e0-144">The following example shows how to resolve the text string "dan" and output the name and email address of each candidate found.</span></span> <span data-ttu-id="192e0-145">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="192e0-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="192e0-146">响应返回最多 100 候选人，尽管可能有 100 多个潜在候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-146">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates.</span></span> <span data-ttu-id="192e0-147">若要确定是否已返回仅更多的候选人的前 100 个候选，检查[IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)对象中的值。</span><span class="sxs-lookup"><span data-stu-id="192e0-147">To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of [IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) in the [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="192e0-148">如果值为 true，没有其他可能候选人;如果值为 false，该方法仅返回前 100 的更多的潜在的候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-148">If the value is true, there are no more possible candidates; if the value is false, the method only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="192e0-149">如果您工作的大型组织，很可能的名称，如"dan"将返回 100 的候选项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="192e0-149">If you work in a large organization, it's likely that a name like "dan" will return the maximum number of 100 candidates.</span></span> <span data-ttu-id="192e0-150">为了减少返回的候选项的数量，限制了您在其中搜索。</span><span class="sxs-lookup"><span data-stu-id="192e0-150">To reduce the number of candidates returned, limit where you search.</span></span> <span data-ttu-id="192e0-151">下一个示例使用[ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx)枚举指定搜索范围以解析不明确名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-151">The next example uses the [ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) enumeration to specify where to search to resolve the ambiguous name.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="192e0-152">如果您将您的联系人存储中已知的联系人文件夹之外的文件夹中，使用重载的方法之一指定位置查找候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-152">If you store your contacts in a folder other than the well-known Contacts folder, use one of the overloaded methods to specify where to look for candidates.</span></span> <span data-ttu-id="192e0-153">下面的示例创建文件夹列表**ResolveName**方法基于文件夹 id。</span><span class="sxs-lookup"><span data-stu-id="192e0-153">The following example creates a folder list for the **ResolveName** method based on the folder ID.</span></span> <span data-ttu-id="192e0-154">为便于阅读缩短了**文件夹 Id** 。</span><span class="sxs-lookup"><span data-stu-id="192e0-154">The **FolderId** has been shortened for readability.</span></span> 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="192e0-155">如果应用筛选器并返回无候选人， [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)将包含零个条目。</span><span class="sxs-lookup"><span data-stu-id="192e0-155">If you apply filters and no candidates are returned, the [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) will contain zero entries.</span></span> <span data-ttu-id="192e0-156">您可以通过查看集合的[Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx)属性进行验证。</span><span class="sxs-lookup"><span data-stu-id="192e0-156">You can verify this by looking at the [Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) property of the collection.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a><span data-ttu-id="192e0-157">使用 EWS 解析模糊名称</span><span class="sxs-lookup"><span data-stu-id="192e0-157">Resolve ambiguous names by using EWS</span></span>
<span data-ttu-id="192e0-158"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="192e0-158"></span></span>

<span data-ttu-id="192e0-159">可以使用[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作来标识可能适合的不明确名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-159">You can use the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to identify possible candidates for an ambiguous name.</span></span> <span data-ttu-id="192e0-160">[UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx)元素包含您想要解析的不明确名称。</span><span class="sxs-lookup"><span data-stu-id="192e0-160">The [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) element contains the ambiguous name you want to resolve.</span></span> <span data-ttu-id="192e0-161">下面的示例演示如何以解析名称 Sadie。</span><span class="sxs-lookup"><span data-stu-id="192e0-161">The following example shows how to resolve the name Sadie.</span></span> <span data-ttu-id="192e0-162">这也是 EWS 托管 API 时您[使用 ResolveName 方法](#bk_EWSMA)，但前者使用不同的有效输出示例名称所使用的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="192e0-162">This is also the XML request that the EWS Managed API uses when you [use the ResolveName method](#bk_EWSMA), except that it uses a different name for valid output examples.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="192e0-163">响应返回最多 100 候选人，尽管可能有 100 个以上的潜在候选人，可确定是否已返回仅更多的候选人的前 100 个候选，检查[IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx)的值[ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)元素的属性。</span><span class="sxs-lookup"><span data-stu-id="192e0-163">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of the [IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) attribute of the [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="192e0-164">如果值为 true，没有其他可能候选人;如果值为 false，该操作将仅返回前 100 的更多的潜在的候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-164">If the value is true, there are no more possible candidates; if the value is false, the operation only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="192e0-165">下面的示例演示 XML 响应时找到一个候选。</span><span class="sxs-lookup"><span data-stu-id="192e0-165">The following example shows the XML response when one candidate is found.</span></span> <span data-ttu-id="192e0-166">请记住， [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)可以包含最多 100 个候选人，每个由[解决方案](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx)元素和及其子元素。</span><span class="sxs-lookup"><span data-stu-id="192e0-166">Remember, the [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) can contain up to 100 candidates, each one represented by the [Resolution](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) element and its child elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="192e0-167">您不总是将附带的不明确名称的候选人。</span><span class="sxs-lookup"><span data-stu-id="192e0-167">You're not always going to come up with candidates for your ambiguous name.</span></span> <span data-ttu-id="192e0-168">下面的示例演示 XML 响应中，为错误，，没有候选发现时。</span><span class="sxs-lookup"><span data-stu-id="192e0-168">The following example shows the XML response, as an error, when no candidates are found.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="192e0-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="192e0-169">See also</span></span>


- [<span data-ttu-id="192e0-170">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="192e0-170">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="192e0-171">通过使用 EWS 在 Exchange 2013 中展开通讯组</span><span class="sxs-lookup"><span data-stu-id="192e0-171">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

