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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 99e4e24c3bca77c7e7d5f2c59bb21cee1317fed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44446390"
---
# <a name="agentlist"></a><span data-ttu-id="1cd4f-103">agentList</span><span class="sxs-lookup"><span data-stu-id="1cd4f-103">agentList</span></span>
  
<span data-ttu-id="1cd4f-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cd4f-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="1cd4f-105">**AgentList**元素包含每个已安装代理的[代理](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="1cd4f-106">configuration</span><span class="sxs-lookup"><span data-stu-id="1cd4f-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="1cd4f-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1cd4f-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="1cd4f-108">agentList</span><span class="sxs-lookup"><span data-stu-id="1cd4f-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="1cd4f-109">**agentListType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1cd4f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1cd4f-110">Attributes and elements</span></span>

<span data-ttu-id="1cd4f-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cd4f-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="1cd4f-112">Attributes</span></span>

<span data-ttu-id="1cd4f-113">无。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1cd4f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="1cd4f-114">Child elements</span></span>

|<span data-ttu-id="1cd4f-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-115">**Element**</span></span>|<span data-ttu-id="1cd4f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cd4f-117">代理</span><span class="sxs-lookup"><span data-stu-id="1cd4f-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="1cd4f-118">包含有关已安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1cd4f-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1cd4f-119">Parent elements</span></span>

|<span data-ttu-id="1cd4f-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-120">**Element**</span></span>|<span data-ttu-id="1cd4f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cd4f-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1cd4f-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="1cd4f-123">包含定义有关已安装代理的代理监视和配置信息的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="1cd4f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1cd4f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cd4f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1cd4f-125">Namespace</span></span>  <br/> |<span data-ttu-id="1cd4f-126">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="1cd4f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="1cd4f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="1cd4f-128">不可用。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="1cd4f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="1cd4f-129">Validation File</span></span>  <br/> |<span data-ttu-id="1cd4f-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="1cd4f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="1cd4f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="1cd4f-132">不正确。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cd4f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1cd4f-133">See also</span></span>

- [<span data-ttu-id="1cd4f-134">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="1cd4f-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

