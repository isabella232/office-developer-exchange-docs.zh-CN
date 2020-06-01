---
title: GetSharingFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolderResponse
api_type:
- schema
ms.assetid: fee90e84-3ad4-4c4b-831f-bbc95070aebf
description: GetSharingFolderResponse 元素定义对 GetSharingFolder 操作请求的响应。
ms.openlocfilehash: 2b5a263b350ae54e87a8fea7cb7cc2d9485b5814
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460482"
---
# <a name="getsharingfolderresponse"></a><span data-ttu-id="c2fd0-103">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c2fd0-103">GetSharingFolderResponse</span></span>

<span data-ttu-id="c2fd0-104">**GetSharingFolderResponse**元素定义对[GetSharingFolder 操作](getsharingfolder-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-104">The **GetSharingFolderResponse** element defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```XML
<GetSharingFolderResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <SharingFolderId/>
</GetSharingFolderResponse>
```

 <span data-ttu-id="c2fd0-105">**GetSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-105">**GetSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2fd0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-106">Attributes and elements</span></span>

<span data-ttu-id="c2fd0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2fd0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c2fd0-108">Attributes</span></span>

|<span data-ttu-id="c2fd0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-109">**Attribute**</span></span>|<span data-ttu-id="c2fd0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2fd0-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c2fd0-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="c2fd0-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="c2fd0-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="c2fd0-114">-成功</span><span class="sxs-lookup"><span data-stu-id="c2fd0-114">-  Success</span></span>  <br/><span data-ttu-id="c2fd0-115">-警告</span><span class="sxs-lookup"><span data-stu-id="c2fd0-115">-  Warning</span></span>  <br/><span data-ttu-id="c2fd0-116">-错误</span><span class="sxs-lookup"><span data-stu-id="c2fd0-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c2fd0-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="c2fd0-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="c2fd0-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-118">**Value**</span></span>|<span data-ttu-id="c2fd0-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2fd0-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-120">**Success**</span></span> <br/> |<span data-ttu-id="c2fd0-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c2fd0-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-122">**Warning**</span></span> <br/> | <span data-ttu-id="c2fd0-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c2fd0-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c2fd0-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="c2fd0-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="c2fd0-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c2fd0-127">-Active Directory 目录服务或 Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-127">-  The Active Directory directory service or Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c2fd0-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="c2fd0-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c2fd0-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c2fd0-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="c2fd0-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-132">**Error**</span></span> <br/> | <span data-ttu-id="c2fd0-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="c2fd0-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="c2fd0-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c2fd0-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="c2fd0-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c2fd0-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="c2fd0-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c2fd0-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="c2fd0-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="c2fd0-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="c2fd0-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c2fd0-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="c2fd0-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="c2fd0-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c2fd0-142">子元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-142">Child elements</span></span>

|<span data-ttu-id="c2fd0-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-143">**Element**</span></span>|<span data-ttu-id="c2fd0-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="c2fd0-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2fd0-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c2fd0-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c2fd0-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c2fd0-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c2fd0-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c2fd0-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c2fd0-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c2fd0-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c2fd0-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="c2fd0-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c2fd0-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c2fd0-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c2fd0-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c2fd0-154">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="c2fd0-154">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="c2fd0-155">表示共享关系中的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-155">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2fd0-156">父元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-156">Parent elements</span></span>

<span data-ttu-id="c2fd0-157">无。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2fd0-158">说明</span><span class="sxs-lookup"><span data-stu-id="c2fd0-158">Remarks</span></span>

<span data-ttu-id="c2fd0-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c2fd0-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2fd0-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2fd0-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2fd0-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2fd0-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2fd0-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2fd0-162">Schema Name</span></span>  <br/> |<span data-ttu-id="c2fd0-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="c2fd0-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2fd0-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2fd0-164">Validation File</span></span>  <br/> |<span data-ttu-id="c2fd0-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c2fd0-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2fd0-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2fd0-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2fd0-167">False</span><span class="sxs-lookup"><span data-stu-id="c2fd0-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2fd0-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2fd0-168">See also</span></span>

- [<span data-ttu-id="c2fd0-169">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c2fd0-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

