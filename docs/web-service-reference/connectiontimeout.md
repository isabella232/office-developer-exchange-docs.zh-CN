---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: ConnectionTimeout 元素指定要保持连接处于打开状态的分钟数。
ms.openlocfilehash: 2bb40ba502853c70ef107c4c740fdfe7073abe31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753485"
---
# <a name="connectiontimeout"></a><span data-ttu-id="11dcb-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="11dcb-103">ConnectionTimeout</span></span>

<span data-ttu-id="11dcb-104">**ConnectionTimeout**元素指定要保持连接处于打开状态的分钟数。</span><span class="sxs-lookup"><span data-stu-id="11dcb-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="11dcb-105">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="11dcb-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="11dcb-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="11dcb-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="11dcb-107">**int**</span><span class="sxs-lookup"><span data-stu-id="11dcb-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11dcb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11dcb-108">Attributes and elements</span></span>

<span data-ttu-id="11dcb-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11dcb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11dcb-110">属性</span><span class="sxs-lookup"><span data-stu-id="11dcb-110">Attributes</span></span>

<span data-ttu-id="11dcb-111">无。</span><span class="sxs-lookup"><span data-stu-id="11dcb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11dcb-112">子元素</span><span class="sxs-lookup"><span data-stu-id="11dcb-112">Child elements</span></span>

<span data-ttu-id="11dcb-113">无。</span><span class="sxs-lookup"><span data-stu-id="11dcb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11dcb-114">父元素</span><span class="sxs-lookup"><span data-stu-id="11dcb-114">Parent elements</span></span>

|<span data-ttu-id="11dcb-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="11dcb-115">**Element**</span></span>|<span data-ttu-id="11dcb-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="11dcb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11dcb-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="11dcb-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="11dcb-118">定义一个请求以获取从流式连接的事件通知。</span><span class="sxs-lookup"><span data-stu-id="11dcb-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11dcb-119">文本值</span><span class="sxs-lookup"><span data-stu-id="11dcb-119">Text value</span></span>

<span data-ttu-id="11dcb-120">文本值表示一个整数，描述的最大分钟时间来保持打开状态的流式连接数。</span><span class="sxs-lookup"><span data-stu-id="11dcb-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="11dcb-121">值必须是介于 1 到 30，非独占之间。</span><span class="sxs-lookup"><span data-stu-id="11dcb-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11dcb-122">备注</span><span class="sxs-lookup"><span data-stu-id="11dcb-122">Remarks</span></span>

<span data-ttu-id="11dcb-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="11dcb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11dcb-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="11dcb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11dcb-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="11dcb-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11dcb-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="11dcb-126">Schema name</span></span>  <br/> |<span data-ttu-id="11dcb-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="11dcb-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="11dcb-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="11dcb-128">Validation file</span></span>  <br/> |<span data-ttu-id="11dcb-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11dcb-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11dcb-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="11dcb-130">Can be empty</span></span>  <br/> |<span data-ttu-id="11dcb-131">False</span><span class="sxs-lookup"><span data-stu-id="11dcb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11dcb-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="11dcb-132">See also</span></span>



[<span data-ttu-id="11dcb-133">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="11dcb-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="11dcb-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="11dcb-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

