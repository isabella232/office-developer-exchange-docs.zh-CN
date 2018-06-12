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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754295"
---
# <a name="fielduri-rule"></a><span data-ttu-id="eb3d5-103">FieldUri （规则）</span><span class="sxs-lookup"><span data-stu-id="eb3d5-103">FieldUri (Rule)</span></span>

<span data-ttu-id="eb3d5-104">**FieldURI**元素指定的规则字段导致验证错误的 URI。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-104">The **FieldURI** element specifies the URI to the rule field that caused the validation error.</span></span> 
  
```XML
<FieldURI/>
```

 <span data-ttu-id="eb3d5-105">**RuleFieldURIType**</span><span class="sxs-lookup"><span data-stu-id="eb3d5-105">**RuleFieldURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb3d5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb3d5-106">Attributes and elements</span></span>

<span data-ttu-id="eb3d5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb3d5-108">属性</span><span class="sxs-lookup"><span data-stu-id="eb3d5-108">Attributes</span></span>

<span data-ttu-id="eb3d5-109">无。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb3d5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eb3d5-110">Child elements</span></span>

<span data-ttu-id="eb3d5-111">无。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb3d5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="eb3d5-112">Parent elements</span></span>

|<span data-ttu-id="eb3d5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb3d5-113">**Element**</span></span>|<span data-ttu-id="eb3d5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb3d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb3d5-115">Error</span><span class="sxs-lookup"><span data-stu-id="eb3d5-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="eb3d5-116">代表对特定规则属性值、 谓词属性值或 action 属性值的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb3d5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="eb3d5-117">Text value</span></span>

<span data-ttu-id="eb3d5-118">此元素的文本值仅限于以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="eb3d5-119">规则 Id</span><span class="sxs-lookup"><span data-stu-id="eb3d5-119">RuleId</span></span>
    
- <span data-ttu-id="eb3d5-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb3d5-120">DisplayName</span></span>
    
- <span data-ttu-id="eb3d5-121">优先级</span><span class="sxs-lookup"><span data-stu-id="eb3d5-121">Priority</span></span>
    
- <span data-ttu-id="eb3d5-122">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="eb3d5-122">IsNotSupported</span></span>
    
- <span data-ttu-id="eb3d5-123">操作</span><span class="sxs-lookup"><span data-stu-id="eb3d5-123">Actions</span></span>
    
- <span data-ttu-id="eb3d5-124">条件： 类别</span><span class="sxs-lookup"><span data-stu-id="eb3d5-124">Condition:Categories</span></span>
    
- <span data-ttu-id="eb3d5-125">ContainsBodyStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-125">Condition:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="eb3d5-126">ContainsHeaderStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-126">Condition:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="eb3d5-127">ContainsRecipientStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-127">Condition:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="eb3d5-128">ContainsSenderStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-128">Condition:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="eb3d5-129">ContainsSubjectOrBodyStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-129">Condition:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="eb3d5-130">ContainsSubjectStrings 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-130">Condition:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="eb3d5-131">FlaggedForAction 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-131">Condition:FlaggedForAction</span></span>
    
- <span data-ttu-id="eb3d5-132">FromAddresses 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-132">Condition:FromAddresses</span></span>
    
- <span data-ttu-id="eb3d5-133">FromConnectedAccounts 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-133">Condition:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="eb3d5-134">HasAttachments 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-134">Condition:HasAttachments</span></span>
    
- <span data-ttu-id="eb3d5-135">条件： 重要性</span><span class="sxs-lookup"><span data-stu-id="eb3d5-135">Condition:Importance</span></span>
    
- <span data-ttu-id="eb3d5-136">IsApprovalRequest 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-136">Condition:IsApprovalRequest</span></span>
    
- <span data-ttu-id="eb3d5-137">IsAutomaticForward 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-137">Condition:IsAutomaticForward</span></span>
    
- <span data-ttu-id="eb3d5-138">IsAutomaticReply 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-138">Condition:IsAutomaticReply</span></span>
    
- <span data-ttu-id="eb3d5-139">进行加密条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-139">Condition:IsEncrypted</span></span>
    
- <span data-ttu-id="eb3d5-140">IsMeetingRequest 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-140">Condition:IsMeetingRequest</span></span>
    
- <span data-ttu-id="eb3d5-141">IsMeetingResponse 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-141">Condition:IsMeetingResponse</span></span>
    
- <span data-ttu-id="eb3d5-142">IsNDR 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-142">Condition:IsNDR</span></span>
    
- <span data-ttu-id="eb3d5-143">IsPermissionControlled 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-143">Condition:IsPermissionControlled</span></span>
    
- <span data-ttu-id="eb3d5-144">IsReadReceipt 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-144">Condition:IsReadReceipt</span></span>
    
