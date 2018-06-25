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
description: IsAllDayEvent 元素指示日历项目或会议请求是否表示全天事件。
ms.openlocfilehash: 81cf1e7d8338275540f264de7cbf194005e7770c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825983"
---
# <a name="isalldayevent"></a><span data-ttu-id="3db60-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="3db60-103">IsAllDayEvent</span></span>

<span data-ttu-id="3db60-104">**IsAllDayEvent**元素指示日历项目或会议请求是否表示全天事件。</span><span class="sxs-lookup"><span data-stu-id="3db60-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="3db60-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3db60-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3db60-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3db60-106">Attributes and elements</span></span>

<span data-ttu-id="3db60-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3db60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3db60-108">属性</span><span class="sxs-lookup"><span data-stu-id="3db60-108">Attributes</span></span>

<span data-ttu-id="3db60-109">无。</span><span class="sxs-lookup"><span data-stu-id="3db60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3db60-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3db60-110">Child elements</span></span>

<span data-ttu-id="3db60-111">无。</span><span class="sxs-lookup"><span data-stu-id="3db60-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3db60-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3db60-112">Parent elements</span></span>

|<span data-ttu-id="3db60-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3db60-113">**Element**</span></span>|<span data-ttu-id="3db60-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3db60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3db60-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="3db60-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3db60-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="3db60-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3db60-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3db60-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3db60-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="3db60-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3db60-119">文本值</span><span class="sxs-lookup"><span data-stu-id="3db60-119">Text value</span></span>

<span data-ttu-id="3db60-120">如果此元素是包含，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="3db60-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="3db60-121">值为**true**指示该项表示全天事件。</span><span class="sxs-lookup"><span data-stu-id="3db60-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="3db60-122">如果值为**false**指示项目跨越小于用户的工作时间。</span><span class="sxs-lookup"><span data-stu-id="3db60-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3db60-123">注解</span><span class="sxs-lookup"><span data-stu-id="3db60-123">Remarks</span></span>

<span data-ttu-id="3db60-124">全天事件跨持续时间的工作时间内定义的邮箱。</span><span class="sxs-lookup"><span data-stu-id="3db60-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="3db60-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3db60-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3db60-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="3db60-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3db60-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="3db60-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3db60-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="3db60-128">Schema name</span></span>  <br/> |<span data-ttu-id="3db60-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="3db60-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="3db60-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="3db60-130">Validation file</span></span>  <br/> |<span data-ttu-id="3db60-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3db60-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3db60-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="3db60-132">Can be empty</span></span>  <br/> |<span data-ttu-id="3db60-133">False</span><span class="sxs-lookup"><span data-stu-id="3db60-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3db60-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3db60-134">See also</span></span>



- [<span data-ttu-id="3db60-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3db60-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

