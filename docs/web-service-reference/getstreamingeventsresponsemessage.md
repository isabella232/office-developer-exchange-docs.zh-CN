---
title: GetStreamingEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEventsResponseMessage
api_type:
- schema
ms.assetid: 655e4e78-af74-48b0-a988-7d86ab368feb
description: GetStreamingEventsResponseMessage 元素包含单个 GetStreamingEvents 操作请求的状态和结果。
ms.openlocfilehash: 055fb7eeb12e241739eb860cecbe398b8a322bd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459144"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="c1c83-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c1c83-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="c1c83-104">**GetStreamingEventsResponseMessage**元素包含单个[GetStreamingEvents 操作](getstreamingevents-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="c1c83-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
```xml
<GetStreamingEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notifications/>
   <ErrorSubscriptionIds/>
   <ConnectionStatus/>
</GetStreamingEventsResponseMessage>
```

 <span data-ttu-id="c1c83-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c1c83-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1c83-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1c83-106">Attributes and elements</span></span>

<span data-ttu-id="c1c83-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1c83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1c83-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c1c83-108">Attributes</span></span>

|<span data-ttu-id="c1c83-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c1c83-109">**Attribute**</span></span>|<span data-ttu-id="c1c83-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1c83-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1c83-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c1c83-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c1c83-112">描述[GetStreamingEvents 操作](getstreamingevents-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c1c83-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="c1c83-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="c1c83-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="c1c83-114">-成功</span><span class="sxs-lookup"><span data-stu-id="c1c83-114">-  Success</span></span>  <br/><span data-ttu-id="c1c83-115">-警告</span><span class="sxs-lookup"><span data-stu-id="c1c83-115">-  Warning</span></span>  <br/><span data-ttu-id="c1c83-116">-错误</span><span class="sxs-lookup"><span data-stu-id="c1c83-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="c1c83-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="c1c83-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="c1c83-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c1c83-118">**Value**</span></span>|<span data-ttu-id="c1c83-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1c83-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1c83-120">成功</span><span class="sxs-lookup"><span data-stu-id="c1c83-120">Success</span></span>  <br/> |<span data-ttu-id="c1c83-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c1c83-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c1c83-122">警告</span><span class="sxs-lookup"><span data-stu-id="c1c83-122">Warning</span></span>  <br/> | <span data-ttu-id="c1c83-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c1c83-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c1c83-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="c1c83-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c1c83-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="c1c83-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="c1c83-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c1c83-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c1c83-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c1c83-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c1c83-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="c1c83-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="c1c83-129">-邮箱数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c1c83-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c1c83-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="c1c83-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="c1c83-131">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="c1c83-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="c1c83-132">错误</span><span class="sxs-lookup"><span data-stu-id="c1c83-132">Error</span></span>  <br/> | <span data-ttu-id="c1c83-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="c1c83-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="c1c83-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="c1c83-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c1c83-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="c1c83-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c1c83-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c1c83-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="c1c83-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c1c83-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="c1c83-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c1c83-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="c1c83-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="c1c83-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c1c83-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="c1c83-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="c1c83-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="c1c83-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1c83-142">子元素</span><span class="sxs-lookup"><span data-stu-id="c1c83-142">Child elements</span></span>

|<span data-ttu-id="c1c83-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1c83-143">**Element**</span></span>|<span data-ttu-id="c1c83-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="c1c83-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c83-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c1c83-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c1c83-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c1c83-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c1c83-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c1c83-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c1c83-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c1c83-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c1c83-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c1c83-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c1c83-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="c1c83-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c1c83-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c1c83-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c1c83-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-154">通知</span><span class="sxs-lookup"><span data-stu-id="c1c83-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="c1c83-155">包含有关订阅以及上次通知之后发生的事件的信息列表。</span><span class="sxs-lookup"><span data-stu-id="c1c83-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="c1c83-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="c1c83-157">包含无效订阅 Id 的列表。</span><span class="sxs-lookup"><span data-stu-id="c1c83-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="c1c83-158">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="c1c83-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="c1c83-159">提供流式订阅的状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c1c83-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1c83-160">父元素</span><span class="sxs-lookup"><span data-stu-id="c1c83-160">Parent elements</span></span>

|<span data-ttu-id="c1c83-161">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1c83-161">**Element**</span></span>|<span data-ttu-id="c1c83-162">**描述**</span><span class="sxs-lookup"><span data-stu-id="c1c83-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c83-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c1c83-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c1c83-164">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c1c83-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1c83-165">文本值</span><span class="sxs-lookup"><span data-stu-id="c1c83-165">Text value</span></span>

<span data-ttu-id="c1c83-166">无。</span><span class="sxs-lookup"><span data-stu-id="c1c83-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1c83-167">说明</span><span class="sxs-lookup"><span data-stu-id="c1c83-167">Remarks</span></span>

<span data-ttu-id="c1c83-168">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c1c83-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1c83-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1c83-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1c83-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1c83-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1c83-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1c83-171">Schema Name</span></span>  <br/> |<span data-ttu-id="c1c83-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="c1c83-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1c83-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1c83-173">Validation File</span></span>  <br/> |<span data-ttu-id="c1c83-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1c83-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1c83-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1c83-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1c83-176">False</span><span class="sxs-lookup"><span data-stu-id="c1c83-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1c83-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1c83-177">See also</span></span>

- [<span data-ttu-id="c1c83-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="c1c83-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="c1c83-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="c1c83-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="c1c83-180">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="c1c83-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

