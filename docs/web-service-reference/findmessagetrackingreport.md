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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754352"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="7a651-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7a651-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="7a651-104">**FindMessageTrackingReport**元素指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="7a651-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
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

 <span data-ttu-id="7a651-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="7a651-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a651-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a651-106">Attributes and elements</span></span>

<span data-ttu-id="7a651-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a651-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a651-108">属性</span><span class="sxs-lookup"><span data-stu-id="7a651-108">Attributes</span></span>

<span data-ttu-id="7a651-109">无。</span><span class="sxs-lookup"><span data-stu-id="7a651-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a651-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7a651-110">Child elements</span></span>

|<span data-ttu-id="7a651-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a651-111">**Element**</span></span>|<span data-ttu-id="7a651-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a651-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a651-113">范围 (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7a651-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="7a651-114">代表邮件跟踪报告应如何扩展。</span><span class="sxs-lookup"><span data-stu-id="7a651-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="7a651-115">域 （邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="7a651-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="7a651-116">包含执行邮件跟踪所在的域的名称。</span><span class="sxs-lookup"><span data-stu-id="7a651-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="7a651-117">发件人 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7a651-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="7a651-118">包含发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="7a651-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a651-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="7a651-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="7a651-120">包含声称的发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="7a651-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a651-121">Recipient</span><span class="sxs-lookup"><span data-stu-id="7a651-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="7a651-122">包含邮件的收件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7a651-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="7a651-123">Subject</span><span class="sxs-lookup"><span data-stu-id="7a651-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="7a651-124">包含电子邮件的主题。</span><span class="sxs-lookup"><span data-stu-id="7a651-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a651-125">开始日期时间</span><span class="sxs-lookup"><span data-stu-id="7a651-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="7a651-126">包含开始的日期和时间的搜索。</span><span class="sxs-lookup"><span data-stu-id="7a651-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a651-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="7a651-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="7a651-128">包含的结束日期和时间搜索。</span><span class="sxs-lookup"><span data-stu-id="7a651-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a651-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="7a651-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="7a651-130">包含搜索的消息标识符。</span><span class="sxs-lookup"><span data-stu-id="7a651-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a651-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="7a651-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="7a651-132">包含其中发送跨内部部署邮件的邮箱的名称。</span><span class="sxs-lookup"><span data-stu-id="7a651-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="7a651-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="7a651-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="7a651-134">表示的诊断报告的详细信息的级别。</span><span class="sxs-lookup"><span data-stu-id="7a651-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="7a651-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="7a651-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="7a651-136">代表跟踪远程站点或林的邮件中的起始点。</span><span class="sxs-lookup"><span data-stu-id="7a651-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="7a651-137">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="7a651-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="7a651-138">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="7a651-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="7a651-139">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="7a651-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a651-140">父元素</span><span class="sxs-lookup"><span data-stu-id="7a651-140">Parent elements</span></span>

<span data-ttu-id="7a651-141">无。</span><span class="sxs-lookup"><span data-stu-id="7a651-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7a651-142">文本值</span><span class="sxs-lookup"><span data-stu-id="7a651-142">Text value</span></span>

<span data-ttu-id="7a651-143">无。</span><span class="sxs-lookup"><span data-stu-id="7a651-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a651-144">备注</span><span class="sxs-lookup"><span data-stu-id="7a651-144">Remarks</span></span>

<span data-ttu-id="7a651-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a651-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a651-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a651-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a651-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a651-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a651-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a651-148">Schema Name</span></span>  <br/> |<span data-ttu-id="7a651-149">消息架构</span><span class="sxs-lookup"><span data-stu-id="7a651-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a651-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a651-150">Validation File</span></span>  <br/> |<span data-ttu-id="7a651-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7a651-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a651-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a651-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a651-153">False</span><span class="sxs-lookup"><span data-stu-id="7a651-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a651-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a651-154">See also</span></span>



[<span data-ttu-id="7a651-155">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="7a651-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="7a651-156">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a651-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

