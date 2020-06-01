---
title: 邮件提示
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: 邮件提示元素表示各种邮件提示类型的值。
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447594"
---
# <a name="mailtips"></a><span data-ttu-id="2377d-103">邮件提示</span><span class="sxs-lookup"><span data-stu-id="2377d-103">MailTips</span></span>

<span data-ttu-id="2377d-104">邮件**提示元素表示**各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="2377d-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 <span data-ttu-id="2377d-105">**邮件提示**</span><span class="sxs-lookup"><span data-stu-id="2377d-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2377d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2377d-106">Attributes and elements</span></span>

<span data-ttu-id="2377d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2377d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2377d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2377d-108">Attributes</span></span>

<span data-ttu-id="2377d-109">无。</span><span class="sxs-lookup"><span data-stu-id="2377d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2377d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2377d-110">Child elements</span></span>

|<span data-ttu-id="2377d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2377d-111">**Element**</span></span>|<span data-ttu-id="2377d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2377d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2377d-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="2377d-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="2377d-114">表示收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="2377d-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="2377d-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="2377d-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="2377d-116">指示在服务器的处理超时过期之前无法评估此元素中的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="2377d-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="2377d-117">外出</span><span class="sxs-lookup"><span data-stu-id="2377d-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="2377d-118">表示响应消息和发送响应消息的持续时间。</span><span class="sxs-lookup"><span data-stu-id="2377d-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="2377d-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="2377d-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="2377d-120">指示收件人的邮箱是否已满。</span><span class="sxs-lookup"><span data-stu-id="2377d-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="2377d-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="2377d-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="2377d-122">代表自定义的邮件提示邮件。</span><span class="sxs-lookup"><span data-stu-id="2377d-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="2377d-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="2377d-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="2377d-124">表示组中所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="2377d-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="2377d-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="2377d-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="2377d-126">表示组中的外部成员的计数。</span><span class="sxs-lookup"><span data-stu-id="2377d-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="2377d-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="2377d-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="2377d-128">表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="2377d-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="2377d-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="2377d-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="2377d-130">指示传递限制是否将阻止发件人的邮件到达收件人。</span><span class="sxs-lookup"><span data-stu-id="2377d-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="2377d-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="2377d-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="2377d-132">指示是否正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="2377d-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="2377d-133">InvalidRecipient （邮件提示）</span><span class="sxs-lookup"><span data-stu-id="2377d-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="2377d-134">指示收件人是否无效。</span><span class="sxs-lookup"><span data-stu-id="2377d-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2377d-135">父元素</span><span class="sxs-lookup"><span data-stu-id="2377d-135">Parent elements</span></span>

|<span data-ttu-id="2377d-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="2377d-136">**Element**</span></span>|<span data-ttu-id="2377d-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="2377d-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2377d-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="2377d-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="2377d-139">代表 "邮件提示设置"。</span><span class="sxs-lookup"><span data-stu-id="2377d-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2377d-140">文本值</span><span class="sxs-lookup"><span data-stu-id="2377d-140">Text value</span></span>

<span data-ttu-id="2377d-141">无。</span><span class="sxs-lookup"><span data-stu-id="2377d-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2377d-142">说明</span><span class="sxs-lookup"><span data-stu-id="2377d-142">Remarks</span></span>

<span data-ttu-id="2377d-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2377d-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2377d-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="2377d-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2377d-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="2377d-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2377d-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="2377d-146">Schema Name</span></span>  <br/> |<span data-ttu-id="2377d-147">消息架构</span><span class="sxs-lookup"><span data-stu-id="2377d-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2377d-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="2377d-148">Validation File</span></span>  <br/> |<span data-ttu-id="2377d-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2377d-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2377d-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="2377d-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="2377d-151">False</span><span class="sxs-lookup"><span data-stu-id="2377d-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2377d-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2377d-152">See also</span></span>



- [<span data-ttu-id="2377d-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2377d-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

