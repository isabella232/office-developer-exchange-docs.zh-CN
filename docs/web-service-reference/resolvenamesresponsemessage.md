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
description: ResolveNamesResponseMessage 元素包含状态和 ResolveNames 操作请求的结果。
ms.openlocfilehash: 953a1f0b19c078d969ffe175c22df02b58c5e939
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827170"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="773e6-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="773e6-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="773e6-104">**ResolveNamesResponseMessage**元素包含状态和[ResolveNames 操作](resolvenames-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="773e6-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="773e6-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="773e6-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="773e6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="773e6-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="773e6-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="773e6-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="773e6-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="773e6-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="773e6-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="773e6-109">Attributes and elements</span></span>

<span data-ttu-id="773e6-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="773e6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="773e6-111">属性</span><span class="sxs-lookup"><span data-stu-id="773e6-111">Attributes</span></span>

|<span data-ttu-id="773e6-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="773e6-112">**Attribute**</span></span>|<span data-ttu-id="773e6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="773e6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="773e6-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="773e6-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="773e6-115">描述[ResolveNames 操作](resolvenames-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="773e6-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="773e6-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="773e6-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="773e6-117">-成功</span><span class="sxs-lookup"><span data-stu-id="773e6-117">-  Success</span></span>  <br/><span data-ttu-id="773e6-118">-警告</span><span class="sxs-lookup"><span data-stu-id="773e6-118">-  Warning</span></span>  <br/><span data-ttu-id="773e6-119">-错误</span><span class="sxs-lookup"><span data-stu-id="773e6-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="773e6-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="773e6-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="773e6-121">**值**</span><span class="sxs-lookup"><span data-stu-id="773e6-121">**Value**</span></span>|<span data-ttu-id="773e6-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="773e6-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="773e6-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="773e6-123">**Success**</span></span> <br/> |<span data-ttu-id="773e6-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="773e6-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="773e6-125">请求的名称是明确，则响应中包含单个收件人时，将发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="773e6-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="773e6-126">**Warning**</span><span class="sxs-lookup"><span data-stu-id="773e6-126">**Warning**</span></span> <br/> | <span data-ttu-id="773e6-127">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="773e6-127">Describes a request that was not processed.</span></span> <span data-ttu-id="773e6-128">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="773e6-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="773e6-129">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="773e6-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="773e6-130">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="773e6-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="773e6-131">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="773e6-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="773e6-132">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="773e6-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="773e6-133">-邮箱数据库 (MDB) 脱机。</span><span class="sxs-lookup"><span data-stu-id="773e6-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="773e6-134">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="773e6-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="773e6-135">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="773e6-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="773e6-136">-请求的名称不明确，则响应中包含多个收件人。</span><span class="sxs-lookup"><span data-stu-id="773e6-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="773e6-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="773e6-137">**Error**</span></span> <br/> | <span data-ttu-id="773e6-138">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="773e6-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="773e6-139">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="773e6-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="773e6-140">的无法解析请求的名称。</span><span class="sxs-lookup"><span data-stu-id="773e6-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="773e6-141">-属性或元素无效。</span><span class="sxs-lookup"><span data-stu-id="773e6-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="773e6-142">-属性或元素超出范围。</span><span class="sxs-lookup"><span data-stu-id="773e6-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="773e6-143">的未知标记。</span><span class="sxs-lookup"><span data-stu-id="773e6-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="773e6-144">-属性或元素在上下文中无效。</span><span class="sxs-lookup"><span data-stu-id="773e6-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="773e6-145">的将出现的任何客户端未经授权的访问尝试。</span><span class="sxs-lookup"><span data-stu-id="773e6-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="773e6-146">的有效的客户端的呼叫的响应中出现服务器端故障。</span><span class="sxs-lookup"><span data-stu-id="773e6-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="773e6-147">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="773e6-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="773e6-148">子元素</span><span class="sxs-lookup"><span data-stu-id="773e6-148">Child elements</span></span>

|<span data-ttu-id="773e6-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="773e6-149">**Element**</span></span>|<span data-ttu-id="773e6-150">**说明**</span><span class="sxs-lookup"><span data-stu-id="773e6-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="773e6-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="773e6-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="773e6-152">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="773e6-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="773e6-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="773e6-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="773e6-154">提供有关请求错误的信息。</span><span class="sxs-lookup"><span data-stu-id="773e6-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="773e6-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="773e6-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="773e6-156">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="773e6-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="773e6-157">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="773e6-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="773e6-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="773e6-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="773e6-159">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="773e6-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="773e6-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="773e6-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="773e6-161">包含的不明确名称解析的数组。</span><span class="sxs-lookup"><span data-stu-id="773e6-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="773e6-162">父元素</span><span class="sxs-lookup"><span data-stu-id="773e6-162">Parent elements</span></span>

|<span data-ttu-id="773e6-163">**元素**</span><span class="sxs-lookup"><span data-stu-id="773e6-163">**Element**</span></span>|<span data-ttu-id="773e6-164">**说明**</span><span class="sxs-lookup"><span data-stu-id="773e6-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="773e6-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="773e6-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="773e6-166">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="773e6-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="773e6-167">注解</span><span class="sxs-lookup"><span data-stu-id="773e6-167">Remarks</span></span>

<span data-ttu-id="773e6-168">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="773e6-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="773e6-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="773e6-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="773e6-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="773e6-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="773e6-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="773e6-171">Schema name</span></span>  <br/> |<span data-ttu-id="773e6-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="773e6-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="773e6-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="773e6-173">Validation file</span></span>  <br/> |<span data-ttu-id="773e6-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="773e6-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="773e6-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="773e6-175">Can be empty</span></span>  <br/> |<span data-ttu-id="773e6-176">False</span><span class="sxs-lookup"><span data-stu-id="773e6-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="773e6-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="773e6-177">See also</span></span>

- [<span data-ttu-id="773e6-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="773e6-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="773e6-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="773e6-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="773e6-180">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="773e6-180">ResolveNames operation</span></span>](resolvenames-operation.md)

