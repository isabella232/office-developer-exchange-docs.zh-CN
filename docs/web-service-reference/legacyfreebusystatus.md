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
description: LegacyFreeBusyStatus 元素表示的日历项目的忙/闲状态。
ms.openlocfilehash: 681d7256dbef09c6c43d33ea1fc92b5d05e73a41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826247"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="0f110-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0f110-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="0f110-104">**LegacyFreeBusyStatus**元素表示的日历项目的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="0f110-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="0f110-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="0f110-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0f110-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0f110-106">Attributes and elements</span></span>

<span data-ttu-id="0f110-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0f110-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f110-108">属性</span><span class="sxs-lookup"><span data-stu-id="0f110-108">Attributes</span></span>

<span data-ttu-id="0f110-109">无。</span><span class="sxs-lookup"><span data-stu-id="0f110-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f110-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0f110-110">Child elements</span></span>

<span data-ttu-id="0f110-111">无。</span><span class="sxs-lookup"><span data-stu-id="0f110-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0f110-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0f110-112">Parent elements</span></span>

|<span data-ttu-id="0f110-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f110-113">**Element**</span></span>|<span data-ttu-id="0f110-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f110-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f110-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="0f110-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0f110-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="0f110-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0f110-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0f110-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0f110-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="0f110-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0f110-119">文本值</span><span class="sxs-lookup"><span data-stu-id="0f110-119">Text value</span></span>

<span data-ttu-id="0f110-120">需要为此元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="0f110-120">A text value is required for this element.</span></span> <span data-ttu-id="0f110-121">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="0f110-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="0f110-122">免费</span><span class="sxs-lookup"><span data-stu-id="0f110-122">Free</span></span> 
- <span data-ttu-id="0f110-123">暂定</span><span class="sxs-lookup"><span data-stu-id="0f110-123">Tentative</span></span>
- <span data-ttu-id="0f110-124">忙碌</span><span class="sxs-lookup"><span data-stu-id="0f110-124">Busy</span></span>
- <span data-ttu-id="0f110-125">OOF</span><span class="sxs-lookup"><span data-stu-id="0f110-125">OOF</span></span>
- <span data-ttu-id="0f110-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="0f110-126">WorkingElsewhere</span></span>
- <span data-ttu-id="0f110-127">NoData</span><span class="sxs-lookup"><span data-stu-id="0f110-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f110-128">备注</span><span class="sxs-lookup"><span data-stu-id="0f110-128">Remarks</span></span>

<span data-ttu-id="0f110-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0f110-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f110-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="0f110-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f110-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="0f110-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f110-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="0f110-132">Schema name</span></span>  <br/> |<span data-ttu-id="0f110-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="0f110-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="0f110-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="0f110-134">Validation file</span></span>  <br/> |<span data-ttu-id="0f110-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0f110-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f110-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="0f110-136">Can be empty</span></span>  <br/> |<span data-ttu-id="0f110-137">False</span><span class="sxs-lookup"><span data-stu-id="0f110-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f110-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f110-138">See also</span></span>

- [<span data-ttu-id="0f110-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0f110-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

