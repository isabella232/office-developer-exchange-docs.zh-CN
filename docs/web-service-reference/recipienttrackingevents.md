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
description: RecipientTrackingEvents 元素表示邮件的一个或多个事件的集合。
ms.openlocfilehash: c0b25a0e22d13bc1f26768b9b7089d96eb2e8cfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468479"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="db106-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="db106-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="db106-104">**RecipientTrackingEvents**元素表示邮件的一个或多个事件的集合。</span><span class="sxs-lookup"><span data-stu-id="db106-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="db106-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="db106-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db106-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db106-106">Attributes and elements</span></span>

<span data-ttu-id="db106-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db106-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db106-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="db106-108">Attributes</span></span>

<span data-ttu-id="db106-109">无。</span><span class="sxs-lookup"><span data-stu-id="db106-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db106-110">子元素</span><span class="sxs-lookup"><span data-stu-id="db106-110">Child elements</span></span>

|<span data-ttu-id="db106-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="db106-111">**Element**</span></span>|<span data-ttu-id="db106-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="db106-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db106-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="db106-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="db106-114">包含跟踪报告中特定事件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="db106-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db106-115">父元素</span><span class="sxs-lookup"><span data-stu-id="db106-115">Parent elements</span></span>

|<span data-ttu-id="db106-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="db106-116">**Element**</span></span>|<span data-ttu-id="db106-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="db106-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db106-118">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="db106-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="db106-119">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="db106-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db106-120">说明</span><span class="sxs-lookup"><span data-stu-id="db106-120">Remarks</span></span>

<span data-ttu-id="db106-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db106-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db106-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="db106-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db106-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="db106-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db106-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="db106-124">Schema Name</span></span>  <br/> |<span data-ttu-id="db106-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="db106-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="db106-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="db106-126">Validation File</span></span>  <br/> |<span data-ttu-id="db106-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db106-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db106-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="db106-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="db106-129">False</span><span class="sxs-lookup"><span data-stu-id="db106-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db106-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db106-130">See also</span></span>



[<span data-ttu-id="db106-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="db106-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="db106-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="db106-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

