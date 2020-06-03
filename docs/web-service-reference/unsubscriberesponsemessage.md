---
title: UnsubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponseMessage
api_type:
- schema
ms.assetid: 92c53b13-0ca1-4b44-b925-b23682e9417c
description: UnsubscribeResponseMessage 元素包含单个取消订阅操作请求的状态和结果。
ms.openlocfilehash: e5b42404d09e6367c134934409ec2a45351e135e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467163"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="1e729-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1e729-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="1e729-104">**UnsubscribeResponseMessage**元素包含单个[取消订阅操作](unsubscribe-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1e729-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="1e729-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="1e729-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="1e729-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1e729-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="1e729-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1e729-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="1e729-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1e729-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e729-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e729-109">Attributes and elements</span></span>

<span data-ttu-id="1e729-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e729-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e729-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="1e729-111">Attributes</span></span>

|<span data-ttu-id="1e729-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="1e729-112">**Attribute**</span></span>|<span data-ttu-id="1e729-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e729-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1e729-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1e729-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1e729-115">描述[取消订阅操作](unsubscribe-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="1e729-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="1e729-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="1e729-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="1e729-117">-成功</span><span class="sxs-lookup"><span data-stu-id="1e729-117">-  Success</span></span>  <br/><span data-ttu-id="1e729-118">-警告</span><span class="sxs-lookup"><span data-stu-id="1e729-118">-  Warning</span></span>  <br/><span data-ttu-id="1e729-119">-错误</span><span class="sxs-lookup"><span data-stu-id="1e729-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1e729-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="1e729-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="1e729-121">**值**</span><span class="sxs-lookup"><span data-stu-id="1e729-121">**Value**</span></span>|<span data-ttu-id="1e729-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e729-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1e729-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="1e729-123">**Success**</span></span> <br/> |<span data-ttu-id="1e729-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="1e729-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1e729-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="1e729-125">**Warning**</span></span> <br/> | <span data-ttu-id="1e729-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="1e729-126">Describes a request that was not processed.</span></span> <span data-ttu-id="1e729-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="1e729-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1e729-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="1e729-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1e729-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1e729-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1e729-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1e729-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1e729-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="1e729-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="1e729-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1e729-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1e729-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="1e729-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="1e729-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="1e729-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="1e729-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="1e729-135">**Error**</span></span> <br/> | <span data-ttu-id="1e729-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="1e729-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1e729-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="1e729-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1e729-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1e729-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1e729-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="1e729-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1e729-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="1e729-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="1e729-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1e729-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1e729-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="1e729-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1e729-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="1e729-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="1e729-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="1e729-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e729-145">子元素</span><span class="sxs-lookup"><span data-stu-id="1e729-145">Child elements</span></span>

|<span data-ttu-id="1e729-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e729-146">**Element**</span></span>|<span data-ttu-id="1e729-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="1e729-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e729-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="1e729-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1e729-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="1e729-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1e729-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1e729-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1e729-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="1e729-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1e729-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1e729-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1e729-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="1e729-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1e729-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="1e729-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1e729-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1e729-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1e729-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="1e729-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1e729-157">父元素</span><span class="sxs-lookup"><span data-stu-id="1e729-157">Parent elements</span></span>

|<span data-ttu-id="1e729-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e729-158">**Element**</span></span>|<span data-ttu-id="1e729-159">**描述**</span><span class="sxs-lookup"><span data-stu-id="1e729-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e729-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1e729-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1e729-161">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="1e729-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e729-162">备注</span><span class="sxs-lookup"><span data-stu-id="1e729-162">Remarks</span></span>

<span data-ttu-id="1e729-163">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e729-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e729-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e729-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e729-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e729-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1e729-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e729-166">Schema Name</span></span>  <br/> |<span data-ttu-id="1e729-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="1e729-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1e729-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e729-168">Validation File</span></span>  <br/> |<span data-ttu-id="1e729-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1e729-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1e729-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e729-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e729-171">False</span><span class="sxs-lookup"><span data-stu-id="1e729-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e729-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e729-172">See also</span></span>

- [<span data-ttu-id="1e729-173">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="1e729-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="1e729-174">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e729-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

