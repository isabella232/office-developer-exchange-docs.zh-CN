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
description: DistinguishedGroupBy 元素 FindItem 查询提供标准分组。
ms.openlocfilehash: 0635366447675bf28dedf3af4f7d76094ee5e0a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753955"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="77e3e-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="77e3e-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="77e3e-104">**DistinguishedGroupBy**元素 FindItem 查询提供标准分组。</span><span class="sxs-lookup"><span data-stu-id="77e3e-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="77e3e-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="77e3e-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="77e3e-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="77e3e-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="77e3e-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="77e3e-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77e3e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77e3e-108">Attributes and elements</span></span>

<span data-ttu-id="77e3e-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77e3e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77e3e-110">属性</span><span class="sxs-lookup"><span data-stu-id="77e3e-110">Attributes</span></span>

<span data-ttu-id="77e3e-111">无。</span><span class="sxs-lookup"><span data-stu-id="77e3e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77e3e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="77e3e-112">Child elements</span></span>

|<span data-ttu-id="77e3e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="77e3e-113">**Element**</span></span>|<span data-ttu-id="77e3e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="77e3e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77e3e-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="77e3e-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="77e3e-116">代表标准分组和聚合的组合 FindItem 操作的机制。</span><span class="sxs-lookup"><span data-stu-id="77e3e-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77e3e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="77e3e-117">Parent elements</span></span>

|<span data-ttu-id="77e3e-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="77e3e-118">**Element**</span></span>|<span data-ttu-id="77e3e-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="77e3e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77e3e-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="77e3e-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="77e3e-121">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="77e3e-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="77e3e-122">下面是此元素的 XPath 表达式:  `/FindItem`</span><span class="sxs-lookup"><span data-stu-id="77e3e-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77e3e-123">备注</span><span class="sxs-lookup"><span data-stu-id="77e3e-123">Remarks</span></span>

<span data-ttu-id="77e3e-124">**DistinguishedGroupBy**元素可以添加到 FindItem 操作时结果必须位于备份分组和时标准组之一满足分组。</span><span class="sxs-lookup"><span data-stu-id="77e3e-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="77e3e-125">如果**DistinguishedGroupBy**元素和[GroupBy](groupby.md)元素均未指定，结果将回来的 FindItem 取消组合。</span><span class="sxs-lookup"><span data-stu-id="77e3e-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="77e3e-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="77e3e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77e3e-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="77e3e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77e3e-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="77e3e-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="77e3e-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="77e3e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="77e3e-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="77e3e-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="77e3e-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="77e3e-131">Validation File</span></span>  <br/> |<span data-ttu-id="77e3e-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="77e3e-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="77e3e-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="77e3e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="77e3e-134">False</span><span class="sxs-lookup"><span data-stu-id="77e3e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77e3e-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77e3e-135">See also</span></span>

- [<span data-ttu-id="77e3e-136">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="77e3e-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="77e3e-137">查找项目</span><span class="sxs-lookup"><span data-stu-id="77e3e-137">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

