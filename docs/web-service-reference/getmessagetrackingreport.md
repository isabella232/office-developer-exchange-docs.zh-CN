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
description: GetMessageTrackingReport 元素包含要检索完整的邮件跟踪报告的指定 ID 的 GetMessageTrackingReport 操作的请求
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754622"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="486f4-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="486f4-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="486f4-104">**GetMessageTrackingReport**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)以检索完整的邮件跟踪报告的指定 ID 的请求</span><span class="sxs-lookup"><span data-stu-id="486f4-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
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

 <span data-ttu-id="486f4-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="486f4-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="486f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="486f4-106">Attributes and elements</span></span>

<span data-ttu-id="486f4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="486f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="486f4-108">属性</span><span class="sxs-lookup"><span data-stu-id="486f4-108">Attributes</span></span>

<span data-ttu-id="486f4-109">无。</span><span class="sxs-lookup"><span data-stu-id="486f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="486f4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="486f4-110">Child elements</span></span>

|<span data-ttu-id="486f4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="486f4-111">**Element**</span></span>|<span data-ttu-id="486f4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="486f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="486f4-113">范围 (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="486f4-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="486f4-114">指定用于执行搜索的位置。</span><span class="sxs-lookup"><span data-stu-id="486f4-114">Specifies where to perform the search.</span></span> <span data-ttu-id="486f4-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="486f4-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="486f4-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="486f4-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="486f4-117">指定用于跟踪报告，若要检索的类型。</span><span class="sxs-lookup"><span data-stu-id="486f4-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="486f4-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="486f4-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="486f4-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="486f4-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="486f4-120">指定要用于指定的跟踪报告的收件人地址。</span><span class="sxs-lookup"><span data-stu-id="486f4-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="486f4-121">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="486f4-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="486f4-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="486f4-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="486f4-123">指定来自**FindMessageTrackingReport**操作标识字符串。</span><span class="sxs-lookup"><span data-stu-id="486f4-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="486f4-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="486f4-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="486f4-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="486f4-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="486f4-126">指定运行任务的用户具有的特权的角色。</span><span class="sxs-lookup"><span data-stu-id="486f4-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="486f4-127">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="486f4-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="486f4-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="486f4-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="486f4-129">指定将用于派生跟踪报告的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="486f4-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="486f4-130">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="486f4-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="486f4-131">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="486f4-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="486f4-132">指定的一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="486f4-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="486f4-133">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="486f4-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="486f4-134">父元素</span><span class="sxs-lookup"><span data-stu-id="486f4-134">Parent elements</span></span>

<span data-ttu-id="486f4-135">无。</span><span class="sxs-lookup"><span data-stu-id="486f4-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="486f4-136">备注</span><span class="sxs-lookup"><span data-stu-id="486f4-136">Remarks</span></span>

<span data-ttu-id="486f4-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="486f4-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="486f4-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="486f4-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="486f4-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="486f4-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="486f4-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="486f4-140">Schema Name</span></span>  <br/> |<span data-ttu-id="486f4-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="486f4-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="486f4-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="486f4-142">Validation File</span></span>  <br/> |<span data-ttu-id="486f4-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="486f4-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="486f4-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="486f4-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="486f4-145">False</span><span class="sxs-lookup"><span data-stu-id="486f4-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="486f4-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="486f4-146">See also</span></span>



[<span data-ttu-id="486f4-147">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="486f4-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="486f4-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="486f4-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

