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
ms.openlocfilehash: 5d022827990b96fd8790ae9566ef49028ebe404c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459957"
---
# <a name="status"></a><span data-ttu-id="fd132-103">状态</span><span class="sxs-lookup"><span data-stu-id="fd132-103">Status</span></span>

<span data-ttu-id="fd132-104">**Status**元素表示任务项的状态。</span><span class="sxs-lookup"><span data-stu-id="fd132-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="fd132-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="fd132-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd132-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fd132-106">Attributes and elements</span></span>

<span data-ttu-id="fd132-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd132-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd132-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fd132-108">Attributes</span></span>

<span data-ttu-id="fd132-109">无。</span><span class="sxs-lookup"><span data-stu-id="fd132-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd132-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fd132-110">Child elements</span></span>

<span data-ttu-id="fd132-111">无。</span><span class="sxs-lookup"><span data-stu-id="fd132-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd132-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fd132-112">Parent elements</span></span>

|<span data-ttu-id="fd132-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fd132-113">**Element**</span></span>|<span data-ttu-id="fd132-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fd132-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd132-115">任务</span><span class="sxs-lookup"><span data-stu-id="fd132-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="fd132-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="fd132-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fd132-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fd132-117">Text value</span></span>

<span data-ttu-id="fd132-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="fd132-118">A text value is required.</span></span> <span data-ttu-id="fd132-119">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="fd132-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="fd132-120">NotStarted</span><span class="sxs-lookup"><span data-stu-id="fd132-120">NotStarted</span></span>
    
- <span data-ttu-id="fd132-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="fd132-121">InProgress</span></span>
    
- <span data-ttu-id="fd132-122">Completed</span><span class="sxs-lookup"><span data-stu-id="fd132-122">Completed</span></span>
    
- <span data-ttu-id="fd132-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="fd132-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="fd132-124">关联表</span><span class="sxs-lookup"><span data-stu-id="fd132-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd132-125">备注</span><span class="sxs-lookup"><span data-stu-id="fd132-125">Remarks</span></span>

<span data-ttu-id="fd132-126">设置[CompleteDate](completedate.md)与将[百分比](percentcomplete.md)设置为100或将**状态**设置为 "已**完成**" 具有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="fd132-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="fd132-127">在设置至少两个属性中的一个请求中，最后处理的属性将确定为这些元素设置的值。</span><span class="sxs-lookup"><span data-stu-id="fd132-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="fd132-128">例如，如果**百分比**为100， **CompleteDate**为1/1/2007，**状态**为 NotStarted，并且按此顺序对属性进行了流式处理，则效果是将任务的**状态**设置为 NotStarted，将**CompleteDate**设置为**null**，并将**百分比**为0。</span><span class="sxs-lookup"><span data-stu-id="fd132-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="fd132-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fd132-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd132-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="fd132-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd132-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="fd132-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd132-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="fd132-132">Schema Name</span></span>  <br/> |<span data-ttu-id="fd132-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="fd132-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd132-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="fd132-134">Validation File</span></span>  <br/> |<span data-ttu-id="fd132-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd132-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd132-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="fd132-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd132-137">False</span><span class="sxs-lookup"><span data-stu-id="fd132-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd132-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fd132-138">See also</span></span>



- [<span data-ttu-id="fd132-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fd132-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="fd132-140">创建任务</span><span class="sxs-lookup"><span data-stu-id="fd132-140">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="fd132-141">删除任务</span><span class="sxs-lookup"><span data-stu-id="fd132-141">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

