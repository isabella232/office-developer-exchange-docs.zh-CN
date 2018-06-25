---
title: GetSharingMetadataResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadataResponseMessage
api_type:
- schema
ms.assetid: d81b8708-ebb2-45c2-861f-b9a814eee6ba
description: GetSharingMetadataResponseMessage 元素包含状态和单个 GetSharingMetadata 操作请求的结果。
ms.openlocfilehash: 24da0a78870b2c92e0751eba0631d58076b96eae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825674"
---
# <a name="getsharingmetadataresponsemessage"></a><span data-ttu-id="bc1e3-103">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bc1e3-103">GetSharingMetadataResponseMessage</span></span>

<span data-ttu-id="bc1e3-104">**GetSharingMetadataResponseMessage**元素包含状态和的单个结果[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-104">The **GetSharingMetadataResponseMessage** element contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponseMessage>
```

 <span data-ttu-id="bc1e3-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc1e3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-106">Attributes and elements</span></span>

<span data-ttu-id="bc1e3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc1e3-108">属性</span><span class="sxs-lookup"><span data-stu-id="bc1e3-108">Attributes</span></span>

|<span data-ttu-id="bc1e3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-109">**Attribute**</span></span>|<span data-ttu-id="bc1e3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc1e3-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bc1e3-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="bc1e3-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="bc1e3-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="bc1e3-114">-成功</span><span class="sxs-lookup"><span data-stu-id="bc1e3-114">-  Success</span></span>  <br/><span data-ttu-id="bc1e3-115">-警告</span><span class="sxs-lookup"><span data-stu-id="bc1e3-115">-  Warning</span></span>  <br/><span data-ttu-id="bc1e3-116">-错误</span><span class="sxs-lookup"><span data-stu-id="bc1e3-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="bc1e3-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="bc1e3-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="bc1e3-118">**值**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-118">**Value**</span></span>|<span data-ttu-id="bc1e3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc1e3-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-120">**Success**</span></span> <br/> |<span data-ttu-id="bc1e3-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bc1e3-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-122">**Warning**</span></span> <br/> | <span data-ttu-id="bc1e3-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-123">Describes a request that was not processed.</span></span> <span data-ttu-id="bc1e3-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="bc1e3-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="bc1e3-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="bc1e3-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="bc1e3-127">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="bc1e3-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="bc1e3-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="bc1e3-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="bc1e3-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="bc1e3-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-132">**Error**</span></span> <br/> | <span data-ttu-id="bc1e3-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="bc1e3-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="bc1e3-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bc1e3-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bc1e3-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="bc1e3-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="bc1e3-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="bc1e3-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="bc1e3-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="bc1e3-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="bc1e3-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bc1e3-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="bc1e3-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="bc1e3-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bc1e3-142">子元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-142">Child elements</span></span>

|<span data-ttu-id="bc1e3-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-143">**Element**</span></span>|<span data-ttu-id="bc1e3-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc1e3-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="bc1e3-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bc1e3-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bc1e3-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bc1e3-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bc1e3-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="bc1e3-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bc1e3-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bc1e3-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="bc1e3-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bc1e3-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bc1e3-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bc1e3-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bc1e3-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="bc1e3-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="bc1e3-155">包含客户端可以使用授权其日历共享或与其他客户端联系人数据的数据结构的集合。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="bc1e3-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="bc1e3-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="bc1e3-157">代表共享请求的文件夹的无效的收件人。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc1e3-158">父元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-158">Parent elements</span></span>

|<span data-ttu-id="bc1e3-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-159">**Element**</span></span>|<span data-ttu-id="bc1e3-160">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc1e3-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bc1e3-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="bc1e3-162">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc1e3-163">备注</span><span class="sxs-lookup"><span data-stu-id="bc1e3-163">Remarks</span></span>

<span data-ttu-id="bc1e3-164">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-164">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc1e3-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc1e3-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc1e3-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc1e3-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bc1e3-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc1e3-167">Schema Name</span></span>  <br/> |<span data-ttu-id="bc1e3-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="bc1e3-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bc1e3-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc1e3-169">Validation File</span></span>  <br/> |<span data-ttu-id="bc1e3-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bc1e3-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc1e3-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc1e3-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc1e3-172">False</span><span class="sxs-lookup"><span data-stu-id="bc1e3-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc1e3-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc1e3-173">See also</span></span>

- [<span data-ttu-id="bc1e3-174">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="bc1e3-174">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="bc1e3-175">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc1e3-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

