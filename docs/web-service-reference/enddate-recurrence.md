---
title: 结束日期（定期）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDate
api_type:
- schema
ms.assetid: 16026595-26f8-4770-8a6d-0d3e4157effd
description: 结束日期元素表示定期任务或具有 EndDateRecurrence 模式类型的日历项目的结束日期。
ms.openlocfilehash: 53d9b04faf1d8f740c858080b5fcbeadf577df0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460160"
---
# <a name="enddate-recurrence"></a><span data-ttu-id="676d6-103">结束日期（定期）</span><span class="sxs-lookup"><span data-stu-id="676d6-103">EndDate (Recurrence)</span></span>

<span data-ttu-id="676d6-104">**结束**日期元素表示定期任务或具有 EndDateRecurrence 模式类型的日历项目的结束日期。</span><span class="sxs-lookup"><span data-stu-id="676d6-104">The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type.</span></span> 
  
```xml
<EndDate/>
```

 <span data-ttu-id="676d6-105">**date**</span><span class="sxs-lookup"><span data-stu-id="676d6-105">**date**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="676d6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="676d6-106">Attributes and elements</span></span>

<span data-ttu-id="676d6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="676d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="676d6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="676d6-108">Attributes</span></span>

<span data-ttu-id="676d6-109">无。</span><span class="sxs-lookup"><span data-stu-id="676d6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="676d6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="676d6-110">Child elements</span></span>

<span data-ttu-id="676d6-111">无。</span><span class="sxs-lookup"><span data-stu-id="676d6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="676d6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="676d6-112">Parent elements</span></span>

|<span data-ttu-id="676d6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="676d6-113">**Element**</span></span>|<span data-ttu-id="676d6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="676d6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="676d6-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="676d6-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="676d6-116">描述项目定期模式的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="676d6-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="676d6-117">文本值</span><span class="sxs-lookup"><span data-stu-id="676d6-117">Text value</span></span>

<span data-ttu-id="676d6-118">如果使用此元素，则表示日期的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="676d6-118">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="676d6-119">值不能大于 4500 00:00:00 的9月1日。</span><span class="sxs-lookup"><span data-stu-id="676d6-119">The value cannot be larger than September 1, 4500 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="676d6-120">说明</span><span class="sxs-lookup"><span data-stu-id="676d6-120">Remarks</span></span>

<span data-ttu-id="676d6-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="676d6-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="676d6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="676d6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="676d6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="676d6-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="676d6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="676d6-124">Schema name</span></span>  <br/> |<span data-ttu-id="676d6-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="676d6-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="676d6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="676d6-126">Validation file</span></span>  <br/> |<span data-ttu-id="676d6-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="676d6-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="676d6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="676d6-128">Can be empty</span></span>  <br/> |<span data-ttu-id="676d6-129">False</span><span class="sxs-lookup"><span data-stu-id="676d6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="676d6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="676d6-130">See also</span></span>



- [<span data-ttu-id="676d6-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="676d6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

