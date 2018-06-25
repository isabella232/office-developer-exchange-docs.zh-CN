---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: DeletedOccurrenceStateDefinition 指定已删除的匹配项的日历项目的状态。
ms.openlocfilehash: ad0434d604ee78ebf1905b60857929e1af4d45f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753796"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="0ef61-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="0ef61-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="0ef61-104">**DeletedOccurrenceStateDefinition**指定已删除的匹配项的日历项目的状态。</span><span class="sxs-lookup"><span data-stu-id="0ef61-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="0ef61-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="0ef61-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ef61-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0ef61-106">Attributes and elements</span></span>

<span data-ttu-id="0ef61-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ef61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ef61-108">属性</span><span class="sxs-lookup"><span data-stu-id="0ef61-108">Attributes</span></span>

<span data-ttu-id="0ef61-109">无。</span><span class="sxs-lookup"><span data-stu-id="0ef61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ef61-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0ef61-110">Child elements</span></span>

|<span data-ttu-id="0ef61-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ef61-111">**Element**</span></span>|<span data-ttu-id="0ef61-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ef61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ef61-113">出现 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="0ef61-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="0ef61-114">指定日历项的匹配项的日期。</span><span class="sxs-lookup"><span data-stu-id="0ef61-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0ef61-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="0ef61-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="0ef61-116">指定一个布尔值，该值指示是否存在日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="0ef61-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ef61-117">父元素</span><span class="sxs-lookup"><span data-stu-id="0ef61-117">Parent elements</span></span>

|<span data-ttu-id="0ef61-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ef61-118">**Element**</span></span>|<span data-ttu-id="0ef61-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ef61-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ef61-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="0ef61-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="0ef61-121">指定状态定义。</span><span class="sxs-lookup"><span data-stu-id="0ef61-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ef61-122">备注</span><span class="sxs-lookup"><span data-stu-id="0ef61-122">Remarks</span></span>

<span data-ttu-id="0ef61-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0ef61-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0ef61-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0ef61-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ef61-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="0ef61-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ef61-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="0ef61-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ef61-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="0ef61-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0ef61-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="0ef61-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="0ef61-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="0ef61-129">Validation File</span></span>  <br/> |<span data-ttu-id="0ef61-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="0ef61-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ef61-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="0ef61-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0ef61-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ef61-132">See also</span></span>

- [<span data-ttu-id="0ef61-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0ef61-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

