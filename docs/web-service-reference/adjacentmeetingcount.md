---
title: AdjacentMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdjacentMeetingCount
api_type:
- schema
ms.assetid: 35045024-f6e1-47d1-89be-f100b7b4f3c7
description: AdjacentMeetingCount 元素表示与会议时间相邻的日历项目的总数。
ms.openlocfilehash: 145010b345c3f9792a37c0662b87649b7f20a618
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463592"
---
# <a name="adjacentmeetingcount"></a><span data-ttu-id="48ade-103">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="48ade-103">AdjacentMeetingCount</span></span>

<span data-ttu-id="48ade-104">**AdjacentMeetingCount**元素表示与会议时间相邻的日历项目的总数。</span><span class="sxs-lookup"><span data-stu-id="48ade-104">The **AdjacentMeetingCount** element represents the total number of calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetingCount/>
```

 <span data-ttu-id="48ade-105">**Int**</span><span class="sxs-lookup"><span data-stu-id="48ade-105">**Int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48ade-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="48ade-106">Attributes and elements</span></span>

<span data-ttu-id="48ade-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="48ade-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48ade-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="48ade-108">Attributes</span></span>

<span data-ttu-id="48ade-109">无。</span><span class="sxs-lookup"><span data-stu-id="48ade-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48ade-110">子元素</span><span class="sxs-lookup"><span data-stu-id="48ade-110">Child elements</span></span>

<span data-ttu-id="48ade-111">无。</span><span class="sxs-lookup"><span data-stu-id="48ade-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48ade-112">父元素</span><span class="sxs-lookup"><span data-stu-id="48ade-112">Parent elements</span></span>

|<span data-ttu-id="48ade-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="48ade-113">**Element**</span></span>|<span data-ttu-id="48ade-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="48ade-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48ade-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="48ade-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="48ade-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="48ade-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="48ade-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="48ade-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="48ade-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="48ade-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="48ade-119">文本值</span><span class="sxs-lookup"><span data-stu-id="48ade-119">Text value</span></span>

<span data-ttu-id="48ade-120">需要表示整数的一个文本值。</span><span class="sxs-lookup"><span data-stu-id="48ade-120">A text value that represents an integer is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48ade-121">说明</span><span class="sxs-lookup"><span data-stu-id="48ade-121">Remarks</span></span>

<span data-ttu-id="48ade-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="48ade-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48ade-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="48ade-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48ade-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="48ade-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48ade-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="48ade-125">Schema name</span></span>  <br/> |<span data-ttu-id="48ade-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="48ade-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="48ade-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="48ade-127">Validation file</span></span>  <br/> |<span data-ttu-id="48ade-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48ade-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48ade-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="48ade-129">Can be empty</span></span>  <br/> |<span data-ttu-id="48ade-130">False</span><span class="sxs-lookup"><span data-stu-id="48ade-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48ade-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="48ade-131">See also</span></span>

- [<span data-ttu-id="48ade-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="48ade-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

