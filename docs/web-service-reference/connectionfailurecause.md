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
ms.openlocfilehash: 6385641eaee140a114906703232974d51d5ce344
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529446"
---
# <a name="connectionfailurecause"></a><span data-ttu-id="ff036-103">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="ff036-103">ConnectionFailureCause</span></span>

<span data-ttu-id="ff036-104">**ConnectionFailureCause**元素指定从电话呼叫断开连接的原因。</span><span class="sxs-lookup"><span data-stu-id="ff036-104">The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call.</span></span> 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 <span data-ttu-id="ff036-105">**ConnectionFailureCauseType**</span><span class="sxs-lookup"><span data-stu-id="ff036-105">**ConnectionFailureCauseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff036-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ff036-106">Attributes and elements</span></span>

<span data-ttu-id="ff036-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ff036-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff036-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ff036-108">Attributes</span></span>

<span data-ttu-id="ff036-109">无。</span><span class="sxs-lookup"><span data-stu-id="ff036-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff036-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ff036-110">Child elements</span></span>

<span data-ttu-id="ff036-111">无。</span><span class="sxs-lookup"><span data-stu-id="ff036-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ff036-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ff036-112">Parent elements</span></span>

|<span data-ttu-id="ff036-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff036-113">**Element**</span></span>|<span data-ttu-id="ff036-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="ff036-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff036-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="ff036-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="ff036-116">指定电话呼叫的状态信息。</span><span class="sxs-lookup"><span data-stu-id="ff036-116">Specifies the state information for a telephone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff036-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ff036-117">Text value</span></span>

<span data-ttu-id="ff036-118">下表列出了**ConnectionFailureCause**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="ff036-118">The following table lists the possible values for the **ConnectionFailureCause** element.</span></span> 
  
<span data-ttu-id="ff036-119">**ConnectionFailureCause 元素值**</span><span class="sxs-lookup"><span data-stu-id="ff036-119">**ConnectionFailureCause element values**</span></span>

|<span data-ttu-id="ff036-120">**值**</span><span class="sxs-lookup"><span data-stu-id="ff036-120">**Value**</span></span>|<span data-ttu-id="ff036-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff036-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff036-122">无</span><span class="sxs-lookup"><span data-stu-id="ff036-122">None</span></span>  <br/> |<span data-ttu-id="ff036-123">呼叫状态不会断开连接，或者断开连接的原因未知。</span><span class="sxs-lookup"><span data-stu-id="ff036-123">Call state is not disconnected or the disconnect reason is not known.</span></span>  <br/> |
|<span data-ttu-id="ff036-124">UserBusy</span><span class="sxs-lookup"><span data-stu-id="ff036-124">UserBusy</span></span>  <br/> |<span data-ttu-id="ff036-125">呼叫方线路正忙。</span><span class="sxs-lookup"><span data-stu-id="ff036-125">The called party line was busy.</span></span>  <br/> |
|<span data-ttu-id="ff036-126">NoAnswer</span><span class="sxs-lookup"><span data-stu-id="ff036-126">NoAnswer</span></span>  <br/> |<span data-ttu-id="ff036-127">被叫方没有应答。</span><span class="sxs-lookup"><span data-stu-id="ff036-127">The called party did not answer.</span></span>  <br/> |
|<span data-ttu-id="ff036-128">才</span><span class="sxs-lookup"><span data-stu-id="ff036-128">Unavailable</span></span>  <br/> |<span data-ttu-id="ff036-129">被叫方号码不可用。</span><span class="sxs-lookup"><span data-stu-id="ff036-129">The called party number was not available.</span></span>  <br/> |
|<span data-ttu-id="ff036-130">其他</span><span class="sxs-lookup"><span data-stu-id="ff036-130">Other</span></span>  <br/> |<span data-ttu-id="ff036-131">捕捉-all 用于其他断开连接的原因。</span><span class="sxs-lookup"><span data-stu-id="ff036-131">Catch-all for other disconnect reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff036-132">说明</span><span class="sxs-lookup"><span data-stu-id="ff036-132">Remarks</span></span>

<span data-ttu-id="ff036-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ff036-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff036-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="ff036-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff036-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="ff036-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff036-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="ff036-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ff036-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="ff036-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff036-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="ff036-138">Validation File</span></span>  <br/> |<span data-ttu-id="ff036-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff036-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff036-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="ff036-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff036-141">False</span><span class="sxs-lookup"><span data-stu-id="ff036-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff036-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff036-142">See also</span></span>



- [<span data-ttu-id="ff036-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ff036-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

