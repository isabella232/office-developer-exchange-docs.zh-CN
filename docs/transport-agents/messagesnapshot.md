---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753082"
---
# <a name="messagesnapshot"></a><span data-ttu-id="aba03-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="aba03-103">messageSnapshot</span></span>

<span data-ttu-id="aba03-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="aba03-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="aba03-105">**MessageSnapshot**元素包含指定是否具有客户端访问或安装了邮箱服务器角色的 Exchange 服务器启用管道跟踪功能属性。</span><span class="sxs-lookup"><span data-stu-id="aba03-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="aba03-106">configuration</span><span class="sxs-lookup"><span data-stu-id="aba03-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="aba03-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="aba03-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="aba03-108">监控</span><span class="sxs-lookup"><span data-stu-id="aba03-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="aba03-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="aba03-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="aba03-110">**messageSnapshotType （布尔值）**</span><span class="sxs-lookup"><span data-stu-id="aba03-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="aba03-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aba03-111">Attributes and elements</span></span>

<span data-ttu-id="aba03-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aba03-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aba03-113">属性</span><span class="sxs-lookup"><span data-stu-id="aba03-113">Attributes</span></span>

|<span data-ttu-id="aba03-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="aba03-114">**Attribute**</span></span>|<span data-ttu-id="aba03-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="aba03-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aba03-116">**启用**</span><span class="sxs-lookup"><span data-stu-id="aba03-116">**enabled**</span></span> <br/> |<span data-ttu-id="aba03-117">一个布尔值，该值指示是否为客户端访问或邮箱服务器启用管道跟踪功能。</span><span class="sxs-lookup"><span data-stu-id="aba03-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="aba03-118">如果启用管道跟踪，则值为**true**否则为值为**false**或不存在元素。</span><span class="sxs-lookup"><span data-stu-id="aba03-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aba03-119">子元素</span><span class="sxs-lookup"><span data-stu-id="aba03-119">Child elements</span></span>

<span data-ttu-id="aba03-120">无。</span><span class="sxs-lookup"><span data-stu-id="aba03-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aba03-121">父元素</span><span class="sxs-lookup"><span data-stu-id="aba03-121">Parent elements</span></span>

|<span data-ttu-id="aba03-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="aba03-122">**Element**</span></span>|<span data-ttu-id="aba03-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="aba03-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aba03-124">监控</span><span class="sxs-lookup"><span data-stu-id="aba03-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="aba03-125">包含定义如何以及何时的传输服务将监视安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="aba03-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="aba03-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="aba03-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aba03-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="aba03-127">Namespace</span></span>  <br/> |<span data-ttu-id="aba03-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="aba03-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="aba03-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="aba03-129">Schema Name</span></span>  <br/> |<span data-ttu-id="aba03-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="aba03-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="aba03-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="aba03-131">Validation File</span></span>  <br/> |<span data-ttu-id="aba03-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="aba03-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="aba03-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="aba03-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="aba03-134">False。</span><span class="sxs-lookup"><span data-stu-id="aba03-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aba03-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aba03-135">See also</span></span>

- [<span data-ttu-id="aba03-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="aba03-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

