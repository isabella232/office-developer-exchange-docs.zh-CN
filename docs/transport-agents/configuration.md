---
title: configuration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 342e52e879534b6a130d286d358138c6095e4563
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753055"
---
# <a name="configuration"></a><span data-ttu-id="d003b-103">configuration</span><span class="sxs-lookup"><span data-stu-id="d003b-103">configuration</span></span>
  
<span data-ttu-id="d003b-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="d003b-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="d003b-105">**Configuration**元素是代理的配置文件的根元素。</span><span class="sxs-lookup"><span data-stu-id="d003b-105">The **configuration** element is the root element for the agents configuration file.</span></span> 
  
- [<span data-ttu-id="d003b-106">configuration</span><span class="sxs-lookup"><span data-stu-id="d003b-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="d003b-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="d003b-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

<span data-ttu-id="d003b-108">**configurationType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="d003b-108">**configurationType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d003b-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d003b-109">Attributes and elements</span></span>

<span data-ttu-id="d003b-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d003b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d003b-111">属性</span><span class="sxs-lookup"><span data-stu-id="d003b-111">Attributes</span></span>

<span data-ttu-id="d003b-112">无。</span><span class="sxs-lookup"><span data-stu-id="d003b-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d003b-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d003b-113">Child elements</span></span>

|<span data-ttu-id="d003b-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="d003b-114">**Element**</span></span>|<span data-ttu-id="d003b-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="d003b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d003b-116">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="d003b-116">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="d003b-117">包含定义监控代理的配置信息和 SMTP 和安装的路由代理的配置信息的元素。</span><span class="sxs-lookup"><span data-stu-id="d003b-117">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d003b-118">父元素</span><span class="sxs-lookup"><span data-stu-id="d003b-118">Parent elements</span></span>

<span data-ttu-id="d003b-119">无。</span><span class="sxs-lookup"><span data-stu-id="d003b-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d003b-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="d003b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d003b-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="d003b-121">Namespace</span></span>  <br/> |<span data-ttu-id="d003b-122">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="d003b-122">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="d003b-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d003b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d003b-124">不可用。</span><span class="sxs-lookup"><span data-stu-id="d003b-124">Not available.</span></span>  <br/> |
|<span data-ttu-id="d003b-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d003b-125">Validation File</span></span>  <br/> |<span data-ttu-id="d003b-126">不可用。</span><span class="sxs-lookup"><span data-stu-id="d003b-126">Not available.</span></span>  <br/> |
|<span data-ttu-id="d003b-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d003b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d003b-128">False。</span><span class="sxs-lookup"><span data-stu-id="d003b-128">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d003b-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d003b-129">See also</span></span>

- [<span data-ttu-id="d003b-130">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="d003b-130">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

