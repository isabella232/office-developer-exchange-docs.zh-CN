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
description: DeleteAttachmentResponseMessage 元素包含单个 DeleteAttachment 操作请求的状态和结果。
ms.openlocfilehash: 3ff253a5c2b6cbd69b7b976f7f41ca8b83814a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464257"
---
# <a name="deleteattachmentresponsemessage"></a><span data-ttu-id="57bab-103">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="57bab-103">DeleteAttachmentResponseMessage</span></span>

<span data-ttu-id="57bab-104">**DeleteAttachmentResponseMessage**元素包含单个[DeleteAttachment 操作](deleteattachment-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="57bab-104">The **DeleteAttachmentResponseMessage** element contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="57bab-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="57bab-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)  
- [<span data-ttu-id="57bab-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="57bab-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="57bab-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="57bab-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

<span data-ttu-id="57bab-108">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="57bab-108">**DeleteAttachmentResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="57bab-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="57bab-109">Attributes and elements</span></span>

<span data-ttu-id="57bab-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57bab-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57bab-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="57bab-111">Attributes</span></span>

|<span data-ttu-id="57bab-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="57bab-112">**Attribute**</span></span>|<span data-ttu-id="57bab-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="57bab-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57bab-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="57bab-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="57bab-115">描述[DeleteAttachment 操作](deleteattachment-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="57bab-115">Describes the status of a [DeleteAttachment operation](deleteattachment-operation.md) response.</span></span><br/><br/><span data-ttu-id="57bab-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="57bab-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="57bab-117">-成功</span><span class="sxs-lookup"><span data-stu-id="57bab-117">-  Success</span></span>  <br/><span data-ttu-id="57bab-118">-警告</span><span class="sxs-lookup"><span data-stu-id="57bab-118">-  Warning</span></span>  <br/><span data-ttu-id="57bab-119">-错误</span><span class="sxs-lookup"><span data-stu-id="57bab-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="57bab-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="57bab-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="57bab-121">**值**</span><span class="sxs-lookup"><span data-stu-id="57bab-121">**Value**</span></span>|<span data-ttu-id="57bab-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="57bab-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57bab-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="57bab-123">**Success**</span></span> <br/> |<span data-ttu-id="57bab-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="57bab-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="57bab-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="57bab-125">**Warning**</span></span> <br/> | <span data-ttu-id="57bab-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="57bab-126">Describes a request that was not processed.</span></span> <span data-ttu-id="57bab-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="57bab-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="57bab-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="57bab-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="57bab-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="57bab-129">- The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="57bab-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="57bab-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="57bab-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="57bab-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="57bab-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="57bab-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="57bab-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="57bab-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="57bab-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="57bab-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="57bab-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="57bab-135">**Error**</span></span> <br/> | <span data-ttu-id="57bab-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="57bab-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="57bab-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="57bab-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="57bab-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="57bab-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="57bab-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="57bab-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="57bab-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="57bab-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="57bab-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="57bab-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="57bab-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="57bab-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="57bab-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="57bab-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="57bab-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="57bab-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="57bab-145">子元素</span><span class="sxs-lookup"><span data-stu-id="57bab-145">Child elements</span></span>

|<span data-ttu-id="57bab-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="57bab-146">**Element**</span></span>|<span data-ttu-id="57bab-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="57bab-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57bab-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="57bab-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="57bab-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="57bab-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="57bab-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="57bab-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="57bab-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="57bab-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="57bab-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="57bab-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="57bab-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="57bab-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="57bab-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="57bab-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="57bab-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="57bab-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="57bab-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="57bab-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="57bab-157">RootItemId</span><span class="sxs-lookup"><span data-stu-id="57bab-157">RootItemId</span></span>](rootitemid.md) <br/> |<span data-ttu-id="57bab-158">标识已删除附件的父项目。</span><span class="sxs-lookup"><span data-stu-id="57bab-158">Identifies the parent item of a deleted attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57bab-159">父元素</span><span class="sxs-lookup"><span data-stu-id="57bab-159">Parent elements</span></span>

|<span data-ttu-id="57bab-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="57bab-160">**Element**</span></span>|<span data-ttu-id="57bab-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="57bab-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57bab-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="57bab-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="57bab-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="57bab-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57bab-164">备注</span><span class="sxs-lookup"><span data-stu-id="57bab-164">Remarks</span></span>

<span data-ttu-id="57bab-165">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="57bab-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57bab-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="57bab-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57bab-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="57bab-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57bab-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="57bab-168">Schema Name</span></span>  <br/> |<span data-ttu-id="57bab-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="57bab-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="57bab-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="57bab-170">Validation File</span></span>  <br/> |<span data-ttu-id="57bab-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="57bab-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57bab-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="57bab-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="57bab-173">False</span><span class="sxs-lookup"><span data-stu-id="57bab-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57bab-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57bab-174">See also</span></span>

- [<span data-ttu-id="57bab-175">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="57bab-175">DeleteAttachment</span></span>](deleteattachment.md) 
- [<span data-ttu-id="57bab-176">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="57bab-176">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="57bab-177">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="57bab-177">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="57bab-178">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="57bab-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

