---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 5848d52a68c8c3f747614015e49becb34bc4cfd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753051"
---
# <a name="agentexecution"></a><span data-ttu-id="73be3-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="73be3-103">agentExecution</span></span>
  
<span data-ttu-id="73be3-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="73be3-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="73be3-105">**AgentExecution**元素定义时间，以毫秒为单位，等待代理以从事件之前它写入事件日志中返回客户端访问或邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="73be3-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="73be3-106">configuration</span><span class="sxs-lookup"><span data-stu-id="73be3-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="73be3-107">监控</span><span class="sxs-lookup"><span data-stu-id="73be3-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="73be3-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="73be3-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="73be3-109">**agentExecutionType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="73be3-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="73be3-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="73be3-110">Attributes and elements</span></span>

<span data-ttu-id="73be3-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="73be3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73be3-112">属性</span><span class="sxs-lookup"><span data-stu-id="73be3-112">Attributes</span></span>

|<span data-ttu-id="73be3-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="73be3-113">**Attribute**</span></span>|<span data-ttu-id="73be3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="73be3-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73be3-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="73be3-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="73be3-116">正整数值，该值指定时间，以毫秒为单位，服务器等待代理以从之前的事件返回事件日志中写入一条警告。</span><span class="sxs-lookup"><span data-stu-id="73be3-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="73be3-117">如果此值太小，可能会降低性能。</span><span class="sxs-lookup"><span data-stu-id="73be3-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="73be3-118">此属性的建议的值为 300000，其等于 5 分钟。</span><span class="sxs-lookup"><span data-stu-id="73be3-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73be3-119">子元素</span><span class="sxs-lookup"><span data-stu-id="73be3-119">Child elements</span></span>

<span data-ttu-id="73be3-120">无。</span><span class="sxs-lookup"><span data-stu-id="73be3-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73be3-121">父元素</span><span class="sxs-lookup"><span data-stu-id="73be3-121">Parent elements</span></span>

|<span data-ttu-id="73be3-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="73be3-122">**Element**</span></span>|<span data-ttu-id="73be3-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="73be3-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73be3-124">监控</span><span class="sxs-lookup"><span data-stu-id="73be3-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="73be3-125">包含定义如何以及何时前端传输服务或的传输服务监视安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="73be3-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="73be3-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="73be3-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73be3-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="73be3-127">Namespace</span></span>  <br/> |<span data-ttu-id="73be3-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="73be3-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="73be3-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="73be3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="73be3-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="73be3-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="73be3-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="73be3-131">Validation File</span></span>  <br/> |<span data-ttu-id="73be3-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="73be3-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="73be3-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="73be3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="73be3-134">False。</span><span class="sxs-lookup"><span data-stu-id="73be3-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73be3-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73be3-135">See also</span></span>

- [<span data-ttu-id="73be3-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="73be3-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

