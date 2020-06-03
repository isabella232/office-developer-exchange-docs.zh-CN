---
title: GetEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEventsResponseMessage
api_type:
- schema
ms.assetid: d433977f-b86a-499e-b9c3-f405ac229358
description: GetEventsResponseMessage 元素包含单个 GetEvents 操作请求的状态和结果。
ms.openlocfilehash: d307aa1f5234ab5a7a2527c55f5e48814ea2687b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462855"
---
# <a name="geteventsresponsemessage"></a><span data-ttu-id="9dd2c-103">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9dd2c-103">GetEventsResponseMessage</span></span>

<span data-ttu-id="9dd2c-104">**GetEventsResponseMessage**元素包含单个[GetEvents 操作](getevents-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-104">The **GetEventsResponseMessage** element contains the status and result of a single [GetEvents operation](getevents-operation.md) request.</span></span> 
  
```xml
<GetEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</GetEventsResponseMessage>
```

 <span data-ttu-id="9dd2c-105">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-105">**GetEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9dd2c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9dd2c-106">Attributes and elements</span></span>

<span data-ttu-id="9dd2c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dd2c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9dd2c-108">Attributes</span></span>

|<span data-ttu-id="9dd2c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-109">**Attribute**</span></span>|<span data-ttu-id="9dd2c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9dd2c-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9dd2c-112">描述[GetEvents 操作](getevents-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-112">Describes the status of a [GetEvents operation](getevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="9dd2c-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="9dd2c-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="9dd2c-114">-成功</span><span class="sxs-lookup"><span data-stu-id="9dd2c-114">-  Success</span></span>  <br/><span data-ttu-id="9dd2c-115">-警告</span><span class="sxs-lookup"><span data-stu-id="9dd2c-115">-  Warning</span></span>  <br/><span data-ttu-id="9dd2c-116">-错误</span><span class="sxs-lookup"><span data-stu-id="9dd2c-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="9dd2c-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="9dd2c-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="9dd2c-118">**值**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-118">**Value**</span></span>|<span data-ttu-id="9dd2c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9dd2c-120">成功</span><span class="sxs-lookup"><span data-stu-id="9dd2c-120">Success</span></span>  <br/> |<span data-ttu-id="9dd2c-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9dd2c-122">警告</span><span class="sxs-lookup"><span data-stu-id="9dd2c-122">Warning</span></span>  <br/> | <span data-ttu-id="9dd2c-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9dd2c-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="9dd2c-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="9dd2c-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="9dd2c-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9dd2c-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="9dd2c-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="9dd2c-129">-邮箱数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9dd2c-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="9dd2c-131">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="9dd2c-132">错误</span><span class="sxs-lookup"><span data-stu-id="9dd2c-132">Error</span></span>  <br/> | <span data-ttu-id="9dd2c-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9dd2c-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="9dd2c-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9dd2c-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="9dd2c-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9dd2c-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="9dd2c-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="9dd2c-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="9dd2c-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="9dd2c-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="9dd2c-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="9dd2c-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="9dd2c-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9dd2c-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="9dd2c-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9dd2c-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9dd2c-142">子元素</span><span class="sxs-lookup"><span data-stu-id="9dd2c-142">Child elements</span></span>

|<span data-ttu-id="9dd2c-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-143">**Element**</span></span>|<span data-ttu-id="9dd2c-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9dd2c-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9dd2c-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9dd2c-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9dd2c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9dd2c-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9dd2c-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9dd2c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9dd2c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9dd2c-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9dd2c-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9dd2c-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9dd2c-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9dd2c-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9dd2c-154">通知</span><span class="sxs-lookup"><span data-stu-id="9dd2c-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9dd2c-155">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9dd2c-156">父元素</span><span class="sxs-lookup"><span data-stu-id="9dd2c-156">Parent elements</span></span>

|<span data-ttu-id="9dd2c-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-157">**Element**</span></span>|<span data-ttu-id="9dd2c-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="9dd2c-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9dd2c-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9dd2c-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9dd2c-160">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9dd2c-161">备注</span><span class="sxs-lookup"><span data-stu-id="9dd2c-161">Remarks</span></span>

<span data-ttu-id="9dd2c-162">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9dd2c-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dd2c-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="9dd2c-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dd2c-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="9dd2c-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9dd2c-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="9dd2c-165">Schema Name</span></span>  <br/> |<span data-ttu-id="9dd2c-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="9dd2c-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9dd2c-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="9dd2c-167">Validation File</span></span>  <br/> |<span data-ttu-id="9dd2c-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9dd2c-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9dd2c-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="9dd2c-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="9dd2c-170">False</span><span class="sxs-lookup"><span data-stu-id="9dd2c-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9dd2c-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9dd2c-171">See also</span></span>

- [<span data-ttu-id="9dd2c-172">GetEvents</span><span class="sxs-lookup"><span data-stu-id="9dd2c-172">GetEvents</span></span>](getevents.md) 
- [<span data-ttu-id="9dd2c-173">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="9dd2c-173">GetEventsResponse</span></span>](geteventsresponse.md)
- [<span data-ttu-id="9dd2c-174">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="9dd2c-174">GetEvents operation</span></span>](getevents-operation.md)

