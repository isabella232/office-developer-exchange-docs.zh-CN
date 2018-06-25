---
title: 错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Errors
api_type:
- schema
ms.assetid: ea37a2b5-e2d1-4089-960f-7014b9535a50
description: 错误元素包含存储通过 Web 服务返回的错误的属性包。
ms.openlocfilehash: a029492c1e3c11cc31d3501bd4ea0024ef8ecb91
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754159"
---
# <a name="errors"></a><span data-ttu-id="1ac7a-103">错误</span><span class="sxs-lookup"><span data-stu-id="1ac7a-103">Errors</span></span>

<span data-ttu-id="1ac7a-104">**错误**元素包含存储通过 Web 服务返回的错误的属性包。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-104">The **Errors** element contains a property bag to store errors that are returned through the Web service.</span></span> 
  
[<span data-ttu-id="1ac7a-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1ac7a-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
[<span data-ttu-id="1ac7a-106">错误</span><span class="sxs-lookup"><span data-stu-id="1ac7a-106">Errors</span></span>](errors-ex15websvcsotherref.md)
  
```xml
<Errors>
   <Properties/>
</Errors>
```

 <span data-ttu-id="1ac7a-107">**ArrayOfArraysOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="1ac7a-107">**ArrayOfArraysOfTrackingPropertiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ac7a-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1ac7a-108">Attributes and elements</span></span>

<span data-ttu-id="1ac7a-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ac7a-110">属性</span><span class="sxs-lookup"><span data-stu-id="1ac7a-110">Attributes</span></span>

<span data-ttu-id="1ac7a-111">无。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ac7a-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1ac7a-112">Child elements</span></span>

|<span data-ttu-id="1ac7a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ac7a-113">**Element**</span></span>|<span data-ttu-id="1ac7a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ac7a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ac7a-115">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1ac7a-115">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1ac7a-116">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-116">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ac7a-117">父元素</span><span class="sxs-lookup"><span data-stu-id="1ac7a-117">Parent elements</span></span>

|<span data-ttu-id="1ac7a-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ac7a-118">**Element**</span></span>|<span data-ttu-id="1ac7a-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ac7a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ac7a-120">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="1ac7a-120">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="1ac7a-121">包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-121">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1ac7a-122">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="1ac7a-122">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="1ac7a-123">包含结果的单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-123">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ac7a-124">文本值</span><span class="sxs-lookup"><span data-stu-id="1ac7a-124">Text value</span></span>

<span data-ttu-id="1ac7a-125">无。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ac7a-126">备注</span><span class="sxs-lookup"><span data-stu-id="1ac7a-126">Remarks</span></span>

<span data-ttu-id="1ac7a-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1ac7a-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ac7a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="1ac7a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ac7a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="1ac7a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1ac7a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="1ac7a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1ac7a-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="1ac7a-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1ac7a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="1ac7a-132">Validation File</span></span>  <br/> |<span data-ttu-id="1ac7a-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1ac7a-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1ac7a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="1ac7a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ac7a-135">False</span><span class="sxs-lookup"><span data-stu-id="1ac7a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ac7a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1ac7a-136">See also</span></span>



[<span data-ttu-id="1ac7a-137">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="1ac7a-137">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="1ac7a-138">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="1ac7a-138">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1ac7a-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1ac7a-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

