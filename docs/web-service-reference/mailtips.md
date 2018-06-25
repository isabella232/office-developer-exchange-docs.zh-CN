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
description: 邮件提示元素表示的邮件提示的各种类型的值。
ms.openlocfilehash: 3a2e95225b09fd2d81db32f821ea3069ab7e7852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826311"
---
# <a name="mailtips"></a><span data-ttu-id="17295-103">邮件提示</span><span class="sxs-lookup"><span data-stu-id="17295-103">MailTips</span></span>

<span data-ttu-id="17295-104">**邮件提示**元素表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="17295-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
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

 <span data-ttu-id="17295-105">**邮件提示**</span><span class="sxs-lookup"><span data-stu-id="17295-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17295-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="17295-106">Attributes and elements</span></span>

<span data-ttu-id="17295-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="17295-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17295-108">属性</span><span class="sxs-lookup"><span data-stu-id="17295-108">Attributes</span></span>

<span data-ttu-id="17295-109">无。</span><span class="sxs-lookup"><span data-stu-id="17295-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17295-110">子元素</span><span class="sxs-lookup"><span data-stu-id="17295-110">Child elements</span></span>

|<span data-ttu-id="17295-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="17295-111">**Element**</span></span>|<span data-ttu-id="17295-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="17295-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17295-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="17295-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="17295-114">代表收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="17295-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="17295-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="17295-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="17295-116">指示服务器的处理超时之前，可能不评估此元素中的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="17295-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="17295-117">外出</span><span class="sxs-lookup"><span data-stu-id="17295-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="17295-118">代表响应消息和发送响应消息持续时间。</span><span class="sxs-lookup"><span data-stu-id="17295-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="17295-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="17295-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="17295-120">指示是否已满的收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="17295-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="17295-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="17295-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="17295-122">代表自定义的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="17295-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="17295-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="17295-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="17295-124">表示组中的所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="17295-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="17295-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="17295-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="17295-126">表示组中的外部成员计数。</span><span class="sxs-lookup"><span data-stu-id="17295-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="17295-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="17295-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="17295-128">表示收件人可以接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="17295-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="17295-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="17295-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="17295-130">指示传递限制是否将到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="17295-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="17295-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="17295-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="17295-132">指示是否正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="17295-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="17295-133">InvalidRecipient （邮件提示）</span><span class="sxs-lookup"><span data-stu-id="17295-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="17295-134">指示收件人无效。</span><span class="sxs-lookup"><span data-stu-id="17295-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17295-135">父元素</span><span class="sxs-lookup"><span data-stu-id="17295-135">Parent elements</span></span>

|<span data-ttu-id="17295-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="17295-136">**Element**</span></span>|<span data-ttu-id="17295-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="17295-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17295-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="17295-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="17295-139">代表邮件提示设置。</span><span class="sxs-lookup"><span data-stu-id="17295-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="17295-140">文本值</span><span class="sxs-lookup"><span data-stu-id="17295-140">Text value</span></span>

<span data-ttu-id="17295-141">无。</span><span class="sxs-lookup"><span data-stu-id="17295-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17295-142">备注</span><span class="sxs-lookup"><span data-stu-id="17295-142">Remarks</span></span>

<span data-ttu-id="17295-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="17295-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17295-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="17295-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17295-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="17295-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="17295-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="17295-146">Schema Name</span></span>  <br/> |<span data-ttu-id="17295-147">消息架构</span><span class="sxs-lookup"><span data-stu-id="17295-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="17295-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="17295-148">Validation File</span></span>  <br/> |<span data-ttu-id="17295-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="17295-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17295-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="17295-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="17295-151">False</span><span class="sxs-lookup"><span data-stu-id="17295-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17295-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="17295-152">See also</span></span>



- [<span data-ttu-id="17295-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="17295-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

