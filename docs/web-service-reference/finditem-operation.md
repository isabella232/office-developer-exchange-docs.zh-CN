---
title: FindItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: 查找有关 FindItem EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 499d1ee80ef323c883fa86eb125d8c037fb37d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462554"
---
# <a name="finditem-operation"></a><span data-ttu-id="6ca20-103">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="6ca20-103">FindItem operation</span></span>

<span data-ttu-id="6ca20-104">查找有关**FindItem** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="6ca20-104">Find information about the **FindItem** EWS operation.</span></span> 
  
<span data-ttu-id="6ca20-105">**FindItem**操作将搜索位于用户邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="6ca20-105">The **FindItem** operation searches for items that are located in a user's mailbox.</span></span> <span data-ttu-id="6ca20-106">此操作提供了多种方法来筛选和设置搜索结果返回给呼叫者的方式。</span><span class="sxs-lookup"><span data-stu-id="6ca20-106">This operation provides many ways to filter and format how search results are returned to the caller.</span></span> 
  
## <a name="using-the-finditem-operation"></a><span data-ttu-id="6ca20-107">使用 FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="6ca20-107">Using the FindItem operation</span></span>

<span data-ttu-id="6ca20-108">**FindItem**操作请求提供了多种方法来搜索邮箱并设置数据在响应中的返回方式。</span><span class="sxs-lookup"><span data-stu-id="6ca20-108">The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response.</span></span> <span data-ttu-id="6ca20-109">您可以在**FindItem**请求中指定以下内容：</span><span class="sxs-lookup"><span data-stu-id="6ca20-109">You can specify the following in a **FindItem** request:</span></span> 
  
- <span data-ttu-id="6ca20-110">搜索是浅表遍历还是软删除遍历。</span><span class="sxs-lookup"><span data-stu-id="6ca20-110">Whether the search is a shallow or soft-deleted traversal.</span></span> <span data-ttu-id="6ca20-111">指定此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-111">Specifying this is required.</span></span> <span data-ttu-id="6ca20-112">请注意，与搜索限制组合在一起的软删除的遍历将导致返回零个项目，即使存在与搜索条件匹配的项目也是如此。</span><span class="sxs-lookup"><span data-stu-id="6ca20-112">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.</span></span>
    
- <span data-ttu-id="6ca20-113">项目的响应形状。</span><span class="sxs-lookup"><span data-stu-id="6ca20-113">The response shape of items.</span></span> <span data-ttu-id="6ca20-114">这标识响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="6ca20-114">This identifies the properties that are returned in the response.</span></span> <span data-ttu-id="6ca20-115">指定此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-115">Specifying this is required.</span></span>
    
- <span data-ttu-id="6ca20-116">要从中执行搜索的文件夹。</span><span class="sxs-lookup"><span data-stu-id="6ca20-116">The folders from which to perform the search.</span></span> <span data-ttu-id="6ca20-117">指定此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-117">Specifying this is required.</span></span>
    
- <span data-ttu-id="6ca20-118">页面中返回视图数据的分页机制和视图类型。</span><span class="sxs-lookup"><span data-stu-id="6ca20-118">The paging mechanism and view types for returning view data in pages.</span></span> <span data-ttu-id="6ca20-119">指定此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-119">Specifying this is optional.</span></span>
    
- <span data-ttu-id="6ca20-120">用于对返回的项进行分组和排序的选项。</span><span class="sxs-lookup"><span data-stu-id="6ca20-120">Options for grouping and sorting the items that are returned.</span></span> <span data-ttu-id="6ca20-121">指定此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-121">Specifying this is optional.</span></span>
    
- <span data-ttu-id="6ca20-122">用于筛选返回的项目的搜索限制或高级查询语法（AQS）字符串。</span><span class="sxs-lookup"><span data-stu-id="6ca20-122">Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned.</span></span> <span data-ttu-id="6ca20-123">有关使用 AQS 进行内容索引搜索的详细信息，请参阅[QueryString （String）](querystring-string.md)。</span><span class="sxs-lookup"><span data-stu-id="6ca20-123">For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md).</span></span> <span data-ttu-id="6ca20-124">指定此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-124">Specifying this is optional.</span></span>
    
- <span data-ttu-id="6ca20-125">响应中返回的项目的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="6ca20-125">The sort order for items returned in the response.</span></span> <span data-ttu-id="6ca20-126">指定此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6ca20-126">Specifying this is optional.</span></span>
    
