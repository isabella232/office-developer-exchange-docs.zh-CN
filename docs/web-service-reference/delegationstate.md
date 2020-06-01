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
description: DelegationState 元素表示委派任务的状态。
ms.openlocfilehash: b938b5a2240283c265006dd47cd6ff475ad80978
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457366"
---
# <a name="delegationstate"></a><span data-ttu-id="b1693-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="b1693-103">DelegationState</span></span>

<span data-ttu-id="b1693-104">**DelegationState**元素表示委派任务的状态。</span><span class="sxs-lookup"><span data-stu-id="b1693-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="b1693-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="b1693-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b1693-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b1693-106">Attributes and elements</span></span>

<span data-ttu-id="b1693-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b1693-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1693-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b1693-108">Attributes</span></span>

<span data-ttu-id="b1693-109">无。</span><span class="sxs-lookup"><span data-stu-id="b1693-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1693-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b1693-110">Child elements</span></span>

<span data-ttu-id="b1693-111">无。</span><span class="sxs-lookup"><span data-stu-id="b1693-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1693-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b1693-112">Parent elements</span></span>

|<span data-ttu-id="b1693-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b1693-113">**Element**</span></span>|<span data-ttu-id="b1693-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b1693-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1693-115">任务</span><span class="sxs-lookup"><span data-stu-id="b1693-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="b1693-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="b1693-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1693-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b1693-117">Text value</span></span>

<span data-ttu-id="b1693-118">这是一个只读属性。</span><span class="sxs-lookup"><span data-stu-id="b1693-118">This is a read-only property.</span></span> <span data-ttu-id="b1693-119">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="b1693-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="b1693-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="b1693-120">NoMatch</span></span>
    
- <span data-ttu-id="b1693-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="b1693-121">OwnNew</span></span>
    
- <span data-ttu-id="b1693-122">所有权</span><span class="sxs-lookup"><span data-stu-id="b1693-122">Owned</span></span>
    
- <span data-ttu-id="b1693-123">Accepted</span><span class="sxs-lookup"><span data-stu-id="b1693-123">Accepted</span></span>
    
- <span data-ttu-id="b1693-124">邀请</span><span class="sxs-lookup"><span data-stu-id="b1693-124">Declined</span></span>
    
- <span data-ttu-id="b1693-125">Max</span><span class="sxs-lookup"><span data-stu-id="b1693-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1693-126">备注</span><span class="sxs-lookup"><span data-stu-id="b1693-126">Remarks</span></span>

<span data-ttu-id="b1693-127">Microsoft Exchange Server 2007 中的 Exchange Web 服务不支持任务分配。</span><span class="sxs-lookup"><span data-stu-id="b1693-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="b1693-128">描述此元素的架构位于正在运行 Exchange 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b1693-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1693-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="b1693-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1693-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1693-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1693-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="b1693-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b1693-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="b1693-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b1693-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="b1693-133">Validation File</span></span>  <br/> |<span data-ttu-id="b1693-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b1693-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1693-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="b1693-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1693-136">False</span><span class="sxs-lookup"><span data-stu-id="b1693-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1693-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b1693-137">See also</span></span>

- [<span data-ttu-id="b1693-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b1693-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

