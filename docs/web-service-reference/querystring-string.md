---
title: 查询字符串 （字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: QueryString 元素指定一组值的匹配 FindPeople 操作请求中的查询字符串返回。 使用没有指定的查询字符串搜索返回从指定的文件夹的所有项。
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826935"
---
# <a name="querystring-string"></a><span data-ttu-id="2a804-104">查询字符串 （字符串）</span><span class="sxs-lookup"><span data-stu-id="2a804-104">QueryString (String)</span></span>

<span data-ttu-id="2a804-105">**QueryString**元素指定一组值的匹配[FindPeople 操作](findpeople-operation.md)请求中的查询字符串返回。</span><span class="sxs-lookup"><span data-stu-id="2a804-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="2a804-106">使用没有指定的**查询字符串**搜索返回从指定的文件夹的所有项。</span><span class="sxs-lookup"><span data-stu-id="2a804-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="2a804-107">**string**</span><span class="sxs-lookup"><span data-stu-id="2a804-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a804-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a804-108">Attributes and elements</span></span>

<span data-ttu-id="2a804-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a804-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a804-110">属性</span><span class="sxs-lookup"><span data-stu-id="2a804-110">Attributes</span></span>

<span data-ttu-id="2a804-111">无。</span><span class="sxs-lookup"><span data-stu-id="2a804-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a804-112">子元素</span><span class="sxs-lookup"><span data-stu-id="2a804-112">Child elements</span></span>

<span data-ttu-id="2a804-113">无。</span><span class="sxs-lookup"><span data-stu-id="2a804-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2a804-114">父元素</span><span class="sxs-lookup"><span data-stu-id="2a804-114">Parent elements</span></span>

|<span data-ttu-id="2a804-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a804-115">**Element**</span></span>|<span data-ttu-id="2a804-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a804-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a804-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="2a804-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="2a804-118">包含[FindPeople 操作](findpeople-operation.md)搜索参数。</span><span class="sxs-lookup"><span data-stu-id="2a804-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a804-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2a804-119">Text value</span></span>

<span data-ttu-id="2a804-120">**QueryString**文本值表示邮箱查询使用[高级查询语法 (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx)的子集。</span><span class="sxs-lookup"><span data-stu-id="2a804-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="2a804-121">有关此元素的语法的信息，请参阅[QueryString (QueryStringType)](querystring-querystringtype.md)。</span><span class="sxs-lookup"><span data-stu-id="2a804-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a804-122">备注</span><span class="sxs-lookup"><span data-stu-id="2a804-122">Remarks</span></span>

<span data-ttu-id="2a804-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2a804-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a804-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a804-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a804-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a804-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a804-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a804-126">Schema name</span></span>  <br/> |<span data-ttu-id="2a804-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="2a804-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a804-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a804-128">Validation file</span></span>  <br/> |<span data-ttu-id="2a804-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a804-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a804-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a804-130">Can be empty</span></span>  <br/> |<span data-ttu-id="2a804-131">False</span><span class="sxs-lookup"><span data-stu-id="2a804-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a804-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a804-132">See also</span></span>



[<span data-ttu-id="2a804-133">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="2a804-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="2a804-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2a804-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

