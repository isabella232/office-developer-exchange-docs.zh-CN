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
description: PurportedSender 元素包含声称的发件人的电子邮件的联系人信息。
ms.openlocfilehash: 1e5b74d60d824c06834cf988557ef64fb84d70c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826937"
---
# <a name="purportedsender"></a><span data-ttu-id="d9d6c-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="d9d6c-103">PurportedSender</span></span>

<span data-ttu-id="d9d6c-104">**PurportedSender**元素包含声称的发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="d9d6c-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="d9d6c-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9d6c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9d6c-106">Attributes and elements</span></span>

<span data-ttu-id="d9d6c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9d6c-108">属性</span><span class="sxs-lookup"><span data-stu-id="d9d6c-108">Attributes</span></span>

<span data-ttu-id="d9d6c-109">无。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9d6c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d9d6c-110">Child elements</span></span>

|<span data-ttu-id="d9d6c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9d6c-111">**Element**</span></span>|<span data-ttu-id="d9d6c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9d6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9d6c-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d9d6c-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="d9d6c-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="d9d6c-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d9d6c-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="d9d6c-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="d9d6c-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="d9d6c-120">代表收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="d9d6c-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-121">The default value is SMTP.</span></span> <span data-ttu-id="d9d6c-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="d9d6c-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="d9d6c-124">代表由的电子邮件地址的邮箱的类型。.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="d9d6c-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="d9d6c-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d9d6c-p105">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9d6c-129">父元素</span><span class="sxs-lookup"><span data-stu-id="d9d6c-129">Parent elements</span></span>

|<span data-ttu-id="d9d6c-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9d6c-130">**Element**</span></span>|<span data-ttu-id="d9d6c-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9d6c-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9d6c-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d9d6c-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="d9d6c-133">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-134">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d9d6c-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="d9d6c-135">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d9d6c-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="d9d6c-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="d9d6c-137">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9d6c-138">文本值</span><span class="sxs-lookup"><span data-stu-id="d9d6c-138">Text value</span></span>

<span data-ttu-id="d9d6c-139">无。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9d6c-140">备注</span><span class="sxs-lookup"><span data-stu-id="d9d6c-140">Remarks</span></span>

<span data-ttu-id="d9d6c-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d9d6c-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9d6c-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9d6c-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9d6c-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9d6c-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9d6c-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9d6c-144">Schema Name</span></span>  <br/> |<span data-ttu-id="d9d6c-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="d9d6c-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9d6c-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9d6c-146">Validation File</span></span>  <br/> |<span data-ttu-id="d9d6c-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9d6c-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9d6c-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9d6c-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9d6c-149">False</span><span class="sxs-lookup"><span data-stu-id="d9d6c-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9d6c-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9d6c-150">See also</span></span>



[<span data-ttu-id="d9d6c-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="d9d6c-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="d9d6c-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d9d6c-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

