---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: FindPeople 元素指定一的组 FindPeople 请求中使用的数据。 将数据包含零个或多个以下元素： 个人形状 （可选）、 索引的页面项视图、 （可选） 限制、 聚合限制 （可选）、 排序顺序 （可选）、 父文件夹 Id 和 （可选） 查询字符串。
ms.openlocfilehash: 79c8a4324cd217232442b781c33223296d8015e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754357"
---
# <a name="findpeople"></a><span data-ttu-id="fe5e5-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="fe5e5-104">FindPeople</span></span>

<span data-ttu-id="fe5e5-105">**FindPeople**元素指定一的组 FindPeople 请求中使用的数据。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="fe5e5-106">将数据包含零个或多个以下元素： 个人形状 （可选）、 索引的页面项视图、 （可选） 限制、 聚合限制 （可选）、 排序顺序 （可选）、 父文件夹 Id 和 （可选） 查询字符串。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
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

 <span data-ttu-id="fe5e5-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="fe5e5-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe5e5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe5e5-108">Attributes and elements</span></span>

<span data-ttu-id="fe5e5-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe5e5-110">属性</span><span class="sxs-lookup"><span data-stu-id="fe5e5-110">Attributes</span></span>

<span data-ttu-id="fe5e5-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe5e5-112">子元素</span><span class="sxs-lookup"><span data-stu-id="fe5e5-112">Child elements</span></span>

<span data-ttu-id="fe5e5-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [限制](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [查询字符串 (QueryStringType)](querystring-querystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="fe5e5-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe5e5-114">父元素</span><span class="sxs-lookup"><span data-stu-id="fe5e5-114">Parent elements</span></span>

<span data-ttu-id="fe5e5-115">无。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe5e5-116">备注</span><span class="sxs-lookup"><span data-stu-id="fe5e5-116">Remarks</span></span>

<span data-ttu-id="fe5e5-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fe5e5-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe5e5-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe5e5-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe5e5-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe5e5-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe5e5-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe5e5-121">Schema name</span></span>  <br/> |<span data-ttu-id="fe5e5-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="fe5e5-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe5e5-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe5e5-123">Validation file</span></span>  <br/> |<span data-ttu-id="fe5e5-124">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fe5e5-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe5e5-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe5e5-125">Can be empty</span></span>  <br/> |<span data-ttu-id="fe5e5-126">false</span><span class="sxs-lookup"><span data-stu-id="fe5e5-126">false</span></span>  <br/> |
   

