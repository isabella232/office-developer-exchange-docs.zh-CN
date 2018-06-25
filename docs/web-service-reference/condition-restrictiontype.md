---
title: 条件 (RestrictionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Condition 元素指定用于标识的末尾搜索 FindItem 或 FindConversation 操作的条件。
ms.openlocfilehash: 513fc21be52a90698f1c292d6d20d7cdaab07371
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753472"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="302b3-103">条件 (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="302b3-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="302b3-104">**Condition**元素指定用于标识的末尾搜索**FindItem**或**FindConversation**操作的条件。</span><span class="sxs-lookup"><span data-stu-id="302b3-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="302b3-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="302b3-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="302b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="302b3-106">Attributes and elements</span></span>

<span data-ttu-id="302b3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="302b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="302b3-108">属性</span><span class="sxs-lookup"><span data-stu-id="302b3-108">Attributes</span></span>

<span data-ttu-id="302b3-109">无。</span><span class="sxs-lookup"><span data-stu-id="302b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="302b3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="302b3-110">Child elements</span></span>

|<span data-ttu-id="302b3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="302b3-111">**Element**</span></span>|<span data-ttu-id="302b3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="302b3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="302b3-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="302b3-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="302b3-114">代表限制中的替代的元素的抽象元素。</span><span class="sxs-lookup"><span data-stu-id="302b3-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="302b3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="302b3-115">Parent elements</span></span>

|<span data-ttu-id="302b3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="302b3-116">**Element**</span></span>|<span data-ttu-id="302b3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="302b3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="302b3-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="302b3-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="302b3-119">标识用于标识的末尾搜索、 搜索和返回，最大条目的搜索方向的起始索引**FindItem**或**FindConversation**操作的条件。</span><span class="sxs-lookup"><span data-stu-id="302b3-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="302b3-120">备注</span><span class="sxs-lookup"><span data-stu-id="302b3-120">Remarks</span></span>

<span data-ttu-id="302b3-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="302b3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="302b3-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="302b3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="302b3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="302b3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="302b3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="302b3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="302b3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="302b3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="302b3-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="302b3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="302b3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="302b3-127">Validation File</span></span>  <br/> |<span data-ttu-id="302b3-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="302b3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="302b3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="302b3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="302b3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="302b3-130">See also</span></span>



- [<span data-ttu-id="302b3-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="302b3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

