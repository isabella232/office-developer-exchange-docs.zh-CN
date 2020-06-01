---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: IsAssignmentEditable 元素表示任务类型。
ms.openlocfilehash: 5eb091b24e2c97f7aa6072044fed998b6c9c1651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468052"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="91e5e-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="91e5e-103">IsAssignmentEditable</span></span>

<span data-ttu-id="91e5e-104">**IsAssignmentEditable**元素表示任务类型。</span><span class="sxs-lookup"><span data-stu-id="91e5e-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="91e5e-105">**整除**</span><span class="sxs-lookup"><span data-stu-id="91e5e-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91e5e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91e5e-106">Attributes and elements</span></span>

<span data-ttu-id="91e5e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91e5e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91e5e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="91e5e-108">Attributes</span></span>

<span data-ttu-id="91e5e-109">无。</span><span class="sxs-lookup"><span data-stu-id="91e5e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91e5e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="91e5e-110">Child elements</span></span>

<span data-ttu-id="91e5e-111">无。</span><span class="sxs-lookup"><span data-stu-id="91e5e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91e5e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="91e5e-112">Parent elements</span></span>

|<span data-ttu-id="91e5e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="91e5e-113">**Element**</span></span>|<span data-ttu-id="91e5e-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="91e5e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91e5e-115">任务</span><span class="sxs-lookup"><span data-stu-id="91e5e-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="91e5e-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="91e5e-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91e5e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="91e5e-117">Text value</span></span>

<span data-ttu-id="91e5e-118">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="91e5e-118">This property is read-only.</span></span> <span data-ttu-id="91e5e-119">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="91e5e-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="91e5e-120">**值**</span><span class="sxs-lookup"><span data-stu-id="91e5e-120">**Value**</span></span>|<span data-ttu-id="91e5e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="91e5e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91e5e-122">0</span><span class="sxs-lookup"><span data-stu-id="91e5e-122">0</span></span>  <br/> |<span data-ttu-id="91e5e-123">所有任务项目的默认值。</span><span class="sxs-lookup"><span data-stu-id="91e5e-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="91e5e-124">1 </span><span class="sxs-lookup"><span data-stu-id="91e5e-124">1</span></span>  <br/> |<span data-ttu-id="91e5e-125">任务要求。</span><span class="sxs-lookup"><span data-stu-id="91e5e-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="91e5e-126">双面</span><span class="sxs-lookup"><span data-stu-id="91e5e-126">2</span></span>  <br/> |<span data-ttu-id="91e5e-127">从任务请求的收件人接受任务。</span><span class="sxs-lookup"><span data-stu-id="91e5e-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="91e5e-128">第三章</span><span class="sxs-lookup"><span data-stu-id="91e5e-128">3</span></span>  <br/> |<span data-ttu-id="91e5e-129">从任务请求的收件人 declination 的任务。</span><span class="sxs-lookup"><span data-stu-id="91e5e-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="91e5e-130">4 </span><span class="sxs-lookup"><span data-stu-id="91e5e-130">4</span></span>  <br/> |<span data-ttu-id="91e5e-131">对上一个任务请求的更新。</span><span class="sxs-lookup"><span data-stu-id="91e5e-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="91e5e-132">5 </span><span class="sxs-lookup"><span data-stu-id="91e5e-132">5</span></span>  <br/> |<span data-ttu-id="91e5e-133">未使用。</span><span class="sxs-lookup"><span data-stu-id="91e5e-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91e5e-134">说明</span><span class="sxs-lookup"><span data-stu-id="91e5e-134">Remarks</span></span>

<span data-ttu-id="91e5e-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91e5e-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91e5e-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="91e5e-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91e5e-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="91e5e-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91e5e-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="91e5e-138">Schema Name</span></span>  <br/> |<span data-ttu-id="91e5e-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="91e5e-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="91e5e-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="91e5e-140">Validation File</span></span>  <br/> |<span data-ttu-id="91e5e-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91e5e-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91e5e-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="91e5e-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="91e5e-143">False</span><span class="sxs-lookup"><span data-stu-id="91e5e-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91e5e-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91e5e-144">See also</span></span>



- [<span data-ttu-id="91e5e-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="91e5e-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

