---
title: Exists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exists
api_type:
- schema
ms.assetid: 55d568bd-8dbc-4d50-b9d7-54b74a54d4b5
description: Exists 元素表示搜索表达式，如果某个项目上存在，则该表达式会返回 true。
ms.openlocfilehash: d30f4b505afcac32afbfeaf2289c964ba145668e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754194"
---
# <a name="exists"></a><span data-ttu-id="e1bb8-103">Exists</span><span class="sxs-lookup"><span data-stu-id="e1bb8-103">Exists</span></span>

<span data-ttu-id="e1bb8-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Exists** 元素表示搜索表达式，如果某个项目上存在，则该表达式会返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-104">The **Exists** element represents a search expression that returns **true** if the supplied property exists on an item.</span></span> 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 <span data-ttu-id="e1bb8-105">**ExistsType**</span><span class="sxs-lookup"><span data-stu-id="e1bb8-105">**ExistsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1bb8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e1bb8-106">Attributes and elements</span></span>

<span data-ttu-id="e1bb8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1bb8-108">属性</span><span class="sxs-lookup"><span data-stu-id="e1bb8-108">Attributes</span></span>

<span data-ttu-id="e1bb8-109">无。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1bb8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e1bb8-110">Child elements</span></span>

|<span data-ttu-id="e1bb8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1bb8-111">**Element**</span></span>|<span data-ttu-id="e1bb8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1bb8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1bb8-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e1bb8-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e1bb8-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e1bb8-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e1bb8-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e1bb8-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e1bb8-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e1bb8-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e1bb8-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-118">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1bb8-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e1bb8-119">Parent elements</span></span>

|<span data-ttu-id="e1bb8-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1bb8-120">**Element**</span></span>|<span data-ttu-id="e1bb8-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1bb8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1bb8-122">限制</span><span class="sxs-lookup"><span data-stu-id="e1bb8-122">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="e1bb8-123">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-123">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="e1bb8-124">not</span><span class="sxs-lookup"><span data-stu-id="e1bb8-124">Not</span></span>](not.md) <br/> |<span data-ttu-id="e1bb8-125">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-125">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="e1bb8-126">And</span><span class="sxs-lookup"><span data-stu-id="e1bb8-126">And</span></span>](and.md) <br/> |<span data-ttu-id="e1bb8-p101">表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。如果 And 中包含的搜索表达式为 **true**，则 And 操作的结果为 **true**。  </span><span class="sxs-lookup"><span data-stu-id="e1bb8-p101">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions. The result of the And operation is **true** if all the search expressions contained within the And are **true**.  </span></span><br/> |
|[<span data-ttu-id="e1bb8-129">或</span><span class="sxs-lookup"><span data-stu-id="e1bb8-129">Or</span></span>](or.md) <br/> |<span data-ttu-id="e1bb8-p102">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。如果其任何子级返回 [true](or.md)，则 **或** 将返回 **true**。  </span><span class="sxs-lookup"><span data-stu-id="e1bb8-p102">Represents a search expression that performs a logical OR on the search expression that it contains. [Or](or.md) will return **true** if any of its children return **true**.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1bb8-132">备注</span><span class="sxs-lookup"><span data-stu-id="e1bb8-132">Remarks</span></span>

<span data-ttu-id="e1bb8-133">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1bb8-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="e1bb8-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1bb8-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="e1bb8-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e1bb8-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="e1bb8-136">Schema Name</span></span>  <br/> |<span data-ttu-id="e1bb8-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="e1bb8-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="e1bb8-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="e1bb8-138">Validation File</span></span>  <br/> |<span data-ttu-id="e1bb8-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e1bb8-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e1bb8-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="e1bb8-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1bb8-141">False</span><span class="sxs-lookup"><span data-stu-id="e1bb8-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1bb8-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1bb8-142">See also</span></span>



- [<span data-ttu-id="e1bb8-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e1bb8-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

