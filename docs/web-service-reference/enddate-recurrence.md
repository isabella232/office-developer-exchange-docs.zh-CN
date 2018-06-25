---
title: EndDate （重复）
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
description: EndDate 元素均表示一个周期性任务或日历项目已 EndDateRecurrence 图案类型的结束日期。
ms.openlocfilehash: b8570a069fc0a2d05044a9c85ab2d5c39d70ccdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754105"
---
# <a name="enddate-recurrence"></a><span data-ttu-id="c056d-103">EndDate （重复）</span><span class="sxs-lookup"><span data-stu-id="c056d-103">EndDate (Recurrence)</span></span>

<span data-ttu-id="c056d-104">**EndDate**元素均表示一个周期性任务或日历项目已 EndDateRecurrence 图案类型的结束日期。</span><span class="sxs-lookup"><span data-stu-id="c056d-104">The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type.</span></span> 
  
```xml
<EndDate/>
```

 <span data-ttu-id="c056d-105">**日期**</span><span class="sxs-lookup"><span data-stu-id="c056d-105">**date**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c056d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c056d-106">Attributes and elements</span></span>

<span data-ttu-id="c056d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c056d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c056d-108">属性</span><span class="sxs-lookup"><span data-stu-id="c056d-108">Attributes</span></span>

<span data-ttu-id="c056d-109">无。</span><span class="sxs-lookup"><span data-stu-id="c056d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c056d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c056d-110">Child elements</span></span>

<span data-ttu-id="c056d-111">无。</span><span class="sxs-lookup"><span data-stu-id="c056d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c056d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c056d-112">Parent elements</span></span>

|<span data-ttu-id="c056d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c056d-113">**Element**</span></span>|<span data-ttu-id="c056d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c056d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c056d-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="c056d-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="c056d-116">介绍的开始日期和结束日期的项目定期模式。</span><span class="sxs-lookup"><span data-stu-id="c056d-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c056d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c056d-117">Text value</span></span>

<span data-ttu-id="c056d-118">如果使用此元素，则需要表示日期的文本值。</span><span class="sxs-lookup"><span data-stu-id="c056d-118">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="c056d-119">值不能大于 9 月 1 日，4500 00:00:00。</span><span class="sxs-lookup"><span data-stu-id="c056d-119">The value cannot be larger than September 1, 4500 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c056d-120">备注</span><span class="sxs-lookup"><span data-stu-id="c056d-120">Remarks</span></span>

<span data-ttu-id="c056d-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c056d-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c056d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="c056d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c056d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="c056d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c056d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="c056d-124">Schema name</span></span>  <br/> |<span data-ttu-id="c056d-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="c056d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c056d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="c056d-126">Validation file</span></span>  <br/> |<span data-ttu-id="c056d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c056d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c056d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="c056d-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c056d-129">False</span><span class="sxs-lookup"><span data-stu-id="c056d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c056d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c056d-130">See also</span></span>



- [<span data-ttu-id="c056d-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c056d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

