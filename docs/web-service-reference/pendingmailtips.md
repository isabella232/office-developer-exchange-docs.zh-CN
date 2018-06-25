---
title: PendingMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: PendingMailTips 元素表示服务器的处理超时之前，可能不评估此元素中的邮件提示。
ms.openlocfilehash: 73d597f6534ea29f7d26d6526c48631251521ae5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826704"
---
# <a name="pendingmailtips"></a><span data-ttu-id="a37b9-103">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="a37b9-103">PendingMailTips</span></span>

<span data-ttu-id="a37b9-104">**PendingMailTips**元素表示服务器的处理超时之前，可能不评估此元素中的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="a37b9-104">The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span> 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 <span data-ttu-id="a37b9-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="a37b9-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a37b9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a37b9-106">Attributes and elements</span></span>

<span data-ttu-id="a37b9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a37b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a37b9-108">属性</span><span class="sxs-lookup"><span data-stu-id="a37b9-108">Attributes</span></span>

<span data-ttu-id="a37b9-109">无。</span><span class="sxs-lookup"><span data-stu-id="a37b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a37b9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a37b9-110">Child elements</span></span>

<span data-ttu-id="a37b9-111">无。</span><span class="sxs-lookup"><span data-stu-id="a37b9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a37b9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a37b9-112">Parent elements</span></span>

|<span data-ttu-id="a37b9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a37b9-113">**Element**</span></span>|<span data-ttu-id="a37b9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a37b9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a37b9-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="a37b9-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="a37b9-116">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="a37b9-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a37b9-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a37b9-117">Text value</span></span>

<span data-ttu-id="a37b9-118">下表列出了**PendingMailTips**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="a37b9-118">The following table lists the possible values for the **PendingMailTips** element.</span></span> 
  
|<span data-ttu-id="a37b9-119">**值**</span><span class="sxs-lookup"><span data-stu-id="a37b9-119">**Value**</span></span>|<span data-ttu-id="a37b9-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="a37b9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a37b9-121">所有</span><span class="sxs-lookup"><span data-stu-id="a37b9-121">All</span></span>  <br/> |<span data-ttu-id="a37b9-122">代表所有可用的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="a37b9-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="a37b9-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="a37b9-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="a37b9-124">代表外出 (OOF) 邮件。</span><span class="sxs-lookup"><span data-stu-id="a37b9-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="a37b9-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="a37b9-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="a37b9-126">表示邮箱已满的状态。</span><span class="sxs-lookup"><span data-stu-id="a37b9-126">Represents the status for a mailbox being full.</span></span>  <br/> |
|<span data-ttu-id="a37b9-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="a37b9-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="a37b9-128">代表自定义邮件提示。</span><span class="sxs-lookup"><span data-stu-id="a37b9-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="a37b9-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="a37b9-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="a37b9-130">表示外部成员计数。</span><span class="sxs-lookup"><span data-stu-id="a37b9-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="a37b9-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="a37b9-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="a37b9-132">表示所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="a37b9-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="a37b9-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="a37b9-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="a37b9-134">表示收件人可以接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="a37b9-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="a37b9-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="a37b9-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="a37b9-136">指示传递限制是否将到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="a37b9-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="a37b9-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="a37b9-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="a37b9-138">指示是否将由审阅者审查发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="a37b9-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="a37b9-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="a37b9-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="a37b9-140">指示收件人无效。</span><span class="sxs-lookup"><span data-stu-id="a37b9-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a37b9-141">备注</span><span class="sxs-lookup"><span data-stu-id="a37b9-141">Remarks</span></span>

<span data-ttu-id="a37b9-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a37b9-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a37b9-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="a37b9-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a37b9-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="a37b9-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a37b9-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="a37b9-145">Schema Name</span></span>  <br/> |<span data-ttu-id="a37b9-146">类型架构</span><span class="sxs-lookup"><span data-stu-id="a37b9-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="a37b9-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="a37b9-147">Validation File</span></span>  <br/> |<span data-ttu-id="a37b9-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a37b9-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a37b9-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="a37b9-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="a37b9-150">False</span><span class="sxs-lookup"><span data-stu-id="a37b9-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a37b9-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a37b9-151">See also</span></span>



- [<span data-ttu-id="a37b9-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a37b9-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

