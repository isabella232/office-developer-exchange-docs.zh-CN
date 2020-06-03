---
title: FindConversationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversationResponse
api_type:
- schema
ms.assetid: a689e29d-5f3d-4deb-81ee-8b6cc60f6dea
description: FindConversationResponse 元素定义对 FindConversation 操作请求的响应。
ms.openlocfilehash: 68acc42045b91ab4b574f32ba3fd622057863015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462638"
---
# <a name="findconversationresponse"></a><span data-ttu-id="66f8f-103">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="66f8f-103">FindConversationResponse</span></span>

<span data-ttu-id="66f8f-104">**FindConversationResponse**元素定义对[FindConversation 操作](findconversation-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="66f8f-104">The **FindConversationResponse** element defines a response to a [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
[<span data-ttu-id="66f8f-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="66f8f-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 <span data-ttu-id="66f8f-106">**FindConversationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="66f8f-106">**FindConversationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66f8f-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-107">Attributes and elements</span></span>

<span data-ttu-id="66f8f-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="66f8f-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66f8f-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="66f8f-109">Attributes</span></span>

|<span data-ttu-id="66f8f-110">**属性**</span><span class="sxs-lookup"><span data-stu-id="66f8f-110">**Attribute**</span></span>|<span data-ttu-id="66f8f-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="66f8f-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66f8f-112">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="66f8f-112">**ResponseClass**</span></span> <br/> | <span data-ttu-id="66f8f-113">描述[FindConversation 操作](findconversation-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="66f8f-113">Describes the status of a [FindConversation operation](findconversation-operation.md) response.</span></span> <br/><br/><span data-ttu-id="66f8f-114">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="66f8f-114">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="66f8f-115">-成功</span><span class="sxs-lookup"><span data-stu-id="66f8f-115">-  Success</span></span>  <br/><span data-ttu-id="66f8f-116">-警告</span><span class="sxs-lookup"><span data-stu-id="66f8f-116">-  Warning</span></span>  <br/><span data-ttu-id="66f8f-117">-错误</span><span class="sxs-lookup"><span data-stu-id="66f8f-117">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="66f8f-118">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="66f8f-118">ResponseClass attribute values</span></span>

|<span data-ttu-id="66f8f-119">**值**</span><span class="sxs-lookup"><span data-stu-id="66f8f-119">**Value**</span></span>|<span data-ttu-id="66f8f-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="66f8f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66f8f-121">**Success**</span><span class="sxs-lookup"><span data-stu-id="66f8f-121">**Success**</span></span> <br/> |<span data-ttu-id="66f8f-122">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="66f8f-122">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="66f8f-123">**警告**</span><span class="sxs-lookup"><span data-stu-id="66f8f-123">**Warning**</span></span> <br/> | <span data-ttu-id="66f8f-124">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="66f8f-124">Describes a request that was not processed.</span></span> <span data-ttu-id="66f8f-125">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="66f8f-125">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="66f8f-126">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="66f8f-126">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="66f8f-127">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66f8f-127">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="66f8f-128">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66f8f-128">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="66f8f-129">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="66f8f-129">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="66f8f-130">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66f8f-130">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="66f8f-131">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="66f8f-131">-  A password is expired.</span></span>  <br/><span data-ttu-id="66f8f-132">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="66f8f-132">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="66f8f-133">**Error**</span><span class="sxs-lookup"><span data-stu-id="66f8f-133">**Error**</span></span> <br/> | <span data-ttu-id="66f8f-134">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="66f8f-134">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="66f8f-135">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="66f8f-135">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="66f8f-136">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="66f8f-136">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="66f8f-137">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-137">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="66f8f-138">-未知标记</span><span class="sxs-lookup"><span data-stu-id="66f8f-138">-  An unknown tag</span></span>  <br/><span data-ttu-id="66f8f-139">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-139">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="66f8f-140">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="66f8f-140">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="66f8f-141">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="66f8f-141">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="66f8f-142">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="66f8f-142">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66f8f-143">子元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-143">Child elements</span></span>

|<span data-ttu-id="66f8f-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="66f8f-144">**Element**</span></span>|<span data-ttu-id="66f8f-145">**描述**</span><span class="sxs-lookup"><span data-stu-id="66f8f-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66f8f-146">对话</span><span class="sxs-lookup"><span data-stu-id="66f8f-146">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="66f8f-147">包含一组对话。</span><span class="sxs-lookup"><span data-stu-id="66f8f-147">Contains an array of conversations.</span></span>  <br/> |
|[<span data-ttu-id="66f8f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="66f8f-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="66f8f-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="66f8f-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="66f8f-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="66f8f-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="66f8f-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="66f8f-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="66f8f-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="66f8f-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="66f8f-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="66f8f-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="66f8f-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="66f8f-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="66f8f-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="66f8f-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="66f8f-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="66f8f-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66f8f-157">父元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-157">Parent elements</span></span>

<span data-ttu-id="66f8f-158">无。</span><span class="sxs-lookup"><span data-stu-id="66f8f-158">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="66f8f-159">文本值</span><span class="sxs-lookup"><span data-stu-id="66f8f-159">Text value</span></span>

<span data-ttu-id="66f8f-160">无。</span><span class="sxs-lookup"><span data-stu-id="66f8f-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66f8f-161">说明</span><span class="sxs-lookup"><span data-stu-id="66f8f-161">Remarks</span></span>

<span data-ttu-id="66f8f-162">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="66f8f-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66f8f-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="66f8f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66f8f-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="66f8f-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66f8f-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="66f8f-165">Schema name</span></span>  <br/> |<span data-ttu-id="66f8f-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="66f8f-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="66f8f-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="66f8f-167">Validation file</span></span>  <br/> |<span data-ttu-id="66f8f-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="66f8f-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66f8f-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="66f8f-169">Can be empty</span></span>  <br/> |<span data-ttu-id="66f8f-170">False</span><span class="sxs-lookup"><span data-stu-id="66f8f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66f8f-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66f8f-171">See also</span></span>

- [<span data-ttu-id="66f8f-172">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="66f8f-172">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="66f8f-173">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="66f8f-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="66f8f-174">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="66f8f-174">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

