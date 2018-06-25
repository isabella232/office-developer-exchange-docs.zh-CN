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
description: UploadItemsResponseMessage 元素包含状态和请求上载单个邮箱项目的结果。
ms.openlocfilehash: 9a1a33011aa1e240ab7e15794e2e89401238ffda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838446"
---
# <a name="uploaditemsresponsemessage"></a><span data-ttu-id="42fdf-103">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="42fdf-103">UploadItemsResponseMessage</span></span>

<span data-ttu-id="42fdf-104">**UploadItemsResponseMessage**元素包含状态和请求上载单个邮箱项目的结果。</span><span class="sxs-lookup"><span data-stu-id="42fdf-104">The **UploadItemsResponseMessage** element contains the status and results of a request to upload a single mailbox item.</span></span> 
  
- [<span data-ttu-id="42fdf-105">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="42fdf-105">UploadItemsResponse</span></span>](uploaditemsresponse.md) 
- [<span data-ttu-id="42fdf-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="42fdf-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="42fdf-107">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="42fdf-107">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 <span data-ttu-id="42fdf-108">**UploadItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="42fdf-108">**UploadItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42fdf-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-109">Attributes and elements</span></span>

<span data-ttu-id="42fdf-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="42fdf-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42fdf-111">属性</span><span class="sxs-lookup"><span data-stu-id="42fdf-111">Attributes</span></span>

|<span data-ttu-id="42fdf-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="42fdf-112">**Attribute**</span></span>|<span data-ttu-id="42fdf-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fdf-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42fdf-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="42fdf-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="42fdf-115">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="42fdf-115">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="42fdf-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="42fdf-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="42fdf-117">-成功</span><span class="sxs-lookup"><span data-stu-id="42fdf-117">-  Success</span></span>  <br/><span data-ttu-id="42fdf-118">-警告</span><span class="sxs-lookup"><span data-stu-id="42fdf-118">-  Warning</span></span>  <br/><span data-ttu-id="42fdf-119">-错误</span><span class="sxs-lookup"><span data-stu-id="42fdf-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="42fdf-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="42fdf-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="42fdf-121">**值**</span><span class="sxs-lookup"><span data-stu-id="42fdf-121">**Value**</span></span>|<span data-ttu-id="42fdf-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fdf-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42fdf-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="42fdf-123">**Success**</span></span> <br/> |<span data-ttu-id="42fdf-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="42fdf-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="42fdf-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="42fdf-125">**Warning**</span></span> <br/> | <span data-ttu-id="42fdf-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="42fdf-126">Describes a request that was not processed.</span></span> <span data-ttu-id="42fdf-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="42fdf-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="42fdf-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="42fdf-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="42fdf-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="42fdf-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="42fdf-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="42fdf-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="42fdf-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="42fdf-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="42fdf-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="42fdf-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="42fdf-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="42fdf-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="42fdf-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="42fdf-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="42fdf-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="42fdf-135">**Error**</span></span> <br/> | <span data-ttu-id="42fdf-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="42fdf-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="42fdf-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="42fdf-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="42fdf-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="42fdf-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="42fdf-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="42fdf-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="42fdf-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="42fdf-142">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="42fdf-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="42fdf-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="42fdf-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="42fdf-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="42fdf-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="42fdf-145">子元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-145">Child elements</span></span>

|<span data-ttu-id="42fdf-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="42fdf-146">**Element**</span></span>|<span data-ttu-id="42fdf-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fdf-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42fdf-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="42fdf-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="42fdf-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="42fdf-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="42fdf-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="42fdf-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="42fdf-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="42fdf-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="42fdf-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="42fdf-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="42fdf-153">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="42fdf-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="42fdf-154">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="42fdf-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="42fdf-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="42fdf-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="42fdf-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="42fdf-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="42fdf-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="42fdf-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="42fdf-158">包含已上载的项目的项标识符。</span><span class="sxs-lookup"><span data-stu-id="42fdf-158">Contains the item identifier of an uploaded item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42fdf-159">父元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-159">Parent elements</span></span>

|<span data-ttu-id="42fdf-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="42fdf-160">**Element**</span></span>|<span data-ttu-id="42fdf-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fdf-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42fdf-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="42fdf-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="42fdf-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="42fdf-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="42fdf-164">文本值</span><span class="sxs-lookup"><span data-stu-id="42fdf-164">Text value</span></span>

<span data-ttu-id="42fdf-165">无。</span><span class="sxs-lookup"><span data-stu-id="42fdf-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42fdf-166">备注</span><span class="sxs-lookup"><span data-stu-id="42fdf-166">Remarks</span></span>

<span data-ttu-id="42fdf-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="42fdf-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42fdf-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="42fdf-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42fdf-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="42fdf-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42fdf-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="42fdf-170">Schema Name</span></span>  <br/> |<span data-ttu-id="42fdf-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="42fdf-171">Message schema</span></span>  <br/> |
|<span data-ttu-id="42fdf-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="42fdf-172">Validation File</span></span>  <br/> |<span data-ttu-id="42fdf-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="42fdf-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42fdf-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="42fdf-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="42fdf-175">False</span><span class="sxs-lookup"><span data-stu-id="42fdf-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42fdf-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42fdf-176">See also</span></span>

- [<span data-ttu-id="42fdf-177">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="42fdf-177">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="42fdf-178">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="42fdf-178">UploadItems operation</span></span>](uploaditems-operation.md)
- [<span data-ttu-id="42fdf-179">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="42fdf-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

