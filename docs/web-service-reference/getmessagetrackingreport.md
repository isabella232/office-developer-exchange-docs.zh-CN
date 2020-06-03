---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: GetMessageTrackingReport 元素包含 GetMessageTrackingReport 操作请求，以检索指定 ID 的完整邮件跟踪报告。
ms.openlocfilehash: 30596acd209580147e0f03e12a7868502159b29c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2020
ms.locfileid: "44466575"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="2fac2-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="2fac2-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="2fac2-104">**GetMessageTrackingReport**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="2fac2-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 <span data-ttu-id="2fac2-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="2fac2-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fac2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2fac2-106">Attributes and elements</span></span>

<span data-ttu-id="2fac2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2fac2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fac2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2fac2-108">Attributes</span></span>

<span data-ttu-id="2fac2-109">无。</span><span class="sxs-lookup"><span data-stu-id="2fac2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fac2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2fac2-110">Child elements</span></span>

|<span data-ttu-id="2fac2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2fac2-111">**Element**</span></span>|<span data-ttu-id="2fac2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2fac2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fac2-113">范围（NonEmptyStringType）</span><span class="sxs-lookup"><span data-stu-id="2fac2-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="2fac2-114">指定执行搜索的位置。</span><span class="sxs-lookup"><span data-stu-id="2fac2-114">Specifies where to perform the search.</span></span> <span data-ttu-id="2fac2-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2fac2-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="2fac2-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="2fac2-117">指定要检索的跟踪报告的类型。</span><span class="sxs-lookup"><span data-stu-id="2fac2-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="2fac2-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2fac2-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="2fac2-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="2fac2-120">指定要用于指定的跟踪报告的收件人地址。</span><span class="sxs-lookup"><span data-stu-id="2fac2-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="2fac2-121">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="2fac2-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="2fac2-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="2fac2-123">指定从**FindMessageTrackingReport**操作获取的标识字符串。</span><span class="sxs-lookup"><span data-stu-id="2fac2-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="2fac2-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2fac2-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="2fac2-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="2fac2-126">指定运行该任务的人员具有特权角色。</span><span class="sxs-lookup"><span data-stu-id="2fac2-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="2fac2-127">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="2fac2-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="2fac2-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="2fac2-129">指定将用于派生跟踪报告的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="2fac2-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="2fac2-130">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="2fac2-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="2fac2-131">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="2fac2-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="2fac2-132">指定一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="2fac2-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="2fac2-133">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="2fac2-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2fac2-134">父元素</span><span class="sxs-lookup"><span data-stu-id="2fac2-134">Parent elements</span></span>

<span data-ttu-id="2fac2-135">无。</span><span class="sxs-lookup"><span data-stu-id="2fac2-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fac2-136">说明</span><span class="sxs-lookup"><span data-stu-id="2fac2-136">Remarks</span></span>

<span data-ttu-id="2fac2-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2fac2-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fac2-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="2fac2-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fac2-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="2fac2-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2fac2-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="2fac2-140">Schema Name</span></span>  <br/> |<span data-ttu-id="2fac2-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="2fac2-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2fac2-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="2fac2-142">Validation File</span></span>  <br/> |<span data-ttu-id="2fac2-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2fac2-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2fac2-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="2fac2-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="2fac2-145">False</span><span class="sxs-lookup"><span data-stu-id="2fac2-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fac2-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2fac2-146">See also</span></span>



[<span data-ttu-id="2fac2-147">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="2fac2-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="2fac2-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2fac2-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

