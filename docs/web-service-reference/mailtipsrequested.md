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
description: MailTipsRequested 元素包含的邮件提示从的服务请求的类型。
ms.openlocfilehash: fa2bef394ea8473aa65bdc2f1d39c0794186fdc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826348"
---
# <a name="mailtipsrequested"></a><span data-ttu-id="e0b0d-103">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="e0b0d-103">MailTipsRequested</span></span>

<span data-ttu-id="e0b0d-104">**MailTipsRequested**元素包含的邮件提示从的服务请求的类型。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-104">The **MailTipsRequested** element contains the types of mail tips requested from the service.</span></span> 
  
```XML
<MailTipsRequested/>
```

 <span data-ttu-id="e0b0d-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="e0b0d-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0b0d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e0b0d-106">Attributes and elements</span></span>

<span data-ttu-id="e0b0d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0b0d-108">属性</span><span class="sxs-lookup"><span data-stu-id="e0b0d-108">Attributes</span></span>

<span data-ttu-id="e0b0d-109">无。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0b0d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e0b0d-110">Child elements</span></span>

<span data-ttu-id="e0b0d-111">无。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0b0d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e0b0d-112">Parent elements</span></span>

|<span data-ttu-id="e0b0d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0b0d-113">**Element**</span></span>|<span data-ttu-id="e0b0d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0b0d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0b0d-115">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="e0b0d-115">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="e0b0d-116">包含要检索的收件人和类型的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-116">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0b0d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e0b0d-117">Text value</span></span>

<span data-ttu-id="e0b0d-118">下表列出了**MailTipsRequested**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-118">The following table lists the possible values for the **MailTipsRequested** element.</span></span> 
  
|<span data-ttu-id="e0b0d-119">**值**</span><span class="sxs-lookup"><span data-stu-id="e0b0d-119">**Value**</span></span>|<span data-ttu-id="e0b0d-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0b0d-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b0d-121">所有</span><span class="sxs-lookup"><span data-stu-id="e0b0d-121">All</span></span>  <br/> |<span data-ttu-id="e0b0d-122">代表所有可用的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="e0b0d-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="e0b0d-124">代表外出 (OOF) 邮件。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="e0b0d-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="e0b0d-126">表示邮箱已满的状态。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-126">Represents the status for a mailbox that is full.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="e0b0d-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="e0b0d-128">代表自定义邮件提示。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="e0b0d-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="e0b0d-130">表示外部成员计数。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="e0b0d-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="e0b0d-132">表示所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="e0b0d-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="e0b0d-134">表示收件人可以接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="e0b0d-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="e0b0d-136">指示传递限制是否将到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="e0b0d-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="e0b0d-138">指示是否将由审阅者审查发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="e0b0d-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="e0b0d-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="e0b0d-140">指示收件人无效。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0b0d-141">备注</span><span class="sxs-lookup"><span data-stu-id="e0b0d-141">Remarks</span></span>

<span data-ttu-id="e0b0d-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e0b0d-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0b0d-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="e0b0d-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0b0d-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="e0b0d-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0b0d-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="e0b0d-145">Schema Name</span></span>  <br/> |<span data-ttu-id="e0b0d-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="e0b0d-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0b0d-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="e0b0d-147">Validation File</span></span>  <br/> |<span data-ttu-id="e0b0d-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0b0d-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0b0d-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="e0b0d-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0b0d-150">False</span><span class="sxs-lookup"><span data-stu-id="e0b0d-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0b0d-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0b0d-151">See also</span></span>



- [<span data-ttu-id="e0b0d-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e0b0d-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

