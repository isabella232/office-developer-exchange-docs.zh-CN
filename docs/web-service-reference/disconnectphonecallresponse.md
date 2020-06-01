---
title: DisconnectPhoneCallResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCallResponse
api_type:
- schema
ms.assetid: 05041799-5b81-4b87-ada8-ce6c506ffe01
description: DisconnectPhoneCallResponse 元素包含单个 DisconnectPhoneCall 请求的状态和结果。
ms.openlocfilehash: 6c0696a1d9ab3242920d051b409105644a6b03aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458444"
---
# <a name="disconnectphonecallresponse"></a><span data-ttu-id="8bccd-103">DisconnectPhoneCallResponse</span><span class="sxs-lookup"><span data-stu-id="8bccd-103">DisconnectPhoneCallResponse</span></span>

<span data-ttu-id="8bccd-104">**DisconnectPhoneCallResponse**元素包含单个**DisconnectPhoneCall**请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="8bccd-104">The **DisconnectPhoneCallResponse** element contains the status and result of a single **DisconnectPhoneCall** request.</span></span> 
  
```xml
<DisconnectPhoneCallResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DisconnectPhoneCallResponse>
```

 <span data-ttu-id="8bccd-105">**DisconnectPhoneCallResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8bccd-105">**DisconnectPhoneCallResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bccd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-106">Attributes and elements</span></span>

<span data-ttu-id="8bccd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8bccd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bccd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8bccd-108">Attributes</span></span>

|<span data-ttu-id="8bccd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8bccd-109">**Attribute**</span></span>|<span data-ttu-id="8bccd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8bccd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8bccd-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8bccd-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8bccd-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="8bccd-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="8bccd-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="8bccd-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="8bccd-114">-成功</span><span class="sxs-lookup"><span data-stu-id="8bccd-114">-  Success</span></span>  <br/><span data-ttu-id="8bccd-115">-警告</span><span class="sxs-lookup"><span data-stu-id="8bccd-115">-  Warning</span></span>  <br/><span data-ttu-id="8bccd-116">-错误</span><span class="sxs-lookup"><span data-stu-id="8bccd-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8bccd-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="8bccd-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="8bccd-118">**值**</span><span class="sxs-lookup"><span data-stu-id="8bccd-118">**Value**</span></span>|<span data-ttu-id="8bccd-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8bccd-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8bccd-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="8bccd-120">**Success**</span></span> <br/> |<span data-ttu-id="8bccd-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="8bccd-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8bccd-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="8bccd-122">**Warning**</span></span> <br/> | <span data-ttu-id="8bccd-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="8bccd-123">Describes a request that was not processed.</span></span> <span data-ttu-id="8bccd-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="8bccd-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8bccd-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="8bccd-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8bccd-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8bccd-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8bccd-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8bccd-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8bccd-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="8bccd-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="8bccd-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8bccd-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8bccd-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="8bccd-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="8bccd-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="8bccd-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="8bccd-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="8bccd-132">**Error**</span></span> <br/> | <span data-ttu-id="8bccd-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="8bccd-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="8bccd-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="8bccd-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8bccd-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="8bccd-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8bccd-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="8bccd-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="8bccd-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="8bccd-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="8bccd-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="8bccd-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8bccd-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="8bccd-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="8bccd-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="8bccd-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8bccd-142">子元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-142">Child elements</span></span>

|<span data-ttu-id="8bccd-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="8bccd-143">**Element**</span></span>|<span data-ttu-id="8bccd-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="8bccd-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8bccd-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="8bccd-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8bccd-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="8bccd-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8bccd-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8bccd-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8bccd-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="8bccd-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8bccd-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8bccd-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8bccd-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="8bccd-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="8bccd-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="8bccd-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8bccd-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8bccd-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8bccd-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="8bccd-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8bccd-154">父元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-154">Parent elements</span></span>

<span data-ttu-id="8bccd-155">无。</span><span class="sxs-lookup"><span data-stu-id="8bccd-155">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8bccd-156">文本值</span><span class="sxs-lookup"><span data-stu-id="8bccd-156">Text value</span></span>

<span data-ttu-id="8bccd-157">无。</span><span class="sxs-lookup"><span data-stu-id="8bccd-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bccd-158">说明</span><span class="sxs-lookup"><span data-stu-id="8bccd-158">Remarks</span></span>

<span data-ttu-id="8bccd-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8bccd-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bccd-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="8bccd-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bccd-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="8bccd-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8bccd-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="8bccd-162">Schema Name</span></span>  <br/> |<span data-ttu-id="8bccd-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="8bccd-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8bccd-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="8bccd-164">Validation File</span></span>  <br/> |<span data-ttu-id="8bccd-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8bccd-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8bccd-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="8bccd-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="8bccd-167">False</span><span class="sxs-lookup"><span data-stu-id="8bccd-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bccd-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8bccd-168">See also</span></span>

- [<span data-ttu-id="8bccd-169">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8bccd-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

