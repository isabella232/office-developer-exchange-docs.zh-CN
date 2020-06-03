---
title: DistinguishedGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedGroupBy
api_type:
- schema
ms.assetid: 6ff3ac48-02ba-40ec-a71b-c401bb2b127c
description: DistinguishedGroupBy 元素提供了 FindItem 查询的标准分组。
ms.openlocfilehash: 004613d55419a19f69e960203ae13d8d906b74c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463137"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="e2bd6-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="e2bd6-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="e2bd6-104">**DistinguishedGroupBy**元素提供了 FindItem 查询的标准分组。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="e2bd6-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="e2bd6-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="e2bd6-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="e2bd6-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="e2bd6-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="e2bd6-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2bd6-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2bd6-108">Attributes and elements</span></span>

<span data-ttu-id="e2bd6-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2bd6-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="e2bd6-110">Attributes</span></span>

<span data-ttu-id="e2bd6-111">无。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2bd6-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e2bd6-112">Child elements</span></span>

|<span data-ttu-id="e2bd6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2bd6-113">**Element**</span></span>|<span data-ttu-id="e2bd6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2bd6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2bd6-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="e2bd6-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="e2bd6-116">表示分组的 FindItem 操作的标准分组和聚合机制。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2bd6-117">父元素</span><span class="sxs-lookup"><span data-stu-id="e2bd6-117">Parent elements</span></span>

|<span data-ttu-id="e2bd6-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2bd6-118">**Element**</span></span>|<span data-ttu-id="e2bd6-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2bd6-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2bd6-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="e2bd6-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e2bd6-121">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="e2bd6-122">下面是此元素的 XPath 表达式:  `/FindItem`</span><span class="sxs-lookup"><span data-stu-id="e2bd6-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2bd6-123">备注</span><span class="sxs-lookup"><span data-stu-id="e2bd6-123">Remarks</span></span>

<span data-ttu-id="e2bd6-124">当必须对结果进行分组并在其中一个标准组满足分组要求时，可以将**DistinguishedGroupBy**元素添加到 FindItem 操作中。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="e2bd6-125">如果**DistinguishedGroupBy**元素和[GroupBy](groupby.md)元素都未指定，则 FindItem 结果将被取消组合。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="e2bd6-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e2bd6-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2bd6-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="e2bd6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2bd6-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="e2bd6-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e2bd6-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e2bd6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e2bd6-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="e2bd6-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e2bd6-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e2bd6-131">Validation File</span></span>  <br/> |<span data-ttu-id="e2bd6-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e2bd6-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2bd6-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e2bd6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2bd6-134">False</span><span class="sxs-lookup"><span data-stu-id="e2bd6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2bd6-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2bd6-135">See also</span></span>

- [<span data-ttu-id="e2bd6-136">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="e2bd6-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="e2bd6-137">查找项目</span><span class="sxs-lookup"><span data-stu-id="e2bd6-137">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

