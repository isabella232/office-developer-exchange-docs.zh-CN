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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44446488"
---
# <a name="agentexecution"></a><span data-ttu-id="e3599-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="e3599-103">agentExecution</span></span>
  
<span data-ttu-id="e3599-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3599-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="e3599-105">**AgentExecution**元素定义客户端访问或邮箱服务器等待代理在写入事件日志之前从事件返回的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="e3599-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="e3599-106">configuration</span><span class="sxs-lookup"><span data-stu-id="e3599-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="e3599-107">监视</span><span class="sxs-lookup"><span data-stu-id="e3599-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="e3599-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="e3599-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="e3599-109">**agentExecutionType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="e3599-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e3599-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3599-110">Attributes and elements</span></span>

<span data-ttu-id="e3599-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3599-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3599-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3599-112">Attributes</span></span>

|<span data-ttu-id="e3599-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="e3599-113">**Attribute**</span></span>|<span data-ttu-id="e3599-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3599-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3599-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="e3599-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="e3599-116">一个正整数值，指定服务器在将警告写入事件日志之前等待代理从事件返回的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="e3599-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="e3599-117">如果此值太小，则性能可能会降低。</span><span class="sxs-lookup"><span data-stu-id="e3599-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="e3599-118">此属性的建议值为300000，相当于5分钟。</span><span class="sxs-lookup"><span data-stu-id="e3599-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e3599-119">子元素</span><span class="sxs-lookup"><span data-stu-id="e3599-119">Child elements</span></span>

<span data-ttu-id="e3599-120">无。</span><span class="sxs-lookup"><span data-stu-id="e3599-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3599-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e3599-121">Parent elements</span></span>

|<span data-ttu-id="e3599-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3599-122">**Element**</span></span>|<span data-ttu-id="e3599-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3599-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3599-124">监视</span><span class="sxs-lookup"><span data-stu-id="e3599-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="e3599-125">包含定义前端传输服务或传输服务如何以及何时监视安装的代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="e3599-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e3599-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3599-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3599-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3599-127">Namespace</span></span>  <br/> |<span data-ttu-id="e3599-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="e3599-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="e3599-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3599-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e3599-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="e3599-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="e3599-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3599-131">Validation File</span></span>  <br/> |<span data-ttu-id="e3599-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="e3599-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="e3599-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3599-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3599-134">不正确。</span><span class="sxs-lookup"><span data-stu-id="e3599-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3599-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3599-135">See also</span></span>

- [<span data-ttu-id="e3599-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="e3599-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

