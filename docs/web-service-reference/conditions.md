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
description: Conditions 元素标识条件，履行时, 将触发规则的规则操作。
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753476"
---
# <a name="conditions"></a><span data-ttu-id="ccec1-103">条件</span><span class="sxs-lookup"><span data-stu-id="ccec1-103">Conditions</span></span>

<span data-ttu-id="ccec1-104">**Conditions**元素标识条件，履行时, 将触发规则的规则操作。</span><span class="sxs-lookup"><span data-stu-id="ccec1-104">The **Conditions** element identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span> 
  
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

 <span data-ttu-id="ccec1-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="ccec1-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccec1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ccec1-106">Attributes and elements</span></span>

<span data-ttu-id="ccec1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ccec1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccec1-108">属性</span><span class="sxs-lookup"><span data-stu-id="ccec1-108">Attributes</span></span>

<span data-ttu-id="ccec1-109">无。</span><span class="sxs-lookup"><span data-stu-id="ccec1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccec1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ccec1-110">Child elements</span></span>

|<span data-ttu-id="ccec1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccec1-111">**Element**</span></span>|<span data-ttu-id="ccec1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccec1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccec1-113">Categories</span><span class="sxs-lookup"><span data-stu-id="ccec1-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ccec1-114">包含必须应用于的条件或例外应用的顺序中的传入邮件的类别。</span><span class="sxs-lookup"><span data-stu-id="ccec1-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="ccec1-116">指示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="ccec1-118">指示必须应用的条件或例外顺序中的传入消息头中显示的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-118">Indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="ccec1-120">指示必须出现在**ToRecipients**或**CcRecipients**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="ccec1-122">指示必须出现在**From**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="ccec1-124">指示必须出现在正文或中的条件或例外应用的顺序的传入邮件的主题的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="ccec1-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="ccec1-126">指示必须在主题中的条件或例外应用的顺序的传入消息中显示的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec1-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="ccec1-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="ccec1-128">指定对传入邮件中的条件或例外的顺序应用操作值，必须在出现的标志。</span><span class="sxs-lookup"><span data-stu-id="ccec1-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="ccec1-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="ccec1-130">指示必须从其发送传入消息的条件或例外的顺序应用中的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ccec1-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="ccec1-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="ccec1-132">表示具有已聚合中的条件或例外的顺序应用传入消息的电子邮件帐户名。</span><span class="sxs-lookup"><span data-stu-id="ccec1-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="ccec1-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="ccec1-134">指示是否具有传入消息，使其具有附件中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ccec1-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-135">Importance</span><span class="sxs-lookup"><span data-stu-id="ccec1-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="ccec1-136">指定对传入邮件中的条件或例外应用的顺序标的重要性。</span><span class="sxs-lookup"><span data-stu-id="ccec1-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="ccec1-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="ccec1-138">指示是否必须审批请求中的条件或例外的顺序应用传入消息。</span><span class="sxs-lookup"><span data-stu-id="ccec1-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="ccec1-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="ccec1-140">指示是否必须按条件或例外的顺序应用自动转发传入消息。</span><span class="sxs-lookup"><span data-stu-id="ccec1-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="ccec1-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="ccec1-142">指示是否必须按条件或例外的顺序应用的自动答复传入消息。</span><span class="sxs-lookup"><span data-stu-id="ccec1-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-143">进行加密</span><span class="sxs-lookup"><span data-stu-id="ccec1-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="ccec1-144">指示是否必须 S/MIME 加密的条件或例外的顺序应用传入消息。</span><span class="sxs-lookup"><span data-stu-id="ccec1-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ccec1-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="ccec1-146">指示是否必须传入消息会议请求中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ccec1-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ccec1-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="ccec1-148">指示是否必须会议传入消息的条件或例外的顺序应用中的响应。</span><span class="sxs-lookup"><span data-stu-id="ccec1-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="ccec1-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="ccec1-150">指示的条件或例外应用的顺序中的传入邮件是否必须以未送达报告 (Ndr)。</span><span class="sxs-lookup"><span data-stu-id="ccec1-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="ccec1-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="ccec1-152">指示传入邮件是否必须进行的条件或例外应用的顺序中控制权限 (受 RMS 保护)。</span><span class="sxs-lookup"><span data-stu-id="ccec1-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="ccec1-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="ccec1-154">指示是否必须读取传入消息中的条件或例外应用的顺序的回执。</span><span class="sxs-lookup"><span data-stu-id="ccec1-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="ccec1-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="ccec1-156">指示传入邮件是否必须 S/MIME 签名中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ccec1-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="ccec1-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="ccec1-158">指示是否传入消息必须应用的条件或例外顺序中的语音邮件消息。</span><span class="sxs-lookup"><span data-stu-id="ccec1-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="ccec1-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="ccec1-160">代表必须在应用的条件或例外顺序中的传入邮件标记的项类。</span><span class="sxs-lookup"><span data-stu-id="ccec1-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="ccec1-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="ccec1-162">代表必须在应用的条件或例外顺序中的传入邮件标记邮件分类。</span><span class="sxs-lookup"><span data-stu-id="ccec1-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="ccec1-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="ccec1-164">指示是否中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中不能邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="ccec1-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="ccec1-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="ccec1-166">指示是否要应用的条件或例外顺序中的传入消息的**CcRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="ccec1-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="ccec1-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="ccec1-168">指示是否邮箱所有者必须是唯一的条件或例外应用的顺序中的传入消息的**ToRecipients**属性中。</span><span class="sxs-lookup"><span data-stu-id="ccec1-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="ccec1-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="ccec1-170">指示需要中的条件或例外的顺序应用发送给传入消息的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ccec1-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="ccec1-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="ccec1-172">指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="ccec1-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="ccec1-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="ccec1-174">指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**或**CcRecipients**属性中的邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="ccec1-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-175">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ccec1-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="ccec1-176">指示必须在应用的条件或例外顺序中的传入邮件标记的敏感度。</span><span class="sxs-lookup"><span data-stu-id="ccec1-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="ccec1-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="ccec1-178">指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。</span><span class="sxs-lookup"><span data-stu-id="ccec1-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="ccec1-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="ccec1-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="ccec1-180">指定的条件或例外的顺序应用必须传入消息的最小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="ccec1-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccec1-181">父元素</span><span class="sxs-lookup"><span data-stu-id="ccec1-181">Parent elements</span></span>

