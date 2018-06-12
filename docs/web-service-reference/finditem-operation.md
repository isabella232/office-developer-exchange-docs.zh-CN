---
title: FindItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: 查找信息 FindItem EWS 操作。
ms.openlocfilehash: b033ac2930981819a20f1336d40058a5f7c03b89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754347"
---
# <a name="finditem-operation"></a><span data-ttu-id="63703-103">FindItem Operation</span><span class="sxs-lookup"><span data-stu-id="63703-103">FindItem operation</span></span>

<span data-ttu-id="63703-104">查找有关**FindItem** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="63703-104">Find information about the **FindItem** EWS operation.</span></span> 
  
<span data-ttu-id="63703-105">**FindItem**操作搜索位于用户的邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="63703-105">The **FindItem** operation searches for items that are located in a user's mailbox.</span></span> <span data-ttu-id="63703-106">此操作提供了许多方式来筛选和搜索结果如何返回到呼叫者的格式。</span><span class="sxs-lookup"><span data-stu-id="63703-106">This operation provides many ways to filter and format how search results are returned to the caller.</span></span> 
  
## <a name="using-the-finditem-operation"></a><span data-ttu-id="63703-107">使用 FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="63703-107">Using the FindItem operation</span></span>

<span data-ttu-id="63703-108">**FindItem**操作请求提供了许多方法，用于搜索的邮箱和如何响应中返回的数据的格式。</span><span class="sxs-lookup"><span data-stu-id="63703-108">The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response.</span></span> <span data-ttu-id="63703-109">您可以指定以下**FindItem**请求中：</span><span class="sxs-lookup"><span data-stu-id="63703-109">You can specify the following in a **FindItem** request:</span></span> 
  
- <span data-ttu-id="63703-110">搜索是否浅表或软删除遍历。</span><span class="sxs-lookup"><span data-stu-id="63703-110">Whether the search is a shallow or soft-deleted traversal.</span></span> <span data-ttu-id="63703-111">指定这是必需的。</span><span class="sxs-lookup"><span data-stu-id="63703-111">Specifying this is required.</span></span> <span data-ttu-id="63703-112">请注意，再加上搜索限制软删除遍历将导致返回零项，即使有匹配的项目的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="63703-112">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.</span></span>
    
- <span data-ttu-id="63703-113">项目响应形状。</span><span class="sxs-lookup"><span data-stu-id="63703-113">The response shape of items.</span></span> <span data-ttu-id="63703-114">这标识响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="63703-114">This identifies the properties that are returned in the response.</span></span> <span data-ttu-id="63703-115">指定这是必需的。</span><span class="sxs-lookup"><span data-stu-id="63703-115">Specifying this is required.</span></span>
    
- <span data-ttu-id="63703-116">要从中执行搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="63703-116">The folders from which to perform the search.</span></span> <span data-ttu-id="63703-117">指定这是必需的。</span><span class="sxs-lookup"><span data-stu-id="63703-117">Specifying this is required.</span></span>
    
- <span data-ttu-id="63703-118">用于返回分页机制和视图类型页中查看数据。</span><span class="sxs-lookup"><span data-stu-id="63703-118">The paging mechanism and view types for returning view data in pages.</span></span> <span data-ttu-id="63703-119">指定这是可选的。</span><span class="sxs-lookup"><span data-stu-id="63703-119">Specifying this is optional.</span></span>
    
- <span data-ttu-id="63703-120">分组和对返回的项排序选项。</span><span class="sxs-lookup"><span data-stu-id="63703-120">Options for grouping and sorting the items that are returned.</span></span> <span data-ttu-id="63703-121">指定这是可选的。</span><span class="sxs-lookup"><span data-stu-id="63703-121">Specifying this is optional.</span></span>
    
- <span data-ttu-id="63703-122">搜索限制或高级查询语法 (AQS) 字符串用于筛选返回的项目。</span><span class="sxs-lookup"><span data-stu-id="63703-122">Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned.</span></span> <span data-ttu-id="63703-123">有关使用 AQS 内容索引的搜索的详细信息，请参阅[QueryString （字符串）](querystring-string.md)。</span><span class="sxs-lookup"><span data-stu-id="63703-123">For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md).</span></span> <span data-ttu-id="63703-124">指定这是可选的。</span><span class="sxs-lookup"><span data-stu-id="63703-124">Specifying this is optional.</span></span>
    
- <span data-ttu-id="63703-125">响应中返回的项的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="63703-125">The sort order for items returned in the response.</span></span> <span data-ttu-id="63703-126">指定这是可选的。</span><span class="sxs-lookup"><span data-stu-id="63703-126">Specifying this is optional.</span></span>
    
