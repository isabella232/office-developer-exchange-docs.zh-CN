---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: RecurringMasterItemIdRanges 元素指定出现范围的数组。
ms.openlocfilehash: 60d987f475bed5d630a1238550e4d14578ebd0d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827016"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="d8dd0-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="d8dd0-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="d8dd0-104">**RecurringMasterItemIdRanges**元素指定出现范围的数组。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="d8dd0-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="d8dd0-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8dd0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d8dd0-106">Attributes and elements</span></span>

<span data-ttu-id="d8dd0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8dd0-108">属性</span><span class="sxs-lookup"><span data-stu-id="d8dd0-108">Attributes</span></span>

|<span data-ttu-id="d8dd0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d8dd0-109">**Attribute**</span></span>|<span data-ttu-id="d8dd0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8dd0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8dd0-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="d8dd0-111">**Id**</span></span> <br/> |<span data-ttu-id="d8dd0-112">**Id**属性的文本值是定期主项目的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="d8dd0-113">这是一个**string**值。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="d8dd0-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="d8dd0-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="d8dd0-115">**更改密钥**属性的文本值是定期主项目更改密钥。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="d8dd0-116">这是一个**string**值。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8dd0-117">子元素</span><span class="sxs-lookup"><span data-stu-id="d8dd0-117">Child elements</span></span>

[<span data-ttu-id="d8dd0-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="d8dd0-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="d8dd0-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d8dd0-119">Parent elements</span></span>

<span data-ttu-id="d8dd0-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="d8dd0-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8dd0-121">备注</span><span class="sxs-lookup"><span data-stu-id="d8dd0-121">Remarks</span></span>

<span data-ttu-id="d8dd0-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d8dd0-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d8dd0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8dd0-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d8dd0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8dd0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d8dd0-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8dd0-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d8dd0-126">Schema name</span></span>  <br/> |<span data-ttu-id="d8dd0-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="d8dd0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8dd0-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d8dd0-128">Validation file</span></span>  <br/> |<span data-ttu-id="d8dd0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d8dd0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8dd0-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d8dd0-130">Can be empty</span></span>  <br/> ||
   

