---
title: LegacyFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LegacyFreeBusyStatus
api_type:
- schema
ms.assetid: ee5f3046-b79f-4f68-9455-1a688cee2745
description: LegacyFreeBusyStatus 元素表示日历项目的忙/闲状态。
ms.openlocfilehash: ecbcae0862c9c02c0a4a61012816e4c2c6ea07b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463228"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="28f1d-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="28f1d-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="28f1d-104">**LegacyFreeBusyStatus**元素表示日历项目的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="28f1d-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="28f1d-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="28f1d-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="28f1d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="28f1d-106">Attributes and elements</span></span>

<span data-ttu-id="28f1d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="28f1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28f1d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="28f1d-108">Attributes</span></span>

<span data-ttu-id="28f1d-109">无。</span><span class="sxs-lookup"><span data-stu-id="28f1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28f1d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="28f1d-110">Child elements</span></span>

<span data-ttu-id="28f1d-111">无。</span><span class="sxs-lookup"><span data-stu-id="28f1d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28f1d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="28f1d-112">Parent elements</span></span>

|<span data-ttu-id="28f1d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="28f1d-113">**Element**</span></span>|<span data-ttu-id="28f1d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="28f1d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28f1d-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="28f1d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="28f1d-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="28f1d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="28f1d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="28f1d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="28f1d-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="28f1d-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28f1d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="28f1d-119">Text value</span></span>

<span data-ttu-id="28f1d-120">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="28f1d-120">A text value is required for this element.</span></span> <span data-ttu-id="28f1d-121">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="28f1d-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="28f1d-122">空闲</span><span class="sxs-lookup"><span data-stu-id="28f1d-122">Free</span></span> 
- <span data-ttu-id="28f1d-123">暂</span><span class="sxs-lookup"><span data-stu-id="28f1d-123">Tentative</span></span>
- <span data-ttu-id="28f1d-124">忙碌</span><span class="sxs-lookup"><span data-stu-id="28f1d-124">Busy</span></span>
- <span data-ttu-id="28f1d-125">OOF</span><span class="sxs-lookup"><span data-stu-id="28f1d-125">OOF</span></span>
- <span data-ttu-id="28f1d-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="28f1d-126">WorkingElsewhere</span></span>
- <span data-ttu-id="28f1d-127">NoData</span><span class="sxs-lookup"><span data-stu-id="28f1d-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28f1d-128">说明</span><span class="sxs-lookup"><span data-stu-id="28f1d-128">Remarks</span></span>

<span data-ttu-id="28f1d-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="28f1d-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28f1d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="28f1d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28f1d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="28f1d-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28f1d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="28f1d-132">Schema name</span></span>  <br/> |<span data-ttu-id="28f1d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="28f1d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="28f1d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="28f1d-134">Validation file</span></span>  <br/> |<span data-ttu-id="28f1d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28f1d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28f1d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="28f1d-136">Can be empty</span></span>  <br/> |<span data-ttu-id="28f1d-137">False</span><span class="sxs-lookup"><span data-stu-id="28f1d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28f1d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28f1d-138">See also</span></span>

- [<span data-ttu-id="28f1d-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="28f1d-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