<span data-ttu-id="63703-127">**FindItem**操作返回仅第一个 512 个字节的任何流式属性。</span><span class="sxs-lookup"><span data-stu-id="63703-127">The **FindItem** operation returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="63703-128">对于 Unicode，它使用以 null 结尾的 Unicode 字符串中返回的前 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="63703-128">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span> <span data-ttu-id="63703-129">它并不返回任何邮件正文格式或收件人列表。</span><span class="sxs-lookup"><span data-stu-id="63703-129">It does not return any of the message body formats or the recipient lists.</span></span> <span data-ttu-id="63703-130">**FindItem**将返回收件人摘要。</span><span class="sxs-lookup"><span data-stu-id="63703-130">**FindItem** will return a recipient summary.</span></span> <span data-ttu-id="63703-131">可以使用[GetItem 操作](getitem-operation.md)获取项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="63703-131">You can use the [GetItem operation](getitem-operation.md) to get the details of an item.</span></span> 
  
 <span data-ttu-id="63703-132">**FindItem**返回仅[Name (EmailAddressType)](name-emailaddresstype.md)元素，并不会返回以下字段的[邮箱](mailbox.md)元素中的[电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md)元素：</span><span class="sxs-lookup"><span data-stu-id="63703-132">**FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields:</span></span> 
  
- <span data-ttu-id="63703-133">邮件[从](from.md)字段</span><span class="sxs-lookup"><span data-stu-id="63703-133">The [From](from.md) field for messages</span></span> 
    
- <span data-ttu-id="63703-134">邮件[发件人](sender.md)字段</span><span class="sxs-lookup"><span data-stu-id="63703-134">The [Sender](sender.md) field for messages</span></span> 
    
- <span data-ttu-id="63703-135">日历项目的[组织者](organizer.md)字段</span><span class="sxs-lookup"><span data-stu-id="63703-135">The [Organizer](organizer.md) field for calendar items</span></span> 
    
> [!NOTE]
> <span data-ttu-id="63703-136">**FindItem**操作可以[CalendarView](calendarview.md)元素中返回结果。</span><span class="sxs-lookup"><span data-stu-id="63703-136">The **FindItem** operation can return results in a [CalendarView](calendarview.md) element.</span></span> <span data-ttu-id="63703-137">**CalendarView**元素可返回单个日历项和定期会议的所有匹配项。</span><span class="sxs-lookup"><span data-stu-id="63703-137">The **CalendarView** element returns single calendar items and all occurrences of recurring meetings.</span></span> <span data-ttu-id="63703-138">如果未使用的**CalendarView**元素，则返回单个日历项和定期母版日历项。</span><span class="sxs-lookup"><span data-stu-id="63703-138">If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned.</span></span> <span data-ttu-id="63703-139">如果未使用的**CalendarView**元素，必须从定期主扩展发生次数。</span><span class="sxs-lookup"><span data-stu-id="63703-139">The occurrences must be expanded from the recurring master if a **CalendarView** element is not used.</span></span> 
  
<span data-ttu-id="63703-140">**FindItem**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="63703-140">The **FindItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="63703-141">**表 1。FindItem 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="63703-141">**Table 1. FindItem operation SOAP headers**</span></span>

|<span data-ttu-id="63703-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="63703-142">**Header**</span></span>|<span data-ttu-id="63703-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="63703-143">**Element**</span></span>|<span data-ttu-id="63703-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="63703-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63703-145">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="63703-145">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="63703-146">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="63703-146">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="63703-147">指定在从服务器中，以秒为单位，或以毫秒为单位的响应中的数据/时间值的分辨率。</span><span class="sxs-lookup"><span data-stu-id="63703-147">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span> <span data-ttu-id="63703-148">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="63703-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="63703-149">**模拟**</span><span class="sxs-lookup"><span data-stu-id="63703-149">**Impersonation**</span></span> <br/> |[<span data-ttu-id="63703-150">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="63703-150">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="63703-151">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="63703-151">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="63703-152">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="63703-152">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="63703-153">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="63703-153">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="63703-154">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="63703-154">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="63703-155">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="63703-155">Identifies the RFC3066 culture to be used to access the mailbox.</span></span> <span data-ttu-id="63703-156">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="63703-156">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="63703-157">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="63703-157">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="63703-158">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="63703-158">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="63703-159">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="63703-159">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="63703-160">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="63703-160">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="63703-161">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="63703-161">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="63703-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="63703-162">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="63703-163">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="63703-163">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="63703-164">这是适用于响应。</span><span class="sxs-lookup"><span data-stu-id="63703-164">This is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="63703-165">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="63703-165">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="63703-166">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="63703-166">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="63703-167">确定要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="63703-167">Identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="63703-168">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="63703-168">This is applicable to a request.</span></span>  <br/> |
   
## <a name="finditem-operation-request-example"></a><span data-ttu-id="63703-169">FindItem 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="63703-169">FindItem operation request example</span></span>

<span data-ttu-id="63703-170">**FindItem**请求的下面的示例演示如何获取由位于已删除邮件文件夹的项目的[BaseShape](baseshape.md)元素**IdOnly**枚举定义的项标识符。</span><span class="sxs-lookup"><span data-stu-id="63703-170">The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

<span data-ttu-id="63703-171">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="63703-171">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="63703-172">FindItem</span><span class="sxs-lookup"><span data-stu-id="63703-172">FindItem</span></span>](finditem.md)
    
