---
title: AdjacentMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdjacentMeetings
api_type:
- schema
ms.assetid: 50a9c381-9166-476e-8421-29e51b94499b
description: AdjacentMeetings 元素标识与会议时间相邻的所有日历项目。
ms.openlocfilehash: 7c89095e24af799df22a848be06a0fd65d53be7f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463578"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="dcdeb-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="dcdeb-103">AdjacentMeetings</span></span>

<span data-ttu-id="dcdeb-104">**AdjacentMeetings**元素标识与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="dcdeb-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="dcdeb-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dcdeb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dcdeb-106">Attributes and elements</span></span>

<span data-ttu-id="dcdeb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcdeb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dcdeb-108">Attributes</span></span>

<span data-ttu-id="dcdeb-109">无。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dcdeb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dcdeb-110">Child elements</span></span>

|<span data-ttu-id="dcdeb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dcdeb-111">**Element**</span></span>|<span data-ttu-id="dcdeb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dcdeb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcdeb-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="dcdeb-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="dcdeb-114">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dcdeb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="dcdeb-115">Parent elements</span></span>

|<span data-ttu-id="dcdeb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="dcdeb-116">**Element**</span></span>|<span data-ttu-id="dcdeb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="dcdeb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcdeb-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="dcdeb-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="dcdeb-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="dcdeb-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="dcdeb-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="dcdeb-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcdeb-122">备注</span><span class="sxs-lookup"><span data-stu-id="dcdeb-122">Remarks</span></span>

<span data-ttu-id="dcdeb-123">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dcdeb-124">[！注意] 根据架构，其他子元素是有效的，但[CalendarItem](calendaritem.md)元素是 Exchange Web 服务（EWS）将在**AdjacentMeetings**元素中返回的唯一子元素。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="dcdeb-125">本主题不列出根据架构有效但不会由 EWS 返回的子元素。</span><span class="sxs-lookup"><span data-stu-id="dcdeb-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="dcdeb-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="dcdeb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcdeb-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="dcdeb-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dcdeb-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="dcdeb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="dcdeb-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="dcdeb-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="dcdeb-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="dcdeb-130">Validation File</span></span>  <br/> |<span data-ttu-id="dcdeb-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dcdeb-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dcdeb-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="dcdeb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="dcdeb-133">False</span><span class="sxs-lookup"><span data-stu-id="dcdeb-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcdeb-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dcdeb-134">See also</span></span>

- [<span data-ttu-id="dcdeb-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dcdeb-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

