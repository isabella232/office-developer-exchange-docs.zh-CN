---
title: 属性 (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: Properties 元素包含一个或多个跟踪属性的列表。
ms.openlocfilehash: 079d2d2c101fdeb7f26d65798048c3c6c59f3e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826897"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="5c39f-103">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="5c39f-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="5c39f-104">**Properties**元素包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="5c39f-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="5c39f-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5c39f-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="5c39f-106">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="5c39f-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="5c39f-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="5c39f-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5c39f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c39f-108">Attributes and elements</span></span>

<span data-ttu-id="5c39f-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c39f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c39f-110">属性</span><span class="sxs-lookup"><span data-stu-id="5c39f-110">Attributes</span></span>

<span data-ttu-id="5c39f-111">无。</span><span class="sxs-lookup"><span data-stu-id="5c39f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c39f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5c39f-112">Child elements</span></span>

|<span data-ttu-id="5c39f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c39f-113">**Element**</span></span>|<span data-ttu-id="5c39f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c39f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c39f-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="5c39f-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="5c39f-116">表示字符串用于创建邮件跟踪报告的属性的名称 / 值的对。</span><span class="sxs-lookup"><span data-stu-id="5c39f-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c39f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5c39f-117">Parent elements</span></span>

|<span data-ttu-id="5c39f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c39f-118">**Element**</span></span>|<span data-ttu-id="5c39f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c39f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c39f-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5c39f-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="5c39f-121">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="5c39f-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="5c39f-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="5c39f-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="5c39f-123">包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="5c39f-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="5c39f-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5c39f-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="5c39f-125">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="5c39f-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="5c39f-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="5c39f-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="5c39f-127">包含结果的单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="5c39f-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="5c39f-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="5c39f-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="5c39f-129">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="5c39f-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="5c39f-130">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5c39f-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="5c39f-131">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="5c39f-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5c39f-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="5c39f-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="5c39f-133">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5c39f-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c39f-134">文本值</span><span class="sxs-lookup"><span data-stu-id="5c39f-134">Text value</span></span>

<span data-ttu-id="5c39f-135">无。</span><span class="sxs-lookup"><span data-stu-id="5c39f-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c39f-136">备注</span><span class="sxs-lookup"><span data-stu-id="5c39f-136">Remarks</span></span>

<span data-ttu-id="5c39f-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5c39f-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c39f-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c39f-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c39f-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c39f-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5c39f-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c39f-140">Schema Name</span></span>  <br/> |<span data-ttu-id="5c39f-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="5c39f-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5c39f-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c39f-142">Validation File</span></span>  <br/> |<span data-ttu-id="5c39f-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5c39f-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c39f-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c39f-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c39f-145">False</span><span class="sxs-lookup"><span data-stu-id="5c39f-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c39f-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c39f-146">See also</span></span>

- [<span data-ttu-id="5c39f-147">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="5c39f-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="5c39f-148">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="5c39f-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="5c39f-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5c39f-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

