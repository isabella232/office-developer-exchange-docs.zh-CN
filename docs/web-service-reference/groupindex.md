---
title: GroupIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIndex
api_type:
- schema
ms.assetid: 7a596ff7-6cc3-4626-a52c-538a92202337
description: GroupIndex 元素表示用于对 FindItem 操作调用中当前项组的项进行分组的属性值。
ms.openlocfilehash: 05f303be92885a15dddf85c85251af04910d835c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530266"
---
# <a name="groupindex"></a><span data-ttu-id="a693e-103">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="a693e-103">GroupIndex</span></span>

<span data-ttu-id="a693e-104">**GroupIndex**元素表示用于对[FindItem 操作](finditem-operation.md)调用中当前项组的项进行分组的属性值。</span><span class="sxs-lookup"><span data-stu-id="a693e-104">The **GroupIndex** element represents the property value that is used to group items for the current group of items in a [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="a693e-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="a693e-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="a693e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a693e-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="a693e-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a693e-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="a693e-108">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="a693e-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="a693e-109">组</span><span class="sxs-lookup"><span data-stu-id="a693e-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="a693e-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="a693e-110">GroupedItems</span></span>](groupeditems.md)
  
[<span data-ttu-id="a693e-111">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="a693e-111">GroupIndex</span></span>](groupindex.md)
  
```xml
<GroupIndex/>
```

 <span data-ttu-id="a693e-112">**string**</span><span class="sxs-lookup"><span data-stu-id="a693e-112">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a693e-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a693e-113">Attributes and elements</span></span>

<span data-ttu-id="a693e-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a693e-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a693e-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="a693e-115">Attributes</span></span>

<span data-ttu-id="a693e-116">无。</span><span class="sxs-lookup"><span data-stu-id="a693e-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a693e-117">子元素</span><span class="sxs-lookup"><span data-stu-id="a693e-117">Child elements</span></span>

<span data-ttu-id="a693e-118">无。</span><span class="sxs-lookup"><span data-stu-id="a693e-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a693e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a693e-119">Parent elements</span></span>

|<span data-ttu-id="a693e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="a693e-120">**Element**</span></span>|<span data-ttu-id="a693e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a693e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a693e-122">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="a693e-122">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="a693e-123">表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。</span><span class="sxs-lookup"><span data-stu-id="a693e-123">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> <span data-ttu-id="a693e-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a693e-124">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a693e-125">文本值</span><span class="sxs-lookup"><span data-stu-id="a693e-125">Text value</span></span>

<span data-ttu-id="a693e-126">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="a693e-126">A text value is required.</span></span> <span data-ttu-id="a693e-127">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="a693e-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a693e-128">备注</span><span class="sxs-lookup"><span data-stu-id="a693e-128">Remarks</span></span>

<span data-ttu-id="a693e-129">此元素仅在[FindItem 操作](finditem-operation.md)响应中出现。</span><span class="sxs-lookup"><span data-stu-id="a693e-129">This element only occurs in a [FindItem operation](finditem-operation.md) response.</span></span> 
  
<span data-ttu-id="a693e-130">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a693e-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a693e-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="a693e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a693e-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="a693e-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a693e-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="a693e-133">Schema name</span></span>  <br/> |<span data-ttu-id="a693e-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="a693e-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="a693e-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="a693e-135">Validation file</span></span>  <br/> |<span data-ttu-id="a693e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a693e-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a693e-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="a693e-137">Can be empty</span></span>  <br/> |<span data-ttu-id="a693e-138">False</span><span class="sxs-lookup"><span data-stu-id="a693e-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a693e-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a693e-139">See also</span></span>



[<span data-ttu-id="a693e-140">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="a693e-140">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="a693e-141">查找项目</span><span class="sxs-lookup"><span data-stu-id="a693e-141">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

