---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: 百分比元素描述任务的完成状态。
ms.openlocfilehash: b7dd2f18bd3ef6addeb6d3a7b004510f35b9cb3d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456883"
---
# <a name="percentcomplete"></a><span data-ttu-id="e8ee2-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e8ee2-103">PercentComplete</span></span>

<span data-ttu-id="e8ee2-104">**百分比**元素描述任务的完成状态。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="e8ee2-105">**加倍**</span><span class="sxs-lookup"><span data-stu-id="e8ee2-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8ee2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e8ee2-106">Attributes and elements</span></span>

<span data-ttu-id="e8ee2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8ee2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e8ee2-108">Attributes</span></span>

<span data-ttu-id="e8ee2-109">无。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8ee2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e8ee2-110">Child elements</span></span>

<span data-ttu-id="e8ee2-111">无。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8ee2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e8ee2-112">Parent elements</span></span>

|<span data-ttu-id="e8ee2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8ee2-113">**Element**</span></span>|<span data-ttu-id="e8ee2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8ee2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8ee2-115">任务</span><span class="sxs-lookup"><span data-stu-id="e8ee2-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="e8ee2-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8ee2-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e8ee2-117">Text value</span></span>

<span data-ttu-id="e8ee2-118">一个代表0到100之间的整数的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8ee2-119">备注</span><span class="sxs-lookup"><span data-stu-id="e8ee2-119">Remarks</span></span>

<span data-ttu-id="e8ee2-120">将**百分比**设置为100与设置[CompleteDate](completedate.md)元素或将[Status](status.md)元素设置为 "**已完成**" 具有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="e8ee2-121">在设置至少两个属性中的一个请求中，最后处理的属性将确定为这些元素设置的值。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="e8ee2-122">例如，如果**百分比**为100，则[CompleteDate](completedate.md)为 2007 1 月1日，且[状态](status.md)为 NotStarted，并且按此顺序对属性进行流式处理，则效果是将任务的[状态](status.md)设置为 NotStarted，将[CompleteDate](completedate.md)设置为**null**，并将**百分比**为0。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="e8ee2-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e8ee2-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8ee2-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e8ee2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8ee2-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e8ee2-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8ee2-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e8ee2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e8ee2-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="e8ee2-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8ee2-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e8ee2-128">Validation File</span></span>  <br/> |<span data-ttu-id="e8ee2-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8ee2-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8ee2-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e8ee2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8ee2-131">False</span><span class="sxs-lookup"><span data-stu-id="e8ee2-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8ee2-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8ee2-132">See also</span></span>



- [<span data-ttu-id="e8ee2-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e8ee2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e8ee2-134">创建任务</span><span class="sxs-lookup"><span data-stu-id="e8ee2-134">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="e8ee2-135">删除任务</span><span class="sxs-lookup"><span data-stu-id="e8ee2-135">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

