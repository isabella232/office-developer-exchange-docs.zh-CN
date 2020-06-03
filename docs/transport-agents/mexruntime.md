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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: f192965a8375eb46d1ca5b46d3b768a3299c284d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461833"
---
# <a name="mexruntime"></a><span data-ttu-id="d9f2c-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="d9f2c-103">mexRuntime</span></span>
  
<span data-ttu-id="d9f2c-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9f2c-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="d9f2c-105">**MexRuntime**元素包含定义代理监视的配置信息和安装的 SMTP 和路由代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="d9f2c-106">configuration</span><span class="sxs-lookup"><span data-stu-id="d9f2c-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="d9f2c-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="d9f2c-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="d9f2c-108">**mexRuntimeType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="d9f2c-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d9f2c-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9f2c-109">Attributes and elements</span></span>

<span data-ttu-id="d9f2c-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9f2c-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="d9f2c-111">Attributes</span></span>

<span data-ttu-id="d9f2c-112">无。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9f2c-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d9f2c-113">Child elements</span></span>

|<span data-ttu-id="d9f2c-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9f2c-114">**Element**</span></span>|<span data-ttu-id="d9f2c-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9f2c-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9f2c-116">监视</span><span class="sxs-lookup"><span data-stu-id="d9f2c-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="d9f2c-117">包含定义如何以及何时安装的传输监视器代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="d9f2c-118">agentList</span><span class="sxs-lookup"><span data-stu-id="d9f2c-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="d9f2c-119">包含已安装的每个代理的[代理](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9f2c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="d9f2c-120">Parent elements</span></span>

|<span data-ttu-id="d9f2c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9f2c-121">**Element**</span></span>|<span data-ttu-id="d9f2c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9f2c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9f2c-123">configuration</span><span class="sxs-lookup"><span data-stu-id="d9f2c-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="d9f2c-124">代理配置文件的根元素。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d9f2c-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9f2c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9f2c-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9f2c-126">Namespace</span></span>  <br/> |<span data-ttu-id="d9f2c-127">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="d9f2c-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9f2c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d9f2c-129">不可用。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="d9f2c-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9f2c-130">Validation File</span></span>  <br/> |<span data-ttu-id="d9f2c-131">不可用。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="d9f2c-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9f2c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9f2c-133">不正确。</span><span class="sxs-lookup"><span data-stu-id="d9f2c-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9f2c-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9f2c-134">See also</span></span>

- [<span data-ttu-id="d9f2c-135">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="d9f2c-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

