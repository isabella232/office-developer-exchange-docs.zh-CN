---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: CalendarItemType 元素表示日历项目的类型。
ms.openlocfilehash: 05e93b6db3ae574c03f6e43c5ebec2288edec3e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527192"
---
# <a name="calendaritemtype"></a><span data-ttu-id="e9f42-103">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="e9f42-103">CalendarItemType</span></span>

<span data-ttu-id="e9f42-104">**CalendarItemType**元素表示日历项目的类型。</span><span class="sxs-lookup"><span data-stu-id="e9f42-104">The **CalendarItemType** element represents the type of a calendar item.</span></span> 
  
```xml
<CalendarItemType/>
```

 <span data-ttu-id="e9f42-105">**CalendarItemTypeType**</span><span class="sxs-lookup"><span data-stu-id="e9f42-105">**CalendarItemTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9f42-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e9f42-106">Attributes and elements</span></span>

<span data-ttu-id="e9f42-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9f42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9f42-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e9f42-108">Attributes</span></span>

<span data-ttu-id="e9f42-109">无。</span><span class="sxs-lookup"><span data-stu-id="e9f42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9f42-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e9f42-110">Child elements</span></span>

<span data-ttu-id="e9f42-111">无。</span><span class="sxs-lookup"><span data-stu-id="e9f42-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9f42-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e9f42-112">Parent elements</span></span>

|<span data-ttu-id="e9f42-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9f42-113">**Element**</span></span>|<span data-ttu-id="e9f42-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9f42-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9f42-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e9f42-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e9f42-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="e9f42-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e9f42-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e9f42-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e9f42-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="e9f42-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9f42-119">文本值</span><span class="sxs-lookup"><span data-stu-id="e9f42-119">Text value</span></span>

<span data-ttu-id="e9f42-120">如果使用此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="e9f42-120">A text value is required if this element is used.</span></span> <span data-ttu-id="e9f42-121">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="e9f42-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="e9f42-122">**单一**项目不与定期日历项目相关联。</span><span class="sxs-lookup"><span data-stu-id="e9f42-122">**Single** The item is not associated with a recurring calendar item.</span></span> 
    
- <span data-ttu-id="e9f42-123">**事件**项目是定期日历项的发生。</span><span class="sxs-lookup"><span data-stu-id="e9f42-123">**Occurrence** The item is an occurrence of a recurring calendar item.</span></span> 
    
- <span data-ttu-id="e9f42-124">**异常**项目是定期日历项目的例外。</span><span class="sxs-lookup"><span data-stu-id="e9f42-124">**Exception** The item is an exception to a recurring calendar item.</span></span> 
    
- <span data-ttu-id="e9f42-125">**RecurringMaster**项目是一组定期日历项目的主控形状。</span><span class="sxs-lookup"><span data-stu-id="e9f42-125">**RecurringMaster** The item is master for a set of recurring calendar items.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e9f42-126">说明</span><span class="sxs-lookup"><span data-stu-id="e9f42-126">Remarks</span></span>

<span data-ttu-id="e9f42-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e9f42-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9f42-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="e9f42-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9f42-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="e9f42-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9f42-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="e9f42-130">Schema name</span></span>  <br/> |<span data-ttu-id="e9f42-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="e9f42-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9f42-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="e9f42-132">Validation file</span></span>  <br/> |<span data-ttu-id="e9f42-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9f42-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9f42-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="e9f42-134">Can be empty</span></span>  <br/> |<span data-ttu-id="e9f42-135">False</span><span class="sxs-lookup"><span data-stu-id="e9f42-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9f42-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9f42-136">See also</span></span>



- [<span data-ttu-id="e9f42-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e9f42-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