<span data-ttu-id="6ca20-127">**FindItem**操作仅返回任何 streamable 属性的前512个字节。</span><span class="sxs-lookup"><span data-stu-id="6ca20-127">The **FindItem** operation returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="6ca20-128">对于 Unicode，它通过使用以 null 结尾的 Unicode 字符串返回前255个字符。</span><span class="sxs-lookup"><span data-stu-id="6ca20-128">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span> <span data-ttu-id="6ca20-129">它不会返回任何邮件正文格式或收件人列表。</span><span class="sxs-lookup"><span data-stu-id="6ca20-129">It does not return any of the message body formats or the recipient lists.</span></span> <span data-ttu-id="6ca20-130">**FindItem**将返回收件人摘要。</span><span class="sxs-lookup"><span data-stu-id="6ca20-130">**FindItem** will return a recipient summary.</span></span> <span data-ttu-id="6ca20-131">您可以使用[GetItem 操作](getitem-operation.md)来获取项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6ca20-131">You can use the [GetItem operation](getitem-operation.md) to get the details of an item.</span></span> 
  
 <span data-ttu-id="6ca20-132">**FindItem**仅返回[Name （EmailAddressType）](name-emailaddresstype.md)元素，并且不会返回以下字段的[邮箱](mailbox.md)元素中的[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)元素：</span><span class="sxs-lookup"><span data-stu-id="6ca20-132">**FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields:</span></span> 
  
- <span data-ttu-id="6ca20-133">邮件的 "[发件人](from.md)" 字段</span><span class="sxs-lookup"><span data-stu-id="6ca20-133">The [From](from.md) field for messages</span></span> 
    
- <span data-ttu-id="6ca20-134">邮件的 "[发件人](sender.md)" 字段</span><span class="sxs-lookup"><span data-stu-id="6ca20-134">The [Sender](sender.md) field for messages</span></span> 
    
- <span data-ttu-id="6ca20-135">日历项目的 "[组织者](organizer.md)" 字段</span><span class="sxs-lookup"><span data-stu-id="6ca20-135">The [Organizer](organizer.md) field for calendar items</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6ca20-136">**FindItem**操作可以返回[CalendarView](calendarview.md)元素中的结果。</span><span class="sxs-lookup"><span data-stu-id="6ca20-136">The **FindItem** operation can return results in a [CalendarView](calendarview.md) element.</span></span> <span data-ttu-id="6ca20-137">**CalendarView**元素返回单个日历项目和定期会议的所有事件。</span><span class="sxs-lookup"><span data-stu-id="6ca20-137">The **CalendarView** element returns single calendar items and all occurrences of recurring meetings.</span></span> <span data-ttu-id="6ca20-138">如果未使用**CalendarView**元素，则将返回单个日历项目和定期主日历项目。</span><span class="sxs-lookup"><span data-stu-id="6ca20-138">If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned.</span></span> <span data-ttu-id="6ca20-139">如果未使用**CalendarView**元素，则必须从定期母版展开此事件。</span><span class="sxs-lookup"><span data-stu-id="6ca20-139">The occurrences must be expanded from the recurring master if a **CalendarView** element is not used.</span></span> 
  
<span data-ttu-id="6ca20-140">**FindItem**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="6ca20-140">The **FindItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="6ca20-141">**表1。FindItem 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="6ca20-141">**Table 1. FindItem operation SOAP headers**</span></span>

|<span data-ttu-id="6ca20-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="6ca20-142">**Header**</span></span>|<span data-ttu-id="6ca20-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ca20-143">**Element**</span></span>|<span data-ttu-id="6ca20-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ca20-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ca20-145">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="6ca20-145">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="6ca20-146">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="6ca20-146">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="6ca20-147">指定对来自服务器的响应中的数据/时间值的解析（以秒或毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="6ca20-147">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span> <span data-ttu-id="6ca20-148">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="6ca20-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6ca20-149">**模拟**</span><span class="sxs-lookup"><span data-stu-id="6ca20-149">**Impersonation**</span></span> <br/> |[<span data-ttu-id="6ca20-150">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="6ca20-150">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="6ca20-151">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="6ca20-151">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="6ca20-152">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="6ca20-152">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6ca20-153">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="6ca20-153">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="6ca20-154">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="6ca20-154">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="6ca20-155">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="6ca20-155">Identifies the RFC3066 culture to be used to access the mailbox.</span></span> <span data-ttu-id="6ca20-156">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="6ca20-156">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6ca20-157">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="6ca20-157">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="6ca20-158">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6ca20-158">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6ca20-159">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="6ca20-159">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="6ca20-160">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="6ca20-160">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6ca20-161">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="6ca20-161">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="6ca20-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6ca20-162">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6ca20-163">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="6ca20-163">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="6ca20-164">这适用于响应。</span><span class="sxs-lookup"><span data-stu-id="6ca20-164">This is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="6ca20-165">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="6ca20-165">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="6ca20-166">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="6ca20-166">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="6ca20-167">标识要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="6ca20-167">Identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="6ca20-168">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="6ca20-168">This is applicable to a request.</span></span>  <br/> |
   
## <a name="finditem-operation-request-example"></a><span data-ttu-id="6ca20-169">FindItem 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="6ca20-169">FindItem operation request example</span></span>

