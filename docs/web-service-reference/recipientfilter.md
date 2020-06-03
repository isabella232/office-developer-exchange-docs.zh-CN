---
title: RecipientFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientFilter
api_type:
- schema
ms.assetid: 956c287a-a38a-49a7-a877-6d2088dfbc06
description: RecipientFilter 元素表示要用于指定邮件跟踪报告的收件人地址。
ms.openlocfilehash: 945adf9155434e0690debfccc7caf70ba0cb94ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465805"
---
# <a name="recipientfilter"></a><span data-ttu-id="62afd-103">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="62afd-103">RecipientFilter</span></span>

<span data-ttu-id="62afd-104">**RecipientFilter**元素表示要用于指定邮件跟踪报告的收件人地址。</span><span class="sxs-lookup"><span data-stu-id="62afd-104">The **RecipientFilter** element represents a recipient address to use with the specified message tracking report.</span></span> 
  
```XML
 <RecipientFilter>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientFilter>
```

 <span data-ttu-id="62afd-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="62afd-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62afd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="62afd-106">Attributes and elements</span></span>

<span data-ttu-id="62afd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="62afd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62afd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="62afd-108">Attributes</span></span>

<span data-ttu-id="62afd-109">无。</span><span class="sxs-lookup"><span data-stu-id="62afd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62afd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="62afd-110">Child elements</span></span>

|<span data-ttu-id="62afd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="62afd-111">**Element**</span></span>|<span data-ttu-id="62afd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="62afd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62afd-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="62afd-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="62afd-114">表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="62afd-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="62afd-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="62afd-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="62afd-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="62afd-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="62afd-117">定义邮箱用户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="62afd-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="62afd-118">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="62afd-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="62afd-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="62afd-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="62afd-120">表示此收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="62afd-120">Represents the routing protocol for this recipient.</span></span> <span data-ttu-id="62afd-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="62afd-121">The default value is SMTP.</span></span> <span data-ttu-id="62afd-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="62afd-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="62afd-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="62afd-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="62afd-124">代表电子邮件地址所代表的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="62afd-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="62afd-125">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="62afd-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="62afd-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="62afd-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="62afd-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="62afd-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62afd-129">父元素</span><span class="sxs-lookup"><span data-stu-id="62afd-129">Parent elements</span></span>

|<span data-ttu-id="62afd-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="62afd-130">**Element**</span></span>|<span data-ttu-id="62afd-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="62afd-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62afd-132">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="62afd-132">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="62afd-133">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="62afd-133">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62afd-134">文本值</span><span class="sxs-lookup"><span data-stu-id="62afd-134">Text value</span></span>

<span data-ttu-id="62afd-135">无。</span><span class="sxs-lookup"><span data-stu-id="62afd-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62afd-136">说明</span><span class="sxs-lookup"><span data-stu-id="62afd-136">Remarks</span></span>

<span data-ttu-id="62afd-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="62afd-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62afd-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="62afd-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62afd-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="62afd-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="62afd-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="62afd-140">Schema Name</span></span>  <br/> |<span data-ttu-id="62afd-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="62afd-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="62afd-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="62afd-142">Validation File</span></span>  <br/> |<span data-ttu-id="62afd-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="62afd-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="62afd-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="62afd-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="62afd-145">False</span><span class="sxs-lookup"><span data-stu-id="62afd-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62afd-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62afd-146">See also</span></span>



[<span data-ttu-id="62afd-147">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="62afd-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="62afd-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="62afd-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

