---
title: agentList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 7dd9d48356932c82dbc048a85b9f02437c6366de
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753053"
---
# <a name="agentlist"></a><span data-ttu-id="e31a2-103">agentList</span><span class="sxs-lookup"><span data-stu-id="e31a2-103">agentList</span></span>
  
<span data-ttu-id="e31a2-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e31a2-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="e31a2-105">**AgentList**元素包含的每个安装代理[代理](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="e31a2-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="e31a2-106">configuration</span><span class="sxs-lookup"><span data-stu-id="e31a2-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="e31a2-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="e31a2-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="e31a2-108">agentList</span><span class="sxs-lookup"><span data-stu-id="e31a2-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="e31a2-109">**agentListType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="e31a2-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e31a2-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e31a2-110">Attributes and elements</span></span>

<span data-ttu-id="e31a2-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e31a2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e31a2-112">属性</span><span class="sxs-lookup"><span data-stu-id="e31a2-112">Attributes</span></span>

<span data-ttu-id="e31a2-113">无。</span><span class="sxs-lookup"><span data-stu-id="e31a2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e31a2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e31a2-114">Child elements</span></span>

|<span data-ttu-id="e31a2-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="e31a2-115">**Element**</span></span>|<span data-ttu-id="e31a2-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="e31a2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e31a2-117">代理</span><span class="sxs-lookup"><span data-stu-id="e31a2-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="e31a2-118">包含安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="e31a2-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e31a2-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e31a2-119">Parent elements</span></span>

|<span data-ttu-id="e31a2-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="e31a2-120">**Element**</span></span>|<span data-ttu-id="e31a2-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e31a2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e31a2-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="e31a2-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="e31a2-123">包含定义监控代理的配置信息和有关安装代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="e31a2-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e31a2-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e31a2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e31a2-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e31a2-125">Namespace</span></span>  <br/> |<span data-ttu-id="e31a2-126">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="e31a2-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="e31a2-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="e31a2-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e31a2-128">不可用。</span><span class="sxs-lookup"><span data-stu-id="e31a2-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="e31a2-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="e31a2-129">Validation File</span></span>  <br/> |<span data-ttu-id="e31a2-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="e31a2-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="e31a2-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="e31a2-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e31a2-132">False。</span><span class="sxs-lookup"><span data-stu-id="e31a2-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e31a2-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e31a2-133">See also</span></span>

- [<span data-ttu-id="e31a2-134">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="e31a2-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

