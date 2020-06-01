---
title: StandardGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: StandardGroupBy 元素表示分组 FindItem 操作的标准分组和聚合机制。
ms.openlocfilehash: 3e135feba322979de3d66d5a45d423654ccc9100
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467555"
---
# <a name="standardgroupby"></a><span data-ttu-id="1aec3-103">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="1aec3-103">StandardGroupBy</span></span>

<span data-ttu-id="1aec3-104">**StandardGroupBy**元素表示分组 FindItem 操作的标准分组和聚合机制。</span><span class="sxs-lookup"><span data-stu-id="1aec3-104">The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span> 
  
[<span data-ttu-id="1aec3-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="1aec3-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="1aec3-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="1aec3-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
[<span data-ttu-id="1aec3-107">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="1aec3-107">StandardGroupBy</span></span>](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 <span data-ttu-id="1aec3-108">**StandardGroupByType**</span><span class="sxs-lookup"><span data-stu-id="1aec3-108">**StandardGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aec3-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1aec3-109">Attributes and elements</span></span>

<span data-ttu-id="1aec3-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1aec3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aec3-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="1aec3-111">Attributes</span></span>

<span data-ttu-id="1aec3-112">无。</span><span class="sxs-lookup"><span data-stu-id="1aec3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aec3-113">子元素</span><span class="sxs-lookup"><span data-stu-id="1aec3-113">Child elements</span></span>

<span data-ttu-id="1aec3-114">无。</span><span class="sxs-lookup"><span data-stu-id="1aec3-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1aec3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1aec3-115">Parent elements</span></span>

|<span data-ttu-id="1aec3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1aec3-116">**Element**</span></span>|<span data-ttu-id="1aec3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1aec3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aec3-118">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="1aec3-118">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="1aec3-119">提供 FindItem 查询的标准分组。</span><span class="sxs-lookup"><span data-stu-id="1aec3-119">Provides standard groupings for FindItem queries.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1aec3-120">文本值</span><span class="sxs-lookup"><span data-stu-id="1aec3-120">Text value</span></span>

<span data-ttu-id="1aec3-121">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="1aec3-121">A text value is required.</span></span> <span data-ttu-id="1aec3-122">可用于此元素的唯一值是**ConversationTopic**。</span><span class="sxs-lookup"><span data-stu-id="1aec3-122">The only value that can be used for this element is **ConversationTopic**.</span></span> <span data-ttu-id="1aec3-123">**ConversationTopic**按邮件分组： ConversationTopic 和项目合计： DateTimeReceived （最大值）。</span><span class="sxs-lookup"><span data-stu-id="1aec3-123">**ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum).</span></span> <span data-ttu-id="1aec3-124">有关聚合的详细信息，请参阅[AggregateOn](aggregateon.md)。</span><span class="sxs-lookup"><span data-stu-id="1aec3-124">For more information about aggregation, see [AggregateOn](aggregateon.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1aec3-125">说明</span><span class="sxs-lookup"><span data-stu-id="1aec3-125">Remarks</span></span>

<span data-ttu-id="1aec3-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1aec3-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aec3-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="1aec3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aec3-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="1aec3-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1aec3-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1aec3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1aec3-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="1aec3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1aec3-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="1aec3-131">Validation File</span></span>  <br/> |<span data-ttu-id="1aec3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1aec3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1aec3-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="1aec3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aec3-134">False</span><span class="sxs-lookup"><span data-stu-id="1aec3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aec3-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1aec3-135">See also</span></span>



[<span data-ttu-id="1aec3-136">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="1aec3-136">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="1aec3-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="1aec3-137">FindItem</span></span>](finditem.md)


[<span data-ttu-id="1aec3-138">查找项目</span><span class="sxs-lookup"><span data-stu-id="1aec3-138">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

