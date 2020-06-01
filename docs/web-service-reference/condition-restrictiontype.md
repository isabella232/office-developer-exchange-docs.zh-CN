---
title: 条件（RestrictionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Condition 元素指定用于标识 FindItem 或 FindConversation 操作的搜索的结束的条件。
ms.openlocfilehash: 00c5b5e615ed9b253c79dae9dc2b89c797853089
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463935"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="dde1d-103">条件（RestrictionType）</span><span class="sxs-lookup"><span data-stu-id="dde1d-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="dde1d-104">**Condition**元素指定用于标识**FindItem**或**FindConversation**操作的搜索的结束的条件。</span><span class="sxs-lookup"><span data-stu-id="dde1d-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="dde1d-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="dde1d-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dde1d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dde1d-106">Attributes and elements</span></span>

<span data-ttu-id="dde1d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dde1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dde1d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dde1d-108">Attributes</span></span>

<span data-ttu-id="dde1d-109">无。</span><span class="sxs-lookup"><span data-stu-id="dde1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dde1d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dde1d-110">Child elements</span></span>

|<span data-ttu-id="dde1d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dde1d-111">**Element**</span></span>|<span data-ttu-id="dde1d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dde1d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dde1d-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="dde1d-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="dde1d-114">表示限制中的替代元素的抽象元素。</span><span class="sxs-lookup"><span data-stu-id="dde1d-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dde1d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="dde1d-115">Parent elements</span></span>

|<span data-ttu-id="dde1d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="dde1d-116">**Element**</span></span>|<span data-ttu-id="dde1d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="dde1d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dde1d-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="dde1d-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="dde1d-119">标识用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**操作的搜索说明。</span><span class="sxs-lookup"><span data-stu-id="dde1d-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dde1d-120">备注</span><span class="sxs-lookup"><span data-stu-id="dde1d-120">Remarks</span></span>

<span data-ttu-id="dde1d-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dde1d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dde1d-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dde1d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dde1d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="dde1d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dde1d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="dde1d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dde1d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="dde1d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="dde1d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="dde1d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="dde1d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="dde1d-127">Validation File</span></span>  <br/> |<span data-ttu-id="dde1d-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="dde1d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dde1d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="dde1d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dde1d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dde1d-130">See also</span></span>



- [<span data-ttu-id="dde1d-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dde1d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

