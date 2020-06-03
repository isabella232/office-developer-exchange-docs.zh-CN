---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: PhoneCallState 元素指定电话呼叫的当前状态。
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468528"
---
# <a name="phonecallstate"></a><span data-ttu-id="15dc3-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="15dc3-103">PhoneCallState</span></span>

<span data-ttu-id="15dc3-104">**PhoneCallState**元素指定电话呼叫的当前状态。</span><span class="sxs-lookup"><span data-stu-id="15dc3-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="15dc3-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="15dc3-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15dc3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15dc3-106">Attributes and elements</span></span>

<span data-ttu-id="15dc3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15dc3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15dc3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="15dc3-108">Attributes</span></span>

<span data-ttu-id="15dc3-109">无。</span><span class="sxs-lookup"><span data-stu-id="15dc3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15dc3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15dc3-110">Child elements</span></span>

<span data-ttu-id="15dc3-111">无。</span><span class="sxs-lookup"><span data-stu-id="15dc3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15dc3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="15dc3-112">Parent elements</span></span>

|<span data-ttu-id="15dc3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="15dc3-113">**Element**</span></span>|<span data-ttu-id="15dc3-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="15dc3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15dc3-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="15dc3-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="15dc3-116">指定电话呼叫的状态信息。</span><span class="sxs-lookup"><span data-stu-id="15dc3-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15dc3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="15dc3-117">Text value</span></span>

<span data-ttu-id="15dc3-118">下表列出了**PhoneCallState**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="15dc3-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="15dc3-119">**PhoneCallState 元素值**</span><span class="sxs-lookup"><span data-stu-id="15dc3-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="15dc3-120">**值**</span><span class="sxs-lookup"><span data-stu-id="15dc3-120">**Value**</span></span>|<span data-ttu-id="15dc3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="15dc3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15dc3-122">待机</span><span class="sxs-lookup"><span data-stu-id="15dc3-122">Idle</span></span>  <br/> |<span data-ttu-id="15dc3-123">初始呼叫状态。</span><span class="sxs-lookup"><span data-stu-id="15dc3-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="15dc3-124">正在连接</span><span class="sxs-lookup"><span data-stu-id="15dc3-124">Connecting</span></span>  <br/> |<span data-ttu-id="15dc3-125">系统正在拨打此呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc3-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="15dc3-126">收到</span><span class="sxs-lookup"><span data-stu-id="15dc3-126">Alerted</span></span>  <br/> |<span data-ttu-id="15dc3-127">呼叫处于 "警报" 状态（电话正在响铃）。</span><span class="sxs-lookup"><span data-stu-id="15dc3-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="15dc3-128">已连接</span><span class="sxs-lookup"><span data-stu-id="15dc3-128">Connected</span></span>  <br/> |<span data-ttu-id="15dc3-129">该呼叫处于 "已连接" 状态。</span><span class="sxs-lookup"><span data-stu-id="15dc3-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="15dc3-130">已断开连接</span><span class="sxs-lookup"><span data-stu-id="15dc3-130">Disconnected</span></span>  <br/> |<span data-ttu-id="15dc3-131">呼叫已断开连接。</span><span class="sxs-lookup"><span data-stu-id="15dc3-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="15dc3-132">即将</span><span class="sxs-lookup"><span data-stu-id="15dc3-132">Incoming</span></span>  <br/> |<span data-ttu-id="15dc3-133">呼叫为入站。</span><span class="sxs-lookup"><span data-stu-id="15dc3-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="15dc3-134">传输</span><span class="sxs-lookup"><span data-stu-id="15dc3-134">Transferring</span></span>  <br/> |<span data-ttu-id="15dc3-135">正在将呼叫转接到另一个目的地。</span><span class="sxs-lookup"><span data-stu-id="15dc3-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="15dc3-136">发送</span><span class="sxs-lookup"><span data-stu-id="15dc3-136">Forwarding</span></span>  <br/> |<span data-ttu-id="15dc3-137">将呼叫转接到另一个目的地。</span><span class="sxs-lookup"><span data-stu-id="15dc3-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15dc3-138">备注</span><span class="sxs-lookup"><span data-stu-id="15dc3-138">Remarks</span></span>

<span data-ttu-id="15dc3-139">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的/ews/目录中。</span><span class="sxs-lookup"><span data-stu-id="15dc3-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15dc3-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="15dc3-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15dc3-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="15dc3-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15dc3-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="15dc3-142">Schema Name</span></span>  <br/> |<span data-ttu-id="15dc3-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="15dc3-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="15dc3-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="15dc3-144">Validation File</span></span>  <br/> |<span data-ttu-id="15dc3-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="15dc3-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15dc3-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="15dc3-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="15dc3-147">False</span><span class="sxs-lookup"><span data-stu-id="15dc3-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15dc3-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15dc3-148">See also</span></span>



- [<span data-ttu-id="15dc3-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15dc3-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

