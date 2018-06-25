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
description: DisconnectPhoneCallResponse 元素包含状态和单个 DisconnectPhoneCall 请求的结果。
ms.openlocfilehash: 06471ea342424298a4e1d5a0562f8ed9866e26d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753906"
---
# <a name="disconnectphonecallresponse"></a><span data-ttu-id="578f1-103">DisconnectPhoneCallResponse</span><span class="sxs-lookup"><span data-stu-id="578f1-103">DisconnectPhoneCallResponse</span></span>

<span data-ttu-id="578f1-104">**DisconnectPhoneCallResponse**元素包含状态和单个**DisconnectPhoneCall**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="578f1-104">The **DisconnectPhoneCallResponse** element contains the status and result of a single **DisconnectPhoneCall** request.</span></span> 
  
```xml
<DisconnectPhoneCallResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DisconnectPhoneCallResponse>
```

 <span data-ttu-id="578f1-105">**DisconnectPhoneCallResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="578f1-105">**DisconnectPhoneCallResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="578f1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="578f1-106">Attributes and elements</span></span>

<span data-ttu-id="578f1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="578f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="578f1-108">属性</span><span class="sxs-lookup"><span data-stu-id="578f1-108">Attributes</span></span>

|<span data-ttu-id="578f1-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="578f1-109">**Attribute**</span></span>|<span data-ttu-id="578f1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="578f1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="578f1-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="578f1-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="578f1-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="578f1-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="578f1-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="578f1-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="578f1-114">-成功</span><span class="sxs-lookup"><span data-stu-id="578f1-114">-  Success</span></span>  <br/><span data-ttu-id="578f1-115">-警告</span><span class="sxs-lookup"><span data-stu-id="578f1-115">-  Warning</span></span>  <br/><span data-ttu-id="578f1-116">-错误</span><span class="sxs-lookup"><span data-stu-id="578f1-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="578f1-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="578f1-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="578f1-118">**值**</span><span class="sxs-lookup"><span data-stu-id="578f1-118">**Value**</span></span>|<span data-ttu-id="578f1-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="578f1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="578f1-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="578f1-120">**Success**</span></span> <br/> |<span data-ttu-id="578f1-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="578f1-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="578f1-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="578f1-122">**Warning**</span></span> <br/> | <span data-ttu-id="578f1-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="578f1-123">Describes a request that was not processed.</span></span> <span data-ttu-id="578f1-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="578f1-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="578f1-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="578f1-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="578f1-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="578f1-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="578f1-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="578f1-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="578f1-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="578f1-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="578f1-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="578f1-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="578f1-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="578f1-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="578f1-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="578f1-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="578f1-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="578f1-132">**Error**</span></span> <br/> | <span data-ttu-id="578f1-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="578f1-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="578f1-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="578f1-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="578f1-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="578f1-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="578f1-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="578f1-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="578f1-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="578f1-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="578f1-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="578f1-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="578f1-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="578f1-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="578f1-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="578f1-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="578f1-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="578f1-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="578f1-142">子元素</span><span class="sxs-lookup"><span data-stu-id="578f1-142">Child elements</span></span>

|<span data-ttu-id="578f1-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="578f1-143">**Element**</span></span>|<span data-ttu-id="578f1-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="578f1-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="578f1-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="578f1-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="578f1-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="578f1-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="578f1-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="578f1-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="578f1-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="578f1-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="578f1-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="578f1-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="578f1-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="578f1-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="578f1-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="578f1-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="578f1-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="578f1-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="578f1-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="578f1-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="578f1-154">父元素</span><span class="sxs-lookup"><span data-stu-id="578f1-154">Parent elements</span></span>

<span data-ttu-id="578f1-155">无。</span><span class="sxs-lookup"><span data-stu-id="578f1-155">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="578f1-156">文本值</span><span class="sxs-lookup"><span data-stu-id="578f1-156">Text value</span></span>

<span data-ttu-id="578f1-157">无。</span><span class="sxs-lookup"><span data-stu-id="578f1-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="578f1-158">备注</span><span class="sxs-lookup"><span data-stu-id="578f1-158">Remarks</span></span>

<span data-ttu-id="578f1-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="578f1-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="578f1-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="578f1-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="578f1-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="578f1-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="578f1-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="578f1-162">Schema Name</span></span>  <br/> |<span data-ttu-id="578f1-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="578f1-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="578f1-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="578f1-164">Validation File</span></span>  <br/> |<span data-ttu-id="578f1-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="578f1-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="578f1-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="578f1-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="578f1-167">False</span><span class="sxs-lookup"><span data-stu-id="578f1-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="578f1-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="578f1-168">See also</span></span>

- [<span data-ttu-id="578f1-169">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="578f1-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

