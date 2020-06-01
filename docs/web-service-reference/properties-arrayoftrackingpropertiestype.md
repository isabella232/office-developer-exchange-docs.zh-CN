---
title: Properties （ArrayOfTrackingPropertiesType）
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
ms.openlocfilehash: 007a4dc14c84c47ea7af8ccacc554c134d563e44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465630"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="670f7-103">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="670f7-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="670f7-104">**Properties**元素包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="670f7-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="670f7-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="670f7-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="670f7-106">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="670f7-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="670f7-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="670f7-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="670f7-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="670f7-108">Attributes and elements</span></span>

<span data-ttu-id="670f7-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="670f7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="670f7-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="670f7-110">Attributes</span></span>

<span data-ttu-id="670f7-111">无。</span><span class="sxs-lookup"><span data-stu-id="670f7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="670f7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="670f7-112">Child elements</span></span>

|<span data-ttu-id="670f7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="670f7-113">**Element**</span></span>|<span data-ttu-id="670f7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="670f7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="670f7-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="670f7-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="670f7-116">表示用于创建邮件跟踪报告的属性的字符串的名称和值对。</span><span class="sxs-lookup"><span data-stu-id="670f7-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="670f7-117">父元素</span><span class="sxs-lookup"><span data-stu-id="670f7-117">Parent elements</span></span>

|<span data-ttu-id="670f7-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="670f7-118">**Element**</span></span>|<span data-ttu-id="670f7-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="670f7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="670f7-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="670f7-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="670f7-121">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="670f7-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="670f7-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="670f7-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="670f7-123">包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="670f7-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="670f7-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="670f7-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="670f7-125">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="670f7-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="670f7-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="670f7-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="670f7-127">包含单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="670f7-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="670f7-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="670f7-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="670f7-129">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="670f7-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="670f7-130">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="670f7-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="670f7-131">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="670f7-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="670f7-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="670f7-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="670f7-133">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="670f7-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="670f7-134">文本值</span><span class="sxs-lookup"><span data-stu-id="670f7-134">Text value</span></span>

<span data-ttu-id="670f7-135">无。</span><span class="sxs-lookup"><span data-stu-id="670f7-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="670f7-136">说明</span><span class="sxs-lookup"><span data-stu-id="670f7-136">Remarks</span></span>

<span data-ttu-id="670f7-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="670f7-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="670f7-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="670f7-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="670f7-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="670f7-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="670f7-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="670f7-140">Schema Name</span></span>  <br/> |<span data-ttu-id="670f7-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="670f7-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="670f7-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="670f7-142">Validation File</span></span>  <br/> |<span data-ttu-id="670f7-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="670f7-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="670f7-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="670f7-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="670f7-145">False</span><span class="sxs-lookup"><span data-stu-id="670f7-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="670f7-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="670f7-146">See also</span></span>

- [<span data-ttu-id="670f7-147">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="670f7-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="670f7-148">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="670f7-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="670f7-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="670f7-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

