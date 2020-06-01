---
title: 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Actions 元素表示在满足条件时可对邮件执行的一组操作。
ms.openlocfilehash: 2ac53778b583595fa8be07f2c5110a9e2df16eca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465063"
---
# <a name="actions"></a><span data-ttu-id="2a8b4-103">操作</span><span class="sxs-lookup"><span data-stu-id="2a8b4-103">Actions</span></span>

<span data-ttu-id="2a8b4-104">**Actions**元素表示在满足条件时可对邮件执行的一组操作。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-104">The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span> 
  
[<span data-ttu-id="2a8b4-105">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="2a8b4-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 <span data-ttu-id="2a8b4-106">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="2a8b4-106">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a8b4-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a8b4-107">Attributes and elements</span></span>

<span data-ttu-id="2a8b4-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a8b4-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="2a8b4-109">Attributes</span></span>

<span data-ttu-id="2a8b4-110">无。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a8b4-111">子元素</span><span class="sxs-lookup"><span data-stu-id="2a8b4-111">Child elements</span></span>

|<span data-ttu-id="2a8b4-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a8b4-112">**Element**</span></span>|<span data-ttu-id="2a8b4-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a8b4-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a8b4-114">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="2a8b4-114">AssignCategories</span></span>](assigncategories.md) <br/> |<span data-ttu-id="2a8b4-115">代表电子邮件上标记的类别。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-115">Represents the categories that are stamped on e-mail messages.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-116">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="2a8b4-116">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="2a8b4-117">标识电子邮件项目将复制到的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-117">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-118">删除</span><span class="sxs-lookup"><span data-stu-id="2a8b4-118">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="2a8b4-119">指示是否将邮件移动到 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-119">Indicates whether messages are to be moved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-120">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="2a8b4-120">ForwardAsAttachmentToRecipients</span></span>](forwardasattachmenttorecipients.md) <br/> |<span data-ttu-id="2a8b4-121">指示邮件将作为附件转发到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-121">Indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-122">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="2a8b4-122">ForwardToRecipients</span></span>](forwardtorecipients.md) <br/> |<span data-ttu-id="2a8b4-123">指示邮件要转发到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-123">Indicates the e-mail addresses to which messages are to be forwarded.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-124">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="2a8b4-124">MarkImportance</span></span>](markimportance.md) <br/> |<span data-ttu-id="2a8b4-125">指定要在邮件上标记的重要性。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-125">Specifies the importance that is to be stamped on messages.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-126">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="2a8b4-126">MarkAsRead</span></span>](markasread.md) <br/> |<span data-ttu-id="2a8b4-127">指示是否将邮件标记为已读。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-127">Indicates whether messages are to be marked as read.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-128">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="2a8b4-128">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="2a8b4-129">标识电子邮件项目将移动到的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-129">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-130">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="2a8b4-130">PermanentDelete</span></span>](permanentdelete.md) <br/> |<span data-ttu-id="2a8b4-131">指示是否要永久删除邮件，而不将其保存到 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-131">Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-132">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="2a8b4-132">RedirectToRecipients</span></span>](redirecttorecipients.md) <br/> |<span data-ttu-id="2a8b4-133">指示邮件将被重定向到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-133">Indicates the e-mail addresses to which messages are to be redirected.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-134">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="2a8b4-134">SendSMSAlertToRecipients</span></span>](sendsmsalerttorecipients.md) <br/> |<span data-ttu-id="2a8b4-135">指示要向其发送短信服务（SMS）警报的移动电话号码。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-135">Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-136">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="2a8b4-136">ServerReplyWithMessage</span></span>](serverreplywithmessage.md) <br/> |<span data-ttu-id="2a8b4-137">指示.</span><span class="sxs-lookup"><span data-stu-id="2a8b4-137">Indicates.</span></span> <span data-ttu-id="2a8b4-138">要作为对传入邮件的答复发送的模板邮件的 ID。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-138">the ID of the template message that is to be sent as a reply to incoming messages.</span></span>  <br/> |
|[<span data-ttu-id="2a8b4-139">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="2a8b4-139">StopProcessingRules</span></span>](stopprocessingrules.md) <br/> |<span data-ttu-id="2a8b4-140">指示是否要计算后续规则。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-140">Indicates whether subsequent rules are to be evaluated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a8b4-141">父元素</span><span class="sxs-lookup"><span data-stu-id="2a8b4-141">Parent elements</span></span>

|<span data-ttu-id="2a8b4-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a8b4-142">**Element**</span></span>|<span data-ttu-id="2a8b4-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a8b4-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a8b4-144">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="2a8b4-144">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="2a8b4-145">代表用户邮箱中的单个规则。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-145">Represents a single rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a8b4-146">文本值</span><span class="sxs-lookup"><span data-stu-id="2a8b4-146">Text value</span></span>

<span data-ttu-id="2a8b4-147">无。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-147">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a8b4-148">说明</span><span class="sxs-lookup"><span data-stu-id="2a8b4-148">Remarks</span></span>

<span data-ttu-id="2a8b4-149">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2a8b4-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a8b4-150">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a8b4-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a8b4-151">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a8b4-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a8b4-152">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a8b4-152">Schema Name</span></span>  <br/> |<span data-ttu-id="2a8b4-153">类型架构</span><span class="sxs-lookup"><span data-stu-id="2a8b4-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a8b4-154">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a8b4-154">Validation File</span></span>  <br/> |<span data-ttu-id="2a8b4-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a8b4-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a8b4-156">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a8b4-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a8b4-157">True</span><span class="sxs-lookup"><span data-stu-id="2a8b4-157">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a8b4-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a8b4-158">See also</span></span>

- [<span data-ttu-id="2a8b4-159">条件</span><span class="sxs-lookup"><span data-stu-id="2a8b4-159">Conditions</span></span>](conditions.md)
- [<span data-ttu-id="2a8b4-160">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2a8b4-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

