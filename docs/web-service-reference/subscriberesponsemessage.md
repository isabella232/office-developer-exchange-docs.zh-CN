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
description: SubscribeResponseMessage 元素包含状态和单个 Subscribe 操作请求的结果。
ms.openlocfilehash: 97c7bd9f12511ff226e75f53278c13481679c8a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827621"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="92926-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="92926-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="92926-104">**SubscribeResponseMessage**元素包含状态和的单个结果[Subscribe 操作](subscribe-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="92926-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="92926-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="92926-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="92926-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="92926-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="92926-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="92926-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
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

 <span data-ttu-id="92926-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="92926-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92926-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92926-109">Attributes and elements</span></span>

<span data-ttu-id="92926-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92926-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92926-111">属性</span><span class="sxs-lookup"><span data-stu-id="92926-111">Attributes</span></span>

|<span data-ttu-id="92926-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="92926-112">**Attribute**</span></span>|<span data-ttu-id="92926-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="92926-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92926-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="92926-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="92926-115">描述[Subscribe 操作](subscribe-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="92926-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="92926-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="92926-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="92926-117">-成功</span><span class="sxs-lookup"><span data-stu-id="92926-117">-  Success</span></span>  <br/><span data-ttu-id="92926-118">-警告</span><span class="sxs-lookup"><span data-stu-id="92926-118">-  Warning</span></span>  <br/><span data-ttu-id="92926-119">-错误</span><span class="sxs-lookup"><span data-stu-id="92926-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="92926-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="92926-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="92926-121">**值**</span><span class="sxs-lookup"><span data-stu-id="92926-121">**Value**</span></span>|<span data-ttu-id="92926-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="92926-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92926-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="92926-123">**Success**</span></span> <br/> |<span data-ttu-id="92926-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="92926-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="92926-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="92926-125">**Warning**</span></span> <br/> | <span data-ttu-id="92926-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="92926-126">Describes a request that was not processed.</span></span> <span data-ttu-id="92926-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="92926-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="92926-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="92926-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="92926-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="92926-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="92926-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="92926-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="92926-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="92926-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="92926-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="92926-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="92926-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="92926-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="92926-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="92926-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="92926-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="92926-135">**Error**</span></span> <br/> | <span data-ttu-id="92926-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="92926-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="92926-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="92926-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="92926-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="92926-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="92926-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="92926-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="92926-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="92926-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="92926-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="92926-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="92926-142">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="92926-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="92926-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="92926-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="92926-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="92926-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92926-145">子元素</span><span class="sxs-lookup"><span data-stu-id="92926-145">Child elements</span></span>

|<span data-ttu-id="92926-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="92926-146">**Element**</span></span>|<span data-ttu-id="92926-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="92926-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92926-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="92926-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="92926-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="92926-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="92926-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="92926-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="92926-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="92926-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="92926-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="92926-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="92926-153">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="92926-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="92926-154">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="92926-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="92926-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="92926-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="92926-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="92926-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="92926-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="92926-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="92926-158">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="92926-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="92926-159">水印</span><span class="sxs-lookup"><span data-stu-id="92926-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="92926-160">代表邮箱事件队列中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="92926-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92926-161">父元素</span><span class="sxs-lookup"><span data-stu-id="92926-161">Parent elements</span></span>

|<span data-ttu-id="92926-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="92926-162">**Element**</span></span>|<span data-ttu-id="92926-163">**说明**</span><span class="sxs-lookup"><span data-stu-id="92926-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92926-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="92926-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="92926-165">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="92926-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92926-166">注解</span><span class="sxs-lookup"><span data-stu-id="92926-166">Remarks</span></span>

<span data-ttu-id="92926-167">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="92926-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92926-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="92926-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92926-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="92926-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="92926-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="92926-170">Schema Name</span></span>  <br/> |<span data-ttu-id="92926-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="92926-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="92926-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="92926-172">Validation File</span></span>  <br/> |<span data-ttu-id="92926-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="92926-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="92926-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="92926-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="92926-175">False</span><span class="sxs-lookup"><span data-stu-id="92926-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92926-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92926-176">See also</span></span>

- [<span data-ttu-id="92926-177">订阅操作</span><span class="sxs-lookup"><span data-stu-id="92926-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="92926-178">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="92926-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="92926-179">取消操作</span><span class="sxs-lookup"><span data-stu-id="92926-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

