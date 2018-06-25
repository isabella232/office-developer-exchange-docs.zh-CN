---
title: CreateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItemResponseMessage
api_type:
- schema
ms.assetid: 595d36c2-f87a-4d50-8e8b-f58d7641564b
description: CreateItemResponseMessage 元素包含状态和单个 CreateItem operation 请求的结果。
ms.openlocfilehash: 099dc799bedb527472bbe7d34cad0dbc8e98bec5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753675"
---
# <a name="createitemresponsemessage"></a><span data-ttu-id="17098-103">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17098-103">CreateItemResponseMessage</span></span>

<span data-ttu-id="17098-104">**CreateItemResponseMessage**元素包含状态和的单个结果[CreateItem operation，](createitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="17098-104">The **CreateItemResponseMessage** element contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="17098-105">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="17098-105">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="17098-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17098-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="17098-107">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17098-107">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
  
```xml
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 <span data-ttu-id="17098-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="17098-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17098-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="17098-109">Attributes and elements</span></span>

<span data-ttu-id="17098-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="17098-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17098-111">属性</span><span class="sxs-lookup"><span data-stu-id="17098-111">Attributes</span></span>

|<span data-ttu-id="17098-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="17098-112">**Attribute**</span></span>|<span data-ttu-id="17098-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="17098-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17098-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="17098-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="17098-115">介绍[CreateItem operation，](createitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="17098-115">Describes the status of a [CreateItem operation](createitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="17098-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="17098-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="17098-117">-成功</span><span class="sxs-lookup"><span data-stu-id="17098-117">-  Success</span></span>  <br/><span data-ttu-id="17098-118">-警告</span><span class="sxs-lookup"><span data-stu-id="17098-118">-  Warning</span></span>  <br/><span data-ttu-id="17098-119">-错误</span><span class="sxs-lookup"><span data-stu-id="17098-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="17098-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="17098-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="17098-121">**值**</span><span class="sxs-lookup"><span data-stu-id="17098-121">**Value**</span></span>|<span data-ttu-id="17098-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="17098-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17098-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="17098-123">**Success**</span></span> <br/> |<span data-ttu-id="17098-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="17098-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="17098-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="17098-125">**Warning**</span></span> <br/> | <span data-ttu-id="17098-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="17098-126">Describes a request that was not processed.</span></span> <span data-ttu-id="17098-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="17098-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="17098-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="17098-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="17098-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="17098-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="17098-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="17098-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="17098-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="17098-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="17098-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="17098-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="17098-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="17098-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="17098-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="17098-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="17098-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="17098-135">**Error**</span></span> <br/> | <span data-ttu-id="17098-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="17098-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="17098-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="17098-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="17098-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="17098-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="17098-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="17098-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="17098-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="17098-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="17098-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="17098-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="17098-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="17098-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="17098-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="17098-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="17098-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="17098-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17098-145">子元素</span><span class="sxs-lookup"><span data-stu-id="17098-145">Child elements</span></span>

|<span data-ttu-id="17098-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="17098-146">**Element**</span></span>|<span data-ttu-id="17098-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="17098-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17098-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="17098-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="17098-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="17098-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="17098-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17098-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="17098-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="17098-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="17098-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="17098-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="17098-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="17098-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="17098-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="17098-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="17098-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="17098-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="17098-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="17098-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="17098-157">Items</span><span class="sxs-lookup"><span data-stu-id="17098-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="17098-158">包含数组的创建的项目。</span><span class="sxs-lookup"><span data-stu-id="17098-158">Contains an array of created items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17098-159">父元素</span><span class="sxs-lookup"><span data-stu-id="17098-159">Parent elements</span></span>

|<span data-ttu-id="17098-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="17098-160">**Element**</span></span>|<span data-ttu-id="17098-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="17098-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17098-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17098-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="17098-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="17098-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17098-164">注解</span><span class="sxs-lookup"><span data-stu-id="17098-164">Remarks</span></span>

<span data-ttu-id="17098-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="17098-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17098-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="17098-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17098-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="17098-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="17098-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="17098-168">Schema Name</span></span>  <br/> |<span data-ttu-id="17098-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="17098-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="17098-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="17098-170">Validation File</span></span>  <br/> |<span data-ttu-id="17098-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="17098-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17098-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="17098-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="17098-173">False</span><span class="sxs-lookup"><span data-stu-id="17098-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17098-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="17098-174">See also</span></span>

- [<span data-ttu-id="17098-175">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="17098-175">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="17098-176">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="17098-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="17098-177">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="17098-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

