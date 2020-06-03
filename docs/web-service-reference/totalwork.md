---
title: TotalWork
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TotalWork
api_type:
- schema
ms.assetid: 1348ffab-bd19-48fc-90dc-fd35e7031700
description: TotalWork 元素包含与任务相关联的工时的说明。
ms.openlocfilehash: 39abd8c670cd8365198d7ebb7b25b865ab8d5188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467499"
---
# <a name="totalwork"></a><span data-ttu-id="dc6d5-103">TotalWork</span><span class="sxs-lookup"><span data-stu-id="dc6d5-103">TotalWork</span></span>

<span data-ttu-id="dc6d5-104">**TotalWork**元素包含与任务相关联的工时的说明。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-104">The **TotalWork** element contains a description of how much work is associated with a task.</span></span> 
  
```xml
<TotalWork/>
```

 <span data-ttu-id="dc6d5-105">**Int**</span><span class="sxs-lookup"><span data-stu-id="dc6d5-105">**Int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc6d5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc6d5-106">Attributes and elements</span></span>

<span data-ttu-id="dc6d5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc6d5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc6d5-108">Attributes</span></span>

<span data-ttu-id="dc6d5-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc6d5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc6d5-110">Child elements</span></span>

<span data-ttu-id="dc6d5-111">无。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc6d5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dc6d5-112">Parent elements</span></span>

|<span data-ttu-id="dc6d5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc6d5-113">**Element**</span></span>|<span data-ttu-id="dc6d5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc6d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc6d5-115">任务</span><span class="sxs-lookup"><span data-stu-id="dc6d5-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="dc6d5-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc6d5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="dc6d5-117">Text value</span></span>

<span data-ttu-id="dc6d5-118">该文本值对应于一个整数，表示与任务相关联的总工作量。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-118">The text value corresponds to an integer that represents the total amount of work that is associated with a task.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc6d5-119">说明</span><span class="sxs-lookup"><span data-stu-id="dc6d5-119">Remarks</span></span>

<span data-ttu-id="dc6d5-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc6d5-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc6d5-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc6d5-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc6d5-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc6d5-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc6d5-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc6d5-123">Schema name</span></span>  <br/> |<span data-ttu-id="dc6d5-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc6d5-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc6d5-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc6d5-125">Validation file</span></span>  <br/> |<span data-ttu-id="dc6d5-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc6d5-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc6d5-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc6d5-127">Can be empty</span></span>  <br/> |<span data-ttu-id="dc6d5-128">False</span><span class="sxs-lookup"><span data-stu-id="dc6d5-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc6d5-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc6d5-129">See also</span></span>



- [<span data-ttu-id="dc6d5-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc6d5-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="dc6d5-131">创建任务</span><span class="sxs-lookup"><span data-stu-id="dc6d5-131">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="dc6d5-132">删除任务</span><span class="sxs-lookup"><span data-stu-id="dc6d5-132">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)
  
[<span data-ttu-id="dc6d5-133">更新任务</span><span class="sxs-lookup"><span data-stu-id="dc6d5-133">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

