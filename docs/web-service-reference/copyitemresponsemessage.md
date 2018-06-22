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
description: CopyItemResponseMessage 元素包含状态和单个 CopyItem 操作请求的结果。
ms.openlocfilehash: 6c1acaff422fd731ca81a3ab244d76a73f3b5c15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753613"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="124f6-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="124f6-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="124f6-104">**CopyItemResponseMessage**元素包含状态和的单个结果[CopyItem 操作](copyitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="124f6-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="124f6-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="124f6-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="124f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="124f6-106">Attributes and elements</span></span>

<span data-ttu-id="124f6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="124f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="124f6-108">属性</span><span class="sxs-lookup"><span data-stu-id="124f6-108">Attributes</span></span>

|<span data-ttu-id="124f6-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="124f6-109">**Attribute**</span></span>|<span data-ttu-id="124f6-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="124f6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="124f6-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="124f6-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="124f6-112">描述[CopyItem 操作](copyitem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="124f6-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="124f6-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="124f6-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="124f6-114">-成功</span><span class="sxs-lookup"><span data-stu-id="124f6-114">- Success</span></span>  <br/><span data-ttu-id="124f6-115">-警告</span><span class="sxs-lookup"><span data-stu-id="124f6-115">-  Warning</span></span>  <br/><span data-ttu-id="124f6-116">-错误</span><span class="sxs-lookup"><span data-stu-id="124f6-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="124f6-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="124f6-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="124f6-118">**值**</span><span class="sxs-lookup"><span data-stu-id="124f6-118">**Value**</span></span>|<span data-ttu-id="124f6-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="124f6-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="124f6-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="124f6-120">**Success**</span></span> <br/> |<span data-ttu-id="124f6-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="124f6-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="124f6-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="124f6-122">**Warning**</span></span> <br/> | <span data-ttu-id="124f6-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="124f6-123">Describes a request that was not processed.</span></span> <span data-ttu-id="124f6-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="124f6-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="124f6-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="124f6-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="124f6-126">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="124f6-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="124f6-127">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="124f6-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="124f6-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="124f6-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="124f6-129">-邮箱数据库 (MDB) 脱机。</span><span class="sxs-lookup"><span data-stu-id="124f6-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="124f6-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="124f6-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="124f6-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="124f6-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="124f6-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="124f6-132">**Error**</span></span> <br/> | <span data-ttu-id="124f6-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="124f6-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="124f6-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="124f6-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="124f6-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="124f6-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="124f6-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="124f6-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="124f6-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="124f6-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="124f6-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="124f6-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="124f6-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="124f6-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="124f6-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="124f6-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="124f6-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="124f6-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="124f6-142">子元素</span><span class="sxs-lookup"><span data-stu-id="124f6-142">Child elements</span></span>

|<span data-ttu-id="124f6-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="124f6-143">**Element**</span></span>|<span data-ttu-id="124f6-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="124f6-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="124f6-145">- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="124f6-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="124f6-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="124f6-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="124f6-147">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="124f6-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="124f6-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="124f6-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="124f6-149">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="124f6-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="124f6-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="124f6-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="124f6-151">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="124f6-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="124f6-152">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="124f6-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="124f6-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="124f6-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="124f6-154">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="124f6-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="124f6-155">Items</span><span class="sxs-lookup"><span data-stu-id="124f6-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="124f6-156">包含数组的复制的项</span><span class="sxs-lookup"><span data-stu-id="124f6-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="124f6-157">父元素</span><span class="sxs-lookup"><span data-stu-id="124f6-157">Parent elements</span></span>

|<span data-ttu-id="124f6-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="124f6-158">**Element**</span></span>|<span data-ttu-id="124f6-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="124f6-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="124f6-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="124f6-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="124f6-161">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="124f6-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="124f6-162">备注</span><span class="sxs-lookup"><span data-stu-id="124f6-162">Remarks</span></span>

<span data-ttu-id="124f6-163">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="124f6-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="124f6-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="124f6-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="124f6-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="124f6-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="124f6-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="124f6-166">Schema name</span></span>  <br/> |<span data-ttu-id="124f6-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="124f6-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="124f6-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="124f6-168">Validation file</span></span>  <br/> |<span data-ttu-id="124f6-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="124f6-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="124f6-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="124f6-170">Can be empty</span></span>  <br/> |<span data-ttu-id="124f6-171">False</span><span class="sxs-lookup"><span data-stu-id="124f6-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="124f6-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="124f6-172">See also</span></span>

- [<span data-ttu-id="124f6-173">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="124f6-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="124f6-174">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="124f6-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

