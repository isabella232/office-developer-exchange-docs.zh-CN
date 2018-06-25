---
title: BlockStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08556ee9-0923-437c-99a4-bb630f04e973
description: BlockStatus 元素指定的项目的阻止状态。
ms.openlocfilehash: 5733738d733578c47b849b9d7c62c9b66cd8922e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753341"
---
# <a name="blockstatus"></a><span data-ttu-id="ceed9-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="ceed9-103">BlockStatus</span></span>

<span data-ttu-id="ceed9-104">**BlockStatus**元素指定的项目的阻止状态。</span><span class="sxs-lookup"><span data-stu-id="ceed9-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="ceed9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ceed9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ceed9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ceed9-106">Attributes and elements</span></span>

<span data-ttu-id="ceed9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ceed9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ceed9-108">属性</span><span class="sxs-lookup"><span data-stu-id="ceed9-108">Attributes</span></span>

<span data-ttu-id="ceed9-109">无。</span><span class="sxs-lookup"><span data-stu-id="ceed9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ceed9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ceed9-110">Child elements</span></span>

<span data-ttu-id="ceed9-111">无。</span><span class="sxs-lookup"><span data-stu-id="ceed9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ceed9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ceed9-112">Parent elements</span></span>

|<span data-ttu-id="ceed9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ceed9-113">**Element**</span></span>|<span data-ttu-id="ceed9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ceed9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ceed9-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="ceed9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ceed9-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="ceed9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ceed9-117">联系人</span><span class="sxs-lookup"><span data-stu-id="ceed9-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ceed9-118">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="ceed9-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ceed9-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ceed9-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ceed9-120">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ceed9-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ceed9-121">Item</span><span class="sxs-lookup"><span data-stu-id="ceed9-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="ceed9-122">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="ceed9-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ceed9-123">文本值</span><span class="sxs-lookup"><span data-stu-id="ceed9-123">Text value</span></span>

<span data-ttu-id="ceed9-124">文本值为**true** **BlockStatus**元素表示项目被阻止。</span><span class="sxs-lookup"><span data-stu-id="ceed9-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="ceed9-125">如果值为**false**指示项目不被阻止。</span><span class="sxs-lookup"><span data-stu-id="ceed9-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ceed9-126">备注</span><span class="sxs-lookup"><span data-stu-id="ceed9-126">Remarks</span></span>

<span data-ttu-id="ceed9-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ceed9-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ceed9-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ceed9-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ceed9-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="ceed9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ceed9-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="ceed9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ceed9-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="ceed9-131">Schema Name</span></span>  <br/> |<span data-ttu-id="ceed9-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="ceed9-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="ceed9-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="ceed9-133">Validation File</span></span>  <br/> |<span data-ttu-id="ceed9-134">types.xsd</span><span class="sxs-lookup"><span data-stu-id="ceed9-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ceed9-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="ceed9-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ceed9-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ceed9-136">See also</span></span>



- [<span data-ttu-id="ceed9-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ceed9-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

