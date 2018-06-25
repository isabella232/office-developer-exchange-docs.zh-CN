---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: ConnectionFailureCause 元素指定从电话呼叫断开连接的原因。
ms.openlocfilehash: 54b4f5b89efdb42ef82dbef8f1af14a39c0ccc6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753484"
---
# <a name="connectionfailurecause"></a><span data-ttu-id="98622-103">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="98622-103">ConnectionFailureCause</span></span>

<span data-ttu-id="98622-104">**ConnectionFailureCause**元素指定从电话呼叫断开连接的原因。</span><span class="sxs-lookup"><span data-stu-id="98622-104">The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call.</span></span> 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 <span data-ttu-id="98622-105">**ConnectionFailureCauseType**</span><span class="sxs-lookup"><span data-stu-id="98622-105">**ConnectionFailureCauseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98622-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="98622-106">Attributes and elements</span></span>

<span data-ttu-id="98622-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="98622-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98622-108">属性</span><span class="sxs-lookup"><span data-stu-id="98622-108">Attributes</span></span>

<span data-ttu-id="98622-109">无。</span><span class="sxs-lookup"><span data-stu-id="98622-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98622-110">子元素</span><span class="sxs-lookup"><span data-stu-id="98622-110">Child elements</span></span>

<span data-ttu-id="98622-111">无。</span><span class="sxs-lookup"><span data-stu-id="98622-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="98622-112">父元素</span><span class="sxs-lookup"><span data-stu-id="98622-112">Parent elements</span></span>

|<span data-ttu-id="98622-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="98622-113">**Element**</span></span>|<span data-ttu-id="98622-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="98622-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98622-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="98622-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="98622-116">指定电话呼叫的状态的信息。</span><span class="sxs-lookup"><span data-stu-id="98622-116">Specifies the state information for a telephone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98622-117">文本值</span><span class="sxs-lookup"><span data-stu-id="98622-117">Text value</span></span>

<span data-ttu-id="98622-118">下表列出了**ConnectionFailureCause**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="98622-118">The following table lists the possible values for the **ConnectionFailureCause** element.</span></span> 
  
<span data-ttu-id="98622-119">**ConnectionFailureCause 元素的值**</span><span class="sxs-lookup"><span data-stu-id="98622-119">**ConnectionFailureCause element values**</span></span>

|<span data-ttu-id="98622-120">**值**</span><span class="sxs-lookup"><span data-stu-id="98622-120">**Value**</span></span>|<span data-ttu-id="98622-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="98622-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98622-122">无</span><span class="sxs-lookup"><span data-stu-id="98622-122">None</span></span>  <br/> |<span data-ttu-id="98622-123">不断开连接的呼叫状态或不知道断开原因。</span><span class="sxs-lookup"><span data-stu-id="98622-123">Call state is not disconnected or the disconnect reason is not known.</span></span>  <br/> |
|<span data-ttu-id="98622-124">UserBusy</span><span class="sxs-lookup"><span data-stu-id="98622-124">UserBusy</span></span>  <br/> |<span data-ttu-id="98622-125">呼叫的方线路繁忙。</span><span class="sxs-lookup"><span data-stu-id="98622-125">The called party line was busy.</span></span>  <br/> |
|<span data-ttu-id="98622-126">NoAnswer</span><span class="sxs-lookup"><span data-stu-id="98622-126">NoAnswer</span></span>  <br/> |<span data-ttu-id="98622-127">呼叫的方没有应答。</span><span class="sxs-lookup"><span data-stu-id="98622-127">The called party did not answer.</span></span>  <br/> |
|<span data-ttu-id="98622-128">不可用</span><span class="sxs-lookup"><span data-stu-id="98622-128">Unavailable</span></span>  <br/> |<span data-ttu-id="98622-129">呼叫的方号码不可用。</span><span class="sxs-lookup"><span data-stu-id="98622-129">The called party number was not available.</span></span>  <br/> |
|<span data-ttu-id="98622-130">其他</span><span class="sxs-lookup"><span data-stu-id="98622-130">Other</span></span>  <br/> |<span data-ttu-id="98622-131">全包式其他断开连接的原因。</span><span class="sxs-lookup"><span data-stu-id="98622-131">Catch-all for other disconnect reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98622-132">备注</span><span class="sxs-lookup"><span data-stu-id="98622-132">Remarks</span></span>

<span data-ttu-id="98622-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="98622-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98622-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="98622-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98622-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="98622-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98622-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="98622-136">Schema Name</span></span>  <br/> |<span data-ttu-id="98622-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="98622-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="98622-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="98622-138">Validation File</span></span>  <br/> |<span data-ttu-id="98622-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="98622-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="98622-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="98622-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="98622-141">False</span><span class="sxs-lookup"><span data-stu-id="98622-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98622-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98622-142">See also</span></span>



- [<span data-ttu-id="98622-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="98622-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

