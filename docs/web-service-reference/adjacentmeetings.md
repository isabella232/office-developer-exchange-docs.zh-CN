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
description: AdjacentMeetings 元素标识所有彼此相邻的会议时间的日历项目。
ms.openlocfilehash: 9ab818f4f67c32c01101cc595ccb92424a872ef0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753128"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="fca26-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="fca26-103">AdjacentMeetings</span></span>

<span data-ttu-id="fca26-104">**AdjacentMeetings**元素标识所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="fca26-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="fca26-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="fca26-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fca26-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fca26-106">Attributes and elements</span></span>

<span data-ttu-id="fca26-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fca26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fca26-108">属性</span><span class="sxs-lookup"><span data-stu-id="fca26-108">Attributes</span></span>

<span data-ttu-id="fca26-109">无。</span><span class="sxs-lookup"><span data-stu-id="fca26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fca26-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fca26-110">Child elements</span></span>

|<span data-ttu-id="fca26-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fca26-111">**Element**</span></span>|<span data-ttu-id="fca26-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fca26-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fca26-113">日历项目</span><span class="sxs-lookup"><span data-stu-id="fca26-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fca26-114">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fca26-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fca26-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fca26-115">Parent elements</span></span>

|<span data-ttu-id="fca26-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fca26-116">**Element**</span></span>|<span data-ttu-id="fca26-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fca26-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fca26-118">日历项目</span><span class="sxs-lookup"><span data-stu-id="fca26-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fca26-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fca26-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fca26-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fca26-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fca26-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="fca26-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fca26-122">注解</span><span class="sxs-lookup"><span data-stu-id="fca26-122">Remarks</span></span>

<span data-ttu-id="fca26-123">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fca26-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fca26-124">尽管其他子元素都有效每个架构，但的[日历项目](calendaritem.md)元素是 Exchange Web Services (EWS) 将返回**AdjacentMeetings**元素中的唯一子元素。</span><span class="sxs-lookup"><span data-stu-id="fca26-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="fca26-125">本主题不会列出的每个架构有效，但不是会通过 EWS 返回子元素。</span><span class="sxs-lookup"><span data-stu-id="fca26-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fca26-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="fca26-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fca26-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="fca26-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fca26-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="fca26-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fca26-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="fca26-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="fca26-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="fca26-130">Validation File</span></span>  <br/> |<span data-ttu-id="fca26-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fca26-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fca26-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="fca26-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fca26-133">False</span><span class="sxs-lookup"><span data-stu-id="fca26-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fca26-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fca26-134">See also</span></span>

- [<span data-ttu-id="fca26-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fca26-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

