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
description: GetItemResponseMessage 元素包含单个 GetItem 操作请求的状态和结果。
ms.openlocfilehash: bd25a82641259e1546bad6eef5c2f6f8f03e98cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458668"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="266d5-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="266d5-103">GetItemResponseMessage</span></span>

<span data-ttu-id="266d5-104">**GetItemResponseMessage**元素包含单个[GetItem 操作](getitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="266d5-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="266d5-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="266d5-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="266d5-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="266d5-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="266d5-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="266d5-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="266d5-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="266d5-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="266d5-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="266d5-109">Attributes and elements</span></span>

<span data-ttu-id="266d5-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="266d5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="266d5-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="266d5-111">Attributes</span></span>

|<span data-ttu-id="266d5-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="266d5-112">**Attribute**</span></span>|<span data-ttu-id="266d5-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="266d5-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="266d5-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="266d5-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="266d5-115">描述[GetItem 操作](getitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="266d5-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="266d5-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="266d5-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="266d5-117">-成功</span><span class="sxs-lookup"><span data-stu-id="266d5-117">- Success</span></span><br/><span data-ttu-id="266d5-118">-警告</span><span class="sxs-lookup"><span data-stu-id="266d5-118">- Warning</span></span><br/><span data-ttu-id="266d5-119">-错误</span><span class="sxs-lookup"><span data-stu-id="266d5-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="266d5-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="266d5-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="266d5-121">**值**</span><span class="sxs-lookup"><span data-stu-id="266d5-121">**Value**</span></span>|<span data-ttu-id="266d5-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="266d5-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="266d5-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="266d5-123">**Success**</span></span> <br/> |<span data-ttu-id="266d5-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="266d5-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="266d5-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="266d5-125">**Warning**</span></span> <br/> | <span data-ttu-id="266d5-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="266d5-126">Describes a request that was not processed.</span></span> <span data-ttu-id="266d5-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="266d5-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="266d5-128">以下是警告的源代码示例：</span><span class="sxs-lookup"><span data-stu-id="266d5-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="266d5-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="266d5-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="266d5-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="266d5-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="266d5-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="266d5-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="266d5-132">-MDB 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="266d5-132">- MDB is offline.</span></span><br/><span data-ttu-id="266d5-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="266d5-133">- Password is expired.</span></span>  <br/><span data-ttu-id="266d5-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="266d5-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="266d5-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="266d5-135">**Error**</span></span> <br/> | <span data-ttu-id="266d5-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="266d5-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="266d5-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="266d5-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="266d5-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="266d5-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="266d5-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="266d5-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="266d5-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="266d5-140">- Unknown tag</span></span><br/><span data-ttu-id="266d5-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="266d5-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="266d5-142">-任何客户端尝试的未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="266d5-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="266d5-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="266d5-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="266d5-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="266d5-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="266d5-145">子元素</span><span class="sxs-lookup"><span data-stu-id="266d5-145">Child elements</span></span>

|<span data-ttu-id="266d5-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="266d5-146">**Element**</span></span>|<span data-ttu-id="266d5-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="266d5-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="266d5-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="266d5-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="266d5-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="266d5-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="266d5-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="266d5-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="266d5-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="266d5-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="266d5-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="266d5-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="266d5-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="266d5-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="266d5-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="266d5-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="266d5-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="266d5-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="266d5-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="266d5-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="266d5-157">Items</span><span class="sxs-lookup"><span data-stu-id="266d5-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="266d5-158">包含返回项的数组。</span><span class="sxs-lookup"><span data-stu-id="266d5-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="266d5-159">父元素</span><span class="sxs-lookup"><span data-stu-id="266d5-159">Parent elements</span></span>

|<span data-ttu-id="266d5-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="266d5-160">**Element**</span></span>|<span data-ttu-id="266d5-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="266d5-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="266d5-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="266d5-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="266d5-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="266d5-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="266d5-164">备注</span><span class="sxs-lookup"><span data-stu-id="266d5-164">Remarks</span></span>

<span data-ttu-id="266d5-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="266d5-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="266d5-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="266d5-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="266d5-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="266d5-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="266d5-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="266d5-168">Schema Name</span></span>  <br/> |<span data-ttu-id="266d5-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="266d5-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="266d5-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="266d5-170">Validation File</span></span>  <br/> |<span data-ttu-id="266d5-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="266d5-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="266d5-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="266d5-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="266d5-173">False</span><span class="sxs-lookup"><span data-stu-id="266d5-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="266d5-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="266d5-174">See also</span></span>

- [<span data-ttu-id="266d5-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="266d5-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="266d5-176">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="266d5-176">GetItem operation</span></span>](getitem-operation.md)

