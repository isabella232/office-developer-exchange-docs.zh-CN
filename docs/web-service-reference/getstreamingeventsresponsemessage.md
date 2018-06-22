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
description: GetStreamingEventsResponseMessage 元素包含状态和单个 GetStreamingEvents 操作请求的结果。
ms.openlocfilehash: 5fcc7ddde41b49a5d8b304da0732f4472c61a76a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825682"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="0cd48-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0cd48-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="0cd48-104">**GetStreamingEventsResponseMessage**元素包含状态和的单个结果[GetStreamingEvents 操作](getstreamingevents-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="0cd48-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="0cd48-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0cd48-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cd48-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-106">Attributes and elements</span></span>

<span data-ttu-id="0cd48-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0cd48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cd48-108">属性</span><span class="sxs-lookup"><span data-stu-id="0cd48-108">Attributes</span></span>

|<span data-ttu-id="0cd48-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0cd48-109">**Attribute**</span></span>|<span data-ttu-id="0cd48-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cd48-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cd48-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0cd48-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0cd48-112">描述[GetStreamingEvents 操作](getstreamingevents-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="0cd48-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="0cd48-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="0cd48-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0cd48-114">-成功</span><span class="sxs-lookup"><span data-stu-id="0cd48-114">-  Success</span></span>  <br/><span data-ttu-id="0cd48-115">-警告</span><span class="sxs-lookup"><span data-stu-id="0cd48-115">-  Warning</span></span>  <br/><span data-ttu-id="0cd48-116">-错误</span><span class="sxs-lookup"><span data-stu-id="0cd48-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="0cd48-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="0cd48-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="0cd48-118">**值**</span><span class="sxs-lookup"><span data-stu-id="0cd48-118">**Value**</span></span>|<span data-ttu-id="0cd48-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cd48-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cd48-120">成功</span><span class="sxs-lookup"><span data-stu-id="0cd48-120">Success</span></span>  <br/> |<span data-ttu-id="0cd48-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="0cd48-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0cd48-122">警告</span><span class="sxs-lookup"><span data-stu-id="0cd48-122">Warning</span></span>  <br/> | <span data-ttu-id="0cd48-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="0cd48-123">Describes a request that was not processed.</span></span> <span data-ttu-id="0cd48-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="0cd48-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0cd48-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="0cd48-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="0cd48-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cd48-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0cd48-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cd48-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="0cd48-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="0cd48-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="0cd48-129">-邮箱数据库 (MDB) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cd48-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0cd48-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="0cd48-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="0cd48-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="0cd48-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="0cd48-132">Error</span><span class="sxs-lookup"><span data-stu-id="0cd48-132">Error</span></span>  <br/> | <span data-ttu-id="0cd48-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="0cd48-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="0cd48-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="0cd48-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0cd48-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0cd48-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="0cd48-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="0cd48-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="0cd48-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="0cd48-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="0cd48-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="0cd48-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="0cd48-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="0cd48-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="0cd48-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0cd48-142">子元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-142">Child elements</span></span>

|<span data-ttu-id="0cd48-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cd48-143">**Element**</span></span>|<span data-ttu-id="0cd48-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cd48-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cd48-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="0cd48-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0cd48-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0cd48-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0cd48-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0cd48-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0cd48-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0cd48-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0cd48-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0cd48-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0cd48-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="0cd48-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0cd48-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0cd48-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0cd48-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-154">通知</span><span class="sxs-lookup"><span data-stu-id="0cd48-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="0cd48-155">包含有关订阅和自上次通知以来发生的事件的信息的列表。</span><span class="sxs-lookup"><span data-stu-id="0cd48-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="0cd48-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="0cd48-157">包含列表的订阅 Id 的无效。</span><span class="sxs-lookup"><span data-stu-id="0cd48-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="0cd48-158">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="0cd48-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="0cd48-159">提供流式订阅的状态的文本的说明。</span><span class="sxs-lookup"><span data-stu-id="0cd48-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0cd48-160">父元素</span><span class="sxs-lookup"><span data-stu-id="0cd48-160">Parent elements</span></span>

|<span data-ttu-id="0cd48-161">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cd48-161">**Element**</span></span>|<span data-ttu-id="0cd48-162">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cd48-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cd48-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0cd48-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0cd48-164">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0cd48-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0cd48-165">文本值</span><span class="sxs-lookup"><span data-stu-id="0cd48-165">Text value</span></span>

<span data-ttu-id="0cd48-166">无。</span><span class="sxs-lookup"><span data-stu-id="0cd48-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cd48-167">备注</span><span class="sxs-lookup"><span data-stu-id="0cd48-167">Remarks</span></span>

<span data-ttu-id="0cd48-168">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0cd48-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cd48-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="0cd48-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cd48-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="0cd48-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0cd48-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="0cd48-171">Schema Name</span></span>  <br/> |<span data-ttu-id="0cd48-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="0cd48-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0cd48-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="0cd48-173">Validation File</span></span>  <br/> |<span data-ttu-id="0cd48-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0cd48-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0cd48-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="0cd48-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="0cd48-176">False</span><span class="sxs-lookup"><span data-stu-id="0cd48-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cd48-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cd48-177">See also</span></span>

- [<span data-ttu-id="0cd48-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="0cd48-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="0cd48-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="0cd48-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="0cd48-180">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="0cd48-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

