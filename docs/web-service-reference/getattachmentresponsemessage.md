---
title: GetAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachmentResponseMessage
api_type:
- schema
ms.assetid: f0a841af-422d-4c82-b710-41e2038dbee4
description: GetAttachmentResponseMessage 元素包含单个 GetAttachment 操作请求的状态和结果。
ms.openlocfilehash: cfe36364431a8fe81c3f62e68356b634f00bee78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457793"
---
# <a name="getattachmentresponsemessage"></a><span data-ttu-id="bf2e7-103">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf2e7-103">GetAttachmentResponseMessage</span></span>

<span data-ttu-id="bf2e7-104">**GetAttachmentResponseMessage**元素包含单个[GetAttachment 操作](getattachment-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-104">The **GetAttachmentResponseMessage** element contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="bf2e7-105">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="bf2e7-105">GetAttachmentResponse</span></span>](getattachmentresponse.md) 
- [<span data-ttu-id="bf2e7-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf2e7-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="bf2e7-107">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf2e7-107">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 <span data-ttu-id="bf2e7-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-108">**AttachmentInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf2e7-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bf2e7-109">Attributes and elements</span></span>

<span data-ttu-id="bf2e7-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf2e7-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="bf2e7-111">Attributes</span></span>

|<span data-ttu-id="bf2e7-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-112">**Attribute**</span></span>|<span data-ttu-id="bf2e7-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf2e7-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bf2e7-115">描述[GetAttachment 操作](getattachment-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-115">Describes the status of a [GetAttachment operation](getattachment-operation.md) response.</span></span><br/><br/> <span data-ttu-id="bf2e7-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="bf2e7-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="bf2e7-117">-成功</span><span class="sxs-lookup"><span data-stu-id="bf2e7-117">-  Success</span></span>  <br/><span data-ttu-id="bf2e7-118">-警告</span><span class="sxs-lookup"><span data-stu-id="bf2e7-118">-  Warning</span></span>  <br/><span data-ttu-id="bf2e7-119">-错误</span><span class="sxs-lookup"><span data-stu-id="bf2e7-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="bf2e7-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="bf2e7-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="bf2e7-121">**值**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-121">**Value**</span></span>|<span data-ttu-id="bf2e7-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf2e7-123">成功</span><span class="sxs-lookup"><span data-stu-id="bf2e7-123">Success</span></span>  <br/> |<span data-ttu-id="bf2e7-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bf2e7-125">警告</span><span class="sxs-lookup"><span data-stu-id="bf2e7-125">Warning</span></span>  <br/> | <span data-ttu-id="bf2e7-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-126">Describes a request that was not processed.</span></span> <span data-ttu-id="bf2e7-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="bf2e7-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="bf2e7-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="bf2e7-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="bf2e7-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="bf2e7-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="bf2e7-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="bf2e7-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="bf2e7-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="bf2e7-135">错误</span><span class="sxs-lookup"><span data-stu-id="bf2e7-135">Error</span></span>  <br/> | <span data-ttu-id="bf2e7-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="bf2e7-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="bf2e7-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bf2e7-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="bf2e7-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bf2e7-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="bf2e7-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="bf2e7-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="bf2e7-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="bf2e7-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="bf2e7-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="bf2e7-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="bf2e7-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bf2e7-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="bf2e7-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="bf2e7-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bf2e7-145">子元素</span><span class="sxs-lookup"><span data-stu-id="bf2e7-145">Child elements</span></span>

|<span data-ttu-id="bf2e7-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-146">**Element**</span></span>|<span data-ttu-id="bf2e7-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf2e7-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="bf2e7-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bf2e7-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bf2e7-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bf2e7-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bf2e7-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="bf2e7-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bf2e7-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bf2e7-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="bf2e7-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bf2e7-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bf2e7-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bf2e7-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bf2e7-157">附件</span><span class="sxs-lookup"><span data-stu-id="bf2e7-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bf2e7-158">包含 ttached 到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-158">Contains the items or files that are ttached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf2e7-159">父元素</span><span class="sxs-lookup"><span data-stu-id="bf2e7-159">Parent elements</span></span>

|<span data-ttu-id="bf2e7-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-160">**Element**</span></span>|<span data-ttu-id="bf2e7-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="bf2e7-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf2e7-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf2e7-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="bf2e7-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf2e7-164">备注</span><span class="sxs-lookup"><span data-stu-id="bf2e7-164">Remarks</span></span>

<span data-ttu-id="bf2e7-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bf2e7-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf2e7-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="bf2e7-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf2e7-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="bf2e7-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bf2e7-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="bf2e7-168">Schema Name</span></span>  <br/> |<span data-ttu-id="bf2e7-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="bf2e7-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bf2e7-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="bf2e7-170">Validation File</span></span>  <br/> |<span data-ttu-id="bf2e7-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bf2e7-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bf2e7-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="bf2e7-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf2e7-173">False</span><span class="sxs-lookup"><span data-stu-id="bf2e7-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf2e7-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf2e7-174">See also</span></span>

- [<span data-ttu-id="bf2e7-175">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="bf2e7-175">GetAttachment</span></span>](getattachment.md) 
- [<span data-ttu-id="bf2e7-176">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="bf2e7-176">GetAttachment operation</span></span>](getattachment-operation.md)

