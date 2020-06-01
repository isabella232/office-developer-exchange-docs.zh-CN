---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: FindPeople 元素指定在 FindPeople 请求中使用的一组数据。 数据包含零个或多个以下元素：角色形状（可选）、索引的页面项目视图、限制（可选）、聚合限制（可选）、排序顺序（可选）、父文件夹 Id 和查询字符串（可选）。
ms.openlocfilehash: 4777601b7146ec857b5c79fa9d4ced59a7247889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462899"
---
# <a name="findpeople"></a><span data-ttu-id="16c12-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="16c12-104">FindPeople</span></span>

<span data-ttu-id="16c12-105">**FindPeople**元素指定在 FindPeople 请求中使用的一组数据。</span><span class="sxs-lookup"><span data-stu-id="16c12-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="16c12-106">数据包含零个或多个以下元素：角色形状（可选）、索引的页面项目视图、限制（可选）、聚合限制（可选）、排序顺序（可选）、父文件夹 Id 和查询字符串（可选）。</span><span class="sxs-lookup"><span data-stu-id="16c12-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
```XML
<FindPeople>
   <PersonaShape/>
   <IndexedPageItemView/>
   <Restriction/>
   <AggregationRestriction/>
   <SortOrder/>
   <ParentFolderId/>
   <QueryString/>
</FindPeople>
```

 <span data-ttu-id="16c12-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="16c12-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16c12-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="16c12-108">Attributes and elements</span></span>

<span data-ttu-id="16c12-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="16c12-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16c12-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="16c12-110">Attributes</span></span>

<span data-ttu-id="16c12-111">无。</span><span class="sxs-lookup"><span data-stu-id="16c12-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16c12-112">子元素</span><span class="sxs-lookup"><span data-stu-id="16c12-112">Child elements</span></span>

<span data-ttu-id="16c12-113">[PersonaShape](personashape.md)  | [IndexedPageItemView](indexedpageitemview.md)  | [限制](restriction.md)  | [AggregationRestriction](aggregationrestriction.md)  | [SortOrder](sortorder.md)  | [ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)  | [QueryString （QueryStringType）](querystring-querystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="16c12-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="16c12-114">父元素</span><span class="sxs-lookup"><span data-stu-id="16c12-114">Parent elements</span></span>

<span data-ttu-id="16c12-115">无。</span><span class="sxs-lookup"><span data-stu-id="16c12-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16c12-116">说明</span><span class="sxs-lookup"><span data-stu-id="16c12-116">Remarks</span></span>

<span data-ttu-id="16c12-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16c12-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="16c12-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="16c12-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16c12-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="16c12-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16c12-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="16c12-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="16c12-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="16c12-121">Schema name</span></span>  <br/> |<span data-ttu-id="16c12-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="16c12-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="16c12-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="16c12-123">Validation file</span></span>  <br/> |<span data-ttu-id="16c12-124">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="16c12-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="16c12-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="16c12-125">Can be empty</span></span>  <br/> |<span data-ttu-id="16c12-126">false</span><span class="sxs-lookup"><span data-stu-id="16c12-126">false</span></span>  <br/> |
   

