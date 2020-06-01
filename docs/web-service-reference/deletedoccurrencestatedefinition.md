---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: DeletedOccurrenceStateDefinition 指定日历项目的已删除事件的状态。
ms.openlocfilehash: ff8ad1d9c35d7bab3f6fe2cd1896bb16384c18e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458794"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="26055-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="26055-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="26055-104">**DeletedOccurrenceStateDefinition**指定日历项目的已删除事件的状态。</span><span class="sxs-lookup"><span data-stu-id="26055-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="26055-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="26055-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26055-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26055-106">Attributes and elements</span></span>

<span data-ttu-id="26055-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26055-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26055-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="26055-108">Attributes</span></span>

<span data-ttu-id="26055-109">无。</span><span class="sxs-lookup"><span data-stu-id="26055-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26055-110">子元素</span><span class="sxs-lookup"><span data-stu-id="26055-110">Child elements</span></span>

|<span data-ttu-id="26055-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="26055-111">**Element**</span></span>|<span data-ttu-id="26055-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="26055-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26055-113">事件（时区转换）</span><span class="sxs-lookup"><span data-stu-id="26055-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="26055-114">指定日历项的发生日期。</span><span class="sxs-lookup"><span data-stu-id="26055-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="26055-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="26055-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="26055-116">指定一个布尔值，该值指示是否存在日历项。</span><span class="sxs-lookup"><span data-stu-id="26055-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26055-117">父元素</span><span class="sxs-lookup"><span data-stu-id="26055-117">Parent elements</span></span>

|<span data-ttu-id="26055-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="26055-118">**Element**</span></span>|<span data-ttu-id="26055-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="26055-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26055-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="26055-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="26055-121">指定状态定义。</span><span class="sxs-lookup"><span data-stu-id="26055-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26055-122">备注</span><span class="sxs-lookup"><span data-stu-id="26055-122">Remarks</span></span>

<span data-ttu-id="26055-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="26055-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="26055-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="26055-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26055-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="26055-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26055-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="26055-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26055-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="26055-127">Schema Name</span></span>  <br/> |<span data-ttu-id="26055-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="26055-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="26055-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="26055-129">Validation File</span></span>  <br/> |<span data-ttu-id="26055-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="26055-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="26055-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="26055-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="26055-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26055-132">See also</span></span>

- [<span data-ttu-id="26055-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="26055-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

