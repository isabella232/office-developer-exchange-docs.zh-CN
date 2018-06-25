---
title: ConvertIdResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponseMessage
api_type:
- schema
ms.assetid: 7a439cae-0268-4328-9ded-af56ad642227
description: ConvertIdResponseMessage 元素包含状态和 ConvertId 操作请求的结果。
ms.openlocfilehash: 6668c0b3254191ca628413bae5ff957c3cb95b5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753605"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="79aea-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="79aea-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="79aea-104">**ConvertIdResponseMessage**元素包含状态和[ConvertId 操作](convertid-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="79aea-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="79aea-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="79aea-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="79aea-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="79aea-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="79aea-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="79aea-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="79aea-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="79aea-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79aea-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="79aea-109">Attributes and elements</span></span>

<span data-ttu-id="79aea-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="79aea-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79aea-111">属性</span><span class="sxs-lookup"><span data-stu-id="79aea-111">Attributes</span></span>

|<span data-ttu-id="79aea-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="79aea-112">**Attribute**</span></span>|<span data-ttu-id="79aea-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="79aea-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79aea-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="79aea-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="79aea-115">描述[ConvertId 操作](convertid-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="79aea-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="79aea-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="79aea-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="79aea-117">-成功</span><span class="sxs-lookup"><span data-stu-id="79aea-117">- Success</span></span>  <br/><span data-ttu-id="79aea-118">-警告</span><span class="sxs-lookup"><span data-stu-id="79aea-118">-  Warning</span></span>  <br/><span data-ttu-id="79aea-119">-错误</span><span class="sxs-lookup"><span data-stu-id="79aea-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="79aea-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="79aea-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="79aea-121">**值**</span><span class="sxs-lookup"><span data-stu-id="79aea-121">**Value**</span></span>|<span data-ttu-id="79aea-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="79aea-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79aea-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="79aea-123">**Success**</span></span> <br/> |<span data-ttu-id="79aea-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="79aea-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="79aea-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="79aea-125">**Warning**</span></span> <br/> | <span data-ttu-id="79aea-126">介绍的请求完全未处理的或为其出现意外的结果。</span><span class="sxs-lookup"><span data-stu-id="79aea-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="79aea-127">**Error**</span><span class="sxs-lookup"><span data-stu-id="79aea-127">**Error**</span></span> <br/> | <span data-ttu-id="79aea-128">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="79aea-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="79aea-129">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="79aea-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="79aea-130">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="79aea-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="79aea-131">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="79aea-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="79aea-132">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="79aea-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="79aea-133">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="79aea-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="79aea-134">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="79aea-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="79aea-135">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="79aea-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="79aea-136">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="79aea-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="79aea-137">子元素</span><span class="sxs-lookup"><span data-stu-id="79aea-137">Child elements</span></span>

|<span data-ttu-id="79aea-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="79aea-138">**Element**</span></span>|<span data-ttu-id="79aea-139">**说明**</span><span class="sxs-lookup"><span data-stu-id="79aea-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79aea-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="79aea-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="79aea-141">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="79aea-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="79aea-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="79aea-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="79aea-143">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="79aea-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="79aea-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="79aea-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="79aea-145">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="79aea-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="79aea-146">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="79aea-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="79aea-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="79aea-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="79aea-148">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="79aea-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="79aea-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="79aea-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="79aea-150">介绍在响应中的转换后的标识符。</span><span class="sxs-lookup"><span data-stu-id="79aea-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79aea-151">父元素</span><span class="sxs-lookup"><span data-stu-id="79aea-151">Parent elements</span></span>

|<span data-ttu-id="79aea-152">**元素**</span><span class="sxs-lookup"><span data-stu-id="79aea-152">**Element**</span></span>|<span data-ttu-id="79aea-153">**说明**</span><span class="sxs-lookup"><span data-stu-id="79aea-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79aea-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="79aea-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="79aea-155">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="79aea-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79aea-156">注解</span><span class="sxs-lookup"><span data-stu-id="79aea-156">Remarks</span></span>

<span data-ttu-id="79aea-157">返回一个响应消息，每个转换后的标识符。</span><span class="sxs-lookup"><span data-stu-id="79aea-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="79aea-158">如果返回错误响应代码，，将从该响应缺少[AlternateId](alternateid.md)元素</span><span class="sxs-lookup"><span data-stu-id="79aea-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="79aea-159">描述此元素的架构位于运行安装了客户端访问服务器角色的 Exchange 2010 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="79aea-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79aea-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="79aea-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79aea-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="79aea-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="79aea-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="79aea-162">Schema Name</span></span>  <br/> |<span data-ttu-id="79aea-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="79aea-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="79aea-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="79aea-164">Validation File</span></span>  <br/> |<span data-ttu-id="79aea-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="79aea-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="79aea-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="79aea-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="79aea-167">False</span><span class="sxs-lookup"><span data-stu-id="79aea-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79aea-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79aea-168">See also</span></span>

- [<span data-ttu-id="79aea-169">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="79aea-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="79aea-170">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="79aea-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

