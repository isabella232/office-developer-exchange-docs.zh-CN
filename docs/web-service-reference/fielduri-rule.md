---
title: FieldUri （规则）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: FieldURI 元素指定的规则字段导致验证错误的 URI。
ms.openlocfilehash: 88ba54994625d3a950b58e900f28c986c31eddac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754295"
---
# <a name="fielduri-rule"></a><span data-ttu-id="861f4-103">FieldUri （规则）</span><span class="sxs-lookup"><span data-stu-id="861f4-103">FieldUri (Rule)</span></span>

<span data-ttu-id="861f4-104">**FieldURI**元素指定的规则字段导致验证错误的 URI。</span><span class="sxs-lookup"><span data-stu-id="861f4-104">The **FieldURI** element specifies the URI to the rule field that caused the validation error.</span></span> 
  
```XML
<FieldURI/>
```

 <span data-ttu-id="861f4-105">**RuleFieldURIType**</span><span class="sxs-lookup"><span data-stu-id="861f4-105">**RuleFieldURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="861f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="861f4-106">Attributes and elements</span></span>

<span data-ttu-id="861f4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="861f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="861f4-108">属性</span><span class="sxs-lookup"><span data-stu-id="861f4-108">Attributes</span></span>

<span data-ttu-id="861f4-109">无。</span><span class="sxs-lookup"><span data-stu-id="861f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="861f4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="861f4-110">Child elements</span></span>

<span data-ttu-id="861f4-111">无。</span><span class="sxs-lookup"><span data-stu-id="861f4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="861f4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="861f4-112">Parent elements</span></span>

|<span data-ttu-id="861f4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="861f4-113">**Element**</span></span>|<span data-ttu-id="861f4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="861f4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="861f4-115">Error</span><span class="sxs-lookup"><span data-stu-id="861f4-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="861f4-116">代表对特定规则属性值、 谓词属性值或 action 属性值的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="861f4-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="861f4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="861f4-117">Text value</span></span>

<span data-ttu-id="861f4-118">此元素的文本值仅限于以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="861f4-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="861f4-119">规则 Id</span><span class="sxs-lookup"><span data-stu-id="861f4-119">RuleId</span></span>
    
- <span data-ttu-id="861f4-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="861f4-120">DisplayName</span></span>
    
- <span data-ttu-id="861f4-121">优先级</span><span class="sxs-lookup"><span data-stu-id="861f4-121">Priority</span></span>
    
- <span data-ttu-id="861f4-122">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="861f4-122">IsNotSupported</span></span>
    
- <span data-ttu-id="861f4-123">操作</span><span class="sxs-lookup"><span data-stu-id="861f4-123">Actions</span></span>
    
- <span data-ttu-id="861f4-124">条件： 类别</span><span class="sxs-lookup"><span data-stu-id="861f4-124">Condition:Categories</span></span>
    
- <span data-ttu-id="861f4-125">ContainsBodyStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-125">Condition:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="861f4-126">ContainsHeaderStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-126">Condition:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="861f4-127">ContainsRecipientStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-127">Condition:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="861f4-128">ContainsSenderStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-128">Condition:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="861f4-129">ContainsSubjectOrBodyStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-129">Condition:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="861f4-130">ContainsSubjectStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-130">Condition:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="861f4-131">FlaggedForAction 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-131">Condition:FlaggedForAction</span></span>
    
- <span data-ttu-id="861f4-132">FromAddresses 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-132">Condition:FromAddresses</span></span>
    
- <span data-ttu-id="861f4-133">FromConnectedAccounts 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-133">Condition:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="861f4-134">HasAttachments 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-134">Condition:HasAttachments</span></span>
    
- <span data-ttu-id="861f4-135">条件： 重要性</span><span class="sxs-lookup"><span data-stu-id="861f4-135">Condition:Importance</span></span>
    
- <span data-ttu-id="861f4-136">IsApprovalRequest 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-136">Condition:IsApprovalRequest</span></span>
    
- <span data-ttu-id="861f4-137">IsAutomaticForward 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-137">Condition:IsAutomaticForward</span></span>
    
- <span data-ttu-id="861f4-138">IsAutomaticReply 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-138">Condition:IsAutomaticReply</span></span>
    
- <span data-ttu-id="861f4-139">进行加密条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-139">Condition:IsEncrypted</span></span>
    
- <span data-ttu-id="861f4-140">IsMeetingRequest 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-140">Condition:IsMeetingRequest</span></span>
    
- <span data-ttu-id="861f4-141">IsMeetingResponse 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-141">Condition:IsMeetingResponse</span></span>
    
- <span data-ttu-id="861f4-142">IsNDR 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-142">Condition:IsNDR</span></span>
    
- <span data-ttu-id="861f4-143">IsPermissionControlled 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-143">Condition:IsPermissionControlled</span></span>
    
