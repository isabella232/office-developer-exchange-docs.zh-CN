---
title: BlockStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08556ee9-0923-437c-99a4-bb630f04e973
description: BlockStatus 元素指定项目的块状态。
ms.openlocfilehash: e88236274bfa70216e872025c2a94231f837df1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462274"
---
# <a name="blockstatus"></a><span data-ttu-id="705c2-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="705c2-103">BlockStatus</span></span>

<span data-ttu-id="705c2-104">**BlockStatus**元素指定项目的块状态。</span><span class="sxs-lookup"><span data-stu-id="705c2-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="705c2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="705c2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="705c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="705c2-106">Attributes and elements</span></span>

<span data-ttu-id="705c2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="705c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="705c2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="705c2-108">Attributes</span></span>

<span data-ttu-id="705c2-109">无。</span><span class="sxs-lookup"><span data-stu-id="705c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="705c2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="705c2-110">Child elements</span></span>

<span data-ttu-id="705c2-111">无。</span><span class="sxs-lookup"><span data-stu-id="705c2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="705c2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="705c2-112">Parent elements</span></span>

|<span data-ttu-id="705c2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="705c2-113">**Element**</span></span>|<span data-ttu-id="705c2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="705c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="705c2-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="705c2-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="705c2-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="705c2-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="705c2-117">联系人</span><span class="sxs-lookup"><span data-stu-id="705c2-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="705c2-118">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="705c2-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="705c2-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="705c2-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="705c2-120">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="705c2-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="705c2-121">项</span><span class="sxs-lookup"><span data-stu-id="705c2-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="705c2-122">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="705c2-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="705c2-123">文本值</span><span class="sxs-lookup"><span data-stu-id="705c2-123">Text value</span></span>

<span data-ttu-id="705c2-124">如果**BlockStatus**元素的文本值为**true** ，则表示项目被阻止。</span><span class="sxs-lookup"><span data-stu-id="705c2-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="705c2-125">如果值为**false** ，则表示项目未被阻止。</span><span class="sxs-lookup"><span data-stu-id="705c2-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="705c2-126">备注</span><span class="sxs-lookup"><span data-stu-id="705c2-126">Remarks</span></span>

<span data-ttu-id="705c2-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="705c2-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="705c2-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="705c2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="705c2-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="705c2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="705c2-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="705c2-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="705c2-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="705c2-131">Schema Name</span></span>  <br/> |<span data-ttu-id="705c2-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="705c2-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="705c2-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="705c2-133">Validation File</span></span>  <br/> |<span data-ttu-id="705c2-134">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="705c2-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="705c2-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="705c2-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="705c2-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="705c2-136">See also</span></span>



- [<span data-ttu-id="705c2-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="705c2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

