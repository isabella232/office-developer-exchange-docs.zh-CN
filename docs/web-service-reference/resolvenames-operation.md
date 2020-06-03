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
description: ResolveNames 操作可解析不明确的电子邮件地址和显示名称。
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468276"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="40cf6-103">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="40cf6-103">ResolveNames operation</span></span>

<span data-ttu-id="40cf6-104">**ResolveNames**操作可解析不明确的电子邮件地址和显示名称。</span><span class="sxs-lookup"><span data-stu-id="40cf6-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="40cf6-105">使用 ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="40cf6-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="40cf6-106">此操作可用于验证别名并将显示名称解析为相应的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="40cf6-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="40cf6-107">如果存在不明确的名称， **ResolveNames**操作响应将提供有关每个邮箱用户的信息，以便客户端应用程序可以解析这些名称。</span><span class="sxs-lookup"><span data-stu-id="40cf6-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="40cf6-108">备注</span><span class="sxs-lookup"><span data-stu-id="40cf6-108">Remarks</span></span>

<span data-ttu-id="40cf6-109">ResolveNames 响应将返回最大为100个候选人。</span><span class="sxs-lookup"><span data-stu-id="40cf6-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="40cf6-110">返回的100候选项是在查找操作中遇到的第一个100。</span><span class="sxs-lookup"><span data-stu-id="40cf6-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="40cf6-111">带有前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。</span><span class="sxs-lookup"><span data-stu-id="40cf6-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="40cf6-112">当您在未解析名称的开头添加路由类型（如 "sip:User1@Contoso.com"）时， **ResolveNames**操作将对该数组的每个值执行部分匹配。</span><span class="sxs-lookup"><span data-stu-id="40cf6-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="40cf6-113">如果不指定路由类型， **ResolveNames**将默认为 smtp 的路由类型，将其与主 smtp 地址属性相匹配，而不会搜索多值数组。</span><span class="sxs-lookup"><span data-stu-id="40cf6-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="40cf6-114">在一个请求中只能指定一个不明确的名称。</span><span class="sxs-lookup"><span data-stu-id="40cf6-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="40cf6-115">先搜索 Active Directory，然后再搜索用户的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="40cf6-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="40cf6-116">从用户的联系人文件夹解析的条目具有非 null 的**ItemId**属性，该属性随后可在 GetItem 请求中使用。</span><span class="sxs-lookup"><span data-stu-id="40cf6-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="40cf6-117">如果是私有通讯组列表的 ID，则可在[ExpandDL 操作](expanddl-operation.md)中使用。</span><span class="sxs-lookup"><span data-stu-id="40cf6-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="40cf6-118">如果将**ReturnFullContactData**属性设置为**true**，则使用**ResolveNames**操作找到的 Active Directory 条目将返回描述[联系人](contact.md)的其他属性。</span><span class="sxs-lookup"><span data-stu-id="40cf6-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="40cf6-119">**ReturnFullContactData**属性不会影响用户的联系人文件夹中的联系人和私有通讯组列表返回的数据。</span><span class="sxs-lookup"><span data-stu-id="40cf6-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="40cf6-120">ResolveNames 请求示例</span><span class="sxs-lookup"><span data-stu-id="40cf6-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="40cf6-121">Description</span><span class="sxs-lookup"><span data-stu-id="40cf6-121">Description</span></span>

<span data-ttu-id="40cf6-122">以下示例的**ResolveNames**请求显示如何解析用户的输入。</span><span class="sxs-lookup"><span data-stu-id="40cf6-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="40cf6-123">代码</span><span class="sxs-lookup"><span data-stu-id="40cf6-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="40cf6-124">备注</span><span class="sxs-lookup"><span data-stu-id="40cf6-124">Comments</span></span>

