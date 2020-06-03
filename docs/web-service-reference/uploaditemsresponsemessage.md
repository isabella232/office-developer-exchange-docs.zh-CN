---
title: UploadItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: UploadItemsResponseMessage 元素包含上载单个邮箱项目的请求的状态和结果。
ms.openlocfilehash: 4049772c560f3d54a31351fe1fbed77fe5780bf8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468493"
---
# <a name="uploaditemsresponsemessage"></a><span data-ttu-id="66be9-103">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66be9-103">UploadItemsResponseMessage</span></span>

<span data-ttu-id="66be9-104">**UploadItemsResponseMessage**元素包含上载单个邮箱项目的请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="66be9-104">The **UploadItemsResponseMessage** element contains the status and results of a request to upload a single mailbox item.</span></span> 
  
- [<span data-ttu-id="66be9-105">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="66be9-105">UploadItemsResponse</span></span>](uploaditemsresponse.md) 
- [<span data-ttu-id="66be9-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="66be9-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="66be9-107">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66be9-107">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 <span data-ttu-id="66be9-108">**UploadItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="66be9-108">**UploadItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66be9-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="66be9-109">Attributes and elements</span></span>

<span data-ttu-id="66be9-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="66be9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66be9-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="66be9-111">Attributes</span></span>

|<span data-ttu-id="66be9-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="66be9-112">**Attribute**</span></span>|<span data-ttu-id="66be9-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="66be9-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66be9-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="66be9-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="66be9-115">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="66be9-115">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="66be9-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="66be9-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="66be9-117">-成功</span><span class="sxs-lookup"><span data-stu-id="66be9-117">-  Success</span></span>  <br/><span data-ttu-id="66be9-118">-警告</span><span class="sxs-lookup"><span data-stu-id="66be9-118">-  Warning</span></span>  <br/><span data-ttu-id="66be9-119">-错误</span><span class="sxs-lookup"><span data-stu-id="66be9-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="66be9-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="66be9-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="66be9-121">**值**</span><span class="sxs-lookup"><span data-stu-id="66be9-121">**Value**</span></span>|<span data-ttu-id="66be9-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="66be9-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66be9-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="66be9-123">**Success**</span></span> <br/> |<span data-ttu-id="66be9-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="66be9-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="66be9-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="66be9-125">**Warning**</span></span> <br/> | <span data-ttu-id="66be9-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="66be9-126">Describes a request that was not processed.</span></span> <span data-ttu-id="66be9-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="66be9-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="66be9-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="66be9-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="66be9-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66be9-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="66be9-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66be9-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="66be9-131">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="66be9-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="66be9-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="66be9-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="66be9-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="66be9-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="66be9-134">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="66be9-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="66be9-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="66be9-135">**Error**</span></span> <br/> | <span data-ttu-id="66be9-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="66be9-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="66be9-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="66be9-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="66be9-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="66be9-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="66be9-139">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="66be9-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="66be9-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="66be9-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="66be9-141">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="66be9-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="66be9-142">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="66be9-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="66be9-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="66be9-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="66be9-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="66be9-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66be9-145">子元素</span><span class="sxs-lookup"><span data-stu-id="66be9-145">Child elements</span></span>

|<span data-ttu-id="66be9-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="66be9-146">**Element**</span></span>|<span data-ttu-id="66be9-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="66be9-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66be9-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="66be9-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="66be9-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="66be9-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="66be9-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="66be9-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="66be9-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="66be9-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="66be9-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="66be9-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="66be9-153">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="66be9-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="66be9-154">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="66be9-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="66be9-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="66be9-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="66be9-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="66be9-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="66be9-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="66be9-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="66be9-158">包含已上载项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="66be9-158">Contains the item identifier of an uploaded item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66be9-159">父元素</span><span class="sxs-lookup"><span data-stu-id="66be9-159">Parent elements</span></span>

|<span data-ttu-id="66be9-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="66be9-160">**Element**</span></span>|<span data-ttu-id="66be9-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="66be9-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66be9-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="66be9-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="66be9-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="66be9-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66be9-164">文本值</span><span class="sxs-lookup"><span data-stu-id="66be9-164">Text value</span></span>

<span data-ttu-id="66be9-165">无。</span><span class="sxs-lookup"><span data-stu-id="66be9-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66be9-166">说明</span><span class="sxs-lookup"><span data-stu-id="66be9-166">Remarks</span></span>

<span data-ttu-id="66be9-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="66be9-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66be9-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="66be9-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66be9-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="66be9-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66be9-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="66be9-170">Schema Name</span></span>  <br/> |<span data-ttu-id="66be9-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="66be9-171">Message schema</span></span>  <br/> |
|<span data-ttu-id="66be9-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="66be9-172">Validation File</span></span>  <br/> |<span data-ttu-id="66be9-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="66be9-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66be9-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="66be9-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="66be9-175">False</span><span class="sxs-lookup"><span data-stu-id="66be9-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66be9-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66be9-176">See also</span></span>

- [<span data-ttu-id="66be9-177">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="66be9-177">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="66be9-178">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="66be9-178">UploadItems operation</span></span>](uploaditems-operation.md)
- [<span data-ttu-id="66be9-179">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="66be9-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