- [<span data-ttu-id="63703-173">ItemShape</span><span class="sxs-lookup"><span data-stu-id="63703-173">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="63703-174">BaseShape</span><span class="sxs-lookup"><span data-stu-id="63703-174">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="63703-175">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="63703-175">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="63703-176">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="63703-176">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="63703-177">对于**FindItem**请求消息的更多选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="63703-177">For more options for a **FindItem** request message, explore the schema hierarchy.</span></span> <span data-ttu-id="63703-178">启动[FindItem](finditem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="63703-178">Start at the [FindItem](finditem.md) element.</span></span> 
  
## <a name="successful-finditem-operation-response"></a><span data-ttu-id="63703-179">成功 FindItem 操作响应</span><span class="sxs-lookup"><span data-stu-id="63703-179">Successful FindItem operation response</span></span>

<span data-ttu-id="63703-180">下面的示例演示对**FindItem**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="63703-180">The following example shows a successful response to the **FindItem** request.</span></span> 
  
<span data-ttu-id="63703-181">[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非通过 EWS 架构强类型的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="63703-181">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema.</span></span> <span data-ttu-id="63703-182">如 IPM 的项目。共享和[消息](message-ex15websvcsotherref.md)元素以返回 IPM.InfoPath。</span><span class="sxs-lookup"><span data-stu-id="63703-182">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="63703-183">Exchange 不在响应中返回基本的[Item](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="63703-183">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="63703-184">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="63703-184">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="63703-185">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="63703-185">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="63703-186">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="63703-186">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="63703-187">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="63703-187">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="63703-188">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="63703-188">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="63703-189">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="63703-189">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="63703-190">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="63703-190">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="63703-191">Items</span><span class="sxs-lookup"><span data-stu-id="63703-191">Items</span></span>](items.md)
    
- [<span data-ttu-id="63703-192">Message</span><span class="sxs-lookup"><span data-stu-id="63703-192">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="63703-193">ItemId</span><span class="sxs-lookup"><span data-stu-id="63703-193">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="63703-194">**FindItem**响应消息的更多选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="63703-194">For more options for a **FindItem** response message, explore the schema hierarchy.</span></span> <span data-ttu-id="63703-195">启动[FindItemResponse](finditemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="63703-195">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="finditem-operation-error-response"></a><span data-ttu-id="63703-196">FindItem 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="63703-196">FindItem operation error response</span></span>

<span data-ttu-id="63703-197">下面的示例演示对**FindItem**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="63703-197">The following example shows an error response to a **FindItem** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="63703-198">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="63703-198">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="63703-199">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="63703-199">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="63703-200">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="63703-200">FindItemResponse</span></span>](finditemresponse.md)
    
- [<span data-ttu-id="63703-201">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="63703-201">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="63703-202">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="63703-202">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
    
- [<span data-ttu-id="63703-203">MessageText</span><span class="sxs-lookup"><span data-stu-id="63703-203">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="63703-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="63703-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="63703-205">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="63703-205">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="63703-206">**FindItem**错误响应消息的更多选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="63703-206">For more options for a **FindItem** error response message, explore the schema hierarchy.</span></span> <span data-ttu-id="63703-207">启动[FindItemResponse](finditemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="63703-207">Start at the [FindItemResponse](finditemresponse.md) element.</span></span> 
  
## <a name="version-differences"></a><span data-ttu-id="63703-208">版本差异</span><span class="sxs-lookup"><span data-stu-id="63703-208">Version differences</span></span>

<span data-ttu-id="63703-209">主要版本 15 开头和结尾的 Exchange 版本生成 15.0.898.11 返回**FindItem**操作用于存档邮箱中搜索多个文件夹时，此 ErrorInvalidOperation 值[ResponseCode](responsecode.md)元素中。</span><span class="sxs-lookup"><span data-stu-id="63703-209">Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63703-210">另请参阅</span><span class="sxs-lookup"><span data-stu-id="63703-210">See also</span></span>

- [<span data-ttu-id="63703-211">查找项目</span><span class="sxs-lookup"><span data-stu-id="63703-211">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [<span data-ttu-id="63703-212">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="63703-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
    
- <span data-ttu-id="63703-213">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="63703-213">**FindItemType**</span></span>
    

