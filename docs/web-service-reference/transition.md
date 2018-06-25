---
title: 转换
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transition
api_type:
- schema
ms.assetid: 23ce171a-a9c9-47ed-a366-822777048eea
description: 转换元素均表示所在的时区转换。
ms.openlocfilehash: 5dcd2f0dae7c3df2dcf660d6fe1a41b216c67b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838287"
---
# <a name="transition"></a><span data-ttu-id="4d364-103">转换</span><span class="sxs-lookup"><span data-stu-id="4d364-103">Transition</span></span>

<span data-ttu-id="4d364-104">**转换**元素均表示所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="4d364-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="4d364-105">**TransitionType**</span><span class="sxs-lookup"><span data-stu-id="4d364-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d364-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d364-106">Attributes and elements</span></span>

<span data-ttu-id="4d364-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d364-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d364-108">属性</span><span class="sxs-lookup"><span data-stu-id="4d364-108">Attributes</span></span>

<span data-ttu-id="4d364-109">无。</span><span class="sxs-lookup"><span data-stu-id="4d364-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d364-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4d364-110">Child elements</span></span>

|<span data-ttu-id="4d364-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d364-111">**Element**</span></span>|<span data-ttu-id="4d364-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d364-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d364-113">To</span><span class="sxs-lookup"><span data-stu-id="4d364-113">To</span></span>](to.md) <br/> |<span data-ttu-id="4d364-114">指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="4d364-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d364-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4d364-115">Parent elements</span></span>

|<span data-ttu-id="4d364-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d364-116">**Element**</span></span>|<span data-ttu-id="4d364-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d364-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d364-118">切换</span><span class="sxs-lookup"><span data-stu-id="4d364-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="4d364-119">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="4d364-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d364-120">注解</span><span class="sxs-lookup"><span data-stu-id="4d364-120">Remarks</span></span>

<span data-ttu-id="4d364-121">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4d364-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d364-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d364-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d364-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d364-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d364-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d364-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4d364-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="4d364-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d364-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d364-126">Validation File</span></span>  <br/> |<span data-ttu-id="4d364-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4d364-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d364-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d364-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d364-129">False</span><span class="sxs-lookup"><span data-stu-id="4d364-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d364-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d364-130">See also</span></span>



- [<span data-ttu-id="4d364-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4d364-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

