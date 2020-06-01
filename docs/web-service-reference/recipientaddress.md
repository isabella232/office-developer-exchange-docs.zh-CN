---
title: RecipientAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientAddress
api_type:
- schema
ms.assetid: 9ae6351a-2c60-4715-a489-5681a13641f9
description: RecipientAddress 元素表示收件人的邮箱。
ms.openlocfilehash: f4b6edd034dd91471e6496f6b0cca65bd3ffb69a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465847"
---
# <a name="recipientaddress"></a><span data-ttu-id="1e29f-103">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="1e29f-103">RecipientAddress</span></span>

<span data-ttu-id="1e29f-104">**RecipientAddress**元素表示收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="1e29f-104">The **RecipientAddress** element represents the mailbox of the recipient.</span></span> 
  
```xml
<RecipientAddress>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientAddress>
```

 <span data-ttu-id="1e29f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="1e29f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e29f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e29f-106">Attributes and elements</span></span>

<span data-ttu-id="1e29f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e29f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e29f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1e29f-108">Attributes</span></span>

<span data-ttu-id="1e29f-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e29f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e29f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e29f-110">Child elements</span></span>

|<span data-ttu-id="1e29f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e29f-111">**Element**</span></span>|<span data-ttu-id="1e29f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e29f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e29f-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1e29f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="1e29f-114">表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="1e29f-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="1e29f-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="1e29f-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1e29f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="1e29f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="1e29f-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1e29f-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1e29f-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="1e29f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="1e29f-120">表示收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="1e29f-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="1e29f-121">默认为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="1e29f-121">The default is SMTP.</span></span> <span data-ttu-id="1e29f-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="1e29f-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1e29f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="1e29f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="1e29f-124">代表电子邮件地址所代表的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="1e29f-124">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="1e29f-125">ItemId</span><span class="sxs-lookup"><span data-stu-id="1e29f-125">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1e29f-p104">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="1e29f-p104">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1e29f-128">父元素</span><span class="sxs-lookup"><span data-stu-id="1e29f-128">Parent elements</span></span>

|<span data-ttu-id="1e29f-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e29f-129">**Element**</span></span>|<span data-ttu-id="1e29f-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e29f-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e29f-131">邮件提示</span><span class="sxs-lookup"><span data-stu-id="1e29f-131">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="1e29f-132">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="1e29f-132">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e29f-133">说明</span><span class="sxs-lookup"><span data-stu-id="1e29f-133">Remarks</span></span>

<span data-ttu-id="1e29f-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e29f-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e29f-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e29f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e29f-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e29f-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e29f-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e29f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="1e29f-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="1e29f-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e29f-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e29f-139">Validation File</span></span>  <br/> |<span data-ttu-id="1e29f-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e29f-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e29f-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e29f-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e29f-142">False</span><span class="sxs-lookup"><span data-stu-id="1e29f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e29f-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e29f-143">See also</span></span>



- [<span data-ttu-id="1e29f-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e29f-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

