---
title: SendingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendingAs
api_type:
- schema
ms.assetid: b43ce19f-9ab0-4946-acb2-c5aafead9d35
description: SendingAs 元素均表示用户要为发送电子邮件地址。
ms.openlocfilehash: a5468ddb8facf99038d319252f7e1c780a888ca1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827338"
---
# <a name="sendingas"></a><span data-ttu-id="8af69-103">SendingAs</span><span class="sxs-lookup"><span data-stu-id="8af69-103">SendingAs</span></span>

<span data-ttu-id="8af69-104">**SendingAs**元素均表示用户要为发送电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8af69-104">The **SendingAs** element represents an e-mail address that a user is trying to send as.</span></span> 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 <span data-ttu-id="8af69-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="8af69-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8af69-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8af69-106">Attributes and elements</span></span>

<span data-ttu-id="8af69-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8af69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8af69-108">属性</span><span class="sxs-lookup"><span data-stu-id="8af69-108">Attributes</span></span>

<span data-ttu-id="8af69-109">无。</span><span class="sxs-lookup"><span data-stu-id="8af69-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8af69-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8af69-110">Child elements</span></span>

|<span data-ttu-id="8af69-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8af69-111">**Element**</span></span>|<span data-ttu-id="8af69-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8af69-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8af69-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8af69-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="8af69-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="8af69-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="8af69-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8af69-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8af69-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="8af69-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="8af69-117">定义邮箱用户的主要简单邮件传输协议 (SMTP) 的地址。</span><span class="sxs-lookup"><span data-stu-id="8af69-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="8af69-118">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8af69-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8af69-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="8af69-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="8af69-120">定义邮箱的地址类型。</span><span class="sxs-lookup"><span data-stu-id="8af69-120">Defines the address type for the mailbox.</span></span> <span data-ttu-id="8af69-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="8af69-121">The default is SMTP.</span></span> <span data-ttu-id="8af69-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8af69-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8af69-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="8af69-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="8af69-124">表示由电子邮件用户的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="8af69-124">Represents the type of mailbox that is represented by an e-mail user.</span></span> <span data-ttu-id="8af69-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8af69-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8af69-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="8af69-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="8af69-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8af69-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8af69-129">父元素</span><span class="sxs-lookup"><span data-stu-id="8af69-129">Parent elements</span></span>

|<span data-ttu-id="8af69-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="8af69-130">**Element**</span></span>|<span data-ttu-id="8af69-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="8af69-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8af69-132">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="8af69-132">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="8af69-133">包含要检索的收件人和类型的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="8af69-133">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8af69-134">文本值</span><span class="sxs-lookup"><span data-stu-id="8af69-134">Text value</span></span>

<span data-ttu-id="8af69-135">无。</span><span class="sxs-lookup"><span data-stu-id="8af69-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8af69-136">备注</span><span class="sxs-lookup"><span data-stu-id="8af69-136">Remarks</span></span>

<span data-ttu-id="8af69-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8af69-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8af69-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="8af69-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8af69-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="8af69-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8af69-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="8af69-140">Schema Name</span></span>  <br/> |<span data-ttu-id="8af69-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="8af69-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8af69-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="8af69-142">Validation File</span></span>  <br/> |<span data-ttu-id="8af69-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8af69-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8af69-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="8af69-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="8af69-145">False</span><span class="sxs-lookup"><span data-stu-id="8af69-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8af69-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8af69-146">See also</span></span>



- [<span data-ttu-id="8af69-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8af69-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

