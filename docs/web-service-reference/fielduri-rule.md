---
title: FieldUri (规则)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: FieldURI 元素指定导致验证错误的规则字段的 URI。
ms.openlocfilehash: 3d88efdf951af580f81b5e2e7a544dcdf70ea830
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461245"
---
# <a name="fielduri-rule"></a><span data-ttu-id="181ac-103">FieldUri (规则)</span><span class="sxs-lookup"><span data-stu-id="181ac-103">FieldUri (Rule)</span></span>

<span data-ttu-id="181ac-104">**FieldURI**元素指定导致验证错误的规则字段的 URI。</span><span class="sxs-lookup"><span data-stu-id="181ac-104">The **FieldURI** element specifies the URI to the rule field that caused the validation error.</span></span> 
  
```XML
<FieldURI/>
```

 <span data-ttu-id="181ac-105">**RuleFieldURIType**</span><span class="sxs-lookup"><span data-stu-id="181ac-105">**RuleFieldURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="181ac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="181ac-106">Attributes and elements</span></span>

<span data-ttu-id="181ac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="181ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="181ac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="181ac-108">Attributes</span></span>

<span data-ttu-id="181ac-109">无。</span><span class="sxs-lookup"><span data-stu-id="181ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="181ac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="181ac-110">Child elements</span></span>

<span data-ttu-id="181ac-111">无。</span><span class="sxs-lookup"><span data-stu-id="181ac-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="181ac-112">父元素</span><span class="sxs-lookup"><span data-stu-id="181ac-112">Parent elements</span></span>

|<span data-ttu-id="181ac-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="181ac-113">**Element**</span></span>|<span data-ttu-id="181ac-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="181ac-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="181ac-115">Error</span><span class="sxs-lookup"><span data-stu-id="181ac-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="181ac-116">表示特定规则属性值、谓词属性值或 action 属性值上的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="181ac-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="181ac-117">文本值</span><span class="sxs-lookup"><span data-stu-id="181ac-117">Text value</span></span>

<span data-ttu-id="181ac-118">此元素的文本值被限制为以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="181ac-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="181ac-119">RuleId</span><span class="sxs-lookup"><span data-stu-id="181ac-119">RuleId</span></span>
    
- <span data-ttu-id="181ac-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="181ac-120">DisplayName</span></span>
    
- <span data-ttu-id="181ac-121">优先级</span><span class="sxs-lookup"><span data-stu-id="181ac-121">Priority</span></span>
    
- <span data-ttu-id="181ac-122">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="181ac-122">IsNotSupported</span></span>
    
- <span data-ttu-id="181ac-123">操作</span><span class="sxs-lookup"><span data-stu-id="181ac-123">Actions</span></span>
    
- <span data-ttu-id="181ac-124">条件：类别</span><span class="sxs-lookup"><span data-stu-id="181ac-124">Condition:Categories</span></span>
    
- <span data-ttu-id="181ac-125">条件： ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-125">Condition:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="181ac-126">条件： ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-126">Condition:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="181ac-127">条件： ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-127">Condition:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="181ac-128">条件： ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-128">Condition:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="181ac-129">条件： ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-129">Condition:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="181ac-130">条件： ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-130">Condition:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="181ac-131">条件： FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="181ac-131">Condition:FlaggedForAction</span></span>
    
- <span data-ttu-id="181ac-132">条件： FromAddresses</span><span class="sxs-lookup"><span data-stu-id="181ac-132">Condition:FromAddresses</span></span>
    
- <span data-ttu-id="181ac-133">条件： FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="181ac-133">Condition:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="181ac-134">条件： HasAttachments</span><span class="sxs-lookup"><span data-stu-id="181ac-134">Condition:HasAttachments</span></span>
    
- <span data-ttu-id="181ac-135">条件：重要性</span><span class="sxs-lookup"><span data-stu-id="181ac-135">Condition:Importance</span></span>
    
- <span data-ttu-id="181ac-136">条件： IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="181ac-136">Condition:IsApprovalRequest</span></span>
    
- <span data-ttu-id="181ac-137">条件： IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="181ac-137">Condition:IsAutomaticForward</span></span>
    
- <span data-ttu-id="181ac-138">条件： IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="181ac-138">Condition:IsAutomaticReply</span></span>
    
- <span data-ttu-id="181ac-139">条件： IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="181ac-139">Condition:IsEncrypted</span></span>
    
- <span data-ttu-id="181ac-140">条件： IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="181ac-140">Condition:IsMeetingRequest</span></span>
    
- <span data-ttu-id="181ac-141">条件： IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="181ac-141">Condition:IsMeetingResponse</span></span>
    
- <span data-ttu-id="181ac-142">条件： IsNDR</span><span class="sxs-lookup"><span data-stu-id="181ac-142">Condition:IsNDR</span></span>
    
- <span data-ttu-id="181ac-143">条件： IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="181ac-143">Condition:IsPermissionControlled</span></span>
    
