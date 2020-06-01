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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 8a58444580c803efb7312df95d75d697bc42e8e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461840"
---
# <a name="messagesnapshot"></a><span data-ttu-id="181e7-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="181e7-103">messageSnapshot</span></span>

<span data-ttu-id="181e7-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="181e7-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="181e7-105">**MessageSnapshot**元素包含一个属性，该属性指定是否为已安装客户端访问或邮箱服务器角色的 Exchange 服务器启用管道跟踪功能。</span><span class="sxs-lookup"><span data-stu-id="181e7-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="181e7-106">configuration</span><span class="sxs-lookup"><span data-stu-id="181e7-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="181e7-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="181e7-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="181e7-108">监视</span><span class="sxs-lookup"><span data-stu-id="181e7-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="181e7-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="181e7-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="181e7-110">**messageSnapshotType （布尔值）**</span><span class="sxs-lookup"><span data-stu-id="181e7-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="181e7-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="181e7-111">Attributes and elements</span></span>

<span data-ttu-id="181e7-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="181e7-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="181e7-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="181e7-113">Attributes</span></span>

|<span data-ttu-id="181e7-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="181e7-114">**Attribute**</span></span>|<span data-ttu-id="181e7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="181e7-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="181e7-116">**enabled**</span><span class="sxs-lookup"><span data-stu-id="181e7-116">**enabled**</span></span> <br/> |<span data-ttu-id="181e7-117">一个布尔值，指示是否为客户端访问或邮箱服务器启用管道跟踪功能。</span><span class="sxs-lookup"><span data-stu-id="181e7-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="181e7-118">如果启用管道跟踪，则此值为**true** ; 否则为 false。否则，该值为**false**或元素不存在。</span><span class="sxs-lookup"><span data-stu-id="181e7-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="181e7-119">子元素</span><span class="sxs-lookup"><span data-stu-id="181e7-119">Child elements</span></span>

<span data-ttu-id="181e7-120">无。</span><span class="sxs-lookup"><span data-stu-id="181e7-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="181e7-121">父元素</span><span class="sxs-lookup"><span data-stu-id="181e7-121">Parent elements</span></span>

|<span data-ttu-id="181e7-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="181e7-122">**Element**</span></span>|<span data-ttu-id="181e7-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="181e7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="181e7-124">监视</span><span class="sxs-lookup"><span data-stu-id="181e7-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="181e7-125">包含定义传输服务如何以及何时监视安装的代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="181e7-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="181e7-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="181e7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="181e7-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="181e7-127">Namespace</span></span>  <br/> |<span data-ttu-id="181e7-128">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="181e7-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="181e7-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="181e7-129">Schema Name</span></span>  <br/> |<span data-ttu-id="181e7-130">不可用。</span><span class="sxs-lookup"><span data-stu-id="181e7-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="181e7-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="181e7-131">Validation File</span></span>  <br/> |<span data-ttu-id="181e7-132">不可用。</span><span class="sxs-lookup"><span data-stu-id="181e7-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="181e7-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="181e7-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="181e7-134">不正确。</span><span class="sxs-lookup"><span data-stu-id="181e7-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="181e7-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="181e7-135">See also</span></span>

- [<span data-ttu-id="181e7-136">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="181e7-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

