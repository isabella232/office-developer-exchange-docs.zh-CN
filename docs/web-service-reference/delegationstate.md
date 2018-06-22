---
title: DelegationState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegationState
api_type:
- schema
ms.assetid: 9dbb83ed-1ded-48f3-8e06-2489fc8b28d5
description: DelegationState 元素均表示委派的任务的状态。
ms.openlocfilehash: 00b0e41ae223f1c70f9a3a21662e8858f8690a86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753782"
---
# <a name="delegationstate"></a><span data-ttu-id="351af-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="351af-103">DelegationState</span></span>

<span data-ttu-id="351af-104">**DelegationState**元素均表示委派的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="351af-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="351af-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="351af-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="351af-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="351af-106">Attributes and elements</span></span>

<span data-ttu-id="351af-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="351af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="351af-108">属性</span><span class="sxs-lookup"><span data-stu-id="351af-108">Attributes</span></span>

<span data-ttu-id="351af-109">无。</span><span class="sxs-lookup"><span data-stu-id="351af-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="351af-110">子元素</span><span class="sxs-lookup"><span data-stu-id="351af-110">Child elements</span></span>

<span data-ttu-id="351af-111">无。</span><span class="sxs-lookup"><span data-stu-id="351af-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="351af-112">父元素</span><span class="sxs-lookup"><span data-stu-id="351af-112">Parent elements</span></span>

|<span data-ttu-id="351af-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="351af-113">**Element**</span></span>|<span data-ttu-id="351af-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="351af-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="351af-115">任务</span><span class="sxs-lookup"><span data-stu-id="351af-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="351af-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="351af-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="351af-117">文本值</span><span class="sxs-lookup"><span data-stu-id="351af-117">Text value</span></span>

<span data-ttu-id="351af-118">这是只读属性。</span><span class="sxs-lookup"><span data-stu-id="351af-118">This is a read-only property.</span></span> <span data-ttu-id="351af-119">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="351af-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="351af-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="351af-120">NoMatch</span></span>
    
- <span data-ttu-id="351af-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="351af-121">OwnNew</span></span>
    
- <span data-ttu-id="351af-122">拥有</span><span class="sxs-lookup"><span data-stu-id="351af-122">Owned</span></span>
    
- <span data-ttu-id="351af-123">接受</span><span class="sxs-lookup"><span data-stu-id="351af-123">Accepted</span></span>
    
- <span data-ttu-id="351af-124">拒绝</span><span class="sxs-lookup"><span data-stu-id="351af-124">Declined</span></span>
    
- <span data-ttu-id="351af-125">Max</span><span class="sxs-lookup"><span data-stu-id="351af-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="351af-126">备注</span><span class="sxs-lookup"><span data-stu-id="351af-126">Remarks</span></span>

<span data-ttu-id="351af-127">Microsoft Exchange Server 2007 中的 Exchange Web 服务不支持任务分配。</span><span class="sxs-lookup"><span data-stu-id="351af-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="351af-128">描述此元素的架构位于正在运行 Exchange 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="351af-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="351af-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="351af-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="351af-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="351af-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="351af-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="351af-131">Schema Name</span></span>  <br/> |<span data-ttu-id="351af-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="351af-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="351af-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="351af-133">Validation File</span></span>  <br/> |<span data-ttu-id="351af-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="351af-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="351af-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="351af-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="351af-136">False</span><span class="sxs-lookup"><span data-stu-id="351af-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="351af-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="351af-137">See also</span></span>

- [<span data-ttu-id="351af-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="351af-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

