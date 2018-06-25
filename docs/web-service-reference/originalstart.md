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
description: OriginalStart 元素均表示日历项目的原始开始时间。
ms.openlocfilehash: 9e5facb3df87ab08e05f23258abdf1767fae64e4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826668"
---
# <a name="originalstart"></a><span data-ttu-id="35f33-103">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="35f33-103">OriginalStart</span></span>

<span data-ttu-id="35f33-104">**OriginalStart**元素均表示日历项目的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="35f33-104">The **OriginalStart** element represents the original start time of a calendar item.</span></span> 
  
```xml
<OriginalStart/>
```

 <span data-ttu-id="35f33-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="35f33-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35f33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35f33-106">Attributes and elements</span></span>

<span data-ttu-id="35f33-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35f33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35f33-108">属性</span><span class="sxs-lookup"><span data-stu-id="35f33-108">Attributes</span></span>

<span data-ttu-id="35f33-109">无。</span><span class="sxs-lookup"><span data-stu-id="35f33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35f33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="35f33-110">Child elements</span></span>

<span data-ttu-id="35f33-111">无。</span><span class="sxs-lookup"><span data-stu-id="35f33-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35f33-112">父元素</span><span class="sxs-lookup"><span data-stu-id="35f33-112">Parent elements</span></span>

|<span data-ttu-id="35f33-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="35f33-113">**Element**</span></span>|<span data-ttu-id="35f33-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="35f33-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35f33-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="35f33-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="35f33-116">表示 Exchange 存储中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="35f33-116">Represents a calendar item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="35f33-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="35f33-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="35f33-118">代表定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="35f33-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="35f33-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="35f33-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="35f33-120">代表定期日历项目的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="35f33-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="35f33-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="35f33-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="35f33-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="35f33-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="35f33-123">匹配项</span><span class="sxs-lookup"><span data-stu-id="35f33-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="35f33-124">代表定期日历项目的一个已修改匹配项。</span><span class="sxs-lookup"><span data-stu-id="35f33-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35f33-125">文本值</span><span class="sxs-lookup"><span data-stu-id="35f33-125">Text value</span></span>

<span data-ttu-id="35f33-126">如果使用此元素，则需要表示日期和时间的文本值。</span><span class="sxs-lookup"><span data-stu-id="35f33-126">A text value that represents a date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35f33-127">备注</span><span class="sxs-lookup"><span data-stu-id="35f33-127">Remarks</span></span>

<span data-ttu-id="35f33-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35f33-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35f33-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="35f33-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35f33-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="35f33-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35f33-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="35f33-131">Schema Name</span></span>  <br/> |<span data-ttu-id="35f33-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="35f33-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="35f33-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="35f33-133">Validation File</span></span>  <br/> |<span data-ttu-id="35f33-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35f33-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35f33-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="35f33-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="35f33-136">False</span><span class="sxs-lookup"><span data-stu-id="35f33-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35f33-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35f33-137">See also</span></span>



- [<span data-ttu-id="35f33-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35f33-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

