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
description: ConvertIdResponseMessage 元素包含 ConvertId 操作请求的状态和结果。
ms.openlocfilehash: cd0154f87390be3516ced4be53f5371d4a348c49
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456218"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="dce17-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dce17-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="dce17-104">**ConvertIdResponseMessage**元素包含[ConvertId 操作](convertid-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="dce17-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="dce17-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="dce17-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="dce17-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dce17-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="dce17-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dce17-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="dce17-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="dce17-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dce17-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dce17-109">Attributes and elements</span></span>

<span data-ttu-id="dce17-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dce17-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dce17-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="dce17-111">Attributes</span></span>

|<span data-ttu-id="dce17-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="dce17-112">**Attribute**</span></span>|<span data-ttu-id="dce17-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="dce17-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dce17-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="dce17-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="dce17-115">描述[ConvertId 操作](convertid-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="dce17-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="dce17-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="dce17-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="dce17-117">-成功</span><span class="sxs-lookup"><span data-stu-id="dce17-117">- Success</span></span>  <br/><span data-ttu-id="dce17-118">-警告</span><span class="sxs-lookup"><span data-stu-id="dce17-118">-  Warning</span></span>  <br/><span data-ttu-id="dce17-119">-错误</span><span class="sxs-lookup"><span data-stu-id="dce17-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="dce17-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="dce17-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="dce17-121">**值**</span><span class="sxs-lookup"><span data-stu-id="dce17-121">**Value**</span></span>|<span data-ttu-id="dce17-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="dce17-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dce17-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="dce17-123">**Success**</span></span> <br/> |<span data-ttu-id="dce17-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="dce17-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="dce17-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="dce17-125">**Warning**</span></span> <br/> | <span data-ttu-id="dce17-126">介绍未完全处理或发生意外结果的请求。</span><span class="sxs-lookup"><span data-stu-id="dce17-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="dce17-127">**Error**</span><span class="sxs-lookup"><span data-stu-id="dce17-127">**Error**</span></span> <br/> | <span data-ttu-id="dce17-128">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="dce17-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="dce17-129">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="dce17-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="dce17-130">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="dce17-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="dce17-131">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="dce17-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="dce17-132">-未知标记</span><span class="sxs-lookup"><span data-stu-id="dce17-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="dce17-133">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="dce17-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="dce17-134">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="dce17-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="dce17-135">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="dce17-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="dce17-136">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="dce17-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dce17-137">子元素</span><span class="sxs-lookup"><span data-stu-id="dce17-137">Child elements</span></span>

|<span data-ttu-id="dce17-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="dce17-138">**Element**</span></span>|<span data-ttu-id="dce17-139">**描述**</span><span class="sxs-lookup"><span data-stu-id="dce17-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce17-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="dce17-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="dce17-141">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="dce17-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="dce17-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dce17-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="dce17-143">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="dce17-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="dce17-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dce17-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="dce17-145">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="dce17-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="dce17-146">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="dce17-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="dce17-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="dce17-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="dce17-148">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="dce17-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="dce17-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="dce17-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="dce17-150">描述响应中的已转换标识符。</span><span class="sxs-lookup"><span data-stu-id="dce17-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dce17-151">父元素</span><span class="sxs-lookup"><span data-stu-id="dce17-151">Parent elements</span></span>

|<span data-ttu-id="dce17-152">**元素**</span><span class="sxs-lookup"><span data-stu-id="dce17-152">**Element**</span></span>|<span data-ttu-id="dce17-153">**描述**</span><span class="sxs-lookup"><span data-stu-id="dce17-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce17-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dce17-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="dce17-155">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="dce17-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dce17-156">备注</span><span class="sxs-lookup"><span data-stu-id="dce17-156">Remarks</span></span>

<span data-ttu-id="dce17-157">返回每个转换的标识符的一个响应消息。</span><span class="sxs-lookup"><span data-stu-id="dce17-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="dce17-158">如果返回错误响应代码，响应中将缺少[AlternateId](alternateid.md)元素，</span><span class="sxs-lookup"><span data-stu-id="dce17-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="dce17-159">描述此元素的架构位于运行 Exchange 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dce17-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dce17-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="dce17-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dce17-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="dce17-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dce17-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="dce17-162">Schema Name</span></span>  <br/> |<span data-ttu-id="dce17-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="dce17-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dce17-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="dce17-164">Validation File</span></span>  <br/> |<span data-ttu-id="dce17-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dce17-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dce17-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="dce17-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="dce17-167">False</span><span class="sxs-lookup"><span data-stu-id="dce17-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dce17-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dce17-168">See also</span></span>

- [<span data-ttu-id="dce17-169">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="dce17-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="dce17-170">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dce17-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

