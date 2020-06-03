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
description: PendingMailTips 元素指示在服务器的处理超时过期之前无法评估此元素中的邮件提示。
ms.openlocfilehash: 715d68b367c3b7251c7406c10c1ec52dcd992a59
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529964"
---
# <a name="pendingmailtips"></a><span data-ttu-id="803dc-103">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="803dc-103">PendingMailTips</span></span>

<span data-ttu-id="803dc-104">**PendingMailTips**元素指示在服务器的处理超时过期之前无法评估此元素中的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="803dc-104">The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span> 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 <span data-ttu-id="803dc-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="803dc-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="803dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="803dc-106">Attributes and elements</span></span>

<span data-ttu-id="803dc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="803dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="803dc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="803dc-108">Attributes</span></span>

<span data-ttu-id="803dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="803dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="803dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="803dc-110">Child elements</span></span>

<span data-ttu-id="803dc-111">无。</span><span class="sxs-lookup"><span data-stu-id="803dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="803dc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="803dc-112">Parent elements</span></span>

|<span data-ttu-id="803dc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="803dc-113">**Element**</span></span>|<span data-ttu-id="803dc-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="803dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="803dc-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="803dc-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="803dc-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="803dc-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="803dc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="803dc-117">Text value</span></span>

<span data-ttu-id="803dc-118">下表列出了**PendingMailTips**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="803dc-118">The following table lists the possible values for the **PendingMailTips** element.</span></span> 
  
|<span data-ttu-id="803dc-119">**值**</span><span class="sxs-lookup"><span data-stu-id="803dc-119">**Value**</span></span>|<span data-ttu-id="803dc-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="803dc-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="803dc-121">所有</span><span class="sxs-lookup"><span data-stu-id="803dc-121">All</span></span>  <br/> |<span data-ttu-id="803dc-122">表示所有可用的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="803dc-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="803dc-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="803dc-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="803dc-124">代表 "外出" （OOF）邮件。</span><span class="sxs-lookup"><span data-stu-id="803dc-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="803dc-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="803dc-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="803dc-126">表示邮箱已满的状态。</span><span class="sxs-lookup"><span data-stu-id="803dc-126">Represents the status for a mailbox being full.</span></span>  <br/> |
|<span data-ttu-id="803dc-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="803dc-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="803dc-128">代表自定义邮件提示。</span><span class="sxs-lookup"><span data-stu-id="803dc-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="803dc-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="803dc-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="803dc-130">表示外部成员的计数。</span><span class="sxs-lookup"><span data-stu-id="803dc-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="803dc-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="803dc-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="803dc-132">表示所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="803dc-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="803dc-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="803dc-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="803dc-134">表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="803dc-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="803dc-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="803dc-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="803dc-136">指示传递限制是否将阻止发件人的邮件到达收件人。</span><span class="sxs-lookup"><span data-stu-id="803dc-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="803dc-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="803dc-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="803dc-138">指示审阅者是否会检查发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="803dc-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="803dc-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="803dc-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="803dc-140">指示收件人是否无效。</span><span class="sxs-lookup"><span data-stu-id="803dc-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="803dc-141">说明</span><span class="sxs-lookup"><span data-stu-id="803dc-141">Remarks</span></span>

<span data-ttu-id="803dc-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="803dc-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="803dc-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="803dc-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="803dc-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="803dc-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="803dc-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="803dc-145">Schema Name</span></span>  <br/> |<span data-ttu-id="803dc-146">类型架构</span><span class="sxs-lookup"><span data-stu-id="803dc-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="803dc-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="803dc-147">Validation File</span></span>  <br/> |<span data-ttu-id="803dc-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="803dc-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="803dc-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="803dc-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="803dc-150">False</span><span class="sxs-lookup"><span data-stu-id="803dc-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="803dc-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="803dc-151">See also</span></span>



- [<span data-ttu-id="803dc-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="803dc-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

