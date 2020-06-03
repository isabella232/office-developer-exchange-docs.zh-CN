---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: MailTipsRequested 元素包含从服务请求的邮件提示的类型。
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465896"
---
# <a name="mailtipsrequested"></a><span data-ttu-id="6d416-103">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="6d416-103">MailTipsRequested</span></span>

<span data-ttu-id="6d416-104">**MailTipsRequested**元素包含从服务请求的邮件提示的类型。</span><span class="sxs-lookup"><span data-stu-id="6d416-104">The **MailTipsRequested** element contains the types of mail tips requested from the service.</span></span> 
  
```XML
<MailTipsRequested/>
```

 <span data-ttu-id="6d416-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="6d416-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d416-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6d416-106">Attributes and elements</span></span>

<span data-ttu-id="6d416-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d416-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d416-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6d416-108">Attributes</span></span>

<span data-ttu-id="6d416-109">无。</span><span class="sxs-lookup"><span data-stu-id="6d416-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d416-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6d416-110">Child elements</span></span>

<span data-ttu-id="6d416-111">无。</span><span class="sxs-lookup"><span data-stu-id="6d416-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d416-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6d416-112">Parent elements</span></span>

|<span data-ttu-id="6d416-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6d416-113">**Element**</span></span>|<span data-ttu-id="6d416-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="6d416-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d416-115">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="6d416-115">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="6d416-116">包含要检索的邮件提示的收件人和类型。</span><span class="sxs-lookup"><span data-stu-id="6d416-116">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d416-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6d416-117">Text value</span></span>

<span data-ttu-id="6d416-118">下表列出了**MailTipsRequested**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="6d416-118">The following table lists the possible values for the **MailTipsRequested** element.</span></span> 
  
|<span data-ttu-id="6d416-119">**值**</span><span class="sxs-lookup"><span data-stu-id="6d416-119">**Value**</span></span>|<span data-ttu-id="6d416-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="6d416-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d416-121">所有</span><span class="sxs-lookup"><span data-stu-id="6d416-121">All</span></span>  <br/> |<span data-ttu-id="6d416-122">表示所有可用的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="6d416-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="6d416-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="6d416-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="6d416-124">代表 "外出" （OOF）邮件。</span><span class="sxs-lookup"><span data-stu-id="6d416-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="6d416-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="6d416-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="6d416-126">表示已满的邮箱的状态。</span><span class="sxs-lookup"><span data-stu-id="6d416-126">Represents the status for a mailbox that is full.</span></span>  <br/> |
|<span data-ttu-id="6d416-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="6d416-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="6d416-128">代表自定义邮件提示。</span><span class="sxs-lookup"><span data-stu-id="6d416-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="6d416-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="6d416-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="6d416-130">表示外部成员的计数。</span><span class="sxs-lookup"><span data-stu-id="6d416-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="6d416-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="6d416-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="6d416-132">表示所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="6d416-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="6d416-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="6d416-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="6d416-134">表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="6d416-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="6d416-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="6d416-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="6d416-136">指示传递限制是否将阻止发件人的邮件到达收件人。</span><span class="sxs-lookup"><span data-stu-id="6d416-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="6d416-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="6d416-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="6d416-138">指示审阅者是否会检查发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="6d416-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="6d416-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="6d416-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="6d416-140">指示收件人是否无效。</span><span class="sxs-lookup"><span data-stu-id="6d416-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d416-141">说明</span><span class="sxs-lookup"><span data-stu-id="6d416-141">Remarks</span></span>

<span data-ttu-id="6d416-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6d416-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d416-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="6d416-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d416-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="6d416-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6d416-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="6d416-145">Schema Name</span></span>  <br/> |<span data-ttu-id="6d416-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="6d416-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6d416-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="6d416-147">Validation File</span></span>  <br/> |<span data-ttu-id="6d416-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6d416-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d416-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="6d416-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d416-150">False</span><span class="sxs-lookup"><span data-stu-id="6d416-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d416-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6d416-151">See also</span></span>



- [<span data-ttu-id="6d416-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6d416-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

