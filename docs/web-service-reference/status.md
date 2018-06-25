---
title: 状态
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: Status 元素表示任务项的状态。
ms.openlocfilehash: 224b61913a5ae8e5b4aa0d756a9f2488df2741bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827584"
---
# <a name="status"></a><span data-ttu-id="1d1d5-103">状态</span><span class="sxs-lookup"><span data-stu-id="1d1d5-103">Status</span></span>

<span data-ttu-id="1d1d5-104">**Status**元素表示任务项的状态。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="1d1d5-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="1d1d5-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d1d5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d1d5-106">Attributes and elements</span></span>

<span data-ttu-id="1d1d5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d1d5-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d1d5-108">Attributes</span></span>

<span data-ttu-id="1d1d5-109">无。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d1d5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1d1d5-110">Child elements</span></span>

<span data-ttu-id="1d1d5-111">无。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d1d5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1d1d5-112">Parent elements</span></span>

|<span data-ttu-id="1d1d5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d1d5-113">**Element**</span></span>|<span data-ttu-id="1d1d5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d1d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d1d5-115">任务</span><span class="sxs-lookup"><span data-stu-id="1d1d5-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="1d1d5-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d1d5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1d1d5-117">Text value</span></span>

<span data-ttu-id="1d1d5-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-118">A text value is required.</span></span> <span data-ttu-id="1d1d5-119">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="1d1d5-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="1d1d5-120">为 NotStarted</span><span class="sxs-lookup"><span data-stu-id="1d1d5-120">NotStarted</span></span>
    
- <span data-ttu-id="1d1d5-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="1d1d5-121">InProgress</span></span>
    
- <span data-ttu-id="1d1d5-122">Completed</span><span class="sxs-lookup"><span data-stu-id="1d1d5-122">Completed</span></span>
    
- <span data-ttu-id="1d1d5-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="1d1d5-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="1d1d5-124">延迟</span><span class="sxs-lookup"><span data-stu-id="1d1d5-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d1d5-125">注解</span><span class="sxs-lookup"><span data-stu-id="1d1d5-125">Remarks</span></span>

<span data-ttu-id="1d1d5-126">设置[CompleteDate](completedate.md)与将[PercentComplete](percentcomplete.md)设置为 100 或**已完成****状态**的效果相同。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="1d1d5-127">在请求中，这些属性的设置至少两个，最后一个处理的属性将确定设置这些元素的值。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="1d1d5-128">例如，如果**PercentComplete**为 100， **CompleteDate**是 1/1/2007，并且**状态**为 NotStarted，并按此顺序流式传输属性，效果将任务的**状态**设置为 NotStarted， **CompleteDate**为**null**，并且为 0 的**完成百分比**。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="1d1d5-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d1d5-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d1d5-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d1d5-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d1d5-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d1d5-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d1d5-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d1d5-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1d1d5-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="1d1d5-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d1d5-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d1d5-134">Validation File</span></span>  <br/> |<span data-ttu-id="1d1d5-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d1d5-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d1d5-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d1d5-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d1d5-137">False</span><span class="sxs-lookup"><span data-stu-id="1d1d5-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d1d5-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1d1d5-138">See also</span></span>



- [<span data-ttu-id="1d1d5-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1d1d5-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1d1d5-140">创建任务</span><span class="sxs-lookup"><span data-stu-id="1d1d5-140">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="1d1d5-141">删除任务</span><span class="sxs-lookup"><span data-stu-id="1d1d5-141">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

