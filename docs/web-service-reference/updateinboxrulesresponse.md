---
title: UpdateInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRulesResponse
api_type:
- schema
ms.assetid: 0947b6aa-0d95-421b-aebb-d03021ecc110
description: UpdateInboxRulesResponse 元素定义对 UpdateInboxRules 请求的响应。
ms.openlocfilehash: 1216a32bdaf2dd5211021add0728844eb62089ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455903"
---
# <a name="updateinboxrulesresponse"></a><span data-ttu-id="eb50d-103">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="eb50d-103">UpdateInboxRulesResponse</span></span>

<span data-ttu-id="eb50d-104">**UpdateInboxRulesResponse**元素定义对 UpdateInboxRules 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="eb50d-104">The **UpdateInboxRulesResponse** element defines a response to an UpdateInboxRules request.</span></span> 
  
```XML
<UpdateInboxRulesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RuleOperationErrors/>
</UpdateInboxRulesResponse>
```

 <span data-ttu-id="eb50d-105">**UpdateInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="eb50d-105">**UpdateInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb50d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-106">Attributes and elements</span></span>

<span data-ttu-id="eb50d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb50d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb50d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="eb50d-108">Attributes</span></span>

|<span data-ttu-id="eb50d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="eb50d-109">**Attribute**</span></span>|<span data-ttu-id="eb50d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb50d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb50d-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="eb50d-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="eb50d-112">描述[取消订阅操作](unsubscribe-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="eb50d-112">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span><br/><br/> <span data-ttu-id="eb50d-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="eb50d-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="eb50d-114">-成功</span><span class="sxs-lookup"><span data-stu-id="eb50d-114">-  Success</span></span>  <br/><span data-ttu-id="eb50d-115">-警告</span><span class="sxs-lookup"><span data-stu-id="eb50d-115">-  Warning</span></span>  <br/><span data-ttu-id="eb50d-116">-错误</span><span class="sxs-lookup"><span data-stu-id="eb50d-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="eb50d-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="eb50d-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="eb50d-118">**值**</span><span class="sxs-lookup"><span data-stu-id="eb50d-118">**Value**</span></span>|<span data-ttu-id="eb50d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb50d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb50d-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="eb50d-120">**Success**</span></span> <br/> |<span data-ttu-id="eb50d-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="eb50d-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="eb50d-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="eb50d-122">**Warning**</span></span> <br/> | <span data-ttu-id="eb50d-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="eb50d-123">Describes a request that was not processed.</span></span> <span data-ttu-id="eb50d-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="eb50d-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="eb50d-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="eb50d-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="eb50d-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eb50d-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="eb50d-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eb50d-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="eb50d-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="eb50d-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="eb50d-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eb50d-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="eb50d-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="eb50d-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="eb50d-131">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="eb50d-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="eb50d-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="eb50d-132">**Error**</span></span> <br/> | <span data-ttu-id="eb50d-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="eb50d-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="eb50d-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="eb50d-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="eb50d-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="eb50d-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="eb50d-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="eb50d-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="eb50d-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="eb50d-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="eb50d-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="eb50d-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="eb50d-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="eb50d-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="eb50d-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="eb50d-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb50d-142">子元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-142">Child elements</span></span>

|<span data-ttu-id="eb50d-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb50d-143">**Element**</span></span>|<span data-ttu-id="eb50d-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="eb50d-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb50d-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="eb50d-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="eb50d-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="eb50d-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="eb50d-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eb50d-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="eb50d-148">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="eb50d-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="eb50d-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="eb50d-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="eb50d-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="eb50d-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="eb50d-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="eb50d-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="eb50d-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="eb50d-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="eb50d-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="eb50d-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="eb50d-154">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="eb50d-154">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="eb50d-155">表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="eb50d-155">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb50d-156">父元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-156">Parent elements</span></span>

<span data-ttu-id="eb50d-157">无。</span><span class="sxs-lookup"><span data-stu-id="eb50d-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eb50d-158">文本值</span><span class="sxs-lookup"><span data-stu-id="eb50d-158">Text value</span></span>

<span data-ttu-id="eb50d-159">无。</span><span class="sxs-lookup"><span data-stu-id="eb50d-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb50d-160">说明</span><span class="sxs-lookup"><span data-stu-id="eb50d-160">Remarks</span></span>

<span data-ttu-id="eb50d-161">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb50d-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb50d-162">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb50d-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb50d-163">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb50d-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb50d-164">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb50d-164">Schema name</span></span>  <br/> |<span data-ttu-id="eb50d-165">消息架构</span><span class="sxs-lookup"><span data-stu-id="eb50d-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb50d-166">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb50d-166">Validation file</span></span>  <br/> |<span data-ttu-id="eb50d-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb50d-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb50d-168">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb50d-168">Can be empty</span></span>  <br/> |<span data-ttu-id="eb50d-169">False</span><span class="sxs-lookup"><span data-stu-id="eb50d-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb50d-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb50d-170">See also</span></span>

- [<span data-ttu-id="eb50d-171">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="eb50d-171">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="eb50d-172">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="eb50d-172">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="eb50d-173">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb50d-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

