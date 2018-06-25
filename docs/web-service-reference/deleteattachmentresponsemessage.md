---
title: DeleteAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponseMessage
api_type:
- schema
ms.assetid: 1edb085f-1674-48e5-8ec3-42351adeac7d
description: DeleteAttachmentResponseMessage 元素包含状态和单个 DeleteAttachment 操作请求的结果。
ms.openlocfilehash: 387e998a393c23f416cc5ad8d6c4a7ad4c92ebc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753797"
---
# <a name="deleteattachmentresponsemessage"></a><span data-ttu-id="8df6c-103">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8df6c-103">DeleteAttachmentResponseMessage</span></span>

<span data-ttu-id="8df6c-104">**DeleteAttachmentResponseMessage**元素包含状态和的单个结果[DeleteAttachment 操作](deleteattachment-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="8df6c-104">The **DeleteAttachmentResponseMessage** element contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8df6c-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="8df6c-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)  
- [<span data-ttu-id="8df6c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8df6c-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="8df6c-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8df6c-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

<span data-ttu-id="8df6c-108">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8df6c-108">**DeleteAttachmentResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8df6c-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-109">Attributes and elements</span></span>

<span data-ttu-id="8df6c-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8df6c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8df6c-111">属性</span><span class="sxs-lookup"><span data-stu-id="8df6c-111">Attributes</span></span>

|<span data-ttu-id="8df6c-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="8df6c-112">**Attribute**</span></span>|<span data-ttu-id="8df6c-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="8df6c-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8df6c-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8df6c-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8df6c-115">描述[DeleteAttachment 操作](deleteattachment-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="8df6c-115">Describes the status of a [DeleteAttachment operation](deleteattachment-operation.md) response.</span></span><br/><br/><span data-ttu-id="8df6c-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="8df6c-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="8df6c-117">-成功</span><span class="sxs-lookup"><span data-stu-id="8df6c-117">-  Success</span></span>  <br/><span data-ttu-id="8df6c-118">-警告</span><span class="sxs-lookup"><span data-stu-id="8df6c-118">-  Warning</span></span>  <br/><span data-ttu-id="8df6c-119">-错误</span><span class="sxs-lookup"><span data-stu-id="8df6c-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8df6c-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="8df6c-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="8df6c-121">**值**</span><span class="sxs-lookup"><span data-stu-id="8df6c-121">**Value**</span></span>|<span data-ttu-id="8df6c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="8df6c-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8df6c-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="8df6c-123">**Success**</span></span> <br/> |<span data-ttu-id="8df6c-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="8df6c-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8df6c-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8df6c-125">**Warning**</span></span> <br/> | <span data-ttu-id="8df6c-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="8df6c-126">Describes a request that was not processed.</span></span> <span data-ttu-id="8df6c-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="8df6c-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8df6c-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="8df6c-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8df6c-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8df6c-129">- The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8df6c-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8df6c-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8df6c-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="8df6c-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8df6c-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="8df6c-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8df6c-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="8df6c-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="8df6c-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="8df6c-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="8df6c-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="8df6c-135">**Error**</span></span> <br/> | <span data-ttu-id="8df6c-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="8df6c-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="8df6c-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="8df6c-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="8df6c-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8df6c-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8df6c-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="8df6c-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="8df6c-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="8df6c-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="8df6c-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="8df6c-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8df6c-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="8df6c-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="8df6c-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="8df6c-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8df6c-145">子元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-145">Child elements</span></span>

|<span data-ttu-id="8df6c-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="8df6c-146">**Element**</span></span>|<span data-ttu-id="8df6c-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="8df6c-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8df6c-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="8df6c-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8df6c-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="8df6c-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8df6c-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8df6c-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8df6c-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="8df6c-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8df6c-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8df6c-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8df6c-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="8df6c-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8df6c-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="8df6c-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8df6c-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8df6c-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8df6c-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="8df6c-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8df6c-157">RootItemId</span><span class="sxs-lookup"><span data-stu-id="8df6c-157">RootItemId</span></span>](rootitemid.md) <br/> |<span data-ttu-id="8df6c-158">标识已删除附件的父项。</span><span class="sxs-lookup"><span data-stu-id="8df6c-158">Identifies the parent item of a deleted attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8df6c-159">父元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-159">Parent elements</span></span>

|<span data-ttu-id="8df6c-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="8df6c-160">**Element**</span></span>|<span data-ttu-id="8df6c-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="8df6c-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8df6c-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8df6c-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8df6c-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="8df6c-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8df6c-164">注解</span><span class="sxs-lookup"><span data-stu-id="8df6c-164">Remarks</span></span>

<span data-ttu-id="8df6c-165">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8df6c-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8df6c-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="8df6c-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8df6c-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="8df6c-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8df6c-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="8df6c-168">Schema Name</span></span>  <br/> |<span data-ttu-id="8df6c-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="8df6c-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8df6c-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="8df6c-170">Validation File</span></span>  <br/> |<span data-ttu-id="8df6c-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8df6c-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8df6c-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="8df6c-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="8df6c-173">False</span><span class="sxs-lookup"><span data-stu-id="8df6c-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8df6c-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8df6c-174">See also</span></span>

- [<span data-ttu-id="8df6c-175">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="8df6c-175">DeleteAttachment</span></span>](deleteattachment.md) 
- [<span data-ttu-id="8df6c-176">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8df6c-176">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="8df6c-177">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="8df6c-177">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="8df6c-178">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8df6c-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

