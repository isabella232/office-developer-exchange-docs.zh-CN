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
description: PhoneCallState 元素指定的电话呼叫的当前状态。
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826761"
---
# <a name="phonecallstate"></a><span data-ttu-id="a6d58-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="a6d58-103">PhoneCallState</span></span>

<span data-ttu-id="a6d58-104">**PhoneCallState**元素指定的电话呼叫的当前状态。</span><span class="sxs-lookup"><span data-stu-id="a6d58-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="a6d58-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="a6d58-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6d58-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6d58-106">Attributes and elements</span></span>

<span data-ttu-id="a6d58-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6d58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6d58-108">属性</span><span class="sxs-lookup"><span data-stu-id="a6d58-108">Attributes</span></span>

<span data-ttu-id="a6d58-109">无。</span><span class="sxs-lookup"><span data-stu-id="a6d58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6d58-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a6d58-110">Child elements</span></span>

<span data-ttu-id="a6d58-111">无。</span><span class="sxs-lookup"><span data-stu-id="a6d58-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6d58-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a6d58-112">Parent elements</span></span>

|<span data-ttu-id="a6d58-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6d58-113">**Element**</span></span>|<span data-ttu-id="a6d58-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6d58-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6d58-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="a6d58-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="a6d58-116">指定的电话的状态信息。</span><span class="sxs-lookup"><span data-stu-id="a6d58-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6d58-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a6d58-117">Text value</span></span>

<span data-ttu-id="a6d58-118">下表列出了**PhoneCallState**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="a6d58-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="a6d58-119">**PhoneCallState 元素的值**</span><span class="sxs-lookup"><span data-stu-id="a6d58-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="a6d58-120">**值**</span><span class="sxs-lookup"><span data-stu-id="a6d58-120">**Value**</span></span>|<span data-ttu-id="a6d58-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6d58-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6d58-122">空闲时间</span><span class="sxs-lookup"><span data-stu-id="a6d58-122">Idle</span></span>  <br/> |<span data-ttu-id="a6d58-123">初始呼叫状态。</span><span class="sxs-lookup"><span data-stu-id="a6d58-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="a6d58-124">正在连接</span><span class="sxs-lookup"><span data-stu-id="a6d58-124">Connecting</span></span>  <br/> |<span data-ttu-id="a6d58-125">系统为拨打此呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6d58-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="a6d58-126">收到通知</span><span class="sxs-lookup"><span data-stu-id="a6d58-126">Alerted</span></span>  <br/> |<span data-ttu-id="a6d58-127">警报状态正在呼叫 （电话响铃）。</span><span class="sxs-lookup"><span data-stu-id="a6d58-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="a6d58-128">已连接</span><span class="sxs-lookup"><span data-stu-id="a6d58-128">Connected</span></span>  <br/> |<span data-ttu-id="a6d58-129">呼叫处于连接状态。</span><span class="sxs-lookup"><span data-stu-id="a6d58-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="a6d58-130">已断开连接</span><span class="sxs-lookup"><span data-stu-id="a6d58-130">Disconnected</span></span>  <br/> |<span data-ttu-id="a6d58-131">将断开呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6d58-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="a6d58-132">传入</span><span class="sxs-lookup"><span data-stu-id="a6d58-132">Incoming</span></span>  <br/> |<span data-ttu-id="a6d58-133">入站呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6d58-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="a6d58-134">转接</span><span class="sxs-lookup"><span data-stu-id="a6d58-134">Transferring</span></span>  <br/> |<span data-ttu-id="a6d58-135">呼叫被转接至其他目标。</span><span class="sxs-lookup"><span data-stu-id="a6d58-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="a6d58-136">转接</span><span class="sxs-lookup"><span data-stu-id="a6d58-136">Forwarding</span></span>  <br/> |<span data-ttu-id="a6d58-137">是要将呼叫转接至其他目标。</span><span class="sxs-lookup"><span data-stu-id="a6d58-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6d58-138">注解</span><span class="sxs-lookup"><span data-stu-id="a6d58-138">Remarks</span></span>

<span data-ttu-id="a6d58-139">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 /ews/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="a6d58-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6d58-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6d58-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6d58-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6d58-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6d58-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6d58-142">Schema Name</span></span>  <br/> |<span data-ttu-id="a6d58-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="a6d58-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6d58-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6d58-144">Validation File</span></span>  <br/> |<span data-ttu-id="a6d58-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6d58-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6d58-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6d58-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6d58-147">False</span><span class="sxs-lookup"><span data-stu-id="a6d58-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6d58-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6d58-148">See also</span></span>



- [<span data-ttu-id="a6d58-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a6d58-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

