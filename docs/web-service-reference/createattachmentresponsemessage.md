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
description: CreateAttachmentResponseMessage 元素包含单个 CreateAttachment 操作请求的状态和结果。
ms.openlocfilehash: 14d8d1936b3cfd52bdb816343c86606cb8ccf76f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458920"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="fda34-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fda34-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="fda34-104">**CreateAttachmentResponseMessage**元素包含单个[CreateAttachment 操作](createattachment-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="fda34-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="fda34-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="fda34-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="fda34-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fda34-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="fda34-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fda34-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="fda34-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fda34-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fda34-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fda34-109">Attributes and elements</span></span>

<span data-ttu-id="fda34-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fda34-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fda34-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="fda34-111">Attributes</span></span>

|<span data-ttu-id="fda34-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="fda34-112">**Attribute**</span></span>|<span data-ttu-id="fda34-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="fda34-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fda34-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fda34-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fda34-115">描述[CreateAttachment 操作](createattachment-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="fda34-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="fda34-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="fda34-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="fda34-117">-成功</span><span class="sxs-lookup"><span data-stu-id="fda34-117">-  Success</span></span>  <br/><span data-ttu-id="fda34-118">-警告</span><span class="sxs-lookup"><span data-stu-id="fda34-118">-  Warning</span></span>  <br/><span data-ttu-id="fda34-119">-错误</span><span class="sxs-lookup"><span data-stu-id="fda34-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="fda34-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="fda34-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="fda34-121">**值**</span><span class="sxs-lookup"><span data-stu-id="fda34-121">**Value**</span></span>|<span data-ttu-id="fda34-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="fda34-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fda34-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="fda34-123">**Success**</span></span> <br/> |<span data-ttu-id="fda34-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="fda34-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fda34-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="fda34-125">**Warning**</span></span> <br/> | <span data-ttu-id="fda34-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="fda34-126">Describes a request that was not processed.</span></span> <span data-ttu-id="fda34-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="fda34-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="fda34-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="fda34-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="fda34-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fda34-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="fda34-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fda34-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="fda34-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="fda34-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="fda34-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fda34-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="fda34-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="fda34-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="fda34-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="fda34-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="fda34-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="fda34-135">**Error**</span></span> <br/> | <span data-ttu-id="fda34-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="fda34-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="fda34-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="fda34-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="fda34-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="fda34-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="fda34-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="fda34-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="fda34-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="fda34-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="fda34-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="fda34-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="fda34-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="fda34-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="fda34-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="fda34-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="fda34-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="fda34-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fda34-145">子元素</span><span class="sxs-lookup"><span data-stu-id="fda34-145">Child elements</span></span>

|<span data-ttu-id="fda34-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="fda34-146">**Element**</span></span>|<span data-ttu-id="fda34-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="fda34-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fda34-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="fda34-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fda34-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="fda34-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fda34-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fda34-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fda34-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="fda34-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="fda34-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fda34-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fda34-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="fda34-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="fda34-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="fda34-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fda34-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fda34-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fda34-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="fda34-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="fda34-157">附件</span><span class="sxs-lookup"><span data-stu-id="fda34-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fda34-158">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="fda34-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fda34-159">父元素</span><span class="sxs-lookup"><span data-stu-id="fda34-159">Parent elements</span></span>

|<span data-ttu-id="fda34-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="fda34-160">**Element**</span></span>|<span data-ttu-id="fda34-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="fda34-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fda34-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fda34-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fda34-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="fda34-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fda34-164">备注</span><span class="sxs-lookup"><span data-stu-id="fda34-164">Remarks</span></span>

<span data-ttu-id="fda34-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fda34-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fda34-166">如果在一次往返行程中，有多个附件附加到某个项目，则最后一条响应邮件中的**RootItemChangeKey**属性是表示包含附件的项目的新更改键的属性。</span><span class="sxs-lookup"><span data-stu-id="fda34-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fda34-167">元素信息</span><span class="sxs-lookup"><span data-stu-id="fda34-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fda34-168">命名空间</span><span class="sxs-lookup"><span data-stu-id="fda34-168">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fda34-169">架构名称</span><span class="sxs-lookup"><span data-stu-id="fda34-169">Schema Name</span></span>  <br/> |<span data-ttu-id="fda34-170">消息架构</span><span class="sxs-lookup"><span data-stu-id="fda34-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fda34-171">验证文件</span><span class="sxs-lookup"><span data-stu-id="fda34-171">Validation File</span></span>  <br/> |<span data-ttu-id="fda34-172">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fda34-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fda34-173">可以为空</span><span class="sxs-lookup"><span data-stu-id="fda34-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="fda34-174">False</span><span class="sxs-lookup"><span data-stu-id="fda34-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fda34-175">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fda34-175">See also</span></span>

- [<span data-ttu-id="fda34-176">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="fda34-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="fda34-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="fda34-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="fda34-178">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="fda34-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="fda34-179">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fda34-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

