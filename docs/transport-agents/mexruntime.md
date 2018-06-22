---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 4a34eedfc16d64cbfa67003ed23cf6eba2bb4bad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753085"
---
# <a name="mexruntime"></a><span data-ttu-id="ba4ee-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="ba4ee-103">mexRuntime</span></span>
  
<span data-ttu-id="ba4ee-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba4ee-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="ba4ee-105">**MexRuntime**元素包含定义监控代理的配置信息和 SMTP 和安装的路由代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="ba4ee-106">configuration</span><span class="sxs-lookup"><span data-stu-id="ba4ee-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="ba4ee-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="ba4ee-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="ba4ee-108">**mexRuntimeType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ba4ee-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba4ee-109">Attributes and elements</span></span>

<span data-ttu-id="ba4ee-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba4ee-111">属性</span><span class="sxs-lookup"><span data-stu-id="ba4ee-111">Attributes</span></span>

<span data-ttu-id="ba4ee-112">无。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba4ee-113">子元素</span><span class="sxs-lookup"><span data-stu-id="ba4ee-113">Child elements</span></span>

|<span data-ttu-id="ba4ee-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-114">**Element**</span></span>|<span data-ttu-id="ba4ee-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba4ee-116">监控</span><span class="sxs-lookup"><span data-stu-id="ba4ee-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="ba4ee-117">包含定义如何以及何时传输监视安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="ba4ee-118">agentList</span><span class="sxs-lookup"><span data-stu-id="ba4ee-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="ba4ee-119">包含用于安装的每个代理[代理](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba4ee-120">父元素</span><span class="sxs-lookup"><span data-stu-id="ba4ee-120">Parent elements</span></span>

|<span data-ttu-id="ba4ee-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-121">**Element**</span></span>|<span data-ttu-id="ba4ee-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba4ee-123">configuration</span><span class="sxs-lookup"><span data-stu-id="ba4ee-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="ba4ee-124">代理配置文件的的根元素。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="ba4ee-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba4ee-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba4ee-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba4ee-126">Namespace</span></span>  <br/> |<span data-ttu-id="ba4ee-127">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="ba4ee-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba4ee-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ba4ee-129">不可用。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="ba4ee-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba4ee-130">Validation File</span></span>  <br/> |<span data-ttu-id="ba4ee-131">不可用。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="ba4ee-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba4ee-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba4ee-133">False。</span><span class="sxs-lookup"><span data-stu-id="ba4ee-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba4ee-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba4ee-134">See also</span></span>

- [<span data-ttu-id="ba4ee-135">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="ba4ee-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

