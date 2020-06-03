---
title: IsAllDayEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAllDayEvent
api_type:
- schema
ms.assetid: 29140a64-9d7a-4a14-a10d-c98197c9831b
description: IsAllDayEvent 元素指示 calendar 项目或会议请求是否代表全天事件。
ms.openlocfilehash: f0c975deecf96e94599a47ef2c33e54a7d1a80b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526534"
---
# <a name="isalldayevent"></a><span data-ttu-id="2f7ff-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="2f7ff-103">IsAllDayEvent</span></span>

<span data-ttu-id="2f7ff-104">**IsAllDayEvent**元素指示 calendar 项目或会议请求是否代表全天事件。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="2f7ff-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f7ff-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f7ff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f7ff-106">Attributes and elements</span></span>

<span data-ttu-id="2f7ff-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f7ff-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f7ff-108">Attributes</span></span>

<span data-ttu-id="2f7ff-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f7ff-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f7ff-110">Child elements</span></span>

<span data-ttu-id="2f7ff-111">无。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f7ff-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2f7ff-112">Parent elements</span></span>

|<span data-ttu-id="2f7ff-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f7ff-113">**Element**</span></span>|<span data-ttu-id="2f7ff-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f7ff-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f7ff-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="2f7ff-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2f7ff-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="2f7ff-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2f7ff-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2f7ff-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f7ff-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2f7ff-119">Text value</span></span>

<span data-ttu-id="2f7ff-120">如果包含此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="2f7ff-121">**如果值为 true** ，则表示项目表示全天事件。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="2f7ff-122">**如果值为 false** ，则表示项的范围少于用户的工作时间。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2f7ff-123">备注</span><span class="sxs-lookup"><span data-stu-id="2f7ff-123">Remarks</span></span>

<span data-ttu-id="2f7ff-124">全天事件会跨越为邮箱定义的工作时间的持续时间。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="2f7ff-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f7ff-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f7ff-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f7ff-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f7ff-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f7ff-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f7ff-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f7ff-128">Schema name</span></span>  <br/> |<span data-ttu-id="2f7ff-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f7ff-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f7ff-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f7ff-130">Validation file</span></span>  <br/> |<span data-ttu-id="2f7ff-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f7ff-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f7ff-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f7ff-132">Can be empty</span></span>  <br/> |<span data-ttu-id="2f7ff-133">False</span><span class="sxs-lookup"><span data-stu-id="2f7ff-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f7ff-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f7ff-134">See also</span></span>



- [<span data-ttu-id="2f7ff-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f7ff-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

