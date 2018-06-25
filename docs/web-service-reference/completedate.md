---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: CompleteDate 元素均表示已完成项目的日期。
ms.openlocfilehash: 00a1ec25be737ec0a5cc874063e1bce19a96cee0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753461"
---
# <a name="completedate"></a><span data-ttu-id="2c858-103">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="2c858-103">CompleteDate</span></span>

<span data-ttu-id="2c858-104">**CompleteDate**元素均表示已完成项目的日期。</span><span class="sxs-lookup"><span data-stu-id="2c858-104">The **CompleteDate** element represents the date on which an item was completed.</span></span> 
  
```xml
<CompleteDate/>
```

 <span data-ttu-id="2c858-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c858-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c858-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2c858-106">Attributes and elements</span></span>

<span data-ttu-id="2c858-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c858-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c858-108">属性</span><span class="sxs-lookup"><span data-stu-id="2c858-108">Attributes</span></span>

<span data-ttu-id="2c858-109">无。</span><span class="sxs-lookup"><span data-stu-id="2c858-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c858-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2c858-110">Child elements</span></span>

<span data-ttu-id="2c858-111">无。</span><span class="sxs-lookup"><span data-stu-id="2c858-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c858-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2c858-112">Parent elements</span></span>

|<span data-ttu-id="2c858-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c858-113">**Element**</span></span>|<span data-ttu-id="2c858-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c858-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c858-115">任务</span><span class="sxs-lookup"><span data-stu-id="2c858-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="2c858-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="2c858-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2c858-117">Flag</span><span class="sxs-lookup"><span data-stu-id="2c858-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="2c858-118">邮箱项目上指定的标志。</span><span class="sxs-lookup"><span data-stu-id="2c858-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c858-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2c858-119">Text value</span></span>

<span data-ttu-id="2c858-120">如果使用此元素，则需要一个文本值，表示的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2c858-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c858-121">注解</span><span class="sxs-lookup"><span data-stu-id="2c858-121">Remarks</span></span>

<span data-ttu-id="2c858-122">设置**CompleteDate**与将[PercentComplete](percentcomplete.md)设置为 100 或**已完成**[状态](status.md)的效果相同。</span><span class="sxs-lookup"><span data-stu-id="2c858-122">Setting **CompleteDate** has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or [Status](status.md) to **Completed**.</span></span> <span data-ttu-id="2c858-123">在请求中，这些属性的设置至少两个，最后一个处理的属性将确定设置这些元素的值。</span><span class="sxs-lookup"><span data-stu-id="2c858-123">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="2c858-124">例如，如果[PercentComplete](percentcomplete.md)为 100， **CompleteDate**是 2007 年 1 月 1 日和[状态](status.md)为**NotStarted**，并且该顺序流式传输属性，将效果设置为 NotStarted**任务的[状态](status.md)**， [CompleteDate](completedate.md)为**null**，并且为 0 的[完成百分比](percentcomplete.md)。</span><span class="sxs-lookup"><span data-stu-id="2c858-124">For example, if [PercentComplete](percentcomplete.md) is 100, **CompleteDate** is January 1, 2007, and [Status](status.md) is **NotStarted**, and the properties are streamed in that order, the effect will be to set the [Status](status.md) of the task to **NotStarted**, the [CompleteDate](completedate.md) to **null**, and [PercentComplete](percentcomplete.md) to 0.</span></span> 
  
<span data-ttu-id="2c858-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2c858-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c858-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="2c858-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c858-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="2c858-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c858-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="2c858-128">Schema Name</span></span>  <br/> |<span data-ttu-id="2c858-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="2c858-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c858-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="2c858-130">Validation File</span></span>  <br/> |<span data-ttu-id="2c858-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c858-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c858-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="2c858-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c858-133">False</span><span class="sxs-lookup"><span data-stu-id="2c858-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c858-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c858-134">See also</span></span>



- [<span data-ttu-id="2c858-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2c858-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2c858-136">创建任务</span><span class="sxs-lookup"><span data-stu-id="2c858-136">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="2c858-137">删除任务</span><span class="sxs-lookup"><span data-stu-id="2c858-137">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

