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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753613"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="8099e-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8099e-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="8099e-104">**CopyItemResponseMessage**元素包含状态和的单个结果[CopyItem 操作](copyitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="8099e-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="8099e-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8099e-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8099e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8099e-106">Attributes and elements</span></span>

<span data-ttu-id="8099e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8099e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8099e-108">属性</span><span class="sxs-lookup"><span data-stu-id="8099e-108">Attributes</span></span>

|<span data-ttu-id="8099e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8099e-109">**Attribute**</span></span>|<span data-ttu-id="8099e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8099e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8099e-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8099e-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8099e-112">描述[CopyItem 操作](copyitem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="8099e-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="8099e-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="8099e-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="8099e-114">-成功</span><span class="sxs-lookup"><span data-stu-id="8099e-114">- Success</span></span>  <br/><span data-ttu-id="8099e-115">-警告</span><span class="sxs-lookup"><span data-stu-id="8099e-115">-  Warning</span></span>  <br/><span data-ttu-id="8099e-116">-错误</span><span class="sxs-lookup"><span data-stu-id="8099e-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8099e-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="8099e-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="8099e-118">**值**</span><span class="sxs-lookup"><span data-stu-id="8099e-118">**Value**</span></span>|<span data-ttu-id="8099e-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8099e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8099e-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="8099e-120">**Success**</span></span> <br/> |<span data-ttu-id="8099e-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="8099e-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8099e-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8099e-122">**Warning**</span></span> <br/> | <span data-ttu-id="8099e-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="8099e-123">Describes a request that was not processed.</span></span> <span data-ttu-id="8099e-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="8099e-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8099e-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="8099e-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8099e-126">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="8099e-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="8099e-127">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="8099e-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="8099e-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="8099e-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8099e-129">-邮箱数据库 (MDB) 脱机。</span><span class="sxs-lookup"><span data-stu-id="8099e-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="8099e-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="8099e-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="8099e-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="8099e-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="8099e-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="8099e-132">**Error**</span></span> <br/> | <span data-ttu-id="8099e-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="8099e-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="8099e-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="8099e-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8099e-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="8099e-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8099e-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="8099e-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8099e-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="8099e-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="8099e-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="8099e-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="8099e-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="8099e-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8099e-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="8099e-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="8099e-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="8099e-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8099e-142">子元素</span><span class="sxs-lookup"><span data-stu-id="8099e-142">Child elements</span></span>

|<span data-ttu-id="8099e-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="8099e-143">**Element**</span></span>|<span data-ttu-id="8099e-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="8099e-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8099e-145">- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="8099e-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="8099e-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="8099e-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8099e-147">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="8099e-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8099e-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8099e-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8099e-149">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="8099e-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8099e-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8099e-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8099e-151">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="8099e-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8099e-152">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="8099e-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8099e-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8099e-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8099e-154">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="8099e-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8099e-155">Items</span><span class="sxs-lookup"><span data-stu-id="8099e-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="8099e-156">包含数组的复制的项</span><span class="sxs-lookup"><span data-stu-id="8099e-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8099e-157">父元素</span><span class="sxs-lookup"><span data-stu-id="8099e-157">Parent elements</span></span>

|<span data-ttu-id="8099e-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="8099e-158">**Element**</span></span>|<span data-ttu-id="8099e-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="8099e-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8099e-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8099e-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8099e-161">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="8099e-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8099e-162">注解</span><span class="sxs-lookup"><span data-stu-id="8099e-162">Remarks</span></span>

<span data-ttu-id="8099e-163">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8099e-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8099e-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="8099e-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8099e-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="8099e-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8099e-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="8099e-166">Schema name</span></span>  <br/> |<span data-ttu-id="8099e-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="8099e-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8099e-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="8099e-168">Validation file</span></span>  <br/> |<span data-ttu-id="8099e-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8099e-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8099e-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="8099e-170">Can be empty</span></span>  <br/> |<span data-ttu-id="8099e-171">False</span><span class="sxs-lookup"><span data-stu-id="8099e-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8099e-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8099e-172">See also</span></span>

- [<span data-ttu-id="8099e-173">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="8099e-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="8099e-174">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="8099e-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

