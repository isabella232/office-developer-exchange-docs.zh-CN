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
description: ConnectionTimeout 元素指定保持连接打开的分钟数。
ms.openlocfilehash: 671e3cf5466ee8b3543036811708bd7f54afdcce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463851"
---
# <a name="connectiontimeout"></a><span data-ttu-id="95273-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="95273-103">ConnectionTimeout</span></span>

<span data-ttu-id="95273-104">**ConnectionTimeout**元素指定保持连接打开的分钟数。</span><span class="sxs-lookup"><span data-stu-id="95273-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="95273-105">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="95273-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="95273-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="95273-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="95273-107">**int**</span><span class="sxs-lookup"><span data-stu-id="95273-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95273-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95273-108">Attributes and elements</span></span>

<span data-ttu-id="95273-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95273-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95273-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="95273-110">Attributes</span></span>

<span data-ttu-id="95273-111">无。</span><span class="sxs-lookup"><span data-stu-id="95273-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95273-112">子元素</span><span class="sxs-lookup"><span data-stu-id="95273-112">Child elements</span></span>

<span data-ttu-id="95273-113">无。</span><span class="sxs-lookup"><span data-stu-id="95273-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95273-114">父元素</span><span class="sxs-lookup"><span data-stu-id="95273-114">Parent elements</span></span>

|<span data-ttu-id="95273-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="95273-115">**Element**</span></span>|<span data-ttu-id="95273-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="95273-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95273-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="95273-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="95273-118">定义从流式连接获取事件通知的请求。</span><span class="sxs-lookup"><span data-stu-id="95273-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95273-119">文本值</span><span class="sxs-lookup"><span data-stu-id="95273-119">Text value</span></span>

<span data-ttu-id="95273-120">该文本值表示一个整数，该整数描述将流式连接保持打开状态的最长时间（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="95273-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="95273-121">值必须介于1和30之间（含这两个值）。</span><span class="sxs-lookup"><span data-stu-id="95273-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95273-122">备注</span><span class="sxs-lookup"><span data-stu-id="95273-122">Remarks</span></span>

<span data-ttu-id="95273-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="95273-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95273-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="95273-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95273-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="95273-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95273-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="95273-126">Schema name</span></span>  <br/> |<span data-ttu-id="95273-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="95273-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="95273-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="95273-128">Validation file</span></span>  <br/> |<span data-ttu-id="95273-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95273-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95273-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="95273-130">Can be empty</span></span>  <br/> |<span data-ttu-id="95273-131">False</span><span class="sxs-lookup"><span data-stu-id="95273-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95273-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95273-132">See also</span></span>



[<span data-ttu-id="95273-133">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="95273-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="95273-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95273-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

