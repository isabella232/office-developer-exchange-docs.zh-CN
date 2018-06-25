---
title: RecipientTrackingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: RecipientTrackingEvents 元素表示一条消息的一个或多个事件的集合。
ms.openlocfilehash: 5fa5df422eff533891d021b77d5443b314d36244
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826993"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="83481-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="83481-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="83481-104">**RecipientTrackingEvents**元素表示一条消息的一个或多个事件的集合。</span><span class="sxs-lookup"><span data-stu-id="83481-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="83481-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="83481-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83481-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="83481-106">Attributes and elements</span></span>

<span data-ttu-id="83481-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="83481-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83481-108">属性</span><span class="sxs-lookup"><span data-stu-id="83481-108">Attributes</span></span>

<span data-ttu-id="83481-109">无。</span><span class="sxs-lookup"><span data-stu-id="83481-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83481-110">子元素</span><span class="sxs-lookup"><span data-stu-id="83481-110">Child elements</span></span>

|<span data-ttu-id="83481-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="83481-111">**Element**</span></span>|<span data-ttu-id="83481-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="83481-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83481-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="83481-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="83481-114">包含用于跟踪报告中的特定事件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="83481-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83481-115">父元素</span><span class="sxs-lookup"><span data-stu-id="83481-115">Parent elements</span></span>

|<span data-ttu-id="83481-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="83481-116">**Element**</span></span>|<span data-ttu-id="83481-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="83481-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83481-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="83481-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="83481-119">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="83481-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83481-120">备注</span><span class="sxs-lookup"><span data-stu-id="83481-120">Remarks</span></span>

<span data-ttu-id="83481-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="83481-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83481-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="83481-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83481-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="83481-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83481-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="83481-124">Schema Name</span></span>  <br/> |<span data-ttu-id="83481-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="83481-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="83481-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="83481-126">Validation File</span></span>  <br/> |<span data-ttu-id="83481-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83481-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83481-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="83481-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="83481-129">False</span><span class="sxs-lookup"><span data-stu-id="83481-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83481-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83481-130">See also</span></span>



[<span data-ttu-id="83481-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="83481-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="83481-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="83481-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

