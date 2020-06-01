---
title: 时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- When
api_type:
- schema
ms.assetid: c7df1333-a33d-4cc6-a08a-34b68843f47d
description: When 元素提供有关何时发生日历或会议项目的信息。
ms.openlocfilehash: 7c5f85184f966d909960bf1d79f5b8d33c67b51a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461854"
---
# <a name="when"></a><span data-ttu-id="da36d-103">时间</span><span class="sxs-lookup"><span data-stu-id="da36d-103">When</span></span>

<span data-ttu-id="da36d-104">**When**元素提供有关何时发生日历或会议项目的信息。</span><span class="sxs-lookup"><span data-stu-id="da36d-104">The **When** element provides information about when a calendar or meeting item occurs.</span></span> 
  
```xml
<When/>
```

 <span data-ttu-id="da36d-105">**String**</span><span class="sxs-lookup"><span data-stu-id="da36d-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da36d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da36d-106">Attributes and elements</span></span>

<span data-ttu-id="da36d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da36d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da36d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="da36d-108">Attributes</span></span>

<span data-ttu-id="da36d-109">无。</span><span class="sxs-lookup"><span data-stu-id="da36d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da36d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="da36d-110">Child elements</span></span>

<span data-ttu-id="da36d-111">无。</span><span class="sxs-lookup"><span data-stu-id="da36d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da36d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="da36d-112">Parent elements</span></span>

|<span data-ttu-id="da36d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="da36d-113">**Element**</span></span>|<span data-ttu-id="da36d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="da36d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da36d-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="da36d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="da36d-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="da36d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="da36d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="da36d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="da36d-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="da36d-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da36d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="da36d-119">Text value</span></span>

<span data-ttu-id="da36d-120">Text 值是一个描述日历项目何时发生的字符串。</span><span class="sxs-lookup"><span data-stu-id="da36d-120">The text value is a string that describes when a calendar item occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da36d-121">说明</span><span class="sxs-lookup"><span data-stu-id="da36d-121">Remarks</span></span>

<span data-ttu-id="da36d-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da36d-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da36d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="da36d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da36d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="da36d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da36d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="da36d-125">Schema name</span></span>  <br/> |<span data-ttu-id="da36d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="da36d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="da36d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="da36d-127">Validation file</span></span>  <br/> |<span data-ttu-id="da36d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da36d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da36d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="da36d-129">Can be empty</span></span>  <br/> |<span data-ttu-id="da36d-130">False</span><span class="sxs-lookup"><span data-stu-id="da36d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da36d-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da36d-131">See also</span></span>



- [<span data-ttu-id="da36d-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da36d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