<span data-ttu-id="40cf6-125">对此请求的响应将返回以 "Jo" 或 "Mi" 开头的所有条目。</span><span class="sxs-lookup"><span data-stu-id="40cf6-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="40cf6-126">返回的项目为公用邮箱、公用和私人通讯组列表和联系人。</span><span class="sxs-lookup"><span data-stu-id="40cf6-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="40cf6-127">仅搜索默认 "个人联系人" 文件夹中的联系人。</span><span class="sxs-lookup"><span data-stu-id="40cf6-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="40cf6-128">以下是**ResolveNames**请求的可能结果：</span><span class="sxs-lookup"><span data-stu-id="40cf6-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="40cf6-129">不包含已解析实体的响应将返回**ResponseClass**属性值等于**Error**。</span><span class="sxs-lookup"><span data-stu-id="40cf6-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="40cf6-130">**MessageText**元素将包含 "**找不到任何结果**"。</span><span class="sxs-lookup"><span data-stu-id="40cf6-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="40cf6-131">包含单个已解析实体的响应将返回一个等于**Success**的**ResponseClass**属性值。</span><span class="sxs-lookup"><span data-stu-id="40cf6-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="40cf6-132">包含多个可能的实体的响应将返回一个等于**警告**的**ResponseClass**属性值。</span><span class="sxs-lookup"><span data-stu-id="40cf6-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="40cf6-133">在这种情况下，无法将实体解析为唯一标识。</span><span class="sxs-lookup"><span data-stu-id="40cf6-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="40cf6-134">**MessageText**元素将包含 "找到多个结果"。</span><span class="sxs-lookup"><span data-stu-id="40cf6-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="40cf6-135">Request 元素</span><span class="sxs-lookup"><span data-stu-id="40cf6-135">Request elements</span></span>

<span data-ttu-id="40cf6-136">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="40cf6-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="40cf6-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="40cf6-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="40cf6-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="40cf6-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="40cf6-139">成功的 ResolveNames 操作响应示例</span><span class="sxs-lookup"><span data-stu-id="40cf6-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="40cf6-140">Description</span><span class="sxs-lookup"><span data-stu-id="40cf6-140">Description</span></span>

<span data-ttu-id="40cf6-141">下面的示例演示对**ResolveNames**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="40cf6-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="40cf6-142">代码</span><span class="sxs-lookup"><span data-stu-id="40cf6-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="40cf6-143">成功的 ResolveNames 响应元素</span><span class="sxs-lookup"><span data-stu-id="40cf6-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="40cf6-144">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="40cf6-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="40cf6-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="40cf6-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="40cf6-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="40cf6-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="40cf6-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="40cf6-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="40cf6-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="40cf6-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="40cf6-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="40cf6-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="40cf6-150">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="40cf6-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="40cf6-151">解决方案</span><span class="sxs-lookup"><span data-stu-id="40cf6-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="40cf6-152">邮箱</span><span class="sxs-lookup"><span data-stu-id="40cf6-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="40cf6-153">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="40cf6-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="40cf6-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="40cf6-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="40cf6-155">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="40cf6-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="40cf6-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="40cf6-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="40cf6-157">联系人</span><span class="sxs-lookup"><span data-stu-id="40cf6-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="40cf6-158">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="40cf6-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="40cf6-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="40cf6-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="40cf6-160">条目（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="40cf6-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="40cf6-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="40cf6-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="40cf6-162">ResolveNames 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="40cf6-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="40cf6-163">Description</span><span class="sxs-lookup"><span data-stu-id="40cf6-163">Description</span></span>

<span data-ttu-id="40cf6-164">下面的示例演示对**ResolveNames**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="40cf6-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="40cf6-165">错误是由尝试解析无法解析的名称导致的。</span><span class="sxs-lookup"><span data-stu-id="40cf6-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="40cf6-166">代码</span><span class="sxs-lookup"><span data-stu-id="40cf6-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="40cf6-167">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="40cf6-167">Error response elements</span></span>

<span data-ttu-id="40cf6-168">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="40cf6-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="40cf6-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="40cf6-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="40cf6-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="40cf6-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="40cf6-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="40cf6-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="40cf6-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="40cf6-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="40cf6-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="40cf6-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="40cf6-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="40cf6-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="40cf6-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="40cf6-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="40cf6-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40cf6-176">See also</span></span>



[<span data-ttu-id="40cf6-177">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="40cf6-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="40cf6-178">使用名称解析</span><span class="sxs-lookup"><span data-stu-id="40cf6-178">Using Name Resolution</span></span>](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

