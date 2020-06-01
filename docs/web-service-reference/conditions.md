---
title: 条件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: 条件元素标识在满足时将触发规则的规则操作的条件。
ms.openlocfilehash: 2c6b4794a87cca79b4c723197b57360ad0ff973d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463200"
---
# <a name="conditions"></a><span data-ttu-id="69c2f-103">条件</span><span class="sxs-lookup"><span data-stu-id="69c2f-103">Conditions</span></span>

<span data-ttu-id="69c2f-104">**条件**元素标识在满足时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="69c2f-104">The **Conditions** element identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span> 
  
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

 <span data-ttu-id="69c2f-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="69c2f-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69c2f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69c2f-106">Attributes and elements</span></span>

<span data-ttu-id="69c2f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69c2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69c2f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="69c2f-108">Attributes</span></span>

<span data-ttu-id="69c2f-109">无。</span><span class="sxs-lookup"><span data-stu-id="69c2f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69c2f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="69c2f-110">Child elements</span></span>

|<span data-ttu-id="69c2f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="69c2f-111">**Element**</span></span>|<span data-ttu-id="69c2f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="69c2f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69c2f-113">Categories</span><span class="sxs-lookup"><span data-stu-id="69c2f-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="69c2f-114">包含必须应用于传入邮件的类别，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="69c2f-116">指示必须出现在传入邮件正文中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="69c2f-118">指示必须出现在传入邮件的标头中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-118">Indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="69c2f-120">指示必须出现在传入邮件的**ToRecipients**或**CcRecipients**属性中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="69c2f-122">指示必须出现在传入邮件的**From**属性中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="69c2f-124">指示必须出现在传入邮件的正文或主题中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="69c2f-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="69c2f-126">指示必须出现在传入邮件主题中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="69c2f-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="69c2f-128">指定必须出现在传入邮件上的 action 值标志，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="69c2f-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="69c2f-130">指示必须将传入邮件发送到的电子邮件地址，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="69c2f-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="69c2f-132">表示要对其进行聚合的传入邮件的电子邮件帐户名称，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="69c2f-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="69c2f-134">指示传入的邮件是否必须具有附件，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-135">Importance</span><span class="sxs-lookup"><span data-stu-id="69c2f-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="69c2f-136">指定在传入邮件上标记的重要性，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="69c2f-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="69c2f-138">指示传入的邮件是否必须是审批请求，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="69c2f-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="69c2f-140">指示传入的邮件是否必须自动转发，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="69c2f-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="69c2f-142">指示传入的邮件是否必须是自动答复，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-143">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="69c2f-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="69c2f-144">指示传入的邮件是否必须进行 S/MIME 加密，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="69c2f-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="69c2f-146">指示传入的邮件是否必须为会议请求，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="69c2f-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="69c2f-148">指示传入的邮件是否必须是会议响应，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="69c2f-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="69c2f-150">指示传入的邮件是否必须为未送达报告（Ndr），以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="69c2f-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="69c2f-152">指示传入的邮件是否必须受权限控制（受 RMS 保护），以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="69c2f-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="69c2f-154">指示传入的邮件是否必须为 "已读" 回执，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="69c2f-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="69c2f-156">指示传入的邮件是否必须进行 S/MIME 签名，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="69c2f-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="69c2f-158">指示传入的邮件是否必须是语音邮件，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="69c2f-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="69c2f-160">表示必须在传入的邮件上标记的项目类，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="69c2f-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="69c2f-162">表示必须在传入的邮件上标记的邮件分类，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="69c2f-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="69c2f-164">指示邮箱的所有者是否不得在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="69c2f-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="69c2f-166">指示邮箱的所有者是否必须在传入邮件的**CcRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="69c2f-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="69c2f-168">指示在传入邮件的**ToRecipients**属性中，邮箱的所有者是否必须是唯一的，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="69c2f-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="69c2f-170">指示必须向其发送传入邮件的电子邮件地址，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="69c2f-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="69c2f-172">指示邮箱的所有者是否必须在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="69c2f-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="69c2f-174">指示邮箱所有者是否必须在传入邮件的**ToRecipients**或**CcRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-175">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="69c2f-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="69c2f-176">指示必须在传入邮件上标记的灵敏度，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="69c2f-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="69c2f-178">指定要在其中接收传入邮件的日期范围，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="69c2f-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="69c2f-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="69c2f-180">指定传入邮件必须满足的最小和最大大小，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="69c2f-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69c2f-181">父元素</span><span class="sxs-lookup"><span data-stu-id="69c2f-181">Parent elements</span></span>

|<span data-ttu-id="69c2f-182">**元素**</span><span class="sxs-lookup"><span data-stu-id="69c2f-182">**Element**</span></span>|<span data-ttu-id="69c2f-183">**说明**</span><span class="sxs-lookup"><span data-stu-id="69c2f-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69c2f-184">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="69c2f-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="69c2f-185">包含单个规则并表示用户邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="69c2f-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69c2f-186">文本值</span><span class="sxs-lookup"><span data-stu-id="69c2f-186">Text value</span></span>

<span data-ttu-id="69c2f-187">无。</span><span class="sxs-lookup"><span data-stu-id="69c2f-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69c2f-188">说明</span><span class="sxs-lookup"><span data-stu-id="69c2f-188">Remarks</span></span>

<span data-ttu-id="69c2f-189">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="69c2f-189">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69c2f-190">元素信息</span><span class="sxs-lookup"><span data-stu-id="69c2f-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69c2f-191">命名空间</span><span class="sxs-lookup"><span data-stu-id="69c2f-191">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69c2f-192">架构名称</span><span class="sxs-lookup"><span data-stu-id="69c2f-192">Schema Name</span></span>  <br/> |<span data-ttu-id="69c2f-193">类型架构</span><span class="sxs-lookup"><span data-stu-id="69c2f-193">Types schema</span></span>  <br/> |
|<span data-ttu-id="69c2f-194">验证文件</span><span class="sxs-lookup"><span data-stu-id="69c2f-194">Validation File</span></span>  <br/> |<span data-ttu-id="69c2f-195">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69c2f-195">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69c2f-196">可以为空</span><span class="sxs-lookup"><span data-stu-id="69c2f-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="69c2f-197">True</span><span class="sxs-lookup"><span data-stu-id="69c2f-197">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69c2f-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69c2f-198">See also</span></span>



[<span data-ttu-id="69c2f-199">异常</span><span class="sxs-lookup"><span data-stu-id="69c2f-199">Exceptions</span></span>](exceptions.md)


- [<span data-ttu-id="69c2f-200">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="69c2f-200">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