- <span data-ttu-id="181ac-144">条件： IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="181ac-144">Condition:IsReadReceipt</span></span>
    
- <span data-ttu-id="181ac-145">条件： IsSigned</span><span class="sxs-lookup"><span data-stu-id="181ac-145">Condition:IsSigned</span></span>
    
- <span data-ttu-id="181ac-146">条件： IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="181ac-146">Condition:IsVoicemail</span></span>
    
- <span data-ttu-id="181ac-147">条件： ItemClasses</span><span class="sxs-lookup"><span data-stu-id="181ac-147">Condition:ItemClasses</span></span>
    
- <span data-ttu-id="181ac-148">条件： MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="181ac-148">Condition:MessageClassifications</span></span>
    
- <span data-ttu-id="181ac-149">条件： NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-149">Condition:NotSentToMe</span></span>
    
- <span data-ttu-id="181ac-150">条件： SentCcMe</span><span class="sxs-lookup"><span data-stu-id="181ac-150">Condition:SentCcMe</span></span>
    
- <span data-ttu-id="181ac-151">条件： SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-151">Condition:SentOnlyToMe</span></span>
    
- <span data-ttu-id="181ac-152">条件： SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="181ac-152">Condition:SentToAddresses</span></span>
    
- <span data-ttu-id="181ac-153">条件： SentToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-153">Condition:SentToMe</span></span>
    
- <span data-ttu-id="181ac-154">条件： SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="181ac-154">Condition:SentToOrCcMe</span></span>
    
- <span data-ttu-id="181ac-155">条件：敏感度</span><span class="sxs-lookup"><span data-stu-id="181ac-155">Condition:Sensitivity</span></span>
    
- <span data-ttu-id="181ac-156">条件： WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="181ac-156">Condition:WithinDateRange</span></span>
    
- <span data-ttu-id="181ac-157">条件： WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="181ac-157">Condition:WithinSizeRange</span></span>
    
- <span data-ttu-id="181ac-158">异常：类别</span><span class="sxs-lookup"><span data-stu-id="181ac-158">Exception:Categories</span></span>
    
- <span data-ttu-id="181ac-159">异常： ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-159">Exception:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="181ac-160">异常： ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-160">Exception:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="181ac-161">异常： ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-161">Exception:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="181ac-162">异常： ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-162">Exception:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="181ac-163">异常： ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-163">Exception:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="181ac-164">异常： ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="181ac-164">Exception:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="181ac-165">异常： FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="181ac-165">Exception:FlaggedForAction</span></span>
    
- <span data-ttu-id="181ac-166">异常： FromAddresses</span><span class="sxs-lookup"><span data-stu-id="181ac-166">Exception:FromAddresses</span></span>
    
- <span data-ttu-id="181ac-167">异常： FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="181ac-167">Exception:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="181ac-168">异常： HasAttachments</span><span class="sxs-lookup"><span data-stu-id="181ac-168">Exception:HasAttachments</span></span>
    
- <span data-ttu-id="181ac-169">异常：重要性</span><span class="sxs-lookup"><span data-stu-id="181ac-169">Exception:Importance</span></span>
    
- <span data-ttu-id="181ac-170">异常： IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="181ac-170">Exception:IsApprovalRequest</span></span>
    
- <span data-ttu-id="181ac-171">异常： IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="181ac-171">Exception:IsAutomaticForward</span></span>
    
- <span data-ttu-id="181ac-172">异常： IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="181ac-172">Exception:IsAutomaticReply</span></span>
    
- <span data-ttu-id="181ac-173">异常： IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="181ac-173">Exception:IsEncrypted</span></span>
    
- <span data-ttu-id="181ac-174">异常： IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="181ac-174">Exception:IsMeetingRequest</span></span>
    
- <span data-ttu-id="181ac-175">异常： IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="181ac-175">Exception:IsMeetingResponse</span></span>
    
- <span data-ttu-id="181ac-176">异常： IsNDR</span><span class="sxs-lookup"><span data-stu-id="181ac-176">Exception:IsNDR</span></span>
    
- <span data-ttu-id="181ac-177">异常： IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="181ac-177">Exception:IsPermissionControlled</span></span>
    
- <span data-ttu-id="181ac-178">异常： IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="181ac-178">Exception:IsReadReceipt</span></span>
    
- <span data-ttu-id="181ac-179">异常： IsSigned</span><span class="sxs-lookup"><span data-stu-id="181ac-179">Exception:IsSigned</span></span>
    
- <span data-ttu-id="181ac-180">异常： IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="181ac-180">Exception:IsVoicemail</span></span>
    
- <span data-ttu-id="181ac-181">异常： ItemClasses</span><span class="sxs-lookup"><span data-stu-id="181ac-181">Exception:ItemClasses</span></span>
    
- <span data-ttu-id="181ac-182">异常： MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="181ac-182">Exception:MessageClassifications</span></span>
    
- <span data-ttu-id="181ac-183">异常： NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-183">Exception:NotSentToMe</span></span>
    
