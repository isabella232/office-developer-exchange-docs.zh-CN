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
description: RecipientFilter 元素均表示要使用指定的邮件跟踪报告的收件人地址。
ms.openlocfilehash: c31ed469132b110a690416b112d5e4e96e44c501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826972"
---
# <a name="recipientfilter"></a><span data-ttu-id="b501f-103">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="b501f-103">RecipientFilter</span></span>

<span data-ttu-id="b501f-104">**RecipientFilter**元素均表示要使用指定的邮件跟踪报告的收件人地址。</span><span class="sxs-lookup"><span data-stu-id="b501f-104">The **RecipientFilter** element represents a recipient address to use with the specified message tracking report.</span></span> 
  
```XML
 <RecipientFilter>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientFilter>
```

 <span data-ttu-id="b501f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="b501f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b501f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b501f-106">Attributes and elements</span></span>

<span data-ttu-id="b501f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b501f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b501f-108">属性</span><span class="sxs-lookup"><span data-stu-id="b501f-108">Attributes</span></span>

<span data-ttu-id="b501f-109">无。</span><span class="sxs-lookup"><span data-stu-id="b501f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b501f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b501f-110">Child elements</span></span>

|<span data-ttu-id="b501f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b501f-111">**Element**</span></span>|<span data-ttu-id="b501f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b501f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b501f-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="b501f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="b501f-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="b501f-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="b501f-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b501f-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b501f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b501f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="b501f-117">定义邮箱用户的主要简单邮件传输协议 (SMTP) 的地址。</span><span class="sxs-lookup"><span data-stu-id="b501f-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="b501f-118">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b501f-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b501f-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="b501f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="b501f-120">表示此收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="b501f-120">Represents the routing protocol for this recipient.</span></span> <span data-ttu-id="b501f-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="b501f-121">The default value is SMTP.</span></span> <span data-ttu-id="b501f-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b501f-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b501f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="b501f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="b501f-124">表示由的电子邮件地址的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="b501f-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="b501f-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b501f-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b501f-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="b501f-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b501f-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b501f-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b501f-129">父元素</span><span class="sxs-lookup"><span data-stu-id="b501f-129">Parent elements</span></span>

|<span data-ttu-id="b501f-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="b501f-130">**Element**</span></span>|<span data-ttu-id="b501f-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="b501f-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b501f-132">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b501f-132">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="b501f-133">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="b501f-133">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b501f-134">文本值</span><span class="sxs-lookup"><span data-stu-id="b501f-134">Text value</span></span>

<span data-ttu-id="b501f-135">无。</span><span class="sxs-lookup"><span data-stu-id="b501f-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b501f-136">备注</span><span class="sxs-lookup"><span data-stu-id="b501f-136">Remarks</span></span>

<span data-ttu-id="b501f-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b501f-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b501f-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="b501f-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b501f-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="b501f-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b501f-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="b501f-140">Schema Name</span></span>  <br/> |<span data-ttu-id="b501f-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="b501f-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b501f-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="b501f-142">Validation File</span></span>  <br/> |<span data-ttu-id="b501f-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b501f-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b501f-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="b501f-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="b501f-145">False</span><span class="sxs-lookup"><span data-stu-id="b501f-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b501f-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b501f-146">See also</span></span>



[<span data-ttu-id="b501f-147">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="b501f-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="b501f-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b501f-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

