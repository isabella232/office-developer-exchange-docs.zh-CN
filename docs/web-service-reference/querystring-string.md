---
title: QueryString （String）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: QueryString 元素指定要返回的一组要返回的值，这些值与 FindPeople 操作请求中的查询字符串相匹配。 未指定 QueryString 的搜索将返回指定文件夹中的所有项目。
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465322"
---
# <a name="querystring-string"></a><span data-ttu-id="38305-104">QueryString （String）</span><span class="sxs-lookup"><span data-stu-id="38305-104">QueryString (String)</span></span>

<span data-ttu-id="38305-105">**QueryString**元素指定要返回的一组要返回的值，这些值与[FindPeople 操作](findpeople-operation.md)请求中的查询字符串相匹配。</span><span class="sxs-lookup"><span data-stu-id="38305-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="38305-106">未指定**QueryString**的搜索将返回指定文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="38305-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="38305-107">**string**</span><span class="sxs-lookup"><span data-stu-id="38305-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38305-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="38305-108">Attributes and elements</span></span>

<span data-ttu-id="38305-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="38305-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38305-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="38305-110">Attributes</span></span>

<span data-ttu-id="38305-111">无。</span><span class="sxs-lookup"><span data-stu-id="38305-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38305-112">子元素</span><span class="sxs-lookup"><span data-stu-id="38305-112">Child elements</span></span>

<span data-ttu-id="38305-113">无。</span><span class="sxs-lookup"><span data-stu-id="38305-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38305-114">父元素</span><span class="sxs-lookup"><span data-stu-id="38305-114">Parent elements</span></span>

|<span data-ttu-id="38305-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="38305-115">**Element**</span></span>|<span data-ttu-id="38305-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="38305-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38305-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="38305-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="38305-118">包含[FindPeople 操作](findpeople-operation.md)搜索的参数。</span><span class="sxs-lookup"><span data-stu-id="38305-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38305-119">文本值</span><span class="sxs-lookup"><span data-stu-id="38305-119">Text value</span></span>

<span data-ttu-id="38305-120">**QueryString** text 值代表使用[高级查询语法（AQS）](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)的子集进行的邮箱查询。</span><span class="sxs-lookup"><span data-stu-id="38305-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="38305-121">有关此元素的语法的信息，请参阅[QueryString （QueryStringType）](querystring-querystringtype.md)。</span><span class="sxs-lookup"><span data-stu-id="38305-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38305-122">备注</span><span class="sxs-lookup"><span data-stu-id="38305-122">Remarks</span></span>

<span data-ttu-id="38305-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="38305-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38305-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="38305-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38305-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="38305-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38305-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="38305-126">Schema name</span></span>  <br/> |<span data-ttu-id="38305-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="38305-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="38305-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="38305-128">Validation file</span></span>  <br/> |<span data-ttu-id="38305-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="38305-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38305-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="38305-130">Can be empty</span></span>  <br/> |<span data-ttu-id="38305-131">False</span><span class="sxs-lookup"><span data-stu-id="38305-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38305-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38305-132">See also</span></span>



[<span data-ttu-id="38305-133">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="38305-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="38305-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="38305-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