- <span data-ttu-id="181ac-184">异常： SentCcMe</span><span class="sxs-lookup"><span data-stu-id="181ac-184">Exception:SentCcMe</span></span>
    
- <span data-ttu-id="181ac-185">异常： SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-185">Exception:SentOnlyToMe</span></span>
    
- <span data-ttu-id="181ac-186">异常： SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="181ac-186">Exception:SentToAddresses</span></span>
    
- <span data-ttu-id="181ac-187">异常： SentToMe</span><span class="sxs-lookup"><span data-stu-id="181ac-187">Exception:SentToMe</span></span>
    
- <span data-ttu-id="181ac-188">异常： SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="181ac-188">Exception:SentToOrCcMe</span></span>
    
- <span data-ttu-id="181ac-189">异常：敏感度</span><span class="sxs-lookup"><span data-stu-id="181ac-189">Exception:Sensitivity</span></span>
    
- <span data-ttu-id="181ac-190">异常： WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="181ac-190">Exception:WithinDateRange</span></span>
    
- <span data-ttu-id="181ac-191">异常： WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="181ac-191">Exception:WithinSizeRange</span></span>
    
- <span data-ttu-id="181ac-192">操作： AssignCategories</span><span class="sxs-lookup"><span data-stu-id="181ac-192">Action:AssignCategories</span></span>
    
- <span data-ttu-id="181ac-193">操作： CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="181ac-193">Action:CopyToFolder</span></span>
    
- <span data-ttu-id="181ac-194">操作：删除</span><span class="sxs-lookup"><span data-stu-id="181ac-194">Action:Delete</span></span>
    
- <span data-ttu-id="181ac-195">操作： ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="181ac-195">Action:ForwardAsAttachmentToRecipients</span></span>
    
- <span data-ttu-id="181ac-196">操作： ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="181ac-196">Action:ForwardToRecipients</span></span>
    
- <span data-ttu-id="181ac-197">操作： MarkImportance</span><span class="sxs-lookup"><span data-stu-id="181ac-197">Action:MarkImportance</span></span>
    
- <span data-ttu-id="181ac-198">操作： MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="181ac-198">Action:MarkAsRead</span></span>
    
- <span data-ttu-id="181ac-199">操作： MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="181ac-199">Action:MoveToFolder</span></span>
    
- <span data-ttu-id="181ac-200">操作： PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="181ac-200">Action:PermanentDelete</span></span>
    
- <span data-ttu-id="181ac-201">操作： RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="181ac-201">Action:RedirectToRecipients</span></span>
    
- <span data-ttu-id="181ac-202">操作： SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="181ac-202">Action:SendSMSAlertToRecipients</span></span>
    
- <span data-ttu-id="181ac-203">操作： ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="181ac-203">Action:ServerReplyWithMessage</span></span>
    
- <span data-ttu-id="181ac-204">操作： StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="181ac-204">Action:StopProcessingRules</span></span>
    
- <span data-ttu-id="181ac-205">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="181ac-205">IsEnabled</span></span>
    
- <span data-ttu-id="181ac-206">IsInError</span><span class="sxs-lookup"><span data-stu-id="181ac-206">IsInError</span></span>
    
- <span data-ttu-id="181ac-207">条件</span><span class="sxs-lookup"><span data-stu-id="181ac-207">Conditions</span></span>
    
- <span data-ttu-id="181ac-208">异常</span><span class="sxs-lookup"><span data-stu-id="181ac-208">Exceptions</span></span>
    
## <a name="remarks"></a><span data-ttu-id="181ac-209">说明</span><span class="sxs-lookup"><span data-stu-id="181ac-209">Remarks</span></span>

<span data-ttu-id="181ac-210">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="181ac-210">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="181ac-211">元素信息</span><span class="sxs-lookup"><span data-stu-id="181ac-211">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="181ac-212">命名空间</span><span class="sxs-lookup"><span data-stu-id="181ac-212">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="181ac-213">架构名称</span><span class="sxs-lookup"><span data-stu-id="181ac-213">Schema Name</span></span>  <br/> |<span data-ttu-id="181ac-214">消息架构</span><span class="sxs-lookup"><span data-stu-id="181ac-214">Messages schema</span></span>  <br/> |
|<span data-ttu-id="181ac-215">验证文件</span><span class="sxs-lookup"><span data-stu-id="181ac-215">Validation File</span></span>  <br/> |<span data-ttu-id="181ac-216">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="181ac-216">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="181ac-217">可以为空</span><span class="sxs-lookup"><span data-stu-id="181ac-217">Can be Empty</span></span>  <br/> |<span data-ttu-id="181ac-218">False</span><span class="sxs-lookup"><span data-stu-id="181ac-218">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="181ac-219">另请参阅</span><span class="sxs-lookup"><span data-stu-id="181ac-219">See also</span></span>



- [<span data-ttu-id="181ac-220">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="181ac-220">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

