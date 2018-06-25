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
description: StandardGroupBy 元素均表示标准分组和聚合的组合 FindItem 操作的机制。
ms.openlocfilehash: 8e2ec72a79ebafc2e5757d6dcebb27c0c53ec0b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827542"
---
# <a name="standardgroupby"></a><span data-ttu-id="89278-103">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="89278-103">StandardGroupBy</span></span>

<span data-ttu-id="89278-104">**StandardGroupBy**元素均表示标准分组和聚合的组合 FindItem 操作的机制。</span><span class="sxs-lookup"><span data-stu-id="89278-104">The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span> 
  
[<span data-ttu-id="89278-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="89278-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="89278-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="89278-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
[<span data-ttu-id="89278-107">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="89278-107">StandardGroupBy</span></span>](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 <span data-ttu-id="89278-108">**StandardGroupByType**</span><span class="sxs-lookup"><span data-stu-id="89278-108">**StandardGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89278-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89278-109">Attributes and elements</span></span>

<span data-ttu-id="89278-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89278-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89278-111">属性</span><span class="sxs-lookup"><span data-stu-id="89278-111">Attributes</span></span>

<span data-ttu-id="89278-112">无。</span><span class="sxs-lookup"><span data-stu-id="89278-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89278-113">子元素</span><span class="sxs-lookup"><span data-stu-id="89278-113">Child elements</span></span>

<span data-ttu-id="89278-114">无。</span><span class="sxs-lookup"><span data-stu-id="89278-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89278-115">父元素</span><span class="sxs-lookup"><span data-stu-id="89278-115">Parent elements</span></span>

|<span data-ttu-id="89278-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="89278-116">**Element**</span></span>|<span data-ttu-id="89278-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="89278-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89278-118">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="89278-118">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="89278-119">提供用于 FindItem 查询标准分组。</span><span class="sxs-lookup"><span data-stu-id="89278-119">Provides standard groupings for FindItem queries.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89278-120">文本值</span><span class="sxs-lookup"><span data-stu-id="89278-120">Text value</span></span>

<span data-ttu-id="89278-121">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="89278-121">A text value is required.</span></span> <span data-ttu-id="89278-122">**ConversationTopic**唯一可用于此元素的值。</span><span class="sxs-lookup"><span data-stu-id="89278-122">The only value that can be used for this element is **ConversationTopic**.</span></span> <span data-ttu-id="89278-123">消息： ConversationTopic 和项目： DateTimeReceived （最多） 上的聚合**ConversationTopic**组。</span><span class="sxs-lookup"><span data-stu-id="89278-123">**ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum).</span></span> <span data-ttu-id="89278-124">有关聚合的详细信息，请参阅[AggregateOn](aggregateon.md)。</span><span class="sxs-lookup"><span data-stu-id="89278-124">For more information about aggregation, see [AggregateOn](aggregateon.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89278-125">备注</span><span class="sxs-lookup"><span data-stu-id="89278-125">Remarks</span></span>

<span data-ttu-id="89278-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="89278-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89278-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="89278-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89278-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="89278-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89278-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="89278-129">Schema Name</span></span>  <br/> |<span data-ttu-id="89278-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="89278-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="89278-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="89278-131">Validation File</span></span>  <br/> |<span data-ttu-id="89278-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89278-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89278-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="89278-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="89278-134">False</span><span class="sxs-lookup"><span data-stu-id="89278-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89278-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89278-135">See also</span></span>



[<span data-ttu-id="89278-136">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="89278-136">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="89278-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="89278-137">FindItem</span></span>](finditem.md)


[<span data-ttu-id="89278-138">查找项目</span><span class="sxs-lookup"><span data-stu-id="89278-138">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

