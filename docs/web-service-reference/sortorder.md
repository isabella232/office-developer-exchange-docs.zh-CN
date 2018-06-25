---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: SortOrder 元素定义项 FindItem 或 FindConversation 请求中的排序方式。
ms.openlocfilehash: e20e5eab7972616c90079786abd78a0f7fedfebe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827519"
---
# <a name="sortorder"></a><span data-ttu-id="1d954-103">SortOrder</span><span class="sxs-lookup"><span data-stu-id="1d954-103">SortOrder</span></span>

<span data-ttu-id="1d954-104">**SortOrder**元素定义项**FindItem**或**FindConversation**请求中的排序方式。</span><span class="sxs-lookup"><span data-stu-id="1d954-104">The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request.</span></span> 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 <span data-ttu-id="1d954-105">**NonEmptyArrayOfFieldOrdersType**</span><span class="sxs-lookup"><span data-stu-id="1d954-105">**NonEmptyArrayOfFieldOrdersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d954-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d954-106">Attributes and elements</span></span>

<span data-ttu-id="1d954-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d954-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d954-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d954-108">Attributes</span></span>

<span data-ttu-id="1d954-109">无。</span><span class="sxs-lookup"><span data-stu-id="1d954-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d954-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1d954-110">Child elements</span></span>

|<span data-ttu-id="1d954-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d954-111">**Element**</span></span>|<span data-ttu-id="1d954-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d954-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d954-113">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="1d954-113">FieldOrder</span></span>](fieldorder.md) <br/> |<span data-ttu-id="1d954-114">代表用于对结果进行排序的单个字段，并指示排序的方向。</span><span class="sxs-lookup"><span data-stu-id="1d954-114">Represents a single field by which to sort results and indicates the direction for the sort.</span></span> <span data-ttu-id="1d954-115">可能包括一个或多个这些元素。</span><span class="sxs-lookup"><span data-stu-id="1d954-115">One or more of these elements may be included.</span></span> <span data-ttu-id="1d954-116">指定排序的顺序应用[FieldOrder](fieldorder.md)元素。</span><span class="sxs-lookup"><span data-stu-id="1d954-116">[FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d954-117">父元素</span><span class="sxs-lookup"><span data-stu-id="1d954-117">Parent elements</span></span>

|<span data-ttu-id="1d954-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d954-118">**Element**</span></span>|<span data-ttu-id="1d954-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d954-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d954-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="1d954-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="1d954-121">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="1d954-121">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="1d954-122">下面是此元素的 XPath 表达式:  `/FindItem`</span><span class="sxs-lookup"><span data-stu-id="1d954-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
|[<span data-ttu-id="1d954-123">FindConversation</span><span class="sxs-lookup"><span data-stu-id="1d954-123">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="1d954-124">定义查找邮箱中的对话的请求。</span><span class="sxs-lookup"><span data-stu-id="1d954-124">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d954-125">文本值</span><span class="sxs-lookup"><span data-stu-id="1d954-125">Text value</span></span>

<span data-ttu-id="1d954-126">无。</span><span class="sxs-lookup"><span data-stu-id="1d954-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d954-127">备注</span><span class="sxs-lookup"><span data-stu-id="1d954-127">Remarks</span></span>

<span data-ttu-id="1d954-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d954-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d954-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d954-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d954-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d954-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d954-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d954-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1d954-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="1d954-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d954-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d954-133">Validation File</span></span>  <br/> |<span data-ttu-id="1d954-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d954-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d954-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d954-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d954-136">False</span><span class="sxs-lookup"><span data-stu-id="1d954-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d954-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1d954-137">See also</span></span>



[<span data-ttu-id="1d954-138">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="1d954-138">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="1d954-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="1d954-139">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="1d954-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1d954-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

