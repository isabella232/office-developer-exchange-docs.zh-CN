---
title: 收件人
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
description: 收件人元素表示发生事件的收件人。
ms.openlocfilehash: eb7e85acf3c2b898b3f0bff4b63168d344e1daa8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465854"
---
# <a name="recipient"></a><span data-ttu-id="411ef-103">收件人</span><span class="sxs-lookup"><span data-stu-id="411ef-103">Recipient</span></span>

<span data-ttu-id="411ef-104">**收件人**元素表示发生事件的收件人。</span><span class="sxs-lookup"><span data-stu-id="411ef-104">The **Recipient** element represents the recipient for whom the event occurred.</span></span> 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 <span data-ttu-id="411ef-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="411ef-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="411ef-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="411ef-106">Attributes and elements</span></span>

<span data-ttu-id="411ef-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="411ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="411ef-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="411ef-108">Attributes</span></span>

<span data-ttu-id="411ef-109">无。</span><span class="sxs-lookup"><span data-stu-id="411ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="411ef-110">子元素</span><span class="sxs-lookup"><span data-stu-id="411ef-110">Child elements</span></span>

|<span data-ttu-id="411ef-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="411ef-111">**Element**</span></span>|<span data-ttu-id="411ef-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="411ef-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="411ef-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="411ef-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="411ef-114">表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="411ef-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="411ef-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="411ef-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="411ef-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="411ef-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="411ef-117">定义邮箱用户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="411ef-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="411ef-118">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="411ef-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="411ef-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="411ef-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="411ef-120">定义供邮箱使用的路由。</span><span class="sxs-lookup"><span data-stu-id="411ef-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="411ef-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="411ef-121">The default value is SMTP.</span></span> <span data-ttu-id="411ef-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="411ef-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="411ef-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="411ef-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="411ef-124">代表电子邮件地址所代表的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="411ef-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="411ef-125">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="411ef-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="411ef-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="411ef-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="411ef-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="411ef-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="411ef-129">父元素</span><span class="sxs-lookup"><span data-stu-id="411ef-129">Parent elements</span></span>

|<span data-ttu-id="411ef-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="411ef-130">**Element**</span></span>|<span data-ttu-id="411ef-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="411ef-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="411ef-132">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="411ef-132">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="411ef-133">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="411ef-133">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="411ef-134">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="411ef-134">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="411ef-135">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="411ef-135">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="411ef-136">文本值</span><span class="sxs-lookup"><span data-stu-id="411ef-136">Text value</span></span>

<span data-ttu-id="411ef-137">无。</span><span class="sxs-lookup"><span data-stu-id="411ef-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="411ef-138">说明</span><span class="sxs-lookup"><span data-stu-id="411ef-138">Remarks</span></span>

<span data-ttu-id="411ef-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="411ef-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="411ef-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="411ef-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="411ef-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="411ef-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="411ef-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="411ef-142">Schema Name</span></span>  <br/> |<span data-ttu-id="411ef-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="411ef-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="411ef-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="411ef-144">Validation File</span></span>  <br/> |<span data-ttu-id="411ef-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="411ef-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="411ef-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="411ef-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="411ef-147">False</span><span class="sxs-lookup"><span data-stu-id="411ef-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="411ef-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="411ef-148">See also</span></span>



- [<span data-ttu-id="411ef-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="411ef-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

