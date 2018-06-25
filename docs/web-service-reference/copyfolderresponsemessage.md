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
description: CopyFolderResponseMessage 元素包含状态和单个 CopyFolder 操作请求的结果。
ms.openlocfilehash: 2bb2b407e0ae6b854d214c4b9d68ac8ed65b2c7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753607"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="c45d2-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c45d2-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="c45d2-104">**CopyFolderResponseMessage**元素包含状态和的单个结果[CopyFolder 操作](copyfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="c45d2-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="c45d2-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c45d2-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="c45d2-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c45d2-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="c45d2-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c45d2-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="c45d2-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c45d2-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c45d2-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-109">Attributes and elements</span></span>

<span data-ttu-id="c45d2-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c45d2-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c45d2-111">属性</span><span class="sxs-lookup"><span data-stu-id="c45d2-111">Attributes</span></span>

|<span data-ttu-id="c45d2-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="c45d2-112">**Attribute**</span></span>|<span data-ttu-id="c45d2-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="c45d2-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c45d2-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c45d2-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c45d2-115">描述[CopyFolder 操作](copyfolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c45d2-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="c45d2-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="c45d2-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="c45d2-117">-成功</span><span class="sxs-lookup"><span data-stu-id="c45d2-117">- Success</span></span>  <br/><span data-ttu-id="c45d2-118">-警告</span><span class="sxs-lookup"><span data-stu-id="c45d2-118">-  Warning</span></span>  <br/><span data-ttu-id="c45d2-119">-错误</span><span class="sxs-lookup"><span data-stu-id="c45d2-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c45d2-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="c45d2-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="c45d2-121">**值**</span><span class="sxs-lookup"><span data-stu-id="c45d2-121">**Value**</span></span>|<span data-ttu-id="c45d2-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="c45d2-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c45d2-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="c45d2-123">**Success**</span></span> <br/> |<span data-ttu-id="c45d2-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c45d2-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c45d2-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="c45d2-125">**Warning**</span></span> <br/> | <span data-ttu-id="c45d2-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c45d2-126">Describes a request that was not processed.</span></span> <span data-ttu-id="c45d2-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="c45d2-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="c45d2-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="c45d2-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="c45d2-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="c45d2-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="c45d2-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="c45d2-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="c45d2-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="c45d2-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="c45d2-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="c45d2-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="c45d2-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="c45d2-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="c45d2-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="c45d2-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="c45d2-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="c45d2-135">**Error**</span></span> <br/> | <span data-ttu-id="c45d2-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="c45d2-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="c45d2-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="c45d2-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c45d2-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c45d2-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="c45d2-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c45d2-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="c45d2-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="c45d2-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="c45d2-142">的尝试的任何客户端未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="c45d2-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="c45d2-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="c45d2-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="c45d2-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="c45d2-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c45d2-145">子元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-145">Child elements</span></span>

|<span data-ttu-id="c45d2-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="c45d2-146">**Element**</span></span>|<span data-ttu-id="c45d2-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="c45d2-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c45d2-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="c45d2-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c45d2-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c45d2-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c45d2-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c45d2-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c45d2-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c45d2-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c45d2-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c45d2-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c45d2-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c45d2-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c45d2-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="c45d2-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c45d2-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c45d2-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c45d2-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c45d2-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c45d2-157">Folders</span><span class="sxs-lookup"><span data-stu-id="c45d2-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c45d2-158">包含复制的文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="c45d2-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c45d2-159">父元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-159">Parent elements</span></span>

|<span data-ttu-id="c45d2-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="c45d2-160">**Element**</span></span>|<span data-ttu-id="c45d2-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="c45d2-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c45d2-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c45d2-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c45d2-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c45d2-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c45d2-164">注解</span><span class="sxs-lookup"><span data-stu-id="c45d2-164">Remarks</span></span>

<span data-ttu-id="c45d2-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c45d2-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c45d2-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="c45d2-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c45d2-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="c45d2-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c45d2-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="c45d2-168">Schema name</span></span>  <br/> |<span data-ttu-id="c45d2-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="c45d2-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c45d2-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="c45d2-170">Validation file</span></span>  <br/> |<span data-ttu-id="c45d2-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c45d2-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c45d2-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="c45d2-172">Can be empty</span></span>  <br/> |<span data-ttu-id="c45d2-173">False</span><span class="sxs-lookup"><span data-stu-id="c45d2-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c45d2-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c45d2-174">See also</span></span>

- [<span data-ttu-id="c45d2-175">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="c45d2-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="c45d2-176">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="c45d2-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="c45d2-177">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c45d2-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

