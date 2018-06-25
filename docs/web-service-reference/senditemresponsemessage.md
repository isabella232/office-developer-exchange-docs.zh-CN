---
title: SendItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponseMessage
api_type:
- schema
ms.assetid: 264f6a2f-c8cc-4c96-86e1-1aabb6f9d8ab
description: SendItemResponseMessage 元素包含状态和单个 SendItem 操作请求的结果。
ms.openlocfilehash: 70355aa2b46303bfceafa2cfe89f1c84896f3158
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827344"
---
# <a name="senditemresponsemessage"></a><span data-ttu-id="04bb1-103">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="04bb1-103">SendItemResponseMessage</span></span>

<span data-ttu-id="04bb1-104">**SendItemResponseMessage**元素包含状态和的单个结果[SendItem 操作](senditem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="04bb1-104">The **SendItemResponseMessage** element contains the status and result of a single [SendItem operation](senditem-operation.md) request.</span></span> 
  
```xml
<SendItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</SendItemResponseMessage>
```

 <span data-ttu-id="04bb1-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="04bb1-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04bb1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-106">Attributes and elements</span></span>

<span data-ttu-id="04bb1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="04bb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04bb1-108">属性</span><span class="sxs-lookup"><span data-stu-id="04bb1-108">Attributes</span></span>

|<span data-ttu-id="04bb1-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="04bb1-109">**Attribute**</span></span>|<span data-ttu-id="04bb1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="04bb1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04bb1-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="04bb1-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="04bb1-112">描述[SendItem 操作](senditem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="04bb1-112">Describes the status of a [SendItem operation](senditem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="04bb1-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="04bb1-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="04bb1-114">-成功</span><span class="sxs-lookup"><span data-stu-id="04bb1-114">-  Success</span></span>  <br/><span data-ttu-id="04bb1-115">-警告</span><span class="sxs-lookup"><span data-stu-id="04bb1-115">-  Warning</span></span>  <br/><span data-ttu-id="04bb1-116">-错误</span><span class="sxs-lookup"><span data-stu-id="04bb1-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="04bb1-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="04bb1-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="04bb1-118">**值**</span><span class="sxs-lookup"><span data-stu-id="04bb1-118">**Value**</span></span>|<span data-ttu-id="04bb1-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="04bb1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04bb1-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="04bb1-120">**Success**</span></span> <br/> |<span data-ttu-id="04bb1-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="04bb1-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="04bb1-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="04bb1-122">**Warning**</span></span> <br/> | <span data-ttu-id="04bb1-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="04bb1-123">Describes a request that was not processed.</span></span> <span data-ttu-id="04bb1-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="04bb1-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="04bb1-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="04bb1-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="04bb1-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="04bb1-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="04bb1-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="04bb1-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="04bb1-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="04bb1-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="04bb1-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="04bb1-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="04bb1-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="04bb1-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="04bb1-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="04bb1-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="04bb1-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="04bb1-132">**Error**</span></span> <br/> | <span data-ttu-id="04bb1-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="04bb1-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="04bb1-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="04bb1-134">The following are examples of sources of errors:</span></span>  <br/> <br/><span data-ttu-id="04bb1-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="04bb1-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="04bb1-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="04bb1-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="04bb1-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="04bb1-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="04bb1-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="04bb1-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="04bb1-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="04bb1-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="04bb1-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="04bb1-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="04bb1-142">子元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-142">Child elements</span></span>

|<span data-ttu-id="04bb1-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="04bb1-143">**Element**</span></span>|<span data-ttu-id="04bb1-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="04bb1-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04bb1-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="04bb1-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="04bb1-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="04bb1-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="04bb1-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="04bb1-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="04bb1-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="04bb1-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="04bb1-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="04bb1-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="04bb1-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="04bb1-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="04bb1-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="04bb1-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="04bb1-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="04bb1-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="04bb1-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="04bb1-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04bb1-154">父元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-154">Parent elements</span></span>

|<span data-ttu-id="04bb1-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="04bb1-155">**Element**</span></span>|<span data-ttu-id="04bb1-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="04bb1-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04bb1-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="04bb1-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="04bb1-158">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="04bb1-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04bb1-159">注解</span><span class="sxs-lookup"><span data-stu-id="04bb1-159">Remarks</span></span>

<span data-ttu-id="04bb1-160">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="04bb1-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04bb1-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="04bb1-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04bb1-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="04bb1-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="04bb1-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="04bb1-163">Schema Name</span></span>  <br/> |<span data-ttu-id="04bb1-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="04bb1-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="04bb1-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="04bb1-165">Validation File</span></span>  <br/> |<span data-ttu-id="04bb1-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="04bb1-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04bb1-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="04bb1-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="04bb1-168">False</span><span class="sxs-lookup"><span data-stu-id="04bb1-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04bb1-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04bb1-169">See also</span></span>

- [<span data-ttu-id="04bb1-170">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="04bb1-170">SendItem operation</span></span>](senditem-operation.md)
- [<span data-ttu-id="04bb1-171">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="04bb1-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