- <span data-ttu-id="861f4-144">IsReadReceipt 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-144">Condition:IsReadReceipt</span></span>
    
- <span data-ttu-id="861f4-145">IsSigned 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-145">Condition:IsSigned</span></span>
    
- <span data-ttu-id="861f4-146">IsVoicemail 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-146">Condition:IsVoicemail</span></span>
    
- <span data-ttu-id="861f4-147">ItemClasses 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-147">Condition:ItemClasses</span></span>
    
- <span data-ttu-id="861f4-148">MessageClassifications 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-148">Condition:MessageClassifications</span></span>
    
- <span data-ttu-id="861f4-149">NotSentToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-149">Condition:NotSentToMe</span></span>
    
- <span data-ttu-id="861f4-150">SentCcMe 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-150">Condition:SentCcMe</span></span>
    
- <span data-ttu-id="861f4-151">SentOnlyToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-151">Condition:SentOnlyToMe</span></span>
    
- <span data-ttu-id="861f4-152">SentToAddresses 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-152">Condition:SentToAddresses</span></span>
    
- <span data-ttu-id="861f4-153">SentToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-153">Condition:SentToMe</span></span>
    
- <span data-ttu-id="861f4-154">SentToOrCcMe 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-154">Condition:SentToOrCcMe</span></span>
    
- <span data-ttu-id="861f4-155">敏感度条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-155">Condition:Sensitivity</span></span>
    
- <span data-ttu-id="861f4-156">WithinDateRange 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-156">Condition:WithinDateRange</span></span>
    
- <span data-ttu-id="861f4-157">WithinSizeRange 条件：</span><span class="sxs-lookup"><span data-stu-id="861f4-157">Condition:WithinSizeRange</span></span>
    
- <span data-ttu-id="861f4-158">异常： 类别</span><span class="sxs-lookup"><span data-stu-id="861f4-158">Exception:Categories</span></span>
    
- <span data-ttu-id="861f4-159">异常： ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-159">Exception:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="861f4-160">异常： ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-160">Exception:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="861f4-161">异常： ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-161">Exception:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="861f4-162">异常： ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-162">Exception:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="861f4-163">异常： ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-163">Exception:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="861f4-164">异常： ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="861f4-164">Exception:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="861f4-165">异常： FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="861f4-165">Exception:FlaggedForAction</span></span>
    
- <span data-ttu-id="861f4-166">异常： FromAddresses</span><span class="sxs-lookup"><span data-stu-id="861f4-166">Exception:FromAddresses</span></span>
    
- <span data-ttu-id="861f4-167">异常： FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="861f4-167">Exception:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="861f4-168">异常： HasAttachments</span><span class="sxs-lookup"><span data-stu-id="861f4-168">Exception:HasAttachments</span></span>
    
- <span data-ttu-id="861f4-169">异常： 重要性</span><span class="sxs-lookup"><span data-stu-id="861f4-169">Exception:Importance</span></span>
    
- <span data-ttu-id="861f4-170">异常： IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="861f4-170">Exception:IsApprovalRequest</span></span>
    
- <span data-ttu-id="861f4-171">异常： IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="861f4-171">Exception:IsAutomaticForward</span></span>
    
- <span data-ttu-id="861f4-172">异常： IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="861f4-172">Exception:IsAutomaticReply</span></span>
    
- <span data-ttu-id="861f4-173">异常： 进行加密</span><span class="sxs-lookup"><span data-stu-id="861f4-173">Exception:IsEncrypted</span></span>
    
- <span data-ttu-id="861f4-174">异常： IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="861f4-174">Exception:IsMeetingRequest</span></span>
    
- <span data-ttu-id="861f4-175">异常： IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="861f4-175">Exception:IsMeetingResponse</span></span>
    
- <span data-ttu-id="861f4-176">异常： IsNDR</span><span class="sxs-lookup"><span data-stu-id="861f4-176">Exception:IsNDR</span></span>
    
- <span data-ttu-id="861f4-177">异常： IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="861f4-177">Exception:IsPermissionControlled</span></span>
    
- <span data-ttu-id="861f4-178">异常： IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="861f4-178">Exception:IsReadReceipt</span></span>
    
- <span data-ttu-id="861f4-179">异常： IsSigned</span><span class="sxs-lookup"><span data-stu-id="861f4-179">Exception:IsSigned</span></span>
    
- <span data-ttu-id="861f4-180">异常： IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="861f4-180">Exception:IsVoicemail</span></span>
    
- <span data-ttu-id="861f4-181">异常： ItemClasses</span><span class="sxs-lookup"><span data-stu-id="861f4-181">Exception:ItemClasses</span></span>
    
- <span data-ttu-id="861f4-182">异常： MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="861f4-182">Exception:MessageClassifications</span></span>
    
- <span data-ttu-id="861f4-183">异常： NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="861f4-183">Exception:NotSentToMe</span></span>
    
