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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754622"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="c22a9-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c22a9-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="c22a9-104">**GetMessageTrackingReport**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)以检索完整的邮件跟踪报告的指定 ID 的请求</span><span class="sxs-lookup"><span data-stu-id="c22a9-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
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

 <span data-ttu-id="c22a9-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="c22a9-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c22a9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c22a9-106">Attributes and elements</span></span>

<span data-ttu-id="c22a9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c22a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c22a9-108">属性</span><span class="sxs-lookup"><span data-stu-id="c22a9-108">Attributes</span></span>

<span data-ttu-id="c22a9-109">无。</span><span class="sxs-lookup"><span data-stu-id="c22a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c22a9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c22a9-110">Child elements</span></span>

|<span data-ttu-id="c22a9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c22a9-111">**Element**</span></span>|<span data-ttu-id="c22a9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c22a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c22a9-113">范围 (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="c22a9-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="c22a9-114">指定用于执行搜索的位置。</span><span class="sxs-lookup"><span data-stu-id="c22a9-114">Specifies where to perform the search.</span></span> <span data-ttu-id="c22a9-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="c22a9-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="c22a9-117">指定用于跟踪报告，若要检索的类型。</span><span class="sxs-lookup"><span data-stu-id="c22a9-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="c22a9-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="c22a9-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="c22a9-120">指定要用于指定的跟踪报告的收件人地址。</span><span class="sxs-lookup"><span data-stu-id="c22a9-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="c22a9-121">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="c22a9-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="c22a9-123">指定来自**FindMessageTrackingReport**操作标识字符串。</span><span class="sxs-lookup"><span data-stu-id="c22a9-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="c22a9-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="c22a9-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="c22a9-126">指定运行任务的用户具有的特权的角色。</span><span class="sxs-lookup"><span data-stu-id="c22a9-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="c22a9-127">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="c22a9-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="c22a9-129">指定将用于派生跟踪报告的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="c22a9-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="c22a9-130">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c22a9-131">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="c22a9-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="c22a9-132">指定的一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="c22a9-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="c22a9-133">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="c22a9-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c22a9-134">父元素</span><span class="sxs-lookup"><span data-stu-id="c22a9-134">Parent elements</span></span>

<span data-ttu-id="c22a9-135">无。</span><span class="sxs-lookup"><span data-stu-id="c22a9-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c22a9-136">备注</span><span class="sxs-lookup"><span data-stu-id="c22a9-136">Remarks</span></span>

<span data-ttu-id="c22a9-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c22a9-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c22a9-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="c22a9-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c22a9-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="c22a9-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c22a9-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="c22a9-140">Schema Name</span></span>  <br/> |<span data-ttu-id="c22a9-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="c22a9-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c22a9-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="c22a9-142">Validation File</span></span>  <br/> |<span data-ttu-id="c22a9-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c22a9-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c22a9-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="c22a9-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="c22a9-145">False</span><span class="sxs-lookup"><span data-stu-id="c22a9-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c22a9-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c22a9-146">See also</span></span>



[<span data-ttu-id="c22a9-147">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="c22a9-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="c22a9-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c22a9-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

