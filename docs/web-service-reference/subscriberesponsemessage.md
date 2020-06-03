---
title: SubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscribeResponseMessage
api_type:
- schema
ms.assetid: d121d38a-a61a-4f9c-a477-fc6d7f9af77e
description: SubscribeResponseMessage 元素包含单个订阅操作请求的状态和结果。
ms.openlocfilehash: eea7356dbcf1887383d56e40a4f6dcd091535fa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465371"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="e615f-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e615f-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="e615f-104">**SubscribeResponseMessage**元素包含单个[订阅操作](subscribe-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e615f-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="e615f-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="e615f-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="e615f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e615f-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="e615f-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e615f-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
```xml
<SubscribeResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SubscriptionId/>
   <Watermark/>
</SubscribeResponseMessage>
```

 <span data-ttu-id="e615f-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e615f-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e615f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e615f-109">Attributes and elements</span></span>

<span data-ttu-id="e615f-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e615f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e615f-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="e615f-111">Attributes</span></span>

|<span data-ttu-id="e615f-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="e615f-112">**Attribute**</span></span>|<span data-ttu-id="e615f-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="e615f-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e615f-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e615f-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e615f-115">描述[订阅操作](subscribe-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="e615f-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="e615f-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="e615f-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e615f-117">-成功</span><span class="sxs-lookup"><span data-stu-id="e615f-117">-  Success</span></span>  <br/><span data-ttu-id="e615f-118">-警告</span><span class="sxs-lookup"><span data-stu-id="e615f-118">-  Warning</span></span>  <br/><span data-ttu-id="e615f-119">-错误</span><span class="sxs-lookup"><span data-stu-id="e615f-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e615f-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="e615f-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="e615f-121">**值**</span><span class="sxs-lookup"><span data-stu-id="e615f-121">**Value**</span></span>|<span data-ttu-id="e615f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="e615f-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e615f-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="e615f-123">**Success**</span></span> <br/> |<span data-ttu-id="e615f-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="e615f-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e615f-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="e615f-125">**Warning**</span></span> <br/> | <span data-ttu-id="e615f-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="e615f-126">Describes a request that was not processed.</span></span> <span data-ttu-id="e615f-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="e615f-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e615f-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="e615f-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="e615f-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e615f-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e615f-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e615f-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e615f-131">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="e615f-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e615f-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e615f-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e615f-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="e615f-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="e615f-134">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="e615f-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e615f-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="e615f-135">**Error**</span></span> <br/> | <span data-ttu-id="e615f-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="e615f-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e615f-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="e615f-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e615f-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="e615f-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e615f-139">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="e615f-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="e615f-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="e615f-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="e615f-141">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="e615f-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e615f-142">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="e615f-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e615f-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="e615f-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="e615f-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="e615f-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e615f-145">子元素</span><span class="sxs-lookup"><span data-stu-id="e615f-145">Child elements</span></span>

|<span data-ttu-id="e615f-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="e615f-146">**Element**</span></span>|<span data-ttu-id="e615f-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="e615f-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e615f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="e615f-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e615f-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e615f-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e615f-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e615f-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e615f-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e615f-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e615f-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e615f-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e615f-153">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e615f-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e615f-154">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="e615f-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e615f-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e615f-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e615f-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e615f-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e615f-157">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="e615f-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="e615f-158">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="e615f-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="e615f-159">Watermark</span><span class="sxs-lookup"><span data-stu-id="e615f-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="e615f-160">表示邮箱事件队列中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="e615f-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e615f-161">父元素</span><span class="sxs-lookup"><span data-stu-id="e615f-161">Parent elements</span></span>

|<span data-ttu-id="e615f-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="e615f-162">**Element**</span></span>|<span data-ttu-id="e615f-163">**描述**</span><span class="sxs-lookup"><span data-stu-id="e615f-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e615f-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e615f-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e615f-165">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e615f-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e615f-166">备注</span><span class="sxs-lookup"><span data-stu-id="e615f-166">Remarks</span></span>

<span data-ttu-id="e615f-167">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e615f-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e615f-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="e615f-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e615f-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="e615f-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e615f-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="e615f-170">Schema Name</span></span>  <br/> |<span data-ttu-id="e615f-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="e615f-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e615f-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="e615f-172">Validation File</span></span>  <br/> |<span data-ttu-id="e615f-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e615f-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e615f-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="e615f-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="e615f-175">False</span><span class="sxs-lookup"><span data-stu-id="e615f-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e615f-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e615f-176">See also</span></span>

- [<span data-ttu-id="e615f-177">订阅操作</span><span class="sxs-lookup"><span data-stu-id="e615f-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="e615f-178">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="e615f-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="e615f-179">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="e615f-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