- <span data-ttu-id="eb3d5-145">IsSigned 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-145">Condition:IsSigned</span></span>
    
- <span data-ttu-id="eb3d5-146">IsVoicemail 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-146">Condition:IsVoicemail</span></span>
    
- <span data-ttu-id="eb3d5-147">ItemClasses 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-147">Condition:ItemClasses</span></span>
    
- <span data-ttu-id="eb3d5-148">MessageClassifications 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-148">Condition:MessageClassifications</span></span>
    
- <span data-ttu-id="eb3d5-149">NotSentToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-149">Condition:NotSentToMe</span></span>
    
- <span data-ttu-id="eb3d5-150">SentCcMe 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-150">Condition:SentCcMe</span></span>
    
- <span data-ttu-id="eb3d5-151">SentOnlyToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-151">Condition:SentOnlyToMe</span></span>
    
- <span data-ttu-id="eb3d5-152">SentToAddresses 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-152">Condition:SentToAddresses</span></span>
    
- <span data-ttu-id="eb3d5-153">SentToMe 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-153">Condition:SentToMe</span></span>
    
- <span data-ttu-id="eb3d5-154">SentToOrCcMe 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-154">Condition:SentToOrCcMe</span></span>
    
- <span data-ttu-id="eb3d5-155">敏感度条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-155">Condition:Sensitivity</span></span>
    
- <span data-ttu-id="eb3d5-156">WithinDateRange 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-156">Condition:WithinDateRange</span></span>
    
- <span data-ttu-id="eb3d5-157">WithinSizeRange 条件：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-157">Condition:WithinSizeRange</span></span>
    
- <span data-ttu-id="eb3d5-158">异常： 类别</span><span class="sxs-lookup"><span data-stu-id="eb3d5-158">Exception:Categories</span></span>
    
- <span data-ttu-id="eb3d5-159">异常： ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-159">Exception:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="eb3d5-160">异常： ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-160">Exception:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="eb3d5-161">异常： ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-161">Exception:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="eb3d5-162">异常： ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-162">Exception:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="eb3d5-163">异常： ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-163">Exception:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="eb3d5-164">异常： ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="eb3d5-164">Exception:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="eb3d5-165">异常： FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="eb3d5-165">Exception:FlaggedForAction</span></span>
    
- <span data-ttu-id="eb3d5-166">异常： FromAddresses</span><span class="sxs-lookup"><span data-stu-id="eb3d5-166">Exception:FromAddresses</span></span>
    
- <span data-ttu-id="eb3d5-167">异常： FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="eb3d5-167">Exception:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="eb3d5-168">异常： HasAttachments</span><span class="sxs-lookup"><span data-stu-id="eb3d5-168">Exception:HasAttachments</span></span>
    
- <span data-ttu-id="eb3d5-169">异常： 重要性</span><span class="sxs-lookup"><span data-stu-id="eb3d5-169">Exception:Importance</span></span>
    
- <span data-ttu-id="eb3d5-170">异常： IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="eb3d5-170">Exception:IsApprovalRequest</span></span>
    
- <span data-ttu-id="eb3d5-171">异常： IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="eb3d5-171">Exception:IsAutomaticForward</span></span>
    
- <span data-ttu-id="eb3d5-172">异常： IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="eb3d5-172">Exception:IsAutomaticReply</span></span>
    
- <span data-ttu-id="eb3d5-173">异常： 进行加密</span><span class="sxs-lookup"><span data-stu-id="eb3d5-173">Exception:IsEncrypted</span></span>
    
- <span data-ttu-id="eb3d5-174">异常： IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="eb3d5-174">Exception:IsMeetingRequest</span></span>
    
- <span data-ttu-id="eb3d5-175">异常： IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="eb3d5-175">Exception:IsMeetingResponse</span></span>
    
- <span data-ttu-id="eb3d5-176">异常： IsNDR</span><span class="sxs-lookup"><span data-stu-id="eb3d5-176">Exception:IsNDR</span></span>
    
- <span data-ttu-id="eb3d5-177">异常： IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="eb3d5-177">Exception:IsPermissionControlled</span></span>
    
- <span data-ttu-id="eb3d5-178">异常： IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="eb3d5-178">Exception:IsReadReceipt</span></span>
    
- <span data-ttu-id="eb3d5-179">异常： IsSigned</span><span class="sxs-lookup"><span data-stu-id="eb3d5-179">Exception:IsSigned</span></span>
    
- <span data-ttu-id="eb3d5-180">异常： IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="eb3d5-180">Exception:IsVoicemail</span></span>
    
- <span data-ttu-id="eb3d5-181">异常： ItemClasses</span><span class="sxs-lookup"><span data-stu-id="eb3d5-181">Exception:ItemClasses</span></span>
    