|<span data-ttu-id="ccec1-182">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccec1-182">**Element**</span></span>|<span data-ttu-id="ccec1-183">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccec1-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccec1-184">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="ccec1-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="ccec1-185">包含单一规则并代表用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="ccec1-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccec1-186">文本值</span><span class="sxs-lookup"><span data-stu-id="ccec1-186">Text value</span></span>

<span data-ttu-id="ccec1-187">无。</span><span class="sxs-lookup"><span data-stu-id="ccec1-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccec1-188">备注</span><span class="sxs-lookup"><span data-stu-id="ccec1-188">Remarks</span></span>

<span data-ttu-id="ccec1-189">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ccec1-189">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccec1-190">元素信息</span><span class="sxs-lookup"><span data-stu-id="ccec1-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccec1-191">命名空间</span><span class="sxs-lookup"><span data-stu-id="ccec1-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccec1-192">架构名称</span><span class="sxs-lookup"><span data-stu-id="ccec1-192">Schema Name</span></span>  <br/> |<span data-ttu-id="ccec1-193">类型架构</span><span class="sxs-lookup"><span data-stu-id="ccec1-193">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccec1-194">验证文件</span><span class="sxs-lookup"><span data-stu-id="ccec1-194">Validation File</span></span>  <br/> |<span data-ttu-id="ccec1-195">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ccec1-195">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccec1-196">可以为空</span><span class="sxs-lookup"><span data-stu-id="ccec1-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccec1-197">True</span><span class="sxs-lookup"><span data-stu-id="ccec1-197">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccec1-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ccec1-198">See also</span></span>



[<span data-ttu-id="ccec1-199">异常</span><span class="sxs-lookup"><span data-stu-id="ccec1-199">Exceptions</span></span>](exceptions.md)


- [<span data-ttu-id="ccec1-200">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ccec1-200">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

