---
title: SendNotificationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResponseMessage
api_type:
- schema
ms.assetid: 2c6d681b-67ac-4331-bc6b-a2e709b638e3
description: SendNotificationResponseMessage 元素包含单个 SendNotification 操作请求的状态和结果。
ms.openlocfilehash: cf44a09624d1b8a7341f9dd98db48472fea7393b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462106"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="434dd-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="434dd-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="434dd-104">**SendNotificationResponseMessage**元素包含单个**SendNotification**操作请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="434dd-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="434dd-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="434dd-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="434dd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="434dd-106">Attributes and elements</span></span>

<span data-ttu-id="434dd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="434dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="434dd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="434dd-108">Attributes</span></span>

|<span data-ttu-id="434dd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="434dd-109">**Attribute**</span></span>|<span data-ttu-id="434dd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="434dd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="434dd-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="434dd-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="434dd-112">描述**SendNotification**操作响应的状态。</span><span class="sxs-lookup"><span data-stu-id="434dd-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="434dd-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="434dd-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="434dd-114">-成功</span><span class="sxs-lookup"><span data-stu-id="434dd-114">-  Success</span></span>  <br/><span data-ttu-id="434dd-115">-警告</span><span class="sxs-lookup"><span data-stu-id="434dd-115">-  Warning</span></span>  <br/><span data-ttu-id="434dd-116">-错误</span><span class="sxs-lookup"><span data-stu-id="434dd-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="434dd-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="434dd-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="434dd-118">**值**</span><span class="sxs-lookup"><span data-stu-id="434dd-118">**Value**</span></span>|<span data-ttu-id="434dd-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="434dd-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="434dd-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="434dd-120">**Success**</span></span> <br/> |<span data-ttu-id="434dd-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="434dd-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="434dd-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="434dd-122">**Warning**</span></span> <br/> | <span data-ttu-id="434dd-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="434dd-123">Describes a request that was not processed.</span></span> <span data-ttu-id="434dd-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="434dd-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="434dd-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="434dd-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="434dd-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="434dd-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="434dd-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="434dd-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="434dd-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="434dd-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="434dd-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="434dd-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="434dd-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="434dd-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="434dd-131">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="434dd-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="434dd-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="434dd-132">**Error**</span></span> <br/> | <span data-ttu-id="434dd-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="434dd-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="434dd-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="434dd-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="434dd-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="434dd-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="434dd-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="434dd-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="434dd-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="434dd-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="434dd-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="434dd-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="434dd-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="434dd-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="434dd-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="434dd-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="434dd-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="434dd-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="434dd-142">子元素</span><span class="sxs-lookup"><span data-stu-id="434dd-142">Child elements</span></span>

|<span data-ttu-id="434dd-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="434dd-143">**Element**</span></span>|<span data-ttu-id="434dd-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="434dd-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="434dd-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="434dd-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="434dd-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="434dd-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="434dd-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="434dd-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="434dd-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="434dd-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="434dd-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="434dd-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="434dd-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="434dd-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="434dd-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="434dd-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="434dd-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="434dd-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="434dd-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="434dd-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="434dd-154">通知</span><span class="sxs-lookup"><span data-stu-id="434dd-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="434dd-155">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="434dd-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="434dd-156">父元素</span><span class="sxs-lookup"><span data-stu-id="434dd-156">Parent elements</span></span>

|<span data-ttu-id="434dd-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="434dd-157">**Element**</span></span>|<span data-ttu-id="434dd-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="434dd-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="434dd-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="434dd-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="434dd-160">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="434dd-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="434dd-161">文本值</span><span class="sxs-lookup"><span data-stu-id="434dd-161">Text value</span></span>

<span data-ttu-id="434dd-162">无。</span><span class="sxs-lookup"><span data-stu-id="434dd-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="434dd-163">说明</span><span class="sxs-lookup"><span data-stu-id="434dd-163">Remarks</span></span>

<span data-ttu-id="434dd-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="434dd-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="434dd-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="434dd-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="434dd-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="434dd-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="434dd-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="434dd-167">Schema Name</span></span>  <br/> |<span data-ttu-id="434dd-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="434dd-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="434dd-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="434dd-169">Validation File</span></span>  <br/> |<span data-ttu-id="434dd-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="434dd-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="434dd-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="434dd-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="434dd-172">False</span><span class="sxs-lookup"><span data-stu-id="434dd-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="434dd-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="434dd-173">See also</span></span>

- [<span data-ttu-id="434dd-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="434dd-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="434dd-175">订阅操作</span><span class="sxs-lookup"><span data-stu-id="434dd-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="434dd-176">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="434dd-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

