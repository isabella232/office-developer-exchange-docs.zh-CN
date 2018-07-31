---
title: ExpandDL 操作
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: ExpandDL 操作公开完整的通讯组列表成员身份。
ms.openlocfilehash: 4af6198ff15407b7fb71cdb4010ff6ce035460d0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353740"
---
# <a name="expanddl-operation"></a><span data-ttu-id="70ba3-103">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="70ba3-103">ExpandDL operation</span></span>

<span data-ttu-id="70ba3-104">ExpandDL 操作公开完整的通讯组列表成员身份。</span><span class="sxs-lookup"><span data-stu-id="70ba3-104">The ExpandDL operation exposes the full membership of distribution lists.</span></span>
  
## <a name="using-the-expanddl-web-method"></a><span data-ttu-id="70ba3-105">使用 ExpandDL Web 方法</span><span class="sxs-lookup"><span data-stu-id="70ba3-105">Using the ExpandDL Web Method</span></span>

<span data-ttu-id="70ba3-106">ExpandDL 操作使用位于 Exchange.asmx Web 服务。</span><span class="sxs-lookup"><span data-stu-id="70ba3-106">The ExpandDL operation uses the Web service that is located in Exchange.asmx.</span></span> <span data-ttu-id="70ba3-107">此 Web 服务方法接受是公共通讯组列表扩展的[电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md)子元素或专用的扩展[ItemId](itemid.md)子元素可以包含一个[邮箱](mailbox.md)元素通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-107">This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list.</span></span> 
  
<span data-ttu-id="70ba3-108">公用通讯组列表可以展开使用下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="70ba3-108">Public distribution lists can be expanded by using one of the following:</span></span>
  
1. <span data-ttu-id="70ba3-109">通讯组列表别名</span><span class="sxs-lookup"><span data-stu-id="70ba3-109">Distribution list alias</span></span>
    
2. <span data-ttu-id="70ba3-110">简单邮件传输协议 (SMTP) 地址</span><span class="sxs-lookup"><span data-stu-id="70ba3-110">The Simple Mail Transfer Protocol (SMTP) address</span></span>
    
3. <span data-ttu-id="70ba3-111">X400</span><span class="sxs-lookup"><span data-stu-id="70ba3-111">X400</span></span>
    
4. <span data-ttu-id="70ba3-112">X500</span><span class="sxs-lookup"><span data-stu-id="70ba3-112">X500</span></span>
    
5. <span data-ttu-id="70ba3-113">Exchange 旧版地址</span><span class="sxs-lookup"><span data-stu-id="70ba3-113">Exchange Legacy address</span></span>
    
6. <span data-ttu-id="70ba3-114">通讯组列表名称</span><span class="sxs-lookup"><span data-stu-id="70ba3-114">The distribution list name</span></span>
    
7. <span data-ttu-id="70ba3-115">显示名称</span><span class="sxs-lookup"><span data-stu-id="70ba3-115">The display name</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="70ba3-116">显示名称不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="70ba3-116">Display names are not unique.</span></span> <span data-ttu-id="70ba3-117">多个帐户可以共享相同的显示名称。</span><span class="sxs-lookup"><span data-stu-id="70ba3-117">Multiple accounts can share the same display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70ba3-118">说明</span><span class="sxs-lookup"><span data-stu-id="70ba3-118">Remarks</span></span>

<span data-ttu-id="70ba3-119">不支持递归扩展。</span><span class="sxs-lookup"><span data-stu-id="70ba3-119">Recursive expansion is not supported.</span></span> <span data-ttu-id="70ba3-120">可以在单个呼叫中展开只有一个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-120">Only one distribution list can be expanded in a single call.</span></span> <span data-ttu-id="70ba3-121">如果多个通讯组列表匹配条件，Web 服务报告的错误。</span><span class="sxs-lookup"><span data-stu-id="70ba3-121">If more than one distribution list match the criteria, the Web service reports an error.</span></span> <span data-ttu-id="70ba3-122">客户端应用程序可以使用模糊名称解析 (ANR) 以查找不明确的通讯组列表，然后选择所需的通讯组列表的正确的电子邮件地址作为参数用于[ExpandDL 操作](expanddl-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="70ba3-122">A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="70ba3-123">有关详细信息，请参阅[ResolveNames 操作](resolvenames-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="70ba3-123">For more information, see [ResolveNames operation](resolvenames-operation.md).</span></span>
  
<span data-ttu-id="70ba3-124">公用通讯组列表在 Active Directory 中的位置。</span><span class="sxs-lookup"><span data-stu-id="70ba3-124">Public distribution lists are located in Active Directory.</span></span> <span data-ttu-id="70ba3-125">它们可以是任何已启用邮件的或动态通讯组。</span><span class="sxs-lookup"><span data-stu-id="70ba3-125">They can be any mail-enabled or dynamic distribution group.</span></span> <span data-ttu-id="70ba3-126">不应从通讯簿中隐藏组和每个成员都应具有一个非空电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="70ba3-126">The group should not be hidden from the address list and each member should have a non-empty e-mail address.</span></span> <span data-ttu-id="70ba3-127">通讯组列表的成员可以是启用邮件的用户和联系人、 公用文件夹和已启用邮件的通讯组列表和动态组。</span><span class="sxs-lookup"><span data-stu-id="70ba3-127">Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.</span></span>
  
