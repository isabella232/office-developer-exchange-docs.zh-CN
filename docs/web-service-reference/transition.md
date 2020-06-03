---
title: 移交
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
description: 转换元素表示时区转换。
ms.openlocfilehash: 05495eb4a493feedc88532cc4bc8b949493481f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467492"
---
# <a name="transition"></a><span data-ttu-id="9c865-103">移交</span><span class="sxs-lookup"><span data-stu-id="9c865-103">Transition</span></span>

<span data-ttu-id="9c865-104">**转换**元素表示时区转换。</span><span class="sxs-lookup"><span data-stu-id="9c865-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="9c865-105">**TransitionType**</span><span class="sxs-lookup"><span data-stu-id="9c865-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c865-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c865-106">Attributes and elements</span></span>

<span data-ttu-id="9c865-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c865-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c865-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9c865-108">Attributes</span></span>

<span data-ttu-id="9c865-109">无。</span><span class="sxs-lookup"><span data-stu-id="9c865-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c865-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9c865-110">Child elements</span></span>

|<span data-ttu-id="9c865-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c865-111">**Element**</span></span>|<span data-ttu-id="9c865-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c865-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c865-113">To</span><span class="sxs-lookup"><span data-stu-id="9c865-113">To</span></span>](to.md) <br/> |<span data-ttu-id="9c865-114">指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="9c865-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c865-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9c865-115">Parent elements</span></span>

|<span data-ttu-id="9c865-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c865-116">**Element**</span></span>|<span data-ttu-id="9c865-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c865-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c865-118">移交</span><span class="sxs-lookup"><span data-stu-id="9c865-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="9c865-119">表示时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="9c865-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c865-120">备注</span><span class="sxs-lookup"><span data-stu-id="9c865-120">Remarks</span></span>

<span data-ttu-id="9c865-121">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c865-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c865-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c865-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c865-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c865-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c865-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c865-124">Schema Name</span></span>  <br/> |<span data-ttu-id="9c865-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="9c865-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c865-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c865-126">Validation File</span></span>  <br/> |<span data-ttu-id="9c865-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c865-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c865-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c865-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c865-129">False</span><span class="sxs-lookup"><span data-stu-id="9c865-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c865-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c865-130">See also</span></span>



- [<span data-ttu-id="9c865-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9c865-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

