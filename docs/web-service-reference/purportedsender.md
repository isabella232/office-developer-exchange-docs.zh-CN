---
title: PurportedSender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PurportedSender
api_type:
- schema
ms.assetid: eb7a54ec-2e48-4030-bbcf-50a31609691b
description: PurportedSender 元素包含所声称的电子邮件发件人的联系人信息。
ms.openlocfilehash: 5ecf352484a423e3955736620bf5a65c4e98099a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468332"
---
# <a name="purportedsender"></a><span data-ttu-id="42171-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="42171-103">PurportedSender</span></span>

<span data-ttu-id="42171-104">**PurportedSender**元素包含所声称的电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="42171-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="42171-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="42171-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42171-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="42171-106">Attributes and elements</span></span>

<span data-ttu-id="42171-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="42171-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42171-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="42171-108">Attributes</span></span>

<span data-ttu-id="42171-109">无。</span><span class="sxs-lookup"><span data-stu-id="42171-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42171-110">子元素</span><span class="sxs-lookup"><span data-stu-id="42171-110">Child elements</span></span>

|<span data-ttu-id="42171-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="42171-111">**Element**</span></span>|<span data-ttu-id="42171-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="42171-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42171-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="42171-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="42171-114">表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="42171-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="42171-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="42171-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="42171-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="42171-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="42171-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="42171-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="42171-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="42171-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="42171-120">表示收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="42171-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="42171-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="42171-121">The default value is SMTP.</span></span> <span data-ttu-id="42171-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="42171-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="42171-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="42171-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="42171-124">代表电子邮件地址所代表的邮箱类型。。</span><span class="sxs-lookup"><span data-stu-id="42171-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="42171-125">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="42171-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="42171-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="42171-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="42171-p105">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="42171-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42171-129">父元素</span><span class="sxs-lookup"><span data-stu-id="42171-129">Parent elements</span></span>

|<span data-ttu-id="42171-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="42171-130">**Element**</span></span>|<span data-ttu-id="42171-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="42171-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42171-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="42171-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="42171-133">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="42171-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="42171-134">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="42171-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="42171-135">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="42171-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="42171-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="42171-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="42171-137">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="42171-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="42171-138">文本值</span><span class="sxs-lookup"><span data-stu-id="42171-138">Text value</span></span>

<span data-ttu-id="42171-139">无。</span><span class="sxs-lookup"><span data-stu-id="42171-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42171-140">说明</span><span class="sxs-lookup"><span data-stu-id="42171-140">Remarks</span></span>

<span data-ttu-id="42171-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="42171-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42171-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="42171-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42171-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="42171-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42171-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="42171-144">Schema Name</span></span>  <br/> |<span data-ttu-id="42171-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="42171-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42171-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="42171-146">Validation File</span></span>  <br/> |<span data-ttu-id="42171-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="42171-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42171-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="42171-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="42171-149">False</span><span class="sxs-lookup"><span data-stu-id="42171-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42171-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42171-150">See also</span></span>



[<span data-ttu-id="42171-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="42171-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="42171-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="42171-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

