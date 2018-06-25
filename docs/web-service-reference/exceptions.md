---
title: 异常
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exceptions
api_type:
- schema
ms.assetid: 7cd63ac2-3441-4ed4-915b-6f90af4b28fc
description: 例外元素标识表示收件箱规则的所有可用规则例外条件的例外。
ms.openlocfilehash: b875b4dc0029bb9e0bc2bb50c41569fb72ef9268
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754185"
---
# <a name="exceptions"></a><span data-ttu-id="d1ce3-103">异常</span><span class="sxs-lookup"><span data-stu-id="d1ce3-103">Exceptions</span></span>

<span data-ttu-id="d1ce3-104">**例外**元素标识表示收件箱规则的所有可用规则例外条件的例外。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-104">The **Exceptions** element identifies the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span> 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 <span data-ttu-id="d1ce3-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="d1ce3-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1ce3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1ce3-106">Attributes and elements</span></span>

<span data-ttu-id="d1ce3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1ce3-108">属性</span><span class="sxs-lookup"><span data-stu-id="d1ce3-108">Attributes</span></span>

<span data-ttu-id="d1ce3-109">无。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1ce3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d1ce3-110">Child elements</span></span>

|<span data-ttu-id="d1ce3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1ce3-111">**Element**</span></span>|<span data-ttu-id="d1ce3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1ce3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1ce3-113">Categories</span><span class="sxs-lookup"><span data-stu-id="d1ce3-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d1ce3-114">包含必须应用于的条件或例外应用的顺序中的传入邮件的类别。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="d1ce3-116">指示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="d1ce3-118">Indicaqtes 必须应用的条件或例外顺序中的传入消息头中显示的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-118">Indicaqtes the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="d1ce3-120">指示必须出现在**ToRecipients**或**CcRecipients**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="d1ce3-122">指示必须出现在**From**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="d1ce3-124">指示必须出现在正文或中的条件或例外应用的顺序的传入邮件的主题的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="d1ce3-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="d1ce3-126">指示必须在主题中的条件或例外应用的顺序的传入消息中显示的字符串。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="d1ce3-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="d1ce3-128">指定对传入邮件中的条件或例外的顺序应用操作值，必须在出现的标志。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="d1ce3-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="d1ce3-130">指示必须从其发送传入消息的条件或例外的顺序应用中的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="d1ce3-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="d1ce3-132">表示具有已聚合中的条件或例外的顺序应用传入消息的电子邮件帐户名。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d1ce3-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d1ce3-134">指示是否具有传入消息，使其具有附件中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-135">Importance</span><span class="sxs-lookup"><span data-stu-id="d1ce3-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d1ce3-136">指定对传入邮件中的条件或例外应用的顺序标的重要性。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="d1ce3-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="d1ce3-138">指示是否必须审批请求中的条件或例外的顺序应用传入消息。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="d1ce3-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="d1ce3-140">指示是否必须按条件或例外的顺序应用自动转发传入消息。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="d1ce3-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="d1ce3-142">指示是否必须按条件或例外的顺序应用的自动答复传入消息。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-143">进行加密</span><span class="sxs-lookup"><span data-stu-id="d1ce3-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="d1ce3-144">指示是否必须 S/MIME 加密的条件或例外的顺序应用传入消息。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d1ce3-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="d1ce3-146">指示是否必须传入消息会议请求中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d1ce3-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="d1ce3-148">指示是否必须会议传入消息的条件或例外的顺序应用中的响应。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="d1ce3-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="d1ce3-150">指示的条件或例外应用的顺序中的传入邮件是否必须以未送达报告 (Ndr)。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="d1ce3-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="d1ce3-152">指示传入邮件是否必须进行的条件或例外应用的顺序中控制权限 (受 RMS 保护)</span><span class="sxs-lookup"><span data-stu-id="d1ce3-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="d1ce3-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="d1ce3-154">指示是否必须读取传入消息中的条件或例外应用的顺序的回执。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="d1ce3-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="d1ce3-156">指示传入邮件是否必须 S/MIME 签名中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="d1ce3-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="d1ce3-158">指示是否传入消息必须应用的条件或例外顺序中的语音邮件消息。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="d1ce3-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="d1ce3-160">代表必须在应用的条件或例外顺序中的传入邮件标记的项类。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="d1ce3-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="d1ce3-162">代表必须在应用的条件或例外顺序中的传入邮件标记邮件分类。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="d1ce3-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="d1ce3-164">指示是否中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中不能邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="d1ce3-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="d1ce3-166">指示是否要应用的条件或例外顺序中的传入消息的**CcRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="d1ce3-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="d1ce3-168">指示是否邮箱所有者必须是唯一的条件或例外应用的顺序中的传入消息的**ToRecipients**属性中。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="d1ce3-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="d1ce3-170">指示需要中的条件或例外的顺序应用发送给传入消息的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="d1ce3-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="d1ce3-172">指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="d1ce3-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="d1ce3-174">指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**或**CcRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-175">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d1ce3-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d1ce3-176">指示必须在应用的条件或例外顺序中的传入邮件标记的敏感度。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="d1ce3-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="d1ce3-178">指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d1ce3-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="d1ce3-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="d1ce3-180">指定的条件或例外的顺序应用必须传入消息的最小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1ce3-181">父元素</span><span class="sxs-lookup"><span data-stu-id="d1ce3-181">Parent elements</span></span>

|<span data-ttu-id="d1ce3-182">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1ce3-182">**Element**</span></span>|<span data-ttu-id="d1ce3-183">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1ce3-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1ce3-184">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="d1ce3-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="d1ce3-185">包含单一规则并代表用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1ce3-186">文本值</span><span class="sxs-lookup"><span data-stu-id="d1ce3-186">Text value</span></span>

<span data-ttu-id="d1ce3-187">无。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1ce3-188">注解</span><span class="sxs-lookup"><span data-stu-id="d1ce3-188">Remarks</span></span>

<span data-ttu-id="d1ce3-189">规则谓词用作规则条件或例外。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-189">The rule predicates are used as rule conditions or exceptions.</span></span>
  
<span data-ttu-id="d1ce3-190">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d1ce3-190">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1ce3-191">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1ce3-191">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1ce3-192">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1ce3-192">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1ce3-193">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1ce3-193">Schema Name</span></span>  <br/> |<span data-ttu-id="d1ce3-194">类型架构</span><span class="sxs-lookup"><span data-stu-id="d1ce3-194">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1ce3-195">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1ce3-195">Validation File</span></span>  <br/> |<span data-ttu-id="d1ce3-196">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1ce3-196">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1ce3-197">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1ce3-197">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1ce3-198">True</span><span class="sxs-lookup"><span data-stu-id="d1ce3-198">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1ce3-199">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1ce3-199">See also</span></span>



[<span data-ttu-id="d1ce3-200">条件</span><span class="sxs-lookup"><span data-stu-id="d1ce3-200">Conditions</span></span>](conditions.md)


- [<span data-ttu-id="d1ce3-201">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d1ce3-201">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

