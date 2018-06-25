---
title: 监控
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
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753081"
---
# <a name="monitoring"></a><span data-ttu-id="177ae-103">监控</span><span class="sxs-lookup"><span data-stu-id="177ae-103">monitoring</span></span>
  
<span data-ttu-id="177ae-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="177ae-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="177ae-105">**监控**元素包含定义如何以及何时的前端传输服务或的传输服务监视安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="177ae-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="177ae-106">configuration</span><span class="sxs-lookup"><span data-stu-id="177ae-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="177ae-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="177ae-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="177ae-108">监控</span><span class="sxs-lookup"><span data-stu-id="177ae-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="177ae-109">**monitoringType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="177ae-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="177ae-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="177ae-110">Attributes and elements</span></span>

<span data-ttu-id="177ae-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="177ae-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="177ae-112">属性</span><span class="sxs-lookup"><span data-stu-id="177ae-112">Attributes</span></span>

<span data-ttu-id="177ae-113">无。</span><span class="sxs-lookup"><span data-stu-id="177ae-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="177ae-114">子元素</span><span class="sxs-lookup"><span data-stu-id="177ae-114">Child elements</span></span>

|<span data-ttu-id="177ae-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="177ae-115">**Element**</span></span>|<span data-ttu-id="177ae-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="177ae-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="177ae-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="177ae-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="177ae-118">定义时间，以毫秒为单位，等待代理以从事件之前它写入事件日志中返回的客户端访问或邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="177ae-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="177ae-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="177ae-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="177ae-120">包含指定是否为客户端访问或邮箱服务器启用管道跟踪功能属性。</span><span class="sxs-lookup"><span data-stu-id="177ae-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="177ae-121">父元素</span><span class="sxs-lookup"><span data-stu-id="177ae-121">Parent elements</span></span>

|<span data-ttu-id="177ae-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="177ae-122">**Element**</span></span>|<span data-ttu-id="177ae-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="177ae-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="177ae-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="177ae-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="177ae-125">包含定义监控代理的配置信息和 SMTP 和安装的路由代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="177ae-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="177ae-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="177ae-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="177ae-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="177ae-127">Namespace</span></span>  <br/> |<span data-ttu-id="177ae-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="177ae-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="177ae-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="177ae-129">Schema Name</span></span>  <br/> |<span data-ttu-id="177ae-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="177ae-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="177ae-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="177ae-131">Validation File</span></span>  <br/> |<span data-ttu-id="177ae-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="177ae-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="177ae-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="177ae-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="177ae-134">False。</span><span class="sxs-lookup"><span data-stu-id="177ae-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="177ae-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="177ae-135">See also</span></span>

- [<span data-ttu-id="177ae-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="177ae-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

