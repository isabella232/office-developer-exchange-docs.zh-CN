---
title: 起始日期（定期）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: 起始日期元素表示定期任务或日历项目的开始日期。
ms.openlocfilehash: 4514f126b1de31c64a2650b9e7cb6b7412a726c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457205"
---
# <a name="startdate-recurrence"></a><span data-ttu-id="09a89-103">起始日期（定期）</span><span class="sxs-lookup"><span data-stu-id="09a89-103">StartDate (Recurrence)</span></span>

<span data-ttu-id="09a89-104">**起始**日期元素表示定期任务或日历项目的开始日期。</span><span class="sxs-lookup"><span data-stu-id="09a89-104">The **StartDate** element represents the start date of a recurring task or calendar item.</span></span> 
  
```xml
<StartDate/>
```

<span data-ttu-id="09a89-105">**Date**</span><span class="sxs-lookup"><span data-stu-id="09a89-105">**Date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="09a89-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="09a89-106">Attributes and elements</span></span>

<span data-ttu-id="09a89-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="09a89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09a89-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="09a89-108">Attributes</span></span>

<span data-ttu-id="09a89-109">无。</span><span class="sxs-lookup"><span data-stu-id="09a89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09a89-110">子元素</span><span class="sxs-lookup"><span data-stu-id="09a89-110">Child elements</span></span>

<span data-ttu-id="09a89-111">无。</span><span class="sxs-lookup"><span data-stu-id="09a89-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09a89-112">父元素</span><span class="sxs-lookup"><span data-stu-id="09a89-112">Parent elements</span></span>

|<span data-ttu-id="09a89-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="09a89-113">**Element**</span></span>|<span data-ttu-id="09a89-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="09a89-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09a89-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="09a89-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="09a89-116">描述项目定期模式的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="09a89-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="09a89-117">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="09a89-117">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="09a89-118">描述不具有定义的结束日期的项目定期模式的开始日期。</span><span class="sxs-lookup"><span data-stu-id="09a89-118">Describes the start date of an item recurrence pattern that does not have a defined end date.</span></span>  <br/> |
|[<span data-ttu-id="09a89-119">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="09a89-119">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="09a89-120">描述定期项目的开始日期和发生次数。</span><span class="sxs-lookup"><span data-stu-id="09a89-120">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09a89-121">文本值</span><span class="sxs-lookup"><span data-stu-id="09a89-121">Text value</span></span>

<span data-ttu-id="09a89-122">如果使用此元素，则表示日期的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="09a89-122">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="09a89-123">值不能小于 Apr、1、1601 00:00:00。</span><span class="sxs-lookup"><span data-stu-id="09a89-123">The value cannot be less than Apr, 1, 1601 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09a89-124">说明</span><span class="sxs-lookup"><span data-stu-id="09a89-124">Remarks</span></span>

<span data-ttu-id="09a89-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="09a89-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09a89-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="09a89-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09a89-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="09a89-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09a89-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="09a89-128">Schema name</span></span>  <br/> |<span data-ttu-id="09a89-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="09a89-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="09a89-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="09a89-130">Validation file</span></span>  <br/> |<span data-ttu-id="09a89-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09a89-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09a89-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="09a89-132">Can be empty</span></span>  <br/> |<span data-ttu-id="09a89-133">False</span><span class="sxs-lookup"><span data-stu-id="09a89-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09a89-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09a89-134">See also</span></span>

- [<span data-ttu-id="09a89-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="09a89-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

