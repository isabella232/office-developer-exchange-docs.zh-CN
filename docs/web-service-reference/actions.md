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
description: Actions 元素表示一的组操作可用于满足条件时要采取的上一条消息。
ms.openlocfilehash: 093d2f28135c6077b6cea488591573af0182934b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753098"
---
# <a name="actions"></a><span data-ttu-id="84c9a-103">操作</span><span class="sxs-lookup"><span data-stu-id="84c9a-103">Actions</span></span>

<span data-ttu-id="84c9a-104">**Actions**元素表示一的组操作可用于满足条件时要采取的上一条消息。</span><span class="sxs-lookup"><span data-stu-id="84c9a-104">The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span> 
  
[<span data-ttu-id="84c9a-105">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="84c9a-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
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

 <span data-ttu-id="84c9a-106">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="84c9a-106">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84c9a-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84c9a-107">Attributes and elements</span></span>

<span data-ttu-id="84c9a-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84c9a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84c9a-109">属性</span><span class="sxs-lookup"><span data-stu-id="84c9a-109">Attributes</span></span>

<span data-ttu-id="84c9a-110">无。</span><span class="sxs-lookup"><span data-stu-id="84c9a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84c9a-111">子元素</span><span class="sxs-lookup"><span data-stu-id="84c9a-111">Child elements</span></span>

|<span data-ttu-id="84c9a-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="84c9a-112">**Element**</span></span>|<span data-ttu-id="84c9a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="84c9a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84c9a-114">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="84c9a-114">AssignCategories</span></span>](assigncategories.md) <br/> |<span data-ttu-id="84c9a-115">代表在电子邮件标记的类别。</span><span class="sxs-lookup"><span data-stu-id="84c9a-115">Represents the categories that are stamped on e-mail messages.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-116">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="84c9a-116">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="84c9a-117">标识的文件夹的电子邮件项目将被复制到的 ID。</span><span class="sxs-lookup"><span data-stu-id="84c9a-117">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-118">删除</span><span class="sxs-lookup"><span data-stu-id="84c9a-118">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="84c9a-119">指示邮件是否被移动到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="84c9a-119">Indicates whether messages are to be moved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-120">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="84c9a-120">ForwardAsAttachmentToRecipients</span></span>](forwardasattachmenttorecipients.md) <br/> |<span data-ttu-id="84c9a-121">指示邮件是作为附件转发的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="84c9a-121">Indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-122">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="84c9a-122">ForwardToRecipients</span></span>](forwardtorecipients.md) <br/> |<span data-ttu-id="84c9a-123">指示邮件将被转接到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="84c9a-123">Indicates the e-mail addresses to which messages are to be forwarded.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-124">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="84c9a-124">MarkImportance</span></span>](markimportance.md) <br/> |<span data-ttu-id="84c9a-125">指定要在邮件上标记的重要性。</span><span class="sxs-lookup"><span data-stu-id="84c9a-125">Specifies the importance that is to be stamped on messages.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-126">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="84c9a-126">MarkAsRead</span></span>](markasread.md) <br/> |<span data-ttu-id="84c9a-127">指示是否要标记为已读消息。</span><span class="sxs-lookup"><span data-stu-id="84c9a-127">Indicates whether messages are to be marked as read.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-128">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="84c9a-128">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="84c9a-129">标识的文件夹的电子邮件项目将移动到的 ID。</span><span class="sxs-lookup"><span data-stu-id="84c9a-129">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-130">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="84c9a-130">PermanentDelete</span></span>](permanentdelete.md) <br/> |<span data-ttu-id="84c9a-131">指示邮件是否被永久删除和不保存到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="84c9a-131">Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-132">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="84c9a-132">RedirectToRecipients</span></span>](redirecttorecipients.md) <br/> |<span data-ttu-id="84c9a-133">指示邮件将被重定向到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="84c9a-133">Indicates the e-mail addresses to which messages are to be redirected.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-134">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="84c9a-134">SendSMSAlertToRecipients</span></span>](sendsmsalerttorecipients.md) <br/> |<span data-ttu-id="84c9a-135">指示短信服务 (SMS) 通知将发送到移动电话号码。</span><span class="sxs-lookup"><span data-stu-id="84c9a-135">Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-136">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="84c9a-136">ServerReplyWithMessage</span></span>](serverreplywithmessage.md) <br/> |<span data-ttu-id="84c9a-137">指示。</span><span class="sxs-lookup"><span data-stu-id="84c9a-137">Indicates.</span></span> <span data-ttu-id="84c9a-138">是作为对传入邮件的回复发送的模板邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="84c9a-138">the ID of the template message that is to be sent as a reply to incoming messages.</span></span>  <br/> |
|[<span data-ttu-id="84c9a-139">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="84c9a-139">StopProcessingRules</span></span>](stopprocessingrules.md) <br/> |<span data-ttu-id="84c9a-140">指示是否要进行求值后续规则。</span><span class="sxs-lookup"><span data-stu-id="84c9a-140">Indicates whether subsequent rules are to be evaluated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84c9a-141">父元素</span><span class="sxs-lookup"><span data-stu-id="84c9a-141">Parent elements</span></span>

|<span data-ttu-id="84c9a-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="84c9a-142">**Element**</span></span>|<span data-ttu-id="84c9a-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="84c9a-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84c9a-144">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="84c9a-144">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="84c9a-145">代表用户的邮箱中的单个规则。</span><span class="sxs-lookup"><span data-stu-id="84c9a-145">Represents a single rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84c9a-146">文本值</span><span class="sxs-lookup"><span data-stu-id="84c9a-146">Text value</span></span>

<span data-ttu-id="84c9a-147">无。</span><span class="sxs-lookup"><span data-stu-id="84c9a-147">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84c9a-148">备注</span><span class="sxs-lookup"><span data-stu-id="84c9a-148">Remarks</span></span>

<span data-ttu-id="84c9a-149">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84c9a-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84c9a-150">元素信息</span><span class="sxs-lookup"><span data-stu-id="84c9a-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84c9a-151">命名空间</span><span class="sxs-lookup"><span data-stu-id="84c9a-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84c9a-152">架构名称</span><span class="sxs-lookup"><span data-stu-id="84c9a-152">Schema Name</span></span>  <br/> |<span data-ttu-id="84c9a-153">类型架构</span><span class="sxs-lookup"><span data-stu-id="84c9a-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="84c9a-154">验证文件</span><span class="sxs-lookup"><span data-stu-id="84c9a-154">Validation File</span></span>  <br/> |<span data-ttu-id="84c9a-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84c9a-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84c9a-156">可以为空</span><span class="sxs-lookup"><span data-stu-id="84c9a-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="84c9a-157">True</span><span class="sxs-lookup"><span data-stu-id="84c9a-157">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84c9a-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84c9a-158">See also</span></span>

- [<span data-ttu-id="84c9a-159">条件</span><span class="sxs-lookup"><span data-stu-id="84c9a-159">Conditions</span></span>](conditions.md)
- [<span data-ttu-id="84c9a-160">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84c9a-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

