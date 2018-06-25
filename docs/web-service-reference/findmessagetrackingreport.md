---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: FindMessageTrackingReport 元素指定条件的邮件，以查找的类型。
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754352"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="0a9c9-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0a9c9-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="0a9c9-104">**FindMessageTrackingReport**元素指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 <span data-ttu-id="0a9c9-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="0a9c9-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a9c9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a9c9-106">Attributes and elements</span></span>

<span data-ttu-id="0a9c9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a9c9-108">属性</span><span class="sxs-lookup"><span data-stu-id="0a9c9-108">Attributes</span></span>

<span data-ttu-id="0a9c9-109">无。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a9c9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0a9c9-110">Child elements</span></span>

|<span data-ttu-id="0a9c9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a9c9-111">**Element**</span></span>|<span data-ttu-id="0a9c9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a9c9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a9c9-113">范围 (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0a9c9-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="0a9c9-114">代表邮件跟踪报告应如何扩展。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-115">域 （邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="0a9c9-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="0a9c9-116">包含执行邮件跟踪所在的域的名称。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-117">发件人 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0a9c9-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="0a9c9-118">包含发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="0a9c9-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="0a9c9-120">包含声称的发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-121">Recipient</span><span class="sxs-lookup"><span data-stu-id="0a9c9-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="0a9c9-122">包含邮件的收件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-123">Subject</span><span class="sxs-lookup"><span data-stu-id="0a9c9-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="0a9c9-124">包含电子邮件的主题。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-125">开始日期时间</span><span class="sxs-lookup"><span data-stu-id="0a9c9-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="0a9c9-126">包含开始的日期和时间的搜索。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="0a9c9-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="0a9c9-128">包含的结束日期和时间搜索。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="0a9c9-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="0a9c9-130">包含搜索的消息标识符。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="0a9c9-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="0a9c9-132">包含其中发送跨内部部署邮件的邮箱的名称。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="0a9c9-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="0a9c9-134">表示的诊断报告的详细信息的级别。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="0a9c9-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="0a9c9-136">代表跟踪远程站点或林的邮件中的起始点。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="0a9c9-137">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0a9c9-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="0a9c9-138">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="0a9c9-139">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a9c9-140">父元素</span><span class="sxs-lookup"><span data-stu-id="0a9c9-140">Parent elements</span></span>

<span data-ttu-id="0a9c9-141">无。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0a9c9-142">文本值</span><span class="sxs-lookup"><span data-stu-id="0a9c9-142">Text value</span></span>

<span data-ttu-id="0a9c9-143">无。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a9c9-144">备注</span><span class="sxs-lookup"><span data-stu-id="0a9c9-144">Remarks</span></span>

<span data-ttu-id="0a9c9-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a9c9-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a9c9-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a9c9-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a9c9-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a9c9-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0a9c9-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a9c9-148">Schema Name</span></span>  <br/> |<span data-ttu-id="0a9c9-149">消息架构</span><span class="sxs-lookup"><span data-stu-id="0a9c9-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0a9c9-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a9c9-150">Validation File</span></span>  <br/> |<span data-ttu-id="0a9c9-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0a9c9-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0a9c9-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a9c9-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a9c9-153">False</span><span class="sxs-lookup"><span data-stu-id="0a9c9-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a9c9-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a9c9-154">See also</span></span>



[<span data-ttu-id="0a9c9-155">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="0a9c9-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="0a9c9-156">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0a9c9-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

