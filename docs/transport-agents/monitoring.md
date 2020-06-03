---
title: 监视
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455826"
---
# <a name="monitoring"></a><span data-ttu-id="1cedf-103">监视</span><span class="sxs-lookup"><span data-stu-id="1cedf-103">monitoring</span></span>
  
<span data-ttu-id="1cedf-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cedf-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="1cedf-105">**Monitoring**元素包含配置信息，用于定义前端传输服务或传输服务如何以及何时监视安装的代理。</span><span class="sxs-lookup"><span data-stu-id="1cedf-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="1cedf-106">configuration</span><span class="sxs-lookup"><span data-stu-id="1cedf-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="1cedf-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1cedf-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="1cedf-108">监视</span><span class="sxs-lookup"><span data-stu-id="1cedf-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="1cedf-109">**monitoringType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="1cedf-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1cedf-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1cedf-110">Attributes and elements</span></span>

<span data-ttu-id="1cedf-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1cedf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cedf-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="1cedf-112">Attributes</span></span>

<span data-ttu-id="1cedf-113">无。</span><span class="sxs-lookup"><span data-stu-id="1cedf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1cedf-114">子元素</span><span class="sxs-lookup"><span data-stu-id="1cedf-114">Child elements</span></span>

|<span data-ttu-id="1cedf-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="1cedf-115">**Element**</span></span>|<span data-ttu-id="1cedf-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="1cedf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cedf-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="1cedf-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="1cedf-118">定义客户端访问或邮箱服务器等待代理在写入事件日志之前从事件返回的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="1cedf-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="1cedf-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="1cedf-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="1cedf-120">包含一个属性，该属性指定是否为客户端访问或邮箱服务器启用管道跟踪功能。</span><span class="sxs-lookup"><span data-stu-id="1cedf-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1cedf-121">父元素</span><span class="sxs-lookup"><span data-stu-id="1cedf-121">Parent elements</span></span>

|<span data-ttu-id="1cedf-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="1cedf-122">**Element**</span></span>|<span data-ttu-id="1cedf-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="1cedf-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cedf-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1cedf-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="1cedf-125">包含用于定义代理监视的配置信息和安装的 SMTP 和路由代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="1cedf-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="1cedf-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="1cedf-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cedf-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="1cedf-127">Namespace</span></span>  <br/> |<span data-ttu-id="1cedf-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="1cedf-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="1cedf-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1cedf-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1cedf-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="1cedf-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="1cedf-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="1cedf-131">Validation File</span></span>  <br/> |<span data-ttu-id="1cedf-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="1cedf-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="1cedf-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="1cedf-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1cedf-134">不正确。</span><span class="sxs-lookup"><span data-stu-id="1cedf-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cedf-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1cedf-135">See also</span></span>

- [<span data-ttu-id="1cedf-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="1cedf-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