<span data-ttu-id="70ba3-128">私人通讯组列表位于用户邮箱的联系人文件夹中。</span><span class="sxs-lookup"><span data-stu-id="70ba3-128">Private distribution lists are located in the Contacts folder of a user's mailbox.</span></span> <span data-ttu-id="70ba3-129">私人通讯组列表没有电子邮件地址，因此其存储项标识符的 ExpandDL 请求中使用。</span><span class="sxs-lookup"><span data-stu-id="70ba3-129">Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request.</span></span> <span data-ttu-id="70ba3-130">私有通讯组列表成员可以是任何启用邮件的用户、 联系人或从 Active Directory 通讯组列表或联系人或私有通讯组列表从用户的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="70ba3-130">Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.</span></span>
  
<span data-ttu-id="70ba3-131">联系人或私人通讯组列表，在响应中返回的项标识符。</span><span class="sxs-lookup"><span data-stu-id="70ba3-131">For contacts or private distribution lists, the item identifiers are returned in the response.</span></span> <span data-ttu-id="70ba3-132">这可以用于获取有关对象的信息或以展开私有通讯组列表中的成员身份。</span><span class="sxs-lookup"><span data-stu-id="70ba3-132">This can be used to get information about the object or to expand membership in a private distribution list.</span></span>
  
## <a name="expanddl-private-distribution-list-request-example"></a><span data-ttu-id="70ba3-133">ExpandDL 私有通讯组列表请求示例</span><span class="sxs-lookup"><span data-stu-id="70ba3-133">ExpandDL Private Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="70ba3-134">说明</span><span class="sxs-lookup"><span data-stu-id="70ba3-134">Description</span></span>

<span data-ttu-id="70ba3-135">ExpandDL 请求的下面的示例演示如何以形成展开私有通讯组列表的请求。</span><span class="sxs-lookup"><span data-stu-id="70ba3-135">The following example of an ExpandDL request shows how to form a request to expand a private distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="70ba3-136">代码</span><span class="sxs-lookup"><span data-stu-id="70ba3-136">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="70ba3-137">注释</span><span class="sxs-lookup"><span data-stu-id="70ba3-137">Comments</span></span>

<span data-ttu-id="70ba3-138">若要展开私有通讯组列表，则[邮箱](mailbox.md)元素将包含该[ItemId](itemid.md)元素标识用户的邮箱中的私人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-138">To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox.</span></span> 
  
## <a name="expanddl-public-distribution-list-request-example"></a><span data-ttu-id="70ba3-139">ExpandDL 公用通讯组列表请求示例</span><span class="sxs-lookup"><span data-stu-id="70ba3-139">ExpandDL Public Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="70ba3-140">说明</span><span class="sxs-lookup"><span data-stu-id="70ba3-140">Description</span></span>

<span data-ttu-id="70ba3-141">ExpandDL 请求的下面的示例演示如何以形成展开公用通讯组列表的请求。</span><span class="sxs-lookup"><span data-stu-id="70ba3-141">The following example of an ExpandDL request shows how to form a request to expand a public distribution list.</span></span> <span data-ttu-id="70ba3-142">该示例演示如何使用以展开通讯组列表的显示名称。</span><span class="sxs-lookup"><span data-stu-id="70ba3-142">The example shows the use of a display name to expand a distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="70ba3-143">代码</span><span class="sxs-lookup"><span data-stu-id="70ba3-143">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="70ba3-144">注释</span><span class="sxs-lookup"><span data-stu-id="70ba3-144">Comments</span></span>

<span data-ttu-id="70ba3-145">对此请求的响应将包含标识通讯组列表中的每个邮箱的**邮箱**元素。</span><span class="sxs-lookup"><span data-stu-id="70ba3-145">The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list.</span></span> <span data-ttu-id="70ba3-146">如果通讯组列表包含在通讯组列表中，必须在单独的通讯组列表扩展执行上嵌入的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-146">If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list.</span></span> <span data-ttu-id="70ba3-147">如果通讯组列表不包含任何成员或请求的通讯组列表不存在， **ResponseClass**属性将不包含的值等于成功。</span><span class="sxs-lookup"><span data-stu-id="70ba3-147">If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="70ba3-148">请求元素</span><span class="sxs-lookup"><span data-stu-id="70ba3-148">Request elements</span></span>

<span data-ttu-id="70ba3-149">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="70ba3-149">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="70ba3-150">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="70ba3-150">ExpandDL</span></span>](expanddl.md)
    
- [<span data-ttu-id="70ba3-151">Mailbox</span><span class="sxs-lookup"><span data-stu-id="70ba3-151">Mailbox</span></span>](mailbox.md)
    
