---
title: ConflictingMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetings
api_type:
- schema
ms.assetid: cfff7a11-7b3a-4995-9815-afedd45ebb0f
description: ConflictingMeetings 元素标识与会议时间冲突的所有日历项目。
ms.openlocfilehash: dc897c9dc33117d379d89bb9bb41104ca02def1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460174"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="1af4a-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="1af4a-103">ConflictingMeetings</span></span>

<span data-ttu-id="1af4a-104">**ConflictingMeetings**元素标识与会议时间冲突的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="1af4a-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="1af4a-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="1af4a-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1af4a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1af4a-106">Attributes and elements</span></span>

<span data-ttu-id="1af4a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1af4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1af4a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1af4a-108">Attributes</span></span>

<span data-ttu-id="1af4a-109">无。</span><span class="sxs-lookup"><span data-stu-id="1af4a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1af4a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1af4a-110">Child elements</span></span>

|<span data-ttu-id="1af4a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1af4a-111">**Element**</span></span>|<span data-ttu-id="1af4a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1af4a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1af4a-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1af4a-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1af4a-114">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="1af4a-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1af4a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1af4a-115">Parent elements</span></span>

|<span data-ttu-id="1af4a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1af4a-116">**Element**</span></span>|<span data-ttu-id="1af4a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1af4a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1af4a-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1af4a-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1af4a-119">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="1af4a-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1af4a-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1af4a-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1af4a-121">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="1af4a-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1af4a-122">备注</span><span class="sxs-lookup"><span data-stu-id="1af4a-122">Remarks</span></span>

<span data-ttu-id="1af4a-123">如果使用此元素，则它必须包含一个或多个子元素。</span><span class="sxs-lookup"><span data-stu-id="1af4a-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="1af4a-124">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1af4a-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1af4a-125">[！注意] 根据架构，其他子元素是有效的，但[CalendarItem](calendaritem.md)元素是 Exchange Web 服务（EWS）将在**ConflictingMeetings**元素中返回的唯一子元素。</span><span class="sxs-lookup"><span data-stu-id="1af4a-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="1af4a-126">本主题不列出根据架构有效但不会由 EWS 返回的子元素。</span><span class="sxs-lookup"><span data-stu-id="1af4a-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1af4a-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="1af4a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1af4a-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="1af4a-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1af4a-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1af4a-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1af4a-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="1af4a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1af4a-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="1af4a-131">Validation File</span></span>  <br/> |<span data-ttu-id="1af4a-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1af4a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1af4a-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="1af4a-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1af4a-134">False</span><span class="sxs-lookup"><span data-stu-id="1af4a-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1af4a-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1af4a-135">See also</span></span>



- [<span data-ttu-id="1af4a-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1af4a-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

