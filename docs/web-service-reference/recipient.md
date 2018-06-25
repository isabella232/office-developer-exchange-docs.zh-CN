---
title: Recipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipient
api_type:
- schema
ms.assetid: 52adbb30-3bfd-48aa-9ea8-9f7d3b4bee44
description: 收件人元素均表示的收件人其发生此事件。
ms.openlocfilehash: e8e8f9d6031d27c7441017c85eb26a143258b183
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826971"
---
# <a name="recipient"></a><span data-ttu-id="568ce-103">Recipient</span><span class="sxs-lookup"><span data-stu-id="568ce-103">Recipient</span></span>

<span data-ttu-id="568ce-104">**收件人**元素均表示的收件人其发生此事件。</span><span class="sxs-lookup"><span data-stu-id="568ce-104">The **Recipient** element represents the recipient for whom the event occurred.</span></span> 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 <span data-ttu-id="568ce-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="568ce-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="568ce-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="568ce-106">Attributes and elements</span></span>

<span data-ttu-id="568ce-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="568ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="568ce-108">属性</span><span class="sxs-lookup"><span data-stu-id="568ce-108">Attributes</span></span>

<span data-ttu-id="568ce-109">无。</span><span class="sxs-lookup"><span data-stu-id="568ce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="568ce-110">子元素</span><span class="sxs-lookup"><span data-stu-id="568ce-110">Child elements</span></span>

|<span data-ttu-id="568ce-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="568ce-111">**Element**</span></span>|<span data-ttu-id="568ce-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="568ce-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="568ce-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="568ce-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="568ce-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="568ce-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="568ce-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="568ce-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="568ce-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="568ce-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="568ce-117">定义邮箱用户的主要简单邮件传输协议 (SMTP) 的地址。</span><span class="sxs-lookup"><span data-stu-id="568ce-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="568ce-118">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="568ce-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="568ce-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="568ce-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="568ce-120">定义用于邮箱路由。</span><span class="sxs-lookup"><span data-stu-id="568ce-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="568ce-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="568ce-121">The default value is SMTP.</span></span> <span data-ttu-id="568ce-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="568ce-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="568ce-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="568ce-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="568ce-124">表示由的电子邮件地址的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="568ce-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="568ce-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="568ce-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="568ce-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="568ce-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="568ce-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="568ce-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="568ce-129">父元素</span><span class="sxs-lookup"><span data-stu-id="568ce-129">Parent elements</span></span>

|<span data-ttu-id="568ce-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="568ce-130">**Element**</span></span>|<span data-ttu-id="568ce-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="568ce-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="568ce-132">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="568ce-132">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="568ce-133">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="568ce-133">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="568ce-134">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="568ce-134">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="568ce-135">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="568ce-135">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="568ce-136">文本值</span><span class="sxs-lookup"><span data-stu-id="568ce-136">Text value</span></span>

<span data-ttu-id="568ce-137">无。</span><span class="sxs-lookup"><span data-stu-id="568ce-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="568ce-138">备注</span><span class="sxs-lookup"><span data-stu-id="568ce-138">Remarks</span></span>

<span data-ttu-id="568ce-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="568ce-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="568ce-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="568ce-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="568ce-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="568ce-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="568ce-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="568ce-142">Schema Name</span></span>  <br/> |<span data-ttu-id="568ce-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="568ce-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="568ce-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="568ce-144">Validation File</span></span>  <br/> |<span data-ttu-id="568ce-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="568ce-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="568ce-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="568ce-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="568ce-147">False</span><span class="sxs-lookup"><span data-stu-id="568ce-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="568ce-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="568ce-148">See also</span></span>



- [<span data-ttu-id="568ce-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="568ce-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

