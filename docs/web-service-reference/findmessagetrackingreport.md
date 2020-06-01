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
description: FindMessageTrackingReport 元素指定要查找的邮件类型的条件。
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462934"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="7a4ca-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7a4ca-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="7a4ca-104">**FindMessageTrackingReport**元素指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
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

 <span data-ttu-id="7a4ca-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a4ca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a4ca-106">Attributes and elements</span></span>

<span data-ttu-id="7a4ca-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a4ca-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a4ca-108">Attributes</span></span>

<span data-ttu-id="7a4ca-109">无。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a4ca-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7a4ca-110">Child elements</span></span>

|<span data-ttu-id="7a4ca-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-111">**Element**</span></span>|<span data-ttu-id="7a4ca-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a4ca-113">范围（NonEmptyStringType）</span><span class="sxs-lookup"><span data-stu-id="7a4ca-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="7a4ca-114">表示邮件跟踪报告的范围。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-115">域（邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="7a4ca-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="7a4ca-116">包含执行邮件跟踪的域的名称。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-117">发件人（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="7a4ca-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="7a4ca-118">包含电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="7a4ca-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="7a4ca-120">包含所声称的电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-121">收件人</span><span class="sxs-lookup"><span data-stu-id="7a4ca-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="7a4ca-122">包含邮件收件人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-123">主题</span><span class="sxs-lookup"><span data-stu-id="7a4ca-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="7a4ca-124">包含电子邮件的主题。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="7a4ca-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="7a4ca-126">包含搜索的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="7a4ca-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="7a4ca-128">包含搜索的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="7a4ca-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="7a4ca-130">包含搜索的邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="7a4ca-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="7a4ca-132">包含发送了跨界邮件的邮箱的名称。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="7a4ca-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="7a4ca-134">表示诊断报告的详细程度。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="7a4ca-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="7a4ca-136">表示跟踪远程站点或林中的邮件的起始点。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="7a4ca-137">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="7a4ca-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="7a4ca-138">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="7a4ca-139">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a4ca-140">父元素</span><span class="sxs-lookup"><span data-stu-id="7a4ca-140">Parent elements</span></span>

<span data-ttu-id="7a4ca-141">无。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7a4ca-142">文本值</span><span class="sxs-lookup"><span data-stu-id="7a4ca-142">Text value</span></span>

<span data-ttu-id="7a4ca-143">无。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a4ca-144">说明</span><span class="sxs-lookup"><span data-stu-id="7a4ca-144">Remarks</span></span>

<span data-ttu-id="7a4ca-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a4ca-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a4ca-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a4ca-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a4ca-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a4ca-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a4ca-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a4ca-148">Schema Name</span></span>  <br/> |<span data-ttu-id="7a4ca-149">消息架构</span><span class="sxs-lookup"><span data-stu-id="7a4ca-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a4ca-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a4ca-150">Validation File</span></span>  <br/> |<span data-ttu-id="7a4ca-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7a4ca-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a4ca-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a4ca-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a4ca-153">False</span><span class="sxs-lookup"><span data-stu-id="7a4ca-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a4ca-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a4ca-154">See also</span></span>



[<span data-ttu-id="7a4ca-155">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="7a4ca-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="7a4ca-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a4ca-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