- <span data-ttu-id="861f4-184">异常： SentCcMe</span><span class="sxs-lookup"><span data-stu-id="861f4-184">Exception:SentCcMe</span></span>
    
- <span data-ttu-id="861f4-185">异常： SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="861f4-185">Exception:SentOnlyToMe</span></span>
    
- <span data-ttu-id="861f4-186">异常： SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="861f4-186">Exception:SentToAddresses</span></span>
    
- <span data-ttu-id="861f4-187">异常： SentToMe</span><span class="sxs-lookup"><span data-stu-id="861f4-187">Exception:SentToMe</span></span>
    
- <span data-ttu-id="861f4-188">异常： SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="861f4-188">Exception:SentToOrCcMe</span></span>
    
- <span data-ttu-id="861f4-189">异常： 敏感度</span><span class="sxs-lookup"><span data-stu-id="861f4-189">Exception:Sensitivity</span></span>
    
- <span data-ttu-id="861f4-190">异常： WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="861f4-190">Exception:WithinDateRange</span></span>
    
- <span data-ttu-id="861f4-191">异常： WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="861f4-191">Exception:WithinSizeRange</span></span>
    
- <span data-ttu-id="861f4-192">AssignCategories 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-192">Action:AssignCategories</span></span>
    
- <span data-ttu-id="861f4-193">CopyToFolder 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-193">Action:CopyToFolder</span></span>
    
- <span data-ttu-id="861f4-194">删除操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-194">Action:Delete</span></span>
    
- <span data-ttu-id="861f4-195">ForwardAsAttachmentToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-195">Action:ForwardAsAttachmentToRecipients</span></span>
    
- <span data-ttu-id="861f4-196">ForwardToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-196">Action:ForwardToRecipients</span></span>
    
- <span data-ttu-id="861f4-197">MarkImportance 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-197">Action:MarkImportance</span></span>
    
- <span data-ttu-id="861f4-198">MarkAsRead 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-198">Action:MarkAsRead</span></span>
    
- <span data-ttu-id="861f4-199">MoveToFolder 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-199">Action:MoveToFolder</span></span>
    
- <span data-ttu-id="861f4-200">PermanentDelete 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-200">Action:PermanentDelete</span></span>
    
- <span data-ttu-id="861f4-201">RedirectToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-201">Action:RedirectToRecipients</span></span>
    
- <span data-ttu-id="861f4-202">SendSMSAlertToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-202">Action:SendSMSAlertToRecipients</span></span>
    
- <span data-ttu-id="861f4-203">ServerReplyWithMessage 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-203">Action:ServerReplyWithMessage</span></span>
    
- <span data-ttu-id="861f4-204">StopProcessingRules 操作：</span><span class="sxs-lookup"><span data-stu-id="861f4-204">Action:StopProcessingRules</span></span>
    
- <span data-ttu-id="861f4-205">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="861f4-205">IsEnabled</span></span>
    
- <span data-ttu-id="861f4-206">IsInError</span><span class="sxs-lookup"><span data-stu-id="861f4-206">IsInError</span></span>
    
- <span data-ttu-id="861f4-207">条件</span><span class="sxs-lookup"><span data-stu-id="861f4-207">Conditions</span></span>
    
- <span data-ttu-id="861f4-208">异常</span><span class="sxs-lookup"><span data-stu-id="861f4-208">Exceptions</span></span>
    
## <a name="remarks"></a><span data-ttu-id="861f4-209">备注</span><span class="sxs-lookup"><span data-stu-id="861f4-209">Remarks</span></span>

<span data-ttu-id="861f4-210">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="861f4-210">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="861f4-211">元素信息</span><span class="sxs-lookup"><span data-stu-id="861f4-211">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="861f4-212">命名空间</span><span class="sxs-lookup"><span data-stu-id="861f4-212">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="861f4-213">架构名称</span><span class="sxs-lookup"><span data-stu-id="861f4-213">Schema Name</span></span>  <br/> |<span data-ttu-id="861f4-214">消息架构</span><span class="sxs-lookup"><span data-stu-id="861f4-214">Messages schema</span></span>  <br/> |
|<span data-ttu-id="861f4-215">验证文件</span><span class="sxs-lookup"><span data-stu-id="861f4-215">Validation File</span></span>  <br/> |<span data-ttu-id="861f4-216">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="861f4-216">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="861f4-217">可以为空</span><span class="sxs-lookup"><span data-stu-id="861f4-217">Can be Empty</span></span>  <br/> |<span data-ttu-id="861f4-218">False</span><span class="sxs-lookup"><span data-stu-id="861f4-218">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="861f4-219">另请参阅</span><span class="sxs-lookup"><span data-stu-id="861f4-219">See also</span></span>



- [<span data-ttu-id="861f4-220">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="861f4-220">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

