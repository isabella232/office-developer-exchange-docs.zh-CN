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
description: SendNotificationResponseMessage 元素包含状态和单个 SendNotification 操作请求的结果。
ms.openlocfilehash: 49677b6d61f525b469679ec3fdcb8aadcca7239d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827348"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="210db-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="210db-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="210db-104">**SendNotificationResponseMessage**元素包含状态和单个**SendNotification**操作请求的结果。</span><span class="sxs-lookup"><span data-stu-id="210db-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="210db-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="210db-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="210db-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="210db-106">Attributes and elements</span></span>

<span data-ttu-id="210db-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="210db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="210db-108">属性</span><span class="sxs-lookup"><span data-stu-id="210db-108">Attributes</span></span>

|<span data-ttu-id="210db-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="210db-109">**Attribute**</span></span>|<span data-ttu-id="210db-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="210db-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="210db-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="210db-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="210db-112">介绍**SendNotification**操作响应的状态。</span><span class="sxs-lookup"><span data-stu-id="210db-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="210db-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="210db-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="210db-114">-成功</span><span class="sxs-lookup"><span data-stu-id="210db-114">-  Success</span></span>  <br/><span data-ttu-id="210db-115">-警告</span><span class="sxs-lookup"><span data-stu-id="210db-115">-  Warning</span></span>  <br/><span data-ttu-id="210db-116">-错误</span><span class="sxs-lookup"><span data-stu-id="210db-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="210db-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="210db-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="210db-118">**值**</span><span class="sxs-lookup"><span data-stu-id="210db-118">**Value**</span></span>|<span data-ttu-id="210db-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="210db-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="210db-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="210db-120">**Success**</span></span> <br/> |<span data-ttu-id="210db-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="210db-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="210db-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="210db-122">**Warning**</span></span> <br/> | <span data-ttu-id="210db-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="210db-123">Describes a request that was not processed.</span></span> <span data-ttu-id="210db-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="210db-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="210db-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="210db-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="210db-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="210db-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="210db-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="210db-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="210db-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="210db-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="210db-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="210db-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="210db-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="210db-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="210db-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="210db-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="210db-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="210db-132">**Error**</span></span> <br/> | <span data-ttu-id="210db-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="210db-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="210db-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="210db-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="210db-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="210db-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="210db-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="210db-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="210db-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="210db-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="210db-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="210db-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="210db-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="210db-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="210db-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="210db-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="210db-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="210db-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="210db-142">子元素</span><span class="sxs-lookup"><span data-stu-id="210db-142">Child elements</span></span>

|<span data-ttu-id="210db-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="210db-143">**Element**</span></span>|<span data-ttu-id="210db-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="210db-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="210db-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="210db-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="210db-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="210db-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="210db-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="210db-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="210db-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="210db-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="210db-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="210db-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="210db-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="210db-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="210db-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="210db-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="210db-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="210db-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="210db-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="210db-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="210db-154">通知</span><span class="sxs-lookup"><span data-stu-id="210db-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="210db-155">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="210db-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="210db-156">父元素</span><span class="sxs-lookup"><span data-stu-id="210db-156">Parent elements</span></span>

|<span data-ttu-id="210db-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="210db-157">**Element**</span></span>|<span data-ttu-id="210db-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="210db-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="210db-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="210db-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="210db-160">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="210db-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="210db-161">文本值</span><span class="sxs-lookup"><span data-stu-id="210db-161">Text value</span></span>

<span data-ttu-id="210db-162">无。</span><span class="sxs-lookup"><span data-stu-id="210db-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="210db-163">备注</span><span class="sxs-lookup"><span data-stu-id="210db-163">Remarks</span></span>

<span data-ttu-id="210db-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="210db-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="210db-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="210db-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="210db-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="210db-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="210db-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="210db-167">Schema Name</span></span>  <br/> |<span data-ttu-id="210db-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="210db-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="210db-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="210db-169">Validation File</span></span>  <br/> |<span data-ttu-id="210db-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="210db-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="210db-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="210db-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="210db-172">False</span><span class="sxs-lookup"><span data-stu-id="210db-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="210db-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="210db-173">See also</span></span>

- [<span data-ttu-id="210db-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="210db-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="210db-175">订阅操作</span><span class="sxs-lookup"><span data-stu-id="210db-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="210db-176">取消操作</span><span class="sxs-lookup"><span data-stu-id="210db-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

