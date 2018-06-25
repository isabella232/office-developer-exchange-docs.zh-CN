---
title: FindFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolderResponseMessage
api_type:
- schema
ms.assetid: 538d64fe-51ae-41d2-bfab-91698678aa1b
description: FindFolderResponseMessage 元素包含状态和单个 FindFolder 操作请求的结果。
ms.openlocfilehash: 5623e5e538e617e5bd4bbc4444328ac83d7b8065
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754335"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="97c8a-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="97c8a-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="97c8a-104">**FindFolderResponseMessage**元素包含状态和的单个结果[FindFolder 操作](findfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="97c8a-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="97c8a-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="97c8a-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="97c8a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="97c8a-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="97c8a-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="97c8a-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="97c8a-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="97c8a-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97c8a-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="97c8a-109">Attributes and elements</span></span>

<span data-ttu-id="97c8a-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="97c8a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97c8a-111">属性</span><span class="sxs-lookup"><span data-stu-id="97c8a-111">Attributes</span></span>

|<span data-ttu-id="97c8a-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="97c8a-112">**Attribute**</span></span>|<span data-ttu-id="97c8a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="97c8a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97c8a-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="97c8a-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="97c8a-115">描述[FindFolder 操作](findfolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="97c8a-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="97c8a-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="97c8a-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="97c8a-117">-成功</span><span class="sxs-lookup"><span data-stu-id="97c8a-117">-  Success</span></span>  <br/><span data-ttu-id="97c8a-118">-警告</span><span class="sxs-lookup"><span data-stu-id="97c8a-118">-  Warning</span></span>  <br/><span data-ttu-id="97c8a-119">-错误</span><span class="sxs-lookup"><span data-stu-id="97c8a-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="97c8a-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="97c8a-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="97c8a-121">**值**</span><span class="sxs-lookup"><span data-stu-id="97c8a-121">**Value**</span></span>|<span data-ttu-id="97c8a-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="97c8a-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97c8a-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="97c8a-123">**Success**</span></span> <br/> |<span data-ttu-id="97c8a-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="97c8a-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="97c8a-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="97c8a-125">**Warning**</span></span> <br/> | <span data-ttu-id="97c8a-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="97c8a-126">Describes a request that was not processed.</span></span> <span data-ttu-id="97c8a-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="97c8a-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="97c8a-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="97c8a-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="97c8a-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="97c8a-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="97c8a-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="97c8a-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="97c8a-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="97c8a-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="97c8a-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="97c8a-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="97c8a-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="97c8a-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="97c8a-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="97c8a-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="97c8a-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="97c8a-135">**Error**</span></span> <br/> | <span data-ttu-id="97c8a-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="97c8a-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="97c8a-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="97c8a-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="97c8a-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="97c8a-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="97c8a-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="97c8a-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="97c8a-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="97c8a-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="97c8a-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="97c8a-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="97c8a-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="97c8a-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="97c8a-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="97c8a-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="97c8a-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="97c8a-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97c8a-145">子元素</span><span class="sxs-lookup"><span data-stu-id="97c8a-145">Child elements</span></span>

|<span data-ttu-id="97c8a-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="97c8a-146">**Element**</span></span>|<span data-ttu-id="97c8a-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="97c8a-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97c8a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="97c8a-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="97c8a-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="97c8a-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="97c8a-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="97c8a-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="97c8a-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="97c8a-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="97c8a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="97c8a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="97c8a-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="97c8a-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="97c8a-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="97c8a-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="97c8a-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="97c8a-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="97c8a-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="97c8a-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="97c8a-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="97c8a-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="97c8a-158">[FindFolder 操作](findfolder-operation.md)期间包含单个根文件夹的搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="97c8a-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="97c8a-159">父元素</span><span class="sxs-lookup"><span data-stu-id="97c8a-159">Parent elements</span></span>

|<span data-ttu-id="97c8a-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="97c8a-160">**Element**</span></span>|<span data-ttu-id="97c8a-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="97c8a-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97c8a-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="97c8a-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="97c8a-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="97c8a-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97c8a-164">注解</span><span class="sxs-lookup"><span data-stu-id="97c8a-164">Remarks</span></span>

<span data-ttu-id="97c8a-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="97c8a-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97c8a-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="97c8a-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97c8a-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="97c8a-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="97c8a-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="97c8a-168">Schema name</span></span>  <br/> |<span data-ttu-id="97c8a-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="97c8a-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="97c8a-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="97c8a-170">Validation file</span></span>  <br/> |<span data-ttu-id="97c8a-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="97c8a-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="97c8a-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="97c8a-172">Can be empty</span></span>  <br/> |<span data-ttu-id="97c8a-173">False</span><span class="sxs-lookup"><span data-stu-id="97c8a-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97c8a-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97c8a-174">See also</span></span>

- [<span data-ttu-id="97c8a-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="97c8a-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="97c8a-176">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="97c8a-176">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

