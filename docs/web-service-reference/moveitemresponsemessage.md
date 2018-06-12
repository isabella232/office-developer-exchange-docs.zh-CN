---
title: MoveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItemResponseMessage
api_type:
- schema
ms.assetid: 1efacb2c-cb76-44ad-b0be-bb47bf2553be
description: MoveItemResponseMessage 元素包含状态和单个 MoveItem 操作请求的结果。
ms.openlocfilehash: af1c10391d9b5b761ab87983eea6321d61231152
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826493"
---
# <a name="moveitemresponsemessage"></a><span data-ttu-id="0cef2-103">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0cef2-103">MoveItemResponseMessage</span></span>

<span data-ttu-id="0cef2-104">**MoveItemResponseMessage**元素包含状态和的单个结果[MoveItem 操作](moveitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="0cef2-104">The **MoveItemResponseMessage** element contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.</span></span> 
  
```xml
<MoveItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</MoveItemResponseMessage>
```

 <span data-ttu-id="0cef2-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0cef2-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cef2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0cef2-106">Attributes and elements</span></span>

<span data-ttu-id="0cef2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0cef2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cef2-108">属性</span><span class="sxs-lookup"><span data-stu-id="0cef2-108">Attributes</span></span>

|<span data-ttu-id="0cef2-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0cef2-109">**Attribute**</span></span>|<span data-ttu-id="0cef2-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cef2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cef2-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0cef2-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0cef2-112">描述[MoveItem 操作](moveitem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="0cef2-112">Describes the status of a [MoveItem operation](moveitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="0cef2-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="0cef2-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0cef2-114">-成功</span><span class="sxs-lookup"><span data-stu-id="0cef2-114">-  Success</span></span>  <br/><span data-ttu-id="0cef2-115">-警告</span><span class="sxs-lookup"><span data-stu-id="0cef2-115">-  Warning</span></span>  <br/><span data-ttu-id="0cef2-116">-错误</span><span class="sxs-lookup"><span data-stu-id="0cef2-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="0cef2-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="0cef2-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="0cef2-118">**值**</span><span class="sxs-lookup"><span data-stu-id="0cef2-118">**Value**</span></span>|<span data-ttu-id="0cef2-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cef2-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cef2-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="0cef2-120">**Success**</span></span> <br/> |<span data-ttu-id="0cef2-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="0cef2-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0cef2-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0cef2-122">**Warning**</span></span> <br/> | <span data-ttu-id="0cef2-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="0cef2-123">Describes a request that was not processed.</span></span> <span data-ttu-id="0cef2-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="0cef2-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0cef2-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="0cef2-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="0cef2-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cef2-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0cef2-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cef2-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="0cef2-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="0cef2-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="0cef2-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0cef2-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0cef2-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="0cef2-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="0cef2-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="0cef2-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="0cef2-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="0cef2-132">**Error**</span></span> <br/> | <span data-ttu-id="0cef2-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="0cef2-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="0cef2-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="0cef2-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0cef2-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="0cef2-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0cef2-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="0cef2-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0cef2-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="0cef2-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="0cef2-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="0cef2-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0cef2-139">的尝试的任何客户端任何未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="0cef2-139">-  Any unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="0cef2-140">的有效的客户端的呼叫的响应中任何服务器端故障。</span><span class="sxs-lookup"><span data-stu-id="0cef2-140">-  Any server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="0cef2-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="0cef2-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0cef2-142">子元素</span><span class="sxs-lookup"><span data-stu-id="0cef2-142">Child elements</span></span>

|<span data-ttu-id="0cef2-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cef2-143">**Element**</span></span>|<span data-ttu-id="0cef2-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cef2-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cef2-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="0cef2-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0cef2-146">响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0cef2-146">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0cef2-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0cef2-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0cef2-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0cef2-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0cef2-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0cef2-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0cef2-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0cef2-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0cef2-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="0cef2-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0cef2-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0cef2-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0cef2-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0cef2-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0cef2-154">Items</span><span class="sxs-lookup"><span data-stu-id="0cef2-154">Items</span></span>](items.md) <br/> |<span data-ttu-id="0cef2-155">包含移动的项的数组。</span><span class="sxs-lookup"><span data-stu-id="0cef2-155">Contains an array of moved items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0cef2-156">父元素</span><span class="sxs-lookup"><span data-stu-id="0cef2-156">Parent elements</span></span>

|<span data-ttu-id="0cef2-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cef2-157">**Element**</span></span>|<span data-ttu-id="0cef2-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cef2-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cef2-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0cef2-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0cef2-160">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0cef2-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cef2-161">备注</span><span class="sxs-lookup"><span data-stu-id="0cef2-161">Remarks</span></span>

<span data-ttu-id="0cef2-162">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0cef2-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cef2-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="0cef2-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cef2-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="0cef2-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0cef2-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="0cef2-165">Schema Name</span></span>  <br/> |<span data-ttu-id="0cef2-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="0cef2-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0cef2-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="0cef2-167">Validation File</span></span>  <br/> |<span data-ttu-id="0cef2-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0cef2-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0cef2-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="0cef2-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="0cef2-170">False</span><span class="sxs-lookup"><span data-stu-id="0cef2-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cef2-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cef2-171">See also</span></span>

- [<span data-ttu-id="0cef2-172">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="0cef2-172">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="0cef2-173">MoveItem</span><span class="sxs-lookup"><span data-stu-id="0cef2-173">MoveItem</span></span>](moveitem.md)

