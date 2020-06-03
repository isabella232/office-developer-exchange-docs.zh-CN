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
description: MoveItemResponseMessage 元素包含单个 MoveItem 操作请求的状态和结果。
ms.openlocfilehash: fd96c34840acd5b6137a2a5d50980dc86202629f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530392"
---
# <a name="moveitemresponsemessage"></a><span data-ttu-id="79c23-103">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="79c23-103">MoveItemResponseMessage</span></span>

<span data-ttu-id="79c23-104">**MoveItemResponseMessage**元素包含单个[MoveItem 操作](moveitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="79c23-104">The **MoveItemResponseMessage** element contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.</span></span> 
  
```xml
<MoveItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</MoveItemResponseMessage>
```

 <span data-ttu-id="79c23-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="79c23-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79c23-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="79c23-106">Attributes and elements</span></span>

<span data-ttu-id="79c23-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="79c23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79c23-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="79c23-108">Attributes</span></span>

|<span data-ttu-id="79c23-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="79c23-109">**Attribute**</span></span>|<span data-ttu-id="79c23-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="79c23-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79c23-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="79c23-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="79c23-112">描述[MoveItem 操作](moveitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="79c23-112">Describes the status of a [MoveItem operation](moveitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="79c23-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="79c23-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="79c23-114">-成功</span><span class="sxs-lookup"><span data-stu-id="79c23-114">-  Success</span></span>  <br/><span data-ttu-id="79c23-115">-警告</span><span class="sxs-lookup"><span data-stu-id="79c23-115">-  Warning</span></span>  <br/><span data-ttu-id="79c23-116">-错误</span><span class="sxs-lookup"><span data-stu-id="79c23-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="79c23-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="79c23-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="79c23-118">**值**</span><span class="sxs-lookup"><span data-stu-id="79c23-118">**Value**</span></span>|<span data-ttu-id="79c23-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="79c23-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79c23-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="79c23-120">**Success**</span></span> <br/> |<span data-ttu-id="79c23-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="79c23-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="79c23-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="79c23-122">**Warning**</span></span> <br/> | <span data-ttu-id="79c23-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="79c23-123">Describes a request that was not processed.</span></span> <span data-ttu-id="79c23-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="79c23-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="79c23-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="79c23-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="79c23-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79c23-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="79c23-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79c23-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="79c23-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="79c23-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="79c23-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79c23-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="79c23-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="79c23-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="79c23-131">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="79c23-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="79c23-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="79c23-132">**Error**</span></span> <br/> | <span data-ttu-id="79c23-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="79c23-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="79c23-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="79c23-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="79c23-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="79c23-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="79c23-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="79c23-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="79c23-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="79c23-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="79c23-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="79c23-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="79c23-139">-任何客户端尝试的任何未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="79c23-139">-  Any unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="79c23-140">-响应有效客户端调用的任何服务器端故障。</span><span class="sxs-lookup"><span data-stu-id="79c23-140">-  Any server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="79c23-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="79c23-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="79c23-142">子元素</span><span class="sxs-lookup"><span data-stu-id="79c23-142">Child elements</span></span>

|<span data-ttu-id="79c23-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="79c23-143">**Element**</span></span>|<span data-ttu-id="79c23-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="79c23-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79c23-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="79c23-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="79c23-146">响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="79c23-146">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="79c23-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="79c23-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="79c23-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="79c23-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="79c23-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="79c23-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="79c23-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="79c23-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="79c23-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="79c23-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="79c23-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="79c23-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="79c23-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="79c23-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="79c23-154">Items</span><span class="sxs-lookup"><span data-stu-id="79c23-154">Items</span></span>](items.md) <br/> |<span data-ttu-id="79c23-155">包含已移动项的数组。</span><span class="sxs-lookup"><span data-stu-id="79c23-155">Contains an array of moved items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79c23-156">父元素</span><span class="sxs-lookup"><span data-stu-id="79c23-156">Parent elements</span></span>

|<span data-ttu-id="79c23-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="79c23-157">**Element**</span></span>|<span data-ttu-id="79c23-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="79c23-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79c23-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="79c23-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="79c23-160">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="79c23-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79c23-161">备注</span><span class="sxs-lookup"><span data-stu-id="79c23-161">Remarks</span></span>

<span data-ttu-id="79c23-162">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="79c23-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79c23-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="79c23-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79c23-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="79c23-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="79c23-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="79c23-165">Schema Name</span></span>  <br/> |<span data-ttu-id="79c23-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="79c23-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="79c23-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="79c23-167">Validation File</span></span>  <br/> |<span data-ttu-id="79c23-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="79c23-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="79c23-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="79c23-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="79c23-170">False</span><span class="sxs-lookup"><span data-stu-id="79c23-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79c23-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79c23-171">See also</span></span>

- [<span data-ttu-id="79c23-172">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="79c23-172">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="79c23-173">MoveItem</span><span class="sxs-lookup"><span data-stu-id="79c23-173">MoveItem</span></span>](moveitem.md)

