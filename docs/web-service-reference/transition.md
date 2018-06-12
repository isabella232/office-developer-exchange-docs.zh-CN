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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838287"
---
# <a name="transition"></a><span data-ttu-id="f6985-103">转换</span><span class="sxs-lookup"><span data-stu-id="f6985-103">Transition</span></span>

<span data-ttu-id="f6985-104">**转换**元素均表示所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="f6985-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="f6985-105">**TransitionType**</span><span class="sxs-lookup"><span data-stu-id="f6985-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6985-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f6985-106">Attributes and elements</span></span>

<span data-ttu-id="f6985-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f6985-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6985-108">属性</span><span class="sxs-lookup"><span data-stu-id="f6985-108">Attributes</span></span>

<span data-ttu-id="f6985-109">无。</span><span class="sxs-lookup"><span data-stu-id="f6985-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6985-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f6985-110">Child elements</span></span>

|<span data-ttu-id="f6985-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f6985-111">**Element**</span></span>|<span data-ttu-id="f6985-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6985-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6985-113">To</span><span class="sxs-lookup"><span data-stu-id="f6985-113">To</span></span>](to.md) <br/> |<span data-ttu-id="f6985-114">指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="f6985-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6985-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f6985-115">Parent elements</span></span>

|<span data-ttu-id="f6985-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f6985-116">**Element**</span></span>|<span data-ttu-id="f6985-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6985-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6985-118">切换</span><span class="sxs-lookup"><span data-stu-id="f6985-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="f6985-119">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="f6985-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6985-120">备注</span><span class="sxs-lookup"><span data-stu-id="f6985-120">Remarks</span></span>

<span data-ttu-id="f6985-121">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f6985-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6985-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f6985-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6985-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f6985-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6985-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f6985-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f6985-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="f6985-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6985-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f6985-126">Validation File</span></span>  <br/> |<span data-ttu-id="f6985-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6985-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6985-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f6985-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6985-129">False</span><span class="sxs-lookup"><span data-stu-id="f6985-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6985-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f6985-130">See also</span></span>



- [<span data-ttu-id="f6985-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f6985-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