- <span data-ttu-id="eb3d5-182">异常： MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="eb3d5-182">Exception:MessageClassifications</span></span>
    
- <span data-ttu-id="eb3d5-183">异常： NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="eb3d5-183">Exception:NotSentToMe</span></span>
    
- <span data-ttu-id="eb3d5-184">异常： SentCcMe</span><span class="sxs-lookup"><span data-stu-id="eb3d5-184">Exception:SentCcMe</span></span>
    
- <span data-ttu-id="eb3d5-185">异常： SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="eb3d5-185">Exception:SentOnlyToMe</span></span>
    
- <span data-ttu-id="eb3d5-186">异常： SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="eb3d5-186">Exception:SentToAddresses</span></span>
    
- <span data-ttu-id="eb3d5-187">异常： SentToMe</span><span class="sxs-lookup"><span data-stu-id="eb3d5-187">Exception:SentToMe</span></span>
    
- <span data-ttu-id="eb3d5-188">异常： SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="eb3d5-188">Exception:SentToOrCcMe</span></span>
    
- <span data-ttu-id="eb3d5-189">异常： 敏感度</span><span class="sxs-lookup"><span data-stu-id="eb3d5-189">Exception:Sensitivity</span></span>
    
- <span data-ttu-id="eb3d5-190">异常： WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="eb3d5-190">Exception:WithinDateRange</span></span>
    
- <span data-ttu-id="eb3d5-191">异常： WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="eb3d5-191">Exception:WithinSizeRange</span></span>
    
- <span data-ttu-id="eb3d5-192">AssignCategories 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-192">Action:AssignCategories</span></span>
    
- <span data-ttu-id="eb3d5-193">CopyToFolder 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-193">Action:CopyToFolder</span></span>
    
- <span data-ttu-id="eb3d5-194">删除操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-194">Action:Delete</span></span>
    
- <span data-ttu-id="eb3d5-195">ForwardAsAttachmentToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-195">Action:ForwardAsAttachmentToRecipients</span></span>
    
- <span data-ttu-id="eb3d5-196">ForwardToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-196">Action:ForwardToRecipients</span></span>
    
- <span data-ttu-id="eb3d5-197">MarkImportance 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-197">Action:MarkImportance</span></span>
    
- <span data-ttu-id="eb3d5-198">MarkAsRead 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-198">Action:MarkAsRead</span></span>
    
- <span data-ttu-id="eb3d5-199">MoveToFolder 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-199">Action:MoveToFolder</span></span>
    
- <span data-ttu-id="eb3d5-200">PermanentDelete 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-200">Action:PermanentDelete</span></span>
    
- <span data-ttu-id="eb3d5-201">RedirectToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-201">Action:RedirectToRecipients</span></span>
    
- <span data-ttu-id="eb3d5-202">SendSMSAlertToRecipients 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-202">Action:SendSMSAlertToRecipients</span></span>
    
- <span data-ttu-id="eb3d5-203">ServerReplyWithMessage 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-203">Action:ServerReplyWithMessage</span></span>
    
- <span data-ttu-id="eb3d5-204">StopProcessingRules 操作：</span><span class="sxs-lookup"><span data-stu-id="eb3d5-204">Action:StopProcessingRules</span></span>
    
- <span data-ttu-id="eb3d5-205">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="eb3d5-205">IsEnabled</span></span>
    
- <span data-ttu-id="eb3d5-206">IsInError</span><span class="sxs-lookup"><span data-stu-id="eb3d5-206">IsInError</span></span>
    
- <span data-ttu-id="eb3d5-207">条件</span><span class="sxs-lookup"><span data-stu-id="eb3d5-207">Conditions</span></span>
    
- <span data-ttu-id="eb3d5-208">异常</span><span class="sxs-lookup"><span data-stu-id="eb3d5-208">Exceptions</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb3d5-209">备注</span><span class="sxs-lookup"><span data-stu-id="eb3d5-209">Remarks</span></span>

<span data-ttu-id="eb3d5-210">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb3d5-210">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb3d5-211">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb3d5-211">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb3d5-212">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb3d5-212">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb3d5-213">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb3d5-213">Schema Name</span></span>  <br/> |<span data-ttu-id="eb3d5-214">消息架构</span><span class="sxs-lookup"><span data-stu-id="eb3d5-214">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb3d5-215">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb3d5-215">Validation File</span></span>  <br/> |<span data-ttu-id="eb3d5-216">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb3d5-216">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb3d5-217">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb3d5-217">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb3d5-218">False</span><span class="sxs-lookup"><span data-stu-id="eb3d5-218">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb3d5-219">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb3d5-219">See also</span></span>



- [<span data-ttu-id="eb3d5-220">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb3d5-220">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

