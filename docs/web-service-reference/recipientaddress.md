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
description: RecipientAddress 元素均表示收件人的邮箱。
ms.openlocfilehash: 10928ac206227cfc21bd83ab5bfa9a55aad354e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826974"
---
# <a name="recipientaddress"></a><span data-ttu-id="b2066-103">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="b2066-103">RecipientAddress</span></span>

<span data-ttu-id="b2066-104">**RecipientAddress**元素均表示收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="b2066-104">The **RecipientAddress** element represents the mailbox of the recipient.</span></span> 
  
```xml
<RecipientAddress>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientAddress>
```

 <span data-ttu-id="b2066-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="b2066-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2066-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b2066-106">Attributes and elements</span></span>

<span data-ttu-id="b2066-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b2066-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2066-108">属性</span><span class="sxs-lookup"><span data-stu-id="b2066-108">Attributes</span></span>

<span data-ttu-id="b2066-109">无。</span><span class="sxs-lookup"><span data-stu-id="b2066-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2066-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b2066-110">Child elements</span></span>

|<span data-ttu-id="b2066-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2066-111">**Element**</span></span>|<span data-ttu-id="b2066-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2066-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2066-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="b2066-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="b2066-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="b2066-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="b2066-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2066-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b2066-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b2066-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="b2066-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2066-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b2066-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="b2066-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="b2066-120">代表收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="b2066-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="b2066-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="b2066-121">The default is SMTP.</span></span> <span data-ttu-id="b2066-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2066-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b2066-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="b2066-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="b2066-124">表示由的电子邮件地址的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="b2066-124">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="b2066-125">ItemId</span><span class="sxs-lookup"><span data-stu-id="b2066-125">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b2066-p104">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="b2066-p104">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2066-128">父元素</span><span class="sxs-lookup"><span data-stu-id="b2066-128">Parent elements</span></span>

|<span data-ttu-id="b2066-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2066-129">**Element**</span></span>|<span data-ttu-id="b2066-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2066-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2066-131">邮件提示</span><span class="sxs-lookup"><span data-stu-id="b2066-131">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="b2066-132">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="b2066-132">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2066-133">备注</span><span class="sxs-lookup"><span data-stu-id="b2066-133">Remarks</span></span>

<span data-ttu-id="b2066-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b2066-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2066-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="b2066-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2066-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="b2066-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b2066-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="b2066-137">Schema Name</span></span>  <br/> |<span data-ttu-id="b2066-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="b2066-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="b2066-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="b2066-139">Validation File</span></span>  <br/> |<span data-ttu-id="b2066-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b2066-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b2066-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="b2066-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="b2066-142">False</span><span class="sxs-lookup"><span data-stu-id="b2066-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2066-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2066-143">See also</span></span>



- [<span data-ttu-id="b2066-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b2066-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

