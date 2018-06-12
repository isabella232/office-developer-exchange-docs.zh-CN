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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826311"
---
# <a name="mailtips"></a><span data-ttu-id="8c9c1-103">邮件提示</span><span class="sxs-lookup"><span data-stu-id="8c9c1-103">MailTips</span></span>

<span data-ttu-id="8c9c1-104">**邮件提示**元素表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
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

 <span data-ttu-id="8c9c1-105">**邮件提示**</span><span class="sxs-lookup"><span data-stu-id="8c9c1-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8c9c1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8c9c1-106">Attributes and elements</span></span>

<span data-ttu-id="8c9c1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c9c1-108">属性</span><span class="sxs-lookup"><span data-stu-id="8c9c1-108">Attributes</span></span>

<span data-ttu-id="8c9c1-109">无。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c9c1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8c9c1-110">Child elements</span></span>

|<span data-ttu-id="8c9c1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8c9c1-111">**Element**</span></span>|<span data-ttu-id="8c9c1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c9c1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c1-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="8c9c1-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="8c9c1-114">代表收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="8c9c1-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="8c9c1-116">指示服务器的处理超时之前，可能不评估此元素中的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-117">外出</span><span class="sxs-lookup"><span data-stu-id="8c9c1-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="8c9c1-118">代表响应消息和发送响应消息持续时间。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="8c9c1-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="8c9c1-120">指示是否已满的收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="8c9c1-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="8c9c1-122">代表自定义的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="8c9c1-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="8c9c1-124">表示组中的所有成员的计数。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="8c9c1-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="8c9c1-126">表示组中的外部成员计数。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="8c9c1-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="8c9c1-128">表示收件人可以接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="8c9c1-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="8c9c1-130">指示传递限制是否将到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="8c9c1-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="8c9c1-132">指示是否正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="8c9c1-133">InvalidRecipient （邮件提示）</span><span class="sxs-lookup"><span data-stu-id="8c9c1-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="8c9c1-134">指示收件人无效。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c9c1-135">父元素</span><span class="sxs-lookup"><span data-stu-id="8c9c1-135">Parent elements</span></span>

|<span data-ttu-id="8c9c1-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="8c9c1-136">**Element**</span></span>|<span data-ttu-id="8c9c1-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c9c1-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c1-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="8c9c1-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="8c9c1-139">代表邮件提示设置。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8c9c1-140">文本值</span><span class="sxs-lookup"><span data-stu-id="8c9c1-140">Text value</span></span>

<span data-ttu-id="8c9c1-141">无。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c9c1-142">备注</span><span class="sxs-lookup"><span data-stu-id="8c9c1-142">Remarks</span></span>

<span data-ttu-id="8c9c1-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8c9c1-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c9c1-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="8c9c1-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c9c1-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="8c9c1-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8c9c1-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="8c9c1-146">Schema Name</span></span>  <br/> |<span data-ttu-id="8c9c1-147">消息架构</span><span class="sxs-lookup"><span data-stu-id="8c9c1-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8c9c1-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="8c9c1-148">Validation File</span></span>  <br/> |<span data-ttu-id="8c9c1-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8c9c1-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8c9c1-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="8c9c1-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="8c9c1-151">False</span><span class="sxs-lookup"><span data-stu-id="8c9c1-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c9c1-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c9c1-152">See also</span></span>



- [<span data-ttu-id="8c9c1-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8c9c1-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

