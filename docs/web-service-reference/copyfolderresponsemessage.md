---
title: CopyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolderResponseMessage
api_type:
- schema
ms.assetid: c82092a9-50ff-4ae1-b819-ebabbf89262b
description: CopyFolderResponseMessage 元素包含单个 CopyFolder 操作请求的状态和结果。
ms.openlocfilehash: 796ec57116e4b4943ca370e45cf0abefe7782c08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458507"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="f2ade-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f2ade-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="f2ade-104">**CopyFolderResponseMessage**元素包含单个[CopyFolder 操作](copyfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="f2ade-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="f2ade-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f2ade-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="f2ade-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f2ade-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="f2ade-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f2ade-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="f2ade-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f2ade-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2ade-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2ade-109">Attributes and elements</span></span>

<span data-ttu-id="f2ade-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2ade-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2ade-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="f2ade-111">Attributes</span></span>

|<span data-ttu-id="f2ade-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="f2ade-112">**Attribute**</span></span>|<span data-ttu-id="f2ade-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2ade-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2ade-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f2ade-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f2ade-115">描述[CopyFolder 操作](copyfolder-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="f2ade-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="f2ade-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="f2ade-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="f2ade-117">-成功</span><span class="sxs-lookup"><span data-stu-id="f2ade-117">- Success</span></span>  <br/><span data-ttu-id="f2ade-118">-警告</span><span class="sxs-lookup"><span data-stu-id="f2ade-118">-  Warning</span></span>  <br/><span data-ttu-id="f2ade-119">-错误</span><span class="sxs-lookup"><span data-stu-id="f2ade-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f2ade-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="f2ade-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="f2ade-121">**值**</span><span class="sxs-lookup"><span data-stu-id="f2ade-121">**Value**</span></span>|<span data-ttu-id="f2ade-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2ade-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2ade-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="f2ade-123">**Success**</span></span> <br/> |<span data-ttu-id="f2ade-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="f2ade-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f2ade-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="f2ade-125">**Warning**</span></span> <br/> | <span data-ttu-id="f2ade-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="f2ade-126">Describes a request that was not processed.</span></span> <span data-ttu-id="f2ade-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="f2ade-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="f2ade-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="f2ade-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="f2ade-129">-Exchange 存储在批处理过程中脱机。</span><span class="sxs-lookup"><span data-stu-id="f2ade-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="f2ade-130">-Active Directory 域服务（AD DS）脱机。</span><span class="sxs-lookup"><span data-stu-id="f2ade-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="f2ade-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="f2ade-132">-邮件数据库（MDB）脱机。</span><span class="sxs-lookup"><span data-stu-id="f2ade-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="f2ade-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="f2ade-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="f2ade-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="f2ade-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="f2ade-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="f2ade-135">**Error**</span></span> <br/> | <span data-ttu-id="f2ade-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="f2ade-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="f2ade-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="f2ade-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f2ade-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="f2ade-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f2ade-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="f2ade-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="f2ade-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="f2ade-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="f2ade-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="f2ade-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="f2ade-142">-任何客户端尝试的未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="f2ade-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="f2ade-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="f2ade-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="f2ade-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="f2ade-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f2ade-145">子元素</span><span class="sxs-lookup"><span data-stu-id="f2ade-145">Child elements</span></span>

|<span data-ttu-id="f2ade-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2ade-146">**Element**</span></span>|<span data-ttu-id="f2ade-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="f2ade-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2ade-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f2ade-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f2ade-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="f2ade-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f2ade-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f2ade-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f2ade-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f2ade-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f2ade-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f2ade-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f2ade-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="f2ade-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f2ade-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="f2ade-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f2ade-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f2ade-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f2ade-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="f2ade-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f2ade-157">Folders</span><span class="sxs-lookup"><span data-stu-id="f2ade-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f2ade-158">包含复制的文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="f2ade-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2ade-159">父元素</span><span class="sxs-lookup"><span data-stu-id="f2ade-159">Parent elements</span></span>

|<span data-ttu-id="f2ade-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2ade-160">**Element**</span></span>|<span data-ttu-id="f2ade-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="f2ade-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2ade-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f2ade-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f2ade-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="f2ade-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2ade-164">备注</span><span class="sxs-lookup"><span data-stu-id="f2ade-164">Remarks</span></span>

<span data-ttu-id="f2ade-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f2ade-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2ade-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2ade-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2ade-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2ade-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2ade-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2ade-168">Schema name</span></span>  <br/> |<span data-ttu-id="f2ade-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="f2ade-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2ade-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2ade-170">Validation file</span></span>  <br/> |<span data-ttu-id="f2ade-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2ade-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2ade-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2ade-172">Can be empty</span></span>  <br/> |<span data-ttu-id="f2ade-173">False</span><span class="sxs-lookup"><span data-stu-id="f2ade-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2ade-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2ade-174">See also</span></span>

- [<span data-ttu-id="f2ade-175">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2ade-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="f2ade-176">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="f2ade-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="f2ade-177">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f2ade-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

