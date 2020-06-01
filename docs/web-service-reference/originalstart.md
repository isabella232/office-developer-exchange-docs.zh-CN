---
title: OriginalStart
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalStart
api_type:
- schema
ms.assetid: 4599dd34-15ee-4d57-b886-732081b50784
description: OriginalStart 元素表示日历项目的原始开始时间。
ms.openlocfilehash: 5346a65c432b8e96cb95e412e3e88fbc40ce36e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462365"
---
# <a name="originalstart"></a><span data-ttu-id="becdf-103">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="becdf-103">OriginalStart</span></span>

<span data-ttu-id="becdf-104">**OriginalStart**元素表示日历项目的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="becdf-104">The **OriginalStart** element represents the original start time of a calendar item.</span></span> 
  
```xml
<OriginalStart/>
```

 <span data-ttu-id="becdf-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="becdf-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="becdf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="becdf-106">Attributes and elements</span></span>

<span data-ttu-id="becdf-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="becdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="becdf-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="becdf-108">Attributes</span></span>

<span data-ttu-id="becdf-109">无。</span><span class="sxs-lookup"><span data-stu-id="becdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="becdf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="becdf-110">Child elements</span></span>

<span data-ttu-id="becdf-111">无。</span><span class="sxs-lookup"><span data-stu-id="becdf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="becdf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="becdf-112">Parent elements</span></span>

|<span data-ttu-id="becdf-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="becdf-113">**Element**</span></span>|<span data-ttu-id="becdf-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="becdf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="becdf-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="becdf-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="becdf-116">表示 Exchange 存储中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="becdf-116">Represents a calendar item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="becdf-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="becdf-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="becdf-118">表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="becdf-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="becdf-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="becdf-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="becdf-120">表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="becdf-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="becdf-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="becdf-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="becdf-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="becdf-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="becdf-123">重复</span><span class="sxs-lookup"><span data-stu-id="becdf-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="becdf-124">代表定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="becdf-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="becdf-125">文本值</span><span class="sxs-lookup"><span data-stu-id="becdf-125">Text value</span></span>

<span data-ttu-id="becdf-126">如果使用此元素，则表示日期和时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="becdf-126">A text value that represents a date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="becdf-127">说明</span><span class="sxs-lookup"><span data-stu-id="becdf-127">Remarks</span></span>

<span data-ttu-id="becdf-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="becdf-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="becdf-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="becdf-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="becdf-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="becdf-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="becdf-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="becdf-131">Schema Name</span></span>  <br/> |<span data-ttu-id="becdf-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="becdf-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="becdf-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="becdf-133">Validation File</span></span>  <br/> |<span data-ttu-id="becdf-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="becdf-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="becdf-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="becdf-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="becdf-136">False</span><span class="sxs-lookup"><span data-stu-id="becdf-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="becdf-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="becdf-137">See also</span></span>



- [<span data-ttu-id="becdf-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="becdf-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

