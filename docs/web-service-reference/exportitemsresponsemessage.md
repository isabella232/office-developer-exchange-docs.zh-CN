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
description: ExportItemsResponseMessage 元素包含状态和请求导出的单个邮箱项目的结果。
ms.openlocfilehash: 99c2ca3f95efff6562ff95350b30fc79c5fb51e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754211"
---
# <a name="exportitemsresponsemessage"></a><span data-ttu-id="4b872-103">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4b872-103">ExportItemsResponseMessage</span></span>

<span data-ttu-id="4b872-104">**ExportItemsResponseMessage**元素包含状态和请求导出的单个邮箱项目的结果。</span><span class="sxs-lookup"><span data-stu-id="4b872-104">The **ExportItemsResponseMessage** element contains the status and results of a request to export a single mailbox item.</span></span> 
  
- [<span data-ttu-id="4b872-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="4b872-105">ExportItemsResponse</span></span>](exportitemsresponse.md)  
- [<span data-ttu-id="4b872-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4b872-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="4b872-107">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4b872-107">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
  
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

<span data-ttu-id="4b872-108">**ExportItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4b872-108">**ExportItemsResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4b872-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b872-109">Attributes and elements</span></span>

<span data-ttu-id="4b872-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b872-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b872-111">属性</span><span class="sxs-lookup"><span data-stu-id="4b872-111">Attributes</span></span>

|<span data-ttu-id="4b872-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="4b872-112">**Attribute**</span></span>|<span data-ttu-id="4b872-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b872-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b872-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4b872-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4b872-115">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="4b872-115">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="4b872-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="4b872-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="4b872-117">-成功</span><span class="sxs-lookup"><span data-stu-id="4b872-117">-  Success</span></span>  <br/><span data-ttu-id="4b872-118">-警告</span><span class="sxs-lookup"><span data-stu-id="4b872-118">-  Warning</span></span>  <br/><span data-ttu-id="4b872-119">-错误</span><span class="sxs-lookup"><span data-stu-id="4b872-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4b872-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="4b872-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="4b872-121">**值**</span><span class="sxs-lookup"><span data-stu-id="4b872-121">**Value**</span></span>|<span data-ttu-id="4b872-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b872-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b872-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="4b872-123">**Success**</span></span> <br/> |<span data-ttu-id="4b872-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="4b872-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4b872-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4b872-125">**Warning**</span></span> <br/> | <span data-ttu-id="4b872-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="4b872-126">Describes a request that was not processed.</span></span> <span data-ttu-id="4b872-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="4b872-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="4b872-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="4b872-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="4b872-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4b872-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4b872-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4b872-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4b872-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="4b872-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="4b872-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4b872-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4b872-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="4b872-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="4b872-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="4b872-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="4b872-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="4b872-135">**Error**</span></span> <br/> | <span data-ttu-id="4b872-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="4b872-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4b872-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="4b872-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="4b872-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="4b872-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="4b872-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="4b872-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="4b872-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="4b872-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="4b872-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="4b872-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="4b872-142">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="4b872-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4b872-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="4b872-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="4b872-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="4b872-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b872-145">子元素</span><span class="sxs-lookup"><span data-stu-id="4b872-145">Child elements</span></span>

|<span data-ttu-id="4b872-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b872-146">**Element**</span></span>|<span data-ttu-id="4b872-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b872-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b872-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="4b872-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4b872-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="4b872-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4b872-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4b872-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4b872-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="4b872-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4b872-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4b872-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4b872-153">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4b872-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="4b872-154">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="4b872-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4b872-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4b872-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4b872-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="4b872-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4b872-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="4b872-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4b872-158">包含导出的项目的项标识符。</span><span class="sxs-lookup"><span data-stu-id="4b872-158">Contains the item identifier of an exported item.</span></span>  <br/> |
|[<span data-ttu-id="4b872-159">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="4b872-159">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="4b872-160">包含导出项的内容。</span><span class="sxs-lookup"><span data-stu-id="4b872-160">Contains the contents of an exported item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b872-161">父元素</span><span class="sxs-lookup"><span data-stu-id="4b872-161">Parent elements</span></span>

|<span data-ttu-id="4b872-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b872-162">**Element**</span></span>|<span data-ttu-id="4b872-163">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b872-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b872-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4b872-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4b872-165">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="4b872-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b872-166">文本值</span><span class="sxs-lookup"><span data-stu-id="4b872-166">Text value</span></span>

<span data-ttu-id="4b872-167">无。</span><span class="sxs-lookup"><span data-stu-id="4b872-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b872-168">备注</span><span class="sxs-lookup"><span data-stu-id="4b872-168">Remarks</span></span>

<span data-ttu-id="4b872-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4b872-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b872-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="4b872-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b872-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="4b872-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4b872-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="4b872-172">Schema Name</span></span>  <br/> |<span data-ttu-id="4b872-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="4b872-173">Message schema</span></span>  <br/> |
|<span data-ttu-id="4b872-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="4b872-174">Validation File</span></span>  <br/> |<span data-ttu-id="4b872-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4b872-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4b872-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="4b872-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b872-177">False</span><span class="sxs-lookup"><span data-stu-id="4b872-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b872-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b872-178">See also</span></span>

- [<span data-ttu-id="4b872-179">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="4b872-179">ExportItems operation</span></span>](exportitems-operation.md) 
- [<span data-ttu-id="4b872-180">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="4b872-180">UploadItems operation</span></span>](uploaditems-operation.md)