- <span data-ttu-id="70ba3-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)用于标识公用通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists.</span></span> <span data-ttu-id="70ba3-153">[ItemId](itemid.md)元素用于标识私人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="70ba3-153">The [ItemId](itemid.md) element is used to identify private distribution lists.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="70ba3-154">介绍这些元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70ba3-154">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-expanddl-response-example"></a><span data-ttu-id="70ba3-155">成功 ExpandDL 响应示例</span><span class="sxs-lookup"><span data-stu-id="70ba3-155">Successful ExpandDL response example</span></span>

### <a name="description"></a><span data-ttu-id="70ba3-156">说明</span><span class="sxs-lookup"><span data-stu-id="70ba3-156">Description</span></span>

<span data-ttu-id="70ba3-157">ExpandDL 响应的下面的示例演示上述请求的响应。</span><span class="sxs-lookup"><span data-stu-id="70ba3-157">The following example of an ExpandDL response shows a response to the request described above.</span></span> <span data-ttu-id="70ba3-158">通讯组列表扩展介绍以下：</span><span class="sxs-lookup"><span data-stu-id="70ba3-158">The distribution list expansion describes the following:</span></span> 
  
- <span data-ttu-id="70ba3-159">通讯组列表的响应中返回的成员数。</span><span class="sxs-lookup"><span data-stu-id="70ba3-159">The number of members of the distribution list that are returned in the response.</span></span>
    
- <span data-ttu-id="70ba3-160">是否则响应中包含通讯组列表的所有的成员。</span><span class="sxs-lookup"><span data-stu-id="70ba3-160">Whether the response contains all the members of the distribution list.</span></span>
    
- <span data-ttu-id="70ba3-161">邮箱的名称。</span><span class="sxs-lookup"><span data-stu-id="70ba3-161">The name of the mailbox.</span></span>
    
- <span data-ttu-id="70ba3-162">邮箱的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="70ba3-162">The e-mail address of the mailbox.</span></span>
    
- <span data-ttu-id="70ba3-163">邮箱路由类型。</span><span class="sxs-lookup"><span data-stu-id="70ba3-163">The routing type for the mailbox.</span></span>
    
- <span data-ttu-id="70ba3-164">邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="70ba3-164">The type of mailbox.</span></span>
    
> [!NOTE]
> <span data-ttu-id="70ba3-165">响应; 中不包括通讯组列表名称因此，您必须跟踪的请求的名称。</span><span class="sxs-lookup"><span data-stu-id="70ba3-165">The distribution list name is not included in the response; therefore, you must keep track of the name from the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="70ba3-166">代码</span><span class="sxs-lookup"><span data-stu-id="70ba3-166">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="70ba3-167">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="70ba3-167">Successful response elements</span></span>

<span data-ttu-id="70ba3-168">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="70ba3-168">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="70ba3-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="70ba3-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="70ba3-170">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="70ba3-170">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="70ba3-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="70ba3-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="70ba3-172">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="70ba3-172">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="70ba3-173">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="70ba3-173">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="70ba3-174">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="70ba3-174">DLExpansion</span></span>](dlexpansion.md)
    
- [<span data-ttu-id="70ba3-175">Mailbox</span><span class="sxs-lookup"><span data-stu-id="70ba3-175">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="70ba3-176">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="70ba3-176">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="70ba3-177">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="70ba3-177">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="70ba3-178">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="70ba3-178">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="70ba3-179">MailboxType</span><span class="sxs-lookup"><span data-stu-id="70ba3-179">MailboxType</span></span>](mailboxtype.md)
    
<span data-ttu-id="70ba3-180">若要查找的响应消息 ExpandDL 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="70ba3-180">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="70ba3-181">启动[ExpandDLResponse](expanddlresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="70ba3-181">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="expanddl-error-response"></a><span data-ttu-id="70ba3-182">ExpandDL 错误响应</span><span class="sxs-lookup"><span data-stu-id="70ba3-182">ExpandDL error response</span></span>

### <a name="description"></a><span data-ttu-id="70ba3-183">说明</span><span class="sxs-lookup"><span data-stu-id="70ba3-183">Description</span></span>

<span data-ttu-id="70ba3-184">下面的示例演示 ExpandDL 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="70ba3-184">The following example shows an error response to an ExpandDL request.</span></span>
  
### <a name="code"></a><span data-ttu-id="70ba3-185">代码</span><span class="sxs-lookup"><span data-stu-id="70ba3-185">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="70ba3-186">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="70ba3-186">Error response elements</span></span>

<span data-ttu-id="70ba3-187">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="70ba3-187">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="70ba3-188">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="70ba3-188">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="70ba3-189">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="70ba3-189">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="70ba3-190">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="70ba3-190">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="70ba3-191">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="70ba3-191">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="70ba3-192">MessageText</span><span class="sxs-lookup"><span data-stu-id="70ba3-192">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="70ba3-193">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="70ba3-193">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="70ba3-194">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="70ba3-194">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="70ba3-195">若要查找的响应消息 ExpandDL 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="70ba3-195">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="70ba3-196">启动[ExpandDLResponse](expanddlresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="70ba3-196">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70ba3-197">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70ba3-197">See also</span></span>

- [<span data-ttu-id="70ba3-198">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="70ba3-198">ResolveNames operation</span></span>](resolvenames-operation.md)
- [<span data-ttu-id="70ba3-199">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70ba3-199">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

