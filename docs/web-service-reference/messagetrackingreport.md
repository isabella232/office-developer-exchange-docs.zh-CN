---
title: MessageTrackingReport
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
description: MessageTrackingReport 元素包含 GetMessageTrackingReport 操作中返回的单个消息。
ms.openlocfilehash: d01e0fbf099d096c7f255a8e94070e330577e6ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826457"
---
# <a name="messagetrackingreport"></a><span data-ttu-id="29ae1-103">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="29ae1-103">MessageTrackingReport</span></span>

<span data-ttu-id="29ae1-104">**MessageTrackingReport**元素包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回单个邮件。</span><span class="sxs-lookup"><span data-stu-id="29ae1-104">The **MessageTrackingReport** element contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
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

 <span data-ttu-id="29ae1-105">**MessageTrackingReportType**</span><span class="sxs-lookup"><span data-stu-id="29ae1-105">**MessageTrackingReportType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29ae1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="29ae1-106">Attributes and elements</span></span>

<span data-ttu-id="29ae1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="29ae1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29ae1-108">属性</span><span class="sxs-lookup"><span data-stu-id="29ae1-108">Attributes</span></span>

<span data-ttu-id="29ae1-109">无。</span><span class="sxs-lookup"><span data-stu-id="29ae1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29ae1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="29ae1-110">Child elements</span></span>

|<span data-ttu-id="29ae1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="29ae1-111">**Element**</span></span>|<span data-ttu-id="29ae1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="29ae1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ae1-113">发件人 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="29ae1-113">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="29ae1-114">包含发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="29ae1-114">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-115">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="29ae1-115">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="29ae1-116">包含声称的发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="29ae1-116">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-117">Subject</span><span class="sxs-lookup"><span data-stu-id="29ae1-117">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="29ae1-118">包含电子邮件的主题。</span><span class="sxs-lookup"><span data-stu-id="29ae1-118">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-119">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="29ae1-119">SubmitTime</span></span>](submittime.md) <br/> |<span data-ttu-id="29ae1-120">包含已提交的电子邮件的一天的时间。</span><span class="sxs-lookup"><span data-stu-id="29ae1-120">Contains the time of day that the e-mail message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-121">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="29ae1-121">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="29ae1-122">包含电子邮件收件人的列表。</span><span class="sxs-lookup"><span data-stu-id="29ae1-122">Contains a list of the recipients of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-123">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="29ae1-123">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="29ae1-124">包含一个或多个跟踪事件的列表的收件人。</span><span class="sxs-lookup"><span data-stu-id="29ae1-124">Contains a list of one or more tracking events for the recipients.</span></span>  <br/> |
|[<span data-ttu-id="29ae1-125">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="29ae1-125">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="29ae1-126">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="29ae1-126">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="29ae1-127">父元素</span><span class="sxs-lookup"><span data-stu-id="29ae1-127">Parent elements</span></span>

|<span data-ttu-id="29ae1-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="29ae1-128">**Element**</span></span>|<span data-ttu-id="29ae1-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="29ae1-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ae1-130">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="29ae1-130">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="29ae1-131">包含结果的单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="29ae1-131">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="29ae1-132">文本值</span><span class="sxs-lookup"><span data-stu-id="29ae1-132">Text value</span></span>

<span data-ttu-id="29ae1-133">无。</span><span class="sxs-lookup"><span data-stu-id="29ae1-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29ae1-134">备注</span><span class="sxs-lookup"><span data-stu-id="29ae1-134">Remarks</span></span>

<span data-ttu-id="29ae1-135">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="29ae1-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29ae1-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="29ae1-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29ae1-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="29ae1-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="29ae1-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="29ae1-138">Schema Name</span></span>  <br/> |<span data-ttu-id="29ae1-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="29ae1-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="29ae1-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="29ae1-140">Validation File</span></span>  <br/> |<span data-ttu-id="29ae1-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="29ae1-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="29ae1-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="29ae1-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="29ae1-143">False</span><span class="sxs-lookup"><span data-stu-id="29ae1-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29ae1-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="29ae1-144">See also</span></span>



[<span data-ttu-id="29ae1-145">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="29ae1-145">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="29ae1-146">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="29ae1-146">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="29ae1-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="29ae1-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
- [<span data-ttu-id="29ae1-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="29ae1-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