<span data-ttu-id="6ca20-170">下面的**FindItem**请求示例演示如何获取由[BaseShape](baseshape.md)元素的**IdOnly**枚举定义的项标识符，这些项是在 "已删除的项目" 文件夹中找到的项。</span><span class="sxs-lookup"><span data-stu-id="6ca20-170">The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6ca20-171">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6ca20-171">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="6ca20-172">FindItem</span><span class="sxs-lookup"><span data-stu-id="6ca20-172">FindItem</span></span>](finditem.md)
    
- [<span data-ttu-id="6ca20-173">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6ca20-173">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="6ca20-174">BaseShape</span><span class="sxs-lookup"><span data-stu-id="6ca20-174">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="6ca20-175">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="6ca20-175">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="6ca20-176">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="6ca20-176">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="6ca20-177">有关**FindItem**请求消息的更多选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="6ca20-177">For more options for a **FindItem** request message, explore the schema hierarchy.</span></span> <span data-ttu-id="6ca20-178">从[FindItem](finditem.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="6ca20-178">Start at the [FindItem](finditem.md) element.</span></span> 
  
## <a name="successful-finditem-operation-response"></a><span data-ttu-id="6ca20-179">成功的 FindItem 操作响应</span><span class="sxs-lookup"><span data-stu-id="6ca20-179">Successful FindItem operation response</span></span>

<span data-ttu-id="6ca20-180">下面的示例演示对**FindItem**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="6ca20-180">The following example shows a successful response to the **FindItem** request.</span></span> 
  
<span data-ttu-id="6ca20-181">[Message](message-ex15websvcsotherref.md)元素表示由 EWS 架构不强类型化的电子邮件和其他所有项目。</span><span class="sxs-lookup"><span data-stu-id="6ca20-181">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema.</span></span> <span data-ttu-id="6ca20-182">项目，如 IPM。共享和 IPM. InfoPath 以[邮件](message-ex15websvcsotherref.md)元素的形式返回。</span><span class="sxs-lookup"><span data-stu-id="6ca20-182">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="6ca20-183">Exchange 不会在响应中返回基本[项目](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="6ca20-183">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6ca20-184">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6ca20-184">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="6ca20-185">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6ca20-185">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6ca20-186">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="6ca20-186">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="6ca20-187">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6ca20-187">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6ca20-188">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6ca20-188">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="6ca20-189">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6ca20-189">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6ca20-190">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="6ca20-190">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="6ca20-191">Items</span><span class="sxs-lookup"><span data-stu-id="6ca20-191">Items</span></span>](items.md)
    
- [<span data-ttu-id="6ca20-192">消息</span><span class="sxs-lookup"><span data-stu-id="6ca20-192">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6ca20-193">ItemId</span><span class="sxs-lookup"><span data-stu-id="6ca20-193">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="6ca20-194">有关**FindItem**响应消息的更多选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="6ca20-194">For more options for a **FindItem** response message, explore the schema hierarchy.</span></span> <span data-ttu-id="6ca20-195">从[FindItemResponse](finditemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="6ca20-195">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="finditem-operation-error-response"></a><span data-ttu-id="6ca20-196">FindItem 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="6ca20-196">FindItem operation error response</span></span>

<span data-ttu-id="6ca20-197">下面的示例演示对**FindItem**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="6ca20-197">The following example shows an error response to a **FindItem** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6ca20-198">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6ca20-198">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="6ca20-199">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6ca20-199">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6ca20-200">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="6ca20-200">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="6ca20-201">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6ca20-201">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6ca20-202">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6ca20-202">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="6ca20-203">MessageText</span><span class="sxs-lookup"><span data-stu-id="6ca20-203">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="6ca20-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6ca20-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6ca20-205">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6ca20-205">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="6ca20-206">有关**FindItem**错误响应消息的更多选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="6ca20-206">For more options for a **FindItem** error response message, explore the schema hierarchy.</span></span> <span data-ttu-id="6ca20-207">从[FindItemResponse](finditemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="6ca20-207">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="version-differences"></a><span data-ttu-id="6ca20-208">版本差异</span><span class="sxs-lookup"><span data-stu-id="6ca20-208">Version differences</span></span>

<span data-ttu-id="6ca20-209">如果使用**FindItem**操作在存档邮箱中搜索多个文件夹，则在[ResponseCode](responsecode.md)元素中，从主要版本15开始并以 "生成 15.0.898.11" 结尾的 Exchange 版本将返回 ErrorInvalidOperation 值。</span><span class="sxs-lookup"><span data-stu-id="6ca20-209">Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ca20-210">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ca20-210">See also</span></span>

- [<span data-ttu-id="6ca20-211">查找项目</span><span class="sxs-lookup"><span data-stu-id="6ca20-211">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [<span data-ttu-id="6ca20-212">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6ca20-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
    
- <span data-ttu-id="6ca20-213">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="6ca20-213">**FindItemType**</span></span>
    

