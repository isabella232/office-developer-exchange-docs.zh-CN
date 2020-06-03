---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: ResolveNamesResponseMessage 元素包含 ResolveNames 操作请求的状态和结果。
ms.openlocfilehash: 12f32008dbbc603fca7adf26057f1f1904d3cfb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455595"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="3f57d-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3f57d-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="3f57d-104">**ResolveNamesResponseMessage**元素包含[ResolveNames 操作](resolvenames-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="3f57d-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="3f57d-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="3f57d-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="3f57d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3f57d-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="3f57d-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3f57d-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="3f57d-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3f57d-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f57d-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3f57d-109">Attributes and elements</span></span>

<span data-ttu-id="3f57d-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3f57d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f57d-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="3f57d-111">Attributes</span></span>

|<span data-ttu-id="3f57d-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="3f57d-112">**Attribute**</span></span>|<span data-ttu-id="3f57d-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f57d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f57d-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3f57d-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3f57d-115">描述[ResolveNames 操作](resolvenames-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="3f57d-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="3f57d-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="3f57d-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="3f57d-117">-成功</span><span class="sxs-lookup"><span data-stu-id="3f57d-117">-  Success</span></span>  <br/><span data-ttu-id="3f57d-118">-警告</span><span class="sxs-lookup"><span data-stu-id="3f57d-118">-  Warning</span></span>  <br/><span data-ttu-id="3f57d-119">-错误</span><span class="sxs-lookup"><span data-stu-id="3f57d-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="3f57d-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="3f57d-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="3f57d-121">**值**</span><span class="sxs-lookup"><span data-stu-id="3f57d-121">**Value**</span></span>|<span data-ttu-id="3f57d-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f57d-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f57d-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="3f57d-123">**Success**</span></span> <br/> |<span data-ttu-id="3f57d-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="3f57d-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="3f57d-125">当请求的名称明确且响应包含单个收件人时，会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="3f57d-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="3f57d-126">**警告**</span><span class="sxs-lookup"><span data-stu-id="3f57d-126">**Warning**</span></span> <br/> | <span data-ttu-id="3f57d-127">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="3f57d-127">Describes a request that was not processed.</span></span> <span data-ttu-id="3f57d-128">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="3f57d-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3f57d-129">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="3f57d-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="3f57d-130">-Exchange 存储在批处理过程中脱机。</span><span class="sxs-lookup"><span data-stu-id="3f57d-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="3f57d-131">-Active Directory 域服务（AD DS）脱机。</span><span class="sxs-lookup"><span data-stu-id="3f57d-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="3f57d-132">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="3f57d-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="3f57d-133">-邮箱数据库（MDB）脱机。</span><span class="sxs-lookup"><span data-stu-id="3f57d-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="3f57d-134">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="3f57d-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="3f57d-135">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="3f57d-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="3f57d-136">-请求的名称不明确，响应中包含多个收件人。</span><span class="sxs-lookup"><span data-stu-id="3f57d-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="3f57d-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="3f57d-137">**Error**</span></span> <br/> | <span data-ttu-id="3f57d-138">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="3f57d-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3f57d-139">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="3f57d-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3f57d-140">-无法解析请求的名称。</span><span class="sxs-lookup"><span data-stu-id="3f57d-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="3f57d-141">-属性或元素无效。</span><span class="sxs-lookup"><span data-stu-id="3f57d-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="3f57d-142">-属性或元素超出范围。</span><span class="sxs-lookup"><span data-stu-id="3f57d-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="3f57d-143">-标记未知。</span><span class="sxs-lookup"><span data-stu-id="3f57d-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="3f57d-144">-上下文中的属性或元素无效。</span><span class="sxs-lookup"><span data-stu-id="3f57d-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="3f57d-145">-发生任何客户端的未经授权的访问尝试。</span><span class="sxs-lookup"><span data-stu-id="3f57d-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="3f57d-146">-响应有效的客户端调用时发生服务器端故障。</span><span class="sxs-lookup"><span data-stu-id="3f57d-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="3f57d-147">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="3f57d-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f57d-148">子元素</span><span class="sxs-lookup"><span data-stu-id="3f57d-148">Child elements</span></span>

|<span data-ttu-id="3f57d-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="3f57d-149">**Element**</span></span>|<span data-ttu-id="3f57d-150">**描述**</span><span class="sxs-lookup"><span data-stu-id="3f57d-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f57d-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="3f57d-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3f57d-152">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="3f57d-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3f57d-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3f57d-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3f57d-154">提供有关请求的错误消息。</span><span class="sxs-lookup"><span data-stu-id="3f57d-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="3f57d-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3f57d-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3f57d-156">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="3f57d-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="3f57d-157">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="3f57d-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3f57d-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3f57d-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3f57d-159">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="3f57d-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3f57d-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="3f57d-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="3f57d-161">包含一个不明确名称的分辨率数组。</span><span class="sxs-lookup"><span data-stu-id="3f57d-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f57d-162">父元素</span><span class="sxs-lookup"><span data-stu-id="3f57d-162">Parent elements</span></span>

|<span data-ttu-id="3f57d-163">**元素**</span><span class="sxs-lookup"><span data-stu-id="3f57d-163">**Element**</span></span>|<span data-ttu-id="3f57d-164">**描述**</span><span class="sxs-lookup"><span data-stu-id="3f57d-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f57d-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3f57d-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3f57d-166">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3f57d-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f57d-167">备注</span><span class="sxs-lookup"><span data-stu-id="3f57d-167">Remarks</span></span>

<span data-ttu-id="3f57d-168">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3f57d-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f57d-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="3f57d-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f57d-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="3f57d-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f57d-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="3f57d-171">Schema name</span></span>  <br/> |<span data-ttu-id="3f57d-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="3f57d-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f57d-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="3f57d-173">Validation file</span></span>  <br/> |<span data-ttu-id="3f57d-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3f57d-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f57d-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="3f57d-175">Can be empty</span></span>  <br/> |<span data-ttu-id="3f57d-176">False</span><span class="sxs-lookup"><span data-stu-id="3f57d-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f57d-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f57d-177">See also</span></span>

- [<span data-ttu-id="3f57d-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="3f57d-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="3f57d-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="3f57d-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="3f57d-180">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="3f57d-180">ResolveNames operation</span></span>](resolvenames-operation.md)

