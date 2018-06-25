---
title: CreateAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponseMessage
api_type:
- schema
ms.assetid: b326e616-3ce0-4dcb-ba75-4ce4b9867211
description: CreateAttachmentResponseMessage 元素包含状态和单个 CreateAttachment 操作请求的结果。
ms.openlocfilehash: a6d3adde07dedb7a2533d6e9c7fc6ff0497792bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753634"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="c602f-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c602f-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="c602f-104">**CreateAttachmentResponseMessage**元素包含状态和的单个结果[CreateAttachment 操作](createattachment-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="c602f-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="c602f-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="c602f-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="c602f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c602f-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="c602f-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c602f-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="c602f-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c602f-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c602f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c602f-109">Attributes and elements</span></span>

<span data-ttu-id="c602f-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c602f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c602f-111">属性</span><span class="sxs-lookup"><span data-stu-id="c602f-111">Attributes</span></span>

|<span data-ttu-id="c602f-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="c602f-112">**Attribute**</span></span>|<span data-ttu-id="c602f-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="c602f-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c602f-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c602f-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c602f-115">描述[CreateAttachment 操作](createattachment-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c602f-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="c602f-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="c602f-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="c602f-117">-成功</span><span class="sxs-lookup"><span data-stu-id="c602f-117">-  Success</span></span>  <br/><span data-ttu-id="c602f-118">-警告</span><span class="sxs-lookup"><span data-stu-id="c602f-118">-  Warning</span></span>  <br/><span data-ttu-id="c602f-119">-错误</span><span class="sxs-lookup"><span data-stu-id="c602f-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c602f-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="c602f-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="c602f-121">**值**</span><span class="sxs-lookup"><span data-stu-id="c602f-121">**Value**</span></span>|<span data-ttu-id="c602f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="c602f-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c602f-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="c602f-123">**Success**</span></span> <br/> |<span data-ttu-id="c602f-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c602f-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c602f-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="c602f-125">**Warning**</span></span> <br/> | <span data-ttu-id="c602f-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c602f-126">Describes a request that was not processed.</span></span> <span data-ttu-id="c602f-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="c602f-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="c602f-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="c602f-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="c602f-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c602f-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c602f-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c602f-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c602f-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="c602f-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="c602f-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c602f-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c602f-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="c602f-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="c602f-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="c602f-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="c602f-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="c602f-135">**Error**</span></span> <br/> | <span data-ttu-id="c602f-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="c602f-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="c602f-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="c602f-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c602f-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="c602f-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c602f-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="c602f-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="c602f-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c602f-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="c602f-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="c602f-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="c602f-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="c602f-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c602f-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="c602f-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="c602f-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="c602f-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c602f-145">子元素</span><span class="sxs-lookup"><span data-stu-id="c602f-145">Child elements</span></span>

|<span data-ttu-id="c602f-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="c602f-146">**Element**</span></span>|<span data-ttu-id="c602f-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="c602f-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c602f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="c602f-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c602f-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c602f-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c602f-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c602f-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c602f-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c602f-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c602f-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c602f-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c602f-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c602f-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c602f-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="c602f-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c602f-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c602f-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c602f-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c602f-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c602f-157">附件</span><span class="sxs-lookup"><span data-stu-id="c602f-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c602f-158">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="c602f-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c602f-159">父元素</span><span class="sxs-lookup"><span data-stu-id="c602f-159">Parent elements</span></span>

|<span data-ttu-id="c602f-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="c602f-160">**Element**</span></span>|<span data-ttu-id="c602f-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="c602f-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c602f-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c602f-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c602f-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c602f-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c602f-164">注解</span><span class="sxs-lookup"><span data-stu-id="c602f-164">Remarks</span></span>

<span data-ttu-id="c602f-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c602f-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c602f-166">如果多个附件往返附加到在单个项，最后一个响应消息中的**RootItemChangeKey**属性是项的表示具有附件的新更改键。</span><span class="sxs-lookup"><span data-stu-id="c602f-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c602f-167">元素信息</span><span class="sxs-lookup"><span data-stu-id="c602f-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c602f-168">命名空间</span><span class="sxs-lookup"><span data-stu-id="c602f-168">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c602f-169">架构名称</span><span class="sxs-lookup"><span data-stu-id="c602f-169">Schema Name</span></span>  <br/> |<span data-ttu-id="c602f-170">消息架构</span><span class="sxs-lookup"><span data-stu-id="c602f-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c602f-171">验证文件</span><span class="sxs-lookup"><span data-stu-id="c602f-171">Validation File</span></span>  <br/> |<span data-ttu-id="c602f-172">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c602f-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c602f-173">可以为空</span><span class="sxs-lookup"><span data-stu-id="c602f-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="c602f-174">False</span><span class="sxs-lookup"><span data-stu-id="c602f-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c602f-175">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c602f-175">See also</span></span>

- [<span data-ttu-id="c602f-176">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="c602f-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="c602f-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="c602f-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="c602f-178">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="c602f-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="c602f-179">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c602f-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

