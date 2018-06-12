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
description: PercentComplete 元素描述任务的完成的状态。
ms.openlocfilehash: 18e53221ecdf60df195445ed7692c03795bdcc1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826717"
---
# <a name="percentcomplete"></a><span data-ttu-id="fa853-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="fa853-103">PercentComplete</span></span>

<span data-ttu-id="fa853-104">**PercentComplete**元素描述任务的完成的状态。</span><span class="sxs-lookup"><span data-stu-id="fa853-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="fa853-105">**双**</span><span class="sxs-lookup"><span data-stu-id="fa853-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa853-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa853-106">Attributes and elements</span></span>

<span data-ttu-id="fa853-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa853-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa853-108">属性</span><span class="sxs-lookup"><span data-stu-id="fa853-108">Attributes</span></span>

<span data-ttu-id="fa853-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa853-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa853-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa853-110">Child elements</span></span>

<span data-ttu-id="fa853-111">无。</span><span class="sxs-lookup"><span data-stu-id="fa853-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa853-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fa853-112">Parent elements</span></span>

|<span data-ttu-id="fa853-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa853-113">**Element**</span></span>|<span data-ttu-id="fa853-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa853-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa853-115">任务</span><span class="sxs-lookup"><span data-stu-id="fa853-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="fa853-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="fa853-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa853-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fa853-117">Text value</span></span>

<span data-ttu-id="fa853-118">所需的文本值，该值代表介于 0 和 100 之间的整数。</span><span class="sxs-lookup"><span data-stu-id="fa853-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa853-119">备注</span><span class="sxs-lookup"><span data-stu-id="fa853-119">Remarks</span></span>

<span data-ttu-id="fa853-120">将**PercentComplete**设置为 100 具有相同的效果设置[CompleteDate](completedate.md)元素或设置为**已完成**的[Status](status.md)元素。</span><span class="sxs-lookup"><span data-stu-id="fa853-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="fa853-121">在请求中，这些属性的设置至少两个，最后一个处理的属性将确定设置这些元素的值。</span><span class="sxs-lookup"><span data-stu-id="fa853-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="fa853-122">例如，如果**PercentComplete**为 100， [CompleteDate](completedate.md)是 2007 年 1 月 1 日和[状态](status.md)为 NotStarted，并且按此顺序流式传输属性，效果将为任务的[状态](status.md)设置为 NotStarted， [CompleteDate](completedate.md)为**null**，并且为 0 的**完成百分比**。</span><span class="sxs-lookup"><span data-stu-id="fa853-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="fa853-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa853-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa853-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa853-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa853-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa853-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa853-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa853-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fa853-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa853-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa853-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa853-128">Validation File</span></span>  <br/> |<span data-ttu-id="fa853-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa853-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa853-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa853-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa853-131">False</span><span class="sxs-lookup"><span data-stu-id="fa853-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa853-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa853-132">See also</span></span>



- [<span data-ttu-id="fa853-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa853-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="fa853-134">创建任务</span><span class="sxs-lookup"><span data-stu-id="fa853-134">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="fa853-135">删除任务</span><span class="sxs-lookup"><span data-stu-id="fa853-135">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

