---
title: 发件人（EmailAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 717eb6d0-d167-4b20-92e2-5d08b96186c4
description: Sender 元素表示邮件发件人的电子邮件地址。
ms.openlocfilehash: 23a487f216a110796d40f3d3e86224c691acc004
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455322"
---
# <a name="sender-emailaddresstype"></a><span data-ttu-id="67532-103">发件人（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="67532-103">Sender (EmailAddressType)</span></span>

<span data-ttu-id="67532-104">**Sender**元素表示邮件发件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="67532-104">The **Sender** element represents the e-mail address for the sender of the message.</span></span> 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 <span data-ttu-id="67532-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="67532-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67532-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67532-106">Attributes and elements</span></span>

<span data-ttu-id="67532-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67532-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67532-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="67532-108">Attributes</span></span>

<span data-ttu-id="67532-109">无。</span><span class="sxs-lookup"><span data-stu-id="67532-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67532-110">子元素</span><span class="sxs-lookup"><span data-stu-id="67532-110">Child elements</span></span>

|<span data-ttu-id="67532-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="67532-111">**Element**</span></span>|<span data-ttu-id="67532-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="67532-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67532-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="67532-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="67532-114">表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="67532-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="67532-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="67532-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="67532-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="67532-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="67532-117">定义邮箱用户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="67532-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="67532-118">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="67532-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="67532-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="67532-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="67532-120">表示收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="67532-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="67532-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="67532-121">The default value is SMTP.</span></span> <span data-ttu-id="67532-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="67532-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="67532-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="67532-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="67532-124">代表电子邮件地址所代表的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="67532-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="67532-125">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="67532-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="67532-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="67532-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="67532-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="67532-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67532-129">父元素</span><span class="sxs-lookup"><span data-stu-id="67532-129">Parent elements</span></span>

|<span data-ttu-id="67532-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="67532-130">**Element**</span></span>|<span data-ttu-id="67532-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="67532-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67532-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="67532-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="67532-133">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="67532-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="67532-134">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="67532-134">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="67532-135">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="67532-135">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="67532-136">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="67532-136">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="67532-137">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="67532-137">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67532-138">文本值</span><span class="sxs-lookup"><span data-stu-id="67532-138">Text value</span></span>

<span data-ttu-id="67532-139">无。</span><span class="sxs-lookup"><span data-stu-id="67532-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67532-140">说明</span><span class="sxs-lookup"><span data-stu-id="67532-140">Remarks</span></span>

<span data-ttu-id="67532-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67532-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67532-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="67532-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67532-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="67532-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67532-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="67532-144">Schema Name</span></span>  <br/> |<span data-ttu-id="67532-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="67532-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="67532-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="67532-146">Validation File</span></span>  <br/> |<span data-ttu-id="67532-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67532-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67532-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="67532-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="67532-149">False</span><span class="sxs-lookup"><span data-stu-id="67532-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67532-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67532-150">See also</span></span>



[<span data-ttu-id="67532-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="67532-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="67532-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67532-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

