---
title: GetSharingMetadataResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadataResponse
api_type:
- schema
ms.assetid: 1acc2d8f-7104-4b36-9c04-dd4fc4f571bb
description: GetSharingMetadataResponse 元素定义对 GetSharingMetadata 操作请求的响应。
ms.openlocfilehash: eabeda2e6138e78858ffb044603f696ec65f3deb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530174"
---
# <a name="getsharingmetadataresponse"></a><span data-ttu-id="b22ab-103">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="b22ab-103">GetSharingMetadataResponse</span></span>

<span data-ttu-id="b22ab-104">**GetSharingMetadataResponse**元素定义对[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="b22ab-104">The **GetSharingMetadataResponse** element defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponse>
```

 <span data-ttu-id="b22ab-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b22ab-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b22ab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b22ab-106">Attributes and elements</span></span>

<span data-ttu-id="b22ab-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b22ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b22ab-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b22ab-108">Attributes</span></span>

|<span data-ttu-id="b22ab-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b22ab-109">**Attribute**</span></span>|<span data-ttu-id="b22ab-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b22ab-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b22ab-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b22ab-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b22ab-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="b22ab-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="b22ab-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="b22ab-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="b22ab-114">-成功</span><span class="sxs-lookup"><span data-stu-id="b22ab-114">-  Success</span></span>  <br/><span data-ttu-id="b22ab-115">-警告</span><span class="sxs-lookup"><span data-stu-id="b22ab-115">-  Warning</span></span>  <br/><span data-ttu-id="b22ab-116">-错误</span><span class="sxs-lookup"><span data-stu-id="b22ab-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b22ab-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="b22ab-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="b22ab-118">**值**</span><span class="sxs-lookup"><span data-stu-id="b22ab-118">**Value**</span></span>|<span data-ttu-id="b22ab-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b22ab-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b22ab-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="b22ab-120">**Success**</span></span> <br/> |<span data-ttu-id="b22ab-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="b22ab-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b22ab-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="b22ab-122">**Warning**</span></span> <br/> | <span data-ttu-id="b22ab-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="b22ab-123">Describes a request that was not processed.</span></span> <span data-ttu-id="b22ab-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="b22ab-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="b22ab-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="b22ab-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b22ab-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="b22ab-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b22ab-127">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="b22ab-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="b22ab-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="b22ab-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="b22ab-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="b22ab-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b22ab-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="b22ab-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="b22ab-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="b22ab-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="b22ab-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="b22ab-132">**Error**</span></span> <br/> | <span data-ttu-id="b22ab-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="b22ab-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="b22ab-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="b22ab-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b22ab-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="b22ab-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b22ab-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="b22ab-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="b22ab-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="b22ab-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="b22ab-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="b22ab-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="b22ab-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="b22ab-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b22ab-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="b22ab-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="b22ab-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="b22ab-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b22ab-142">子元素</span><span class="sxs-lookup"><span data-stu-id="b22ab-142">Child elements</span></span>

|<span data-ttu-id="b22ab-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="b22ab-143">**Element**</span></span>|<span data-ttu-id="b22ab-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="b22ab-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b22ab-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="b22ab-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b22ab-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="b22ab-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b22ab-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b22ab-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b22ab-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="b22ab-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b22ab-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b22ab-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b22ab-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="b22ab-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="b22ab-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="b22ab-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b22ab-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b22ab-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b22ab-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="b22ab-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b22ab-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="b22ab-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="b22ab-155">包含一组数据结构，客户端可以使用这些结构来授权与其他客户端共享其日历或联系人数据。</span><span class="sxs-lookup"><span data-stu-id="b22ab-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="b22ab-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="b22ab-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="b22ab-157">表示无效的文件夹共享请求的收件人。</span><span class="sxs-lookup"><span data-stu-id="b22ab-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b22ab-158">父元素</span><span class="sxs-lookup"><span data-stu-id="b22ab-158">Parent elements</span></span>

<span data-ttu-id="b22ab-159">无。</span><span class="sxs-lookup"><span data-stu-id="b22ab-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b22ab-160">说明</span><span class="sxs-lookup"><span data-stu-id="b22ab-160">Remarks</span></span>

<span data-ttu-id="b22ab-161">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="b22ab-161">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b22ab-162">元素信息</span><span class="sxs-lookup"><span data-stu-id="b22ab-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b22ab-163">命名空间</span><span class="sxs-lookup"><span data-stu-id="b22ab-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b22ab-164">架构名称</span><span class="sxs-lookup"><span data-stu-id="b22ab-164">Schema Name</span></span>  <br/> |<span data-ttu-id="b22ab-165">消息架构</span><span class="sxs-lookup"><span data-stu-id="b22ab-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b22ab-166">验证文件</span><span class="sxs-lookup"><span data-stu-id="b22ab-166">Validation File</span></span>  <br/> |<span data-ttu-id="b22ab-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b22ab-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b22ab-168">可以为空</span><span class="sxs-lookup"><span data-stu-id="b22ab-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="b22ab-169">False</span><span class="sxs-lookup"><span data-stu-id="b22ab-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b22ab-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b22ab-170">See also</span></span>

- [<span data-ttu-id="b22ab-171">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="b22ab-171">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="b22ab-172">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b22ab-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

