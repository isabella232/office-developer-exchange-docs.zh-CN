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
description: IsAssignmentEditable 元素均表示任务类型。
ms.openlocfilehash: 91922c4d6abd4d88ac9e36dd3d4c0224fc1ee716
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825992"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="43008-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="43008-103">IsAssignmentEditable</span></span>

<span data-ttu-id="43008-104">**IsAssignmentEditable**元素均表示任务类型。</span><span class="sxs-lookup"><span data-stu-id="43008-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="43008-105">**整数**</span><span class="sxs-lookup"><span data-stu-id="43008-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43008-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43008-106">Attributes and elements</span></span>

<span data-ttu-id="43008-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43008-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43008-108">属性</span><span class="sxs-lookup"><span data-stu-id="43008-108">Attributes</span></span>

<span data-ttu-id="43008-109">无。</span><span class="sxs-lookup"><span data-stu-id="43008-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43008-110">子元素</span><span class="sxs-lookup"><span data-stu-id="43008-110">Child elements</span></span>

<span data-ttu-id="43008-111">无。</span><span class="sxs-lookup"><span data-stu-id="43008-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43008-112">父元素</span><span class="sxs-lookup"><span data-stu-id="43008-112">Parent elements</span></span>

|<span data-ttu-id="43008-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="43008-113">**Element**</span></span>|<span data-ttu-id="43008-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="43008-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43008-115">任务</span><span class="sxs-lookup"><span data-stu-id="43008-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="43008-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="43008-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43008-117">文本值</span><span class="sxs-lookup"><span data-stu-id="43008-117">Text value</span></span>

<span data-ttu-id="43008-118">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="43008-118">This property is read-only.</span></span> <span data-ttu-id="43008-119">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="43008-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="43008-120">**值**</span><span class="sxs-lookup"><span data-stu-id="43008-120">**Value**</span></span>|<span data-ttu-id="43008-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="43008-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43008-122">0</span><span class="sxs-lookup"><span data-stu-id="43008-122">0</span></span>  <br/> |<span data-ttu-id="43008-123">所有任务项的默认值。</span><span class="sxs-lookup"><span data-stu-id="43008-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="43008-124">1</span><span class="sxs-lookup"><span data-stu-id="43008-124">1</span></span>  <br/> |<span data-ttu-id="43008-125">任务要求。</span><span class="sxs-lookup"><span data-stu-id="43008-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="43008-126">2</span><span class="sxs-lookup"><span data-stu-id="43008-126">2</span></span>  <br/> |<span data-ttu-id="43008-127">接受任务从收件人的任务要求。</span><span class="sxs-lookup"><span data-stu-id="43008-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="43008-128">3</span><span class="sxs-lookup"><span data-stu-id="43008-128">3</span></span>  <br/> |<span data-ttu-id="43008-129">从收件人的任务请求任务拒绝。</span><span class="sxs-lookup"><span data-stu-id="43008-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="43008-130">4</span><span class="sxs-lookup"><span data-stu-id="43008-130">4</span></span>  <br/> |<span data-ttu-id="43008-131">对上一任务请求的更新。</span><span class="sxs-lookup"><span data-stu-id="43008-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="43008-132">5</span><span class="sxs-lookup"><span data-stu-id="43008-132">5</span></span>  <br/> |<span data-ttu-id="43008-133">不使用。</span><span class="sxs-lookup"><span data-stu-id="43008-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43008-134">备注</span><span class="sxs-lookup"><span data-stu-id="43008-134">Remarks</span></span>

<span data-ttu-id="43008-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43008-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43008-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="43008-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43008-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="43008-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43008-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="43008-138">Schema Name</span></span>  <br/> |<span data-ttu-id="43008-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="43008-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="43008-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="43008-140">Validation File</span></span>  <br/> |<span data-ttu-id="43008-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43008-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43008-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="43008-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="43008-143">False</span><span class="sxs-lookup"><span data-stu-id="43008-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43008-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43008-144">See also</span></span>



- [<span data-ttu-id="43008-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43008-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

