---
title: 发件人 (EmailAddressType)
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
description: 发件人元素表示邮件的发件人的电子邮件地址。
ms.openlocfilehash: bac62412caf1044c13015f1d9d7ef63552747c1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827320"
---
# <a name="sender-emailaddresstype"></a><span data-ttu-id="4e933-103">发件人 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4e933-103">Sender (EmailAddressType)</span></span>

<span data-ttu-id="4e933-104">**发件人**元素表示邮件的发件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="4e933-104">The **Sender** element represents the e-mail address for the sender of the message.</span></span> 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 <span data-ttu-id="4e933-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="4e933-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e933-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e933-106">Attributes and elements</span></span>

<span data-ttu-id="4e933-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e933-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e933-108">属性</span><span class="sxs-lookup"><span data-stu-id="4e933-108">Attributes</span></span>

<span data-ttu-id="4e933-109">无。</span><span class="sxs-lookup"><span data-stu-id="4e933-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e933-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4e933-110">Child elements</span></span>

|<span data-ttu-id="4e933-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e933-111">**Element**</span></span>|<span data-ttu-id="4e933-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e933-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e933-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4e933-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="4e933-114">代表邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="4e933-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="4e933-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="4e933-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4e933-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="4e933-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="4e933-117">定义邮箱用户的主要简单邮件传输协议 (SMTP) 的地址。</span><span class="sxs-lookup"><span data-stu-id="4e933-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="4e933-118">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="4e933-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4e933-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="4e933-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="4e933-120">代表收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="4e933-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="4e933-121">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="4e933-121">The default value is SMTP.</span></span> <span data-ttu-id="4e933-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="4e933-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4e933-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="4e933-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="4e933-124">表示由的电子邮件地址的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="4e933-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="4e933-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="4e933-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4e933-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="4e933-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4e933-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="4e933-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e933-129">父元素</span><span class="sxs-lookup"><span data-stu-id="4e933-129">Parent elements</span></span>

|<span data-ttu-id="4e933-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e933-130">**Element**</span></span>|<span data-ttu-id="4e933-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e933-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e933-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4e933-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="4e933-133">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="4e933-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="4e933-134">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="4e933-134">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="4e933-135">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="4e933-135">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="4e933-136">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4e933-136">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="4e933-137">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="4e933-137">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e933-138">文本值</span><span class="sxs-lookup"><span data-stu-id="4e933-138">Text value</span></span>

<span data-ttu-id="4e933-139">无。</span><span class="sxs-lookup"><span data-stu-id="4e933-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e933-140">备注</span><span class="sxs-lookup"><span data-stu-id="4e933-140">Remarks</span></span>

<span data-ttu-id="4e933-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4e933-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e933-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e933-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e933-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e933-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e933-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e933-144">Schema Name</span></span>  <br/> |<span data-ttu-id="4e933-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="4e933-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e933-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e933-146">Validation File</span></span>  <br/> |<span data-ttu-id="4e933-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e933-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e933-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e933-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e933-149">False</span><span class="sxs-lookup"><span data-stu-id="4e933-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e933-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e933-150">See also</span></span>



[<span data-ttu-id="4e933-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="4e933-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="4e933-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4e933-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

