---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: RecurringMasterItemIdRanges 元素指定发生的范围的数组。
ms.openlocfilehash: 784676844c5c58c65b8cc6177843bf26d351b7d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528753"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="979fd-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="979fd-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="979fd-104">**RecurringMasterItemIdRanges**元素指定发生的范围的数组。</span><span class="sxs-lookup"><span data-stu-id="979fd-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="979fd-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="979fd-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="979fd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="979fd-106">Attributes and elements</span></span>

<span data-ttu-id="979fd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="979fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="979fd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="979fd-108">Attributes</span></span>

|<span data-ttu-id="979fd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="979fd-109">**Attribute**</span></span>|<span data-ttu-id="979fd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="979fd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="979fd-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="979fd-111">**Id**</span></span> <br/> |<span data-ttu-id="979fd-112">**Id**属性的文本值是定期主项目的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="979fd-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="979fd-113">这是一个**字符串**值。</span><span class="sxs-lookup"><span data-stu-id="979fd-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="979fd-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="979fd-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="979fd-115">**ChangeKey**属性的文本值是定期主项目的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="979fd-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="979fd-116">这是一个**字符串**值。</span><span class="sxs-lookup"><span data-stu-id="979fd-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="979fd-117">子元素</span><span class="sxs-lookup"><span data-stu-id="979fd-117">Child elements</span></span>

[<span data-ttu-id="979fd-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="979fd-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="979fd-119">父元素</span><span class="sxs-lookup"><span data-stu-id="979fd-119">Parent elements</span></span>

<span data-ttu-id="979fd-120">[ItemIds](itemids.md)  | [GlobalItemIds](globalitemids.md)  | [DraftItemIds](draftitemids.md)  | [ContactIds](contactids.md)  | [Groupid](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="979fd-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="979fd-121">备注</span><span class="sxs-lookup"><span data-stu-id="979fd-121">Remarks</span></span>

<span data-ttu-id="979fd-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="979fd-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="979fd-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="979fd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="979fd-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="979fd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="979fd-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="979fd-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="979fd-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="979fd-126">Schema name</span></span>  <br/> |<span data-ttu-id="979fd-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="979fd-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="979fd-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="979fd-128">Validation file</span></span>  <br/> |<span data-ttu-id="979fd-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="979fd-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="979fd-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="979fd-130">Can be empty</span></span>  <br/> ||
   

