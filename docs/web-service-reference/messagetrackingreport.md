---
title: Search-messagetrackingreport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: Search-messagetrackingreport 元素包含 GetMessageTrackingReport 操作中返回的单个邮件。
ms.openlocfilehash: fc3e56fbb1bee411fa31751f558f520874133076
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463214"
---
# <a name="messagetrackingreport"></a><span data-ttu-id="c0109-103">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="c0109-103">MessageTrackingReport</span></span>

<span data-ttu-id="c0109-104">**Search-messagetrackingreport**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回的单个邮件。</span><span class="sxs-lookup"><span data-stu-id="c0109-104">The **MessageTrackingReport** element contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
```XML
<MessageTrackingReport>
   <Sender/>
   <PurportedSender/>
   <Subject/>
   <SubmitTime/>
   <OriginalRecipients/>
   <RecipientTrackingEvents/>
   <Properties/>
</MessageTrackingReport>
```

 <span data-ttu-id="c0109-105">**MessageTrackingReportType**</span><span class="sxs-lookup"><span data-stu-id="c0109-105">**MessageTrackingReportType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0109-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0109-106">Attributes and elements</span></span>

<span data-ttu-id="c0109-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0109-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0109-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c0109-108">Attributes</span></span>

<span data-ttu-id="c0109-109">无。</span><span class="sxs-lookup"><span data-stu-id="c0109-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0109-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c0109-110">Child elements</span></span>

|<span data-ttu-id="c0109-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0109-111">**Element**</span></span>|<span data-ttu-id="c0109-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0109-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0109-113">发件人（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="c0109-113">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="c0109-114">包含电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="c0109-114">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c0109-115">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="c0109-115">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="c0109-116">包含所声称的电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="c0109-116">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c0109-117">主题</span><span class="sxs-lookup"><span data-stu-id="c0109-117">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="c0109-118">包含电子邮件的主题。</span><span class="sxs-lookup"><span data-stu-id="c0109-118">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c0109-119">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="c0109-119">SubmitTime</span></span>](submittime.md) <br/> |<span data-ttu-id="c0109-120">包含电子邮件提交日期的时间。</span><span class="sxs-lookup"><span data-stu-id="c0109-120">Contains the time of day that the e-mail message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="c0109-121">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="c0109-121">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="c0109-122">包含电子邮件收件人的列表。</span><span class="sxs-lookup"><span data-stu-id="c0109-122">Contains a list of the recipients of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c0109-123">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="c0109-123">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="c0109-124">包含收件人的一个或多个跟踪事件的列表。</span><span class="sxs-lookup"><span data-stu-id="c0109-124">Contains a list of one or more tracking events for the recipients.</span></span>  <br/> |
|[<span data-ttu-id="c0109-125">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="c0109-125">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="c0109-126">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="c0109-126">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0109-127">父元素</span><span class="sxs-lookup"><span data-stu-id="c0109-127">Parent elements</span></span>

|<span data-ttu-id="c0109-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0109-128">**Element**</span></span>|<span data-ttu-id="c0109-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0109-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0109-130">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="c0109-130">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="c0109-131">包含单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="c0109-131">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0109-132">文本值</span><span class="sxs-lookup"><span data-stu-id="c0109-132">Text value</span></span>

<span data-ttu-id="c0109-133">无。</span><span class="sxs-lookup"><span data-stu-id="c0109-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0109-134">说明</span><span class="sxs-lookup"><span data-stu-id="c0109-134">Remarks</span></span>

<span data-ttu-id="c0109-135">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0109-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0109-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0109-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0109-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0109-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0109-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0109-138">Schema Name</span></span>  <br/> |<span data-ttu-id="c0109-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="c0109-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0109-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0109-140">Validation File</span></span>  <br/> |<span data-ttu-id="c0109-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0109-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0109-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0109-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0109-143">False</span><span class="sxs-lookup"><span data-stu-id="c0109-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0109-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0109-144">See also</span></span>



[<span data-ttu-id="c0109-145">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="c0109-145">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="c0109-146">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="c0109-146">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="c0109-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0109-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
- [<span data-ttu-id="c0109-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0109-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

