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
description: GetEventsResponseMessage 元素包含状态和单个 GetEvents 操作请求的结果。
ms.openlocfilehash: 90e79194182f61ba7298ef67b1070b1aa239073d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754541"
---
# <a name="geteventsresponsemessage"></a><span data-ttu-id="99611-103">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99611-103">GetEventsResponseMessage</span></span>

<span data-ttu-id="99611-104">**GetEventsResponseMessage**元素包含状态和的单个结果[GetEvents 操作](getevents-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="99611-104">The **GetEventsResponseMessage** element contains the status and result of a single [GetEvents operation](getevents-operation.md) request.</span></span> 
  
```xml
<GetEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</GetEventsResponseMessage>
```

 <span data-ttu-id="99611-105">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="99611-105">**GetEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99611-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="99611-106">Attributes and elements</span></span>

<span data-ttu-id="99611-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="99611-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99611-108">属性</span><span class="sxs-lookup"><span data-stu-id="99611-108">Attributes</span></span>

|<span data-ttu-id="99611-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="99611-109">**Attribute**</span></span>|<span data-ttu-id="99611-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="99611-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99611-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="99611-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="99611-112">描述[GetEvents 操作](getevents-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="99611-112">Describes the status of a [GetEvents operation](getevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="99611-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="99611-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="99611-114">-成功</span><span class="sxs-lookup"><span data-stu-id="99611-114">-  Success</span></span>  <br/><span data-ttu-id="99611-115">-警告</span><span class="sxs-lookup"><span data-stu-id="99611-115">-  Warning</span></span>  <br/><span data-ttu-id="99611-116">-错误</span><span class="sxs-lookup"><span data-stu-id="99611-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="99611-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="99611-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="99611-118">**值**</span><span class="sxs-lookup"><span data-stu-id="99611-118">**Value**</span></span>|<span data-ttu-id="99611-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="99611-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99611-120">成功</span><span class="sxs-lookup"><span data-stu-id="99611-120">Success</span></span>  <br/> |<span data-ttu-id="99611-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="99611-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="99611-122">警告</span><span class="sxs-lookup"><span data-stu-id="99611-122">Warning</span></span>  <br/> | <span data-ttu-id="99611-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="99611-123">Describes a request that was not processed.</span></span> <span data-ttu-id="99611-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="99611-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="99611-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="99611-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="99611-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="99611-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="99611-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="99611-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="99611-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="99611-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="99611-129">-邮箱数据库 (MDB) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="99611-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="99611-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="99611-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="99611-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="99611-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="99611-132">Error</span><span class="sxs-lookup"><span data-stu-id="99611-132">Error</span></span>  <br/> | <span data-ttu-id="99611-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="99611-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="99611-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="99611-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="99611-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="99611-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="99611-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="99611-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="99611-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="99611-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="99611-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="99611-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="99611-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="99611-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="99611-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="99611-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="99611-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="99611-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99611-142">子元素</span><span class="sxs-lookup"><span data-stu-id="99611-142">Child elements</span></span>

|<span data-ttu-id="99611-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="99611-143">**Element**</span></span>|<span data-ttu-id="99611-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="99611-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99611-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="99611-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="99611-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="99611-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="99611-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="99611-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="99611-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="99611-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="99611-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="99611-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="99611-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="99611-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="99611-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="99611-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="99611-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="99611-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="99611-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="99611-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="99611-154">通知</span><span class="sxs-lookup"><span data-stu-id="99611-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="99611-155">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="99611-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99611-156">父元素</span><span class="sxs-lookup"><span data-stu-id="99611-156">Parent elements</span></span>

|<span data-ttu-id="99611-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="99611-157">**Element**</span></span>|<span data-ttu-id="99611-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="99611-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99611-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="99611-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="99611-160">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="99611-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99611-161">备注</span><span class="sxs-lookup"><span data-stu-id="99611-161">Remarks</span></span>

<span data-ttu-id="99611-162">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="99611-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99611-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="99611-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99611-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="99611-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99611-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="99611-165">Schema Name</span></span>  <br/> |<span data-ttu-id="99611-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="99611-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="99611-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="99611-167">Validation File</span></span>  <br/> |<span data-ttu-id="99611-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="99611-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99611-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="99611-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="99611-170">False</span><span class="sxs-lookup"><span data-stu-id="99611-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99611-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99611-171">See also</span></span>

- [<span data-ttu-id="99611-172">GetEvents</span><span class="sxs-lookup"><span data-stu-id="99611-172">GetEvents</span></span>](getevents.md) 
- [<span data-ttu-id="99611-173">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="99611-173">GetEventsResponse</span></span>](geteventsresponse.md)
- [<span data-ttu-id="99611-174">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="99611-174">GetEvents operation</span></span>](getevents-operation.md)
