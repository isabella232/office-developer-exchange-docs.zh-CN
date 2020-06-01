---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: GetInboxRulesResponse 元素定义对 GetInboxRules 操作请求的响应。
ms.openlocfilehash: 0d67d7eaf6ffbeeb790249190a98f252dbdb9c87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458283"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="c79e8-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="c79e8-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="c79e8-104">**GetInboxRulesResponse**元素定义对[GetInboxRules 操作](getinboxrules-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c79e8-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
```XML
<GetInboxRulesResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <OutlookRuleBlobExists/>
   <InboxRules/>
</GetInboxRulesResponse>
```

 <span data-ttu-id="c79e8-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="c79e8-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c79e8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c79e8-106">Attributes and elements</span></span>

<span data-ttu-id="c79e8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c79e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c79e8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c79e8-108">Attributes</span></span>

|<span data-ttu-id="c79e8-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c79e8-109">**Attribute**</span></span>|<span data-ttu-id="c79e8-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c79e8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c79e8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c79e8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c79e8-112">描述[GetInboxRules 操作](getinboxrules-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c79e8-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="c79e8-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="c79e8-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="c79e8-114">-成功</span><span class="sxs-lookup"><span data-stu-id="c79e8-114">-  Success</span></span>  <br/><span data-ttu-id="c79e8-115">-警告</span><span class="sxs-lookup"><span data-stu-id="c79e8-115">-  Warning</span></span>  <br/><span data-ttu-id="c79e8-116">-错误</span><span class="sxs-lookup"><span data-stu-id="c79e8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="c79e8-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="c79e8-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="c79e8-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c79e8-118">**Value**</span></span>|<span data-ttu-id="c79e8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c79e8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c79e8-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="c79e8-120">**Success**</span></span> <br/> |<span data-ttu-id="c79e8-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c79e8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c79e8-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="c79e8-122">**Warning**</span></span> <br/> | <span data-ttu-id="c79e8-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c79e8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c79e8-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="c79e8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c79e8-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="c79e8-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="c79e8-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c79e8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c79e8-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c79e8-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c79e8-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="c79e8-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="c79e8-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c79e8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c79e8-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="c79e8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c79e8-131">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="c79e8-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="c79e8-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c79e8-132">**Error**</span></span> <br/> | <span data-ttu-id="c79e8-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="c79e8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="c79e8-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="c79e8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c79e8-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="c79e8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c79e8-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c79e8-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="c79e8-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c79e8-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="c79e8-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c79e8-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="c79e8-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="c79e8-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c79e8-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="c79e8-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="c79e8-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="c79e8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c79e8-142">子元素</span><span class="sxs-lookup"><span data-stu-id="c79e8-142">Child elements</span></span>

|<span data-ttu-id="c79e8-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c79e8-143">**Element**</span></span>|<span data-ttu-id="c79e8-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="c79e8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c79e8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c79e8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c79e8-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c79e8-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c79e8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c79e8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c79e8-148">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="c79e8-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="c79e8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c79e8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c79e8-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c79e8-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c79e8-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="c79e8-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c79e8-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c79e8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c79e8-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c79e8-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c79e8-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="c79e8-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="c79e8-155">指示用户的邮箱中是否存在 Microsoft Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="c79e8-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c79e8-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="c79e8-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="c79e8-157">表示用户邮箱中的规则的数组。</span><span class="sxs-lookup"><span data-stu-id="c79e8-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c79e8-158">父元素</span><span class="sxs-lookup"><span data-stu-id="c79e8-158">Parent elements</span></span>

<span data-ttu-id="c79e8-159">无。</span><span class="sxs-lookup"><span data-stu-id="c79e8-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c79e8-160">文本值</span><span class="sxs-lookup"><span data-stu-id="c79e8-160">Text value</span></span>

<span data-ttu-id="c79e8-161">无。</span><span class="sxs-lookup"><span data-stu-id="c79e8-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c79e8-162">说明</span><span class="sxs-lookup"><span data-stu-id="c79e8-162">Remarks</span></span>

<span data-ttu-id="c79e8-163">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c79e8-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c79e8-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="c79e8-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c79e8-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="c79e8-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c79e8-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="c79e8-166">Schema name</span></span>  <br/> |<span data-ttu-id="c79e8-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="c79e8-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c79e8-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="c79e8-168">Validation file</span></span>  <br/> |<span data-ttu-id="c79e8-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c79e8-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c79e8-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="c79e8-170">Can be empty</span></span>  <br/> |<span data-ttu-id="c79e8-171">False</span><span class="sxs-lookup"><span data-stu-id="c79e8-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c79e8-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c79e8-172">See also</span></span>

- [<span data-ttu-id="c79e8-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c79e8-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="c79e8-174">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="c79e8-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

