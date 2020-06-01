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
description: CompleteDate 元素表示项目完成的日期。
ms.openlocfilehash: fff3d5d3105bf63c9cdd34cbcf828d57ca287b86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461420"
---
# <a name="completedate"></a><span data-ttu-id="b6342-103">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="b6342-103">CompleteDate</span></span>

<span data-ttu-id="b6342-104">**CompleteDate**元素表示项目完成的日期。</span><span class="sxs-lookup"><span data-stu-id="b6342-104">The **CompleteDate** element represents the date on which an item was completed.</span></span> 
  
```xml
<CompleteDate/>
```

 <span data-ttu-id="b6342-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="b6342-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6342-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b6342-106">Attributes and elements</span></span>

<span data-ttu-id="b6342-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b6342-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6342-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b6342-108">Attributes</span></span>

<span data-ttu-id="b6342-109">无。</span><span class="sxs-lookup"><span data-stu-id="b6342-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6342-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b6342-110">Child elements</span></span>

<span data-ttu-id="b6342-111">无。</span><span class="sxs-lookup"><span data-stu-id="b6342-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6342-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b6342-112">Parent elements</span></span>

|<span data-ttu-id="b6342-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6342-113">**Element**</span></span>|<span data-ttu-id="b6342-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6342-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6342-115">任务</span><span class="sxs-lookup"><span data-stu-id="b6342-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="b6342-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="b6342-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b6342-117">Flag</span><span class="sxs-lookup"><span data-stu-id="b6342-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="b6342-118">指定邮箱项目的标志。</span><span class="sxs-lookup"><span data-stu-id="b6342-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6342-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b6342-119">Text value</span></span>

<span data-ttu-id="b6342-120">如果使用此元素，则表示日期和时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="b6342-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6342-121">备注</span><span class="sxs-lookup"><span data-stu-id="b6342-121">Remarks</span></span>

<span data-ttu-id="b6342-122">设置**CompleteDate**与将[百分比](percentcomplete.md)设置为100或将[状态](status.md)设置为 "已**完成**" 具有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="b6342-122">Setting **CompleteDate** has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or [Status](status.md) to **Completed**.</span></span> <span data-ttu-id="b6342-123">在设置至少两个属性中的一个请求中，最后处理的属性将确定为这些元素设置的值。</span><span class="sxs-lookup"><span data-stu-id="b6342-123">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="b6342-124">例如，如果[百分比](percentcomplete.md)为100，则**CompleteDate**为 2007 1 月1日，且[状态](status.md)为**NotStarted**，并且按该顺序对属性进行了流式处理，则效果是将任务的[状态](status.md)设置为**NotStarted**，将[CompleteDate](completedate.md)设置为 null，[并将](percentcomplete.md)**值**为0。</span><span class="sxs-lookup"><span data-stu-id="b6342-124">For example, if [PercentComplete](percentcomplete.md) is 100, **CompleteDate** is January 1, 2007, and [Status](status.md) is **NotStarted**, and the properties are streamed in that order, the effect will be to set the [Status](status.md) of the task to **NotStarted**, the [CompleteDate](completedate.md) to **null**, and [PercentComplete](percentcomplete.md) to 0.</span></span> 
  
<span data-ttu-id="b6342-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b6342-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6342-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b6342-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6342-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b6342-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6342-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b6342-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b6342-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="b6342-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b6342-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b6342-130">Validation File</span></span>  <br/> |<span data-ttu-id="b6342-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b6342-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6342-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b6342-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6342-133">False</span><span class="sxs-lookup"><span data-stu-id="b6342-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6342-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6342-134">See also</span></span>



- [<span data-ttu-id="b6342-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b6342-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b6342-136">创建任务</span><span class="sxs-lookup"><span data-stu-id="b6342-136">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="b6342-137">删除任务</span><span class="sxs-lookup"><span data-stu-id="b6342-137">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

