---
title: GetItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: GetItemResponseMessage 元素包含状态和单个 GetItem 操作请求的结果。
ms.openlocfilehash: 0c8527258d4637ede053e189dfb918b910c859d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754610"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="9ed6b-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9ed6b-103">GetItemResponseMessage</span></span>

<span data-ttu-id="9ed6b-104">**GetItemResponseMessage**元素包含状态和的单个结果[GetItem 操作](getitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="9ed6b-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="9ed6b-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="9ed6b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9ed6b-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="9ed6b-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9ed6b-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="9ed6b-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9ed6b-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ed6b-109">Attributes and elements</span></span>

<span data-ttu-id="9ed6b-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ed6b-111">属性</span><span class="sxs-lookup"><span data-stu-id="9ed6b-111">Attributes</span></span>

|<span data-ttu-id="9ed6b-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-112">**Attribute**</span></span>|<span data-ttu-id="9ed6b-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ed6b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9ed6b-115">描述[GetItem 操作](getitem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="9ed6b-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="9ed6b-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="9ed6b-117">-成功</span><span class="sxs-lookup"><span data-stu-id="9ed6b-117">- Success</span></span><br/><span data-ttu-id="9ed6b-118">-警告</span><span class="sxs-lookup"><span data-stu-id="9ed6b-118">- Warning</span></span><br/><span data-ttu-id="9ed6b-119">-错误</span><span class="sxs-lookup"><span data-stu-id="9ed6b-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9ed6b-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="9ed6b-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="9ed6b-121">**值**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-121">**Value**</span></span>|<span data-ttu-id="9ed6b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ed6b-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-123">**Success**</span></span> <br/> |<span data-ttu-id="9ed6b-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9ed6b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-125">**Warning**</span></span> <br/> | <span data-ttu-id="9ed6b-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-126">Describes a request that was not processed.</span></span> <span data-ttu-id="9ed6b-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="9ed6b-128">警告的源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="9ed6b-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="9ed6b-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="9ed6b-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="9ed6b-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="9ed6b-132">-MDB 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-132">- MDB is offline.</span></span><br/><span data-ttu-id="9ed6b-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-133">- Password is expired.</span></span>  <br/><span data-ttu-id="9ed6b-134">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="9ed6b-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-135">**Error**</span></span> <br/> | <span data-ttu-id="9ed6b-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="9ed6b-137">下面是个错误的源的示例：</span><span class="sxs-lookup"><span data-stu-id="9ed6b-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="9ed6b-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="9ed6b-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="9ed6b-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="9ed6b-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="9ed6b-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="9ed6b-140">- Unknown tag</span></span><br/><span data-ttu-id="9ed6b-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="9ed6b-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="9ed6b-142">的尝试的任何客户端未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="9ed6b-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="9ed6b-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="9ed6b-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="9ed6b-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="9ed6b-145">子元素</span><span class="sxs-lookup"><span data-stu-id="9ed6b-145">Child elements</span></span>

|<span data-ttu-id="9ed6b-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-146">**Element**</span></span>|<span data-ttu-id="9ed6b-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ed6b-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="9ed6b-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9ed6b-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9ed6b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9ed6b-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9ed6b-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9ed6b-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9ed6b-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9ed6b-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9ed6b-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9ed6b-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9ed6b-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9ed6b-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9ed6b-157">Items</span><span class="sxs-lookup"><span data-stu-id="9ed6b-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="9ed6b-158">包含数组返回的项。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ed6b-159">父元素</span><span class="sxs-lookup"><span data-stu-id="9ed6b-159">Parent elements</span></span>

|<span data-ttu-id="9ed6b-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-160">**Element**</span></span>|<span data-ttu-id="9ed6b-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ed6b-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ed6b-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9ed6b-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9ed6b-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ed6b-164">注解</span><span class="sxs-lookup"><span data-stu-id="9ed6b-164">Remarks</span></span>

<span data-ttu-id="9ed6b-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9ed6b-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ed6b-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ed6b-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ed6b-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ed6b-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9ed6b-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ed6b-168">Schema Name</span></span>  <br/> |<span data-ttu-id="9ed6b-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="9ed6b-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9ed6b-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ed6b-170">Validation File</span></span>  <br/> |<span data-ttu-id="9ed6b-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9ed6b-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9ed6b-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ed6b-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ed6b-173">False</span><span class="sxs-lookup"><span data-stu-id="9ed6b-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ed6b-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ed6b-174">See also</span></span>

- [<span data-ttu-id="9ed6b-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="9ed6b-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="9ed6b-176">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="9ed6b-176">GetItem operation</span></span>](getitem-operation.md)

