---
title: ResolveNames 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: ResolveNames 操作解析不明确的电子邮件地址和显示名称。
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827162"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="e0676-103">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="e0676-103">ResolveNames operation</span></span>

<span data-ttu-id="e0676-104">**ResolveNames**操作解析不明确的电子邮件地址和显示名称。</span><span class="sxs-lookup"><span data-stu-id="e0676-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="e0676-105">使用 ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="e0676-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="e0676-106">此操作可用于验证别名并解析为适当的邮箱的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e0676-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="e0676-107">如果存在不明确的名称， **ResolveNames**操作响应将提供有关每个邮箱用户的信息，以便客户端应用程序可以解析名称。</span><span class="sxs-lookup"><span data-stu-id="e0676-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0676-108">注解</span><span class="sxs-lookup"><span data-stu-id="e0676-108">Remarks</span></span>

<span data-ttu-id="e0676-109">ResolveNames 响应返回最多 100 候选人。</span><span class="sxs-lookup"><span data-stu-id="e0676-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="e0676-110">返回 100 候选人应该是查找操作中遇到的第一个 100。</span><span class="sxs-lookup"><span data-stu-id="e0676-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="e0676-111">多值数组中保存前缀的路由类型，如 smtp 或 sip，与电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="e0676-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="e0676-112">无法解析的名称，例如"sip:User1@Contoso.com"的开头添加路由类型时， **ResolveNames**操作执行针对该数组的每个值的部分匹配。</span><span class="sxs-lookup"><span data-stu-id="e0676-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="e0676-113">如果不指定传送类型， **ResolveNames**将默认为 smtp 的路由类型、 匹配到主 smtp 地址属性，以及不搜索多值数组。</span><span class="sxs-lookup"><span data-stu-id="e0676-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="e0676-114">可以在单个请求中指定只有一个不明确的名称。</span><span class="sxs-lookup"><span data-stu-id="e0676-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="e0676-115">首先，搜索 active Directory，然后搜索用户的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="e0676-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="e0676-116">来自用户的联系人文件夹解析的项有一个非空**ItemId**属性，然后可以使用 GetItem 请求中。</span><span class="sxs-lookup"><span data-stu-id="e0676-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="e0676-117">如果是私人通讯组列表的 ID，然后它可在[ExpandDL 操作](expanddl-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="e0676-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="e0676-118">如果**ReturnFullContactData**属性设置为**true**，则找到**ResolveNames**操作的 Active Directory 条目将返回描述[联系人](contact.md)的其他属性。</span><span class="sxs-lookup"><span data-stu-id="e0676-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="e0676-119">**ReturnFullContactData**属性不会影响的联系人和专用返回的数据从用户的联系人文件夹的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="e0676-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="e0676-120">ResolveNames 请求示例</span><span class="sxs-lookup"><span data-stu-id="e0676-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="e0676-121">说明</span><span class="sxs-lookup"><span data-stu-id="e0676-121">Description</span></span>

<span data-ttu-id="e0676-122">**ResolveNames**请求的下面的示例演示如何解决用户的条目。</span><span class="sxs-lookup"><span data-stu-id="e0676-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="e0676-123">代码</span><span class="sxs-lookup"><span data-stu-id="e0676-123">Code</span></span>

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
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="e0676-124">注释</span><span class="sxs-lookup"><span data-stu-id="e0676-124">Comments</span></span>

<span data-ttu-id="e0676-125">对此请求的响应将返回"Jo"或"英里。"开头的所有条目</span><span class="sxs-lookup"><span data-stu-id="e0676-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="e0676-126">返回的项是公用邮箱、 公共和私有通讯组列表和联系人。</span><span class="sxs-lookup"><span data-stu-id="e0676-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0676-127">仅在默认的个人联系人文件夹中的联系人进行搜索。</span><span class="sxs-lookup"><span data-stu-id="e0676-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="e0676-128">以下是**ResolveNames**请求的可能结果：</span><span class="sxs-lookup"><span data-stu-id="e0676-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="e0676-129">不包含解析的实体的响应将返回**ResponseClass**属性值等于**错误**。</span><span class="sxs-lookup"><span data-stu-id="e0676-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="e0676-130">**MessageText**元素将包含"**未找到结果**"。</span><span class="sxs-lookup"><span data-stu-id="e0676-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="e0676-131">包含单个解析的实体的响应将返回**ResponseClass**属性值等于**成功**。</span><span class="sxs-lookup"><span data-stu-id="e0676-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="e0676-132">包含多个可能的实体的响应将返回**ResponseClass**属性值等于**警告**。</span><span class="sxs-lookup"><span data-stu-id="e0676-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="e0676-133">在这种情况下，实体无法解析为唯一标识。</span><span class="sxs-lookup"><span data-stu-id="e0676-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="e0676-134">**MessageText**元素将包含"找到多个结果。"</span><span class="sxs-lookup"><span data-stu-id="e0676-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="e0676-135">请求元素</span><span class="sxs-lookup"><span data-stu-id="e0676-135">Request elements</span></span>

<span data-ttu-id="e0676-136">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e0676-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e0676-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e0676-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="e0676-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="e0676-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="e0676-139">成功 ResolveNames 操作响应示例</span><span class="sxs-lookup"><span data-stu-id="e0676-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="e0676-140">说明</span><span class="sxs-lookup"><span data-stu-id="e0676-140">Description</span></span>

<span data-ttu-id="e0676-141">下面的示例演示对**ResolveNames**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="e0676-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e0676-142">代码</span><span class="sxs-lookup"><span data-stu-id="e0676-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
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

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="e0676-143">成功 ResolveNames 响应元素</span><span class="sxs-lookup"><span data-stu-id="e0676-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="e0676-144">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e0676-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e0676-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e0676-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e0676-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e0676-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="e0676-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e0676-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e0676-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e0676-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="e0676-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0676-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0676-150">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e0676-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="e0676-151">解决方法</span><span class="sxs-lookup"><span data-stu-id="e0676-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="e0676-152">Mailbox</span><span class="sxs-lookup"><span data-stu-id="e0676-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="e0676-153">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e0676-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="e0676-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e0676-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="e0676-155">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e0676-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="e0676-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="e0676-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="e0676-157">Contact</span><span class="sxs-lookup"><span data-stu-id="e0676-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="e0676-158">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="e0676-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="e0676-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="e0676-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="e0676-160">条目 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="e0676-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="e0676-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="e0676-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="e0676-162">ResolveNames 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="e0676-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="e0676-163">说明</span><span class="sxs-lookup"><span data-stu-id="e0676-163">Description</span></span>

<span data-ttu-id="e0676-164">下面的示例演示对**ResolveNames**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="e0676-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="e0676-165">尝试解析无法解析名称被导致错误。</span><span class="sxs-lookup"><span data-stu-id="e0676-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e0676-166">代码</span><span class="sxs-lookup"><span data-stu-id="e0676-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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

### <a name="error-response-elements"></a><span data-ttu-id="e0676-167">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="e0676-167">Error response elements</span></span>

<span data-ttu-id="e0676-168">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e0676-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="e0676-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e0676-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e0676-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e0676-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="e0676-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e0676-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e0676-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e0676-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="e0676-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="e0676-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e0676-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0676-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0676-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e0676-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="e0676-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0676-176">See also</span></span>



[<span data-ttu-id="e0676-177">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="e0676-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="e0676-178">使用名称解析</span><span class="sxs-lookup"><span data-stu-id="e0676-178">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

