---
title: CopyItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItemResponseMessage
api_type:
- schema
ms.assetid: a43fe442-12c8-44ab-912c-8a226c9bb3e7
description: CopyItemResponseMessage 元素包含单个 CopyItem 操作请求的状态和结果。
ms.openlocfilehash: 99449a4c05d0b2ea13dfca4235aa5f40d54d1214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466442"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="18164-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="18164-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="18164-104">**CopyItemResponseMessage**元素包含单个[CopyItem 操作](copyitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="18164-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="18164-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="18164-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18164-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18164-106">Attributes and elements</span></span>

<span data-ttu-id="18164-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18164-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18164-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="18164-108">Attributes</span></span>

|<span data-ttu-id="18164-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="18164-109">**Attribute**</span></span>|<span data-ttu-id="18164-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="18164-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18164-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="18164-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="18164-112">描述[CopyItem 操作](copyitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="18164-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="18164-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="18164-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="18164-114">-成功</span><span class="sxs-lookup"><span data-stu-id="18164-114">- Success</span></span>  <br/><span data-ttu-id="18164-115">-警告</span><span class="sxs-lookup"><span data-stu-id="18164-115">-  Warning</span></span>  <br/><span data-ttu-id="18164-116">-错误</span><span class="sxs-lookup"><span data-stu-id="18164-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="18164-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="18164-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="18164-118">**值**</span><span class="sxs-lookup"><span data-stu-id="18164-118">**Value**</span></span>|<span data-ttu-id="18164-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="18164-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18164-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="18164-120">**Success**</span></span> <br/> |<span data-ttu-id="18164-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="18164-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="18164-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="18164-122">**Warning**</span></span> <br/> | <span data-ttu-id="18164-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="18164-123">Describes a request that was not processed.</span></span> <span data-ttu-id="18164-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="18164-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="18164-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="18164-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="18164-126">-Exchange 存储在批处理过程中脱机。</span><span class="sxs-lookup"><span data-stu-id="18164-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="18164-127">-Active Directory 域服务（AD DS）脱机。</span><span class="sxs-lookup"><span data-stu-id="18164-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="18164-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="18164-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="18164-129">-邮箱数据库（MDB）脱机。</span><span class="sxs-lookup"><span data-stu-id="18164-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="18164-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="18164-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="18164-131">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="18164-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="18164-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="18164-132">**Error**</span></span> <br/> | <span data-ttu-id="18164-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="18164-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="18164-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="18164-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="18164-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="18164-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="18164-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="18164-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="18164-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="18164-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="18164-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="18164-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="18164-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="18164-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="18164-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="18164-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="18164-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="18164-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18164-142">子元素</span><span class="sxs-lookup"><span data-stu-id="18164-142">Child elements</span></span>

|<span data-ttu-id="18164-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="18164-143">**Element**</span></span>|<span data-ttu-id="18164-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="18164-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18164-145">- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="18164-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="18164-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="18164-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="18164-147">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="18164-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="18164-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="18164-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="18164-149">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="18164-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="18164-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="18164-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="18164-151">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="18164-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="18164-152">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="18164-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="18164-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="18164-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="18164-154">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="18164-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="18164-155">Items</span><span class="sxs-lookup"><span data-stu-id="18164-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="18164-156">包含复制项的数组</span><span class="sxs-lookup"><span data-stu-id="18164-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18164-157">父元素</span><span class="sxs-lookup"><span data-stu-id="18164-157">Parent elements</span></span>

|<span data-ttu-id="18164-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="18164-158">**Element**</span></span>|<span data-ttu-id="18164-159">**描述**</span><span class="sxs-lookup"><span data-stu-id="18164-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18164-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="18164-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="18164-161">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="18164-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18164-162">备注</span><span class="sxs-lookup"><span data-stu-id="18164-162">Remarks</span></span>

<span data-ttu-id="18164-163">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18164-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18164-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="18164-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18164-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="18164-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18164-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="18164-166">Schema name</span></span>  <br/> |<span data-ttu-id="18164-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="18164-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18164-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="18164-168">Validation file</span></span>  <br/> |<span data-ttu-id="18164-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="18164-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18164-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="18164-170">Can be empty</span></span>  <br/> |<span data-ttu-id="18164-171">False</span><span class="sxs-lookup"><span data-stu-id="18164-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18164-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18164-172">See also</span></span>

- [<span data-ttu-id="18164-173">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="18164-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="18164-174">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="18164-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

