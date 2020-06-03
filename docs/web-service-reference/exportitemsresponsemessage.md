---
title: ExportItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItemsResponseMessage
api_type:
- schema
ms.assetid: 830fb008-3c45-4988-9041-91a3da3fe689
description: ExportItemsResponseMessage 元素包含导出单个邮箱项目的请求的状态和结果。
ms.openlocfilehash: 3265836ce6d9d6ef97a4e598bbb3f50e7c5047c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468944"
---
# <a name="exportitemsresponsemessage"></a><span data-ttu-id="d9372-103">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9372-103">ExportItemsResponseMessage</span></span>

<span data-ttu-id="d9372-104">**ExportItemsResponseMessage**元素包含导出单个邮箱项目的请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="d9372-104">The **ExportItemsResponseMessage** element contains the status and results of a request to export a single mailbox item.</span></span> 
  
- [<span data-ttu-id="d9372-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="d9372-105">ExportItemsResponse</span></span>](exportitemsresponse.md)  
- [<span data-ttu-id="d9372-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d9372-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="d9372-107">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9372-107">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
  
```XML
<ExportItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
   <Data/>
</ExportItemsResponseMessage>
```

<span data-ttu-id="d9372-108">**ExportItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d9372-108">**ExportItemsResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d9372-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9372-109">Attributes and elements</span></span>

<span data-ttu-id="d9372-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9372-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9372-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="d9372-111">Attributes</span></span>

|<span data-ttu-id="d9372-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="d9372-112">**Attribute**</span></span>|<span data-ttu-id="d9372-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9372-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9372-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d9372-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d9372-115">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="d9372-115">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="d9372-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="d9372-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="d9372-117">-成功</span><span class="sxs-lookup"><span data-stu-id="d9372-117">-  Success</span></span>  <br/><span data-ttu-id="d9372-118">-警告</span><span class="sxs-lookup"><span data-stu-id="d9372-118">-  Warning</span></span>  <br/><span data-ttu-id="d9372-119">-错误</span><span class="sxs-lookup"><span data-stu-id="d9372-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d9372-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="d9372-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="d9372-121">**值**</span><span class="sxs-lookup"><span data-stu-id="d9372-121">**Value**</span></span>|<span data-ttu-id="d9372-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9372-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9372-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="d9372-123">**Success**</span></span> <br/> |<span data-ttu-id="d9372-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="d9372-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d9372-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="d9372-125">**Warning**</span></span> <br/> | <span data-ttu-id="d9372-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="d9372-126">Describes a request that was not processed.</span></span> <span data-ttu-id="d9372-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="d9372-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="d9372-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="d9372-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="d9372-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="d9372-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d9372-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="d9372-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d9372-131">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="d9372-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="d9372-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="d9372-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d9372-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="d9372-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="d9372-134">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="d9372-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="d9372-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="d9372-135">**Error**</span></span> <br/> | <span data-ttu-id="d9372-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="d9372-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d9372-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="d9372-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d9372-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="d9372-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d9372-139">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="d9372-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d9372-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="d9372-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="d9372-141">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="d9372-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d9372-142">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="d9372-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d9372-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="d9372-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d9372-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="d9372-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d9372-145">子元素</span><span class="sxs-lookup"><span data-stu-id="d9372-145">Child elements</span></span>

|<span data-ttu-id="d9372-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9372-146">**Element**</span></span>|<span data-ttu-id="d9372-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="d9372-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9372-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="d9372-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d9372-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="d9372-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d9372-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d9372-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d9372-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="d9372-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d9372-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d9372-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d9372-153">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="d9372-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="d9372-154">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="d9372-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d9372-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d9372-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d9372-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="d9372-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d9372-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="d9372-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d9372-158">包含导出项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="d9372-158">Contains the item identifier of an exported item.</span></span>  <br/> |
|[<span data-ttu-id="d9372-159">Data （base64Binary）</span><span class="sxs-lookup"><span data-stu-id="d9372-159">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="d9372-160">包含导出项目的内容。</span><span class="sxs-lookup"><span data-stu-id="d9372-160">Contains the contents of an exported item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9372-161">父元素</span><span class="sxs-lookup"><span data-stu-id="d9372-161">Parent elements</span></span>

|<span data-ttu-id="d9372-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9372-162">**Element**</span></span>|<span data-ttu-id="d9372-163">**描述**</span><span class="sxs-lookup"><span data-stu-id="d9372-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9372-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d9372-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d9372-165">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="d9372-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9372-166">文本值</span><span class="sxs-lookup"><span data-stu-id="d9372-166">Text value</span></span>

<span data-ttu-id="d9372-167">无。</span><span class="sxs-lookup"><span data-stu-id="d9372-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9372-168">说明</span><span class="sxs-lookup"><span data-stu-id="d9372-168">Remarks</span></span>

<span data-ttu-id="d9372-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d9372-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9372-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9372-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9372-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9372-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9372-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9372-172">Schema Name</span></span>  <br/> |<span data-ttu-id="d9372-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="d9372-173">Message schema</span></span>  <br/> |
|<span data-ttu-id="d9372-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9372-174">Validation File</span></span>  <br/> |<span data-ttu-id="d9372-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9372-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9372-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9372-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9372-177">False</span><span class="sxs-lookup"><span data-stu-id="d9372-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9372-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9372-178">See also</span></span>

- [<span data-ttu-id="d9372-179">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="d9372-179">ExportItems operation</span></span>](exportitems-operation.md) 
- [<span data-ttu-id="d9372-180">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="d9372-180">UploadItems operation</span></span>](uploaditems-operation.md)

