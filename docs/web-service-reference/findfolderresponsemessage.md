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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754335"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="0e0df-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0e0df-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="0e0df-104">**FindFolderResponseMessage**元素包含状态和的单个结果[FindFolder 操作](findfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="0e0df-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="0e0df-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0e0df-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="0e0df-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0e0df-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="0e0df-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0e0df-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="0e0df-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0e0df-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e0df-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0e0df-109">Attributes and elements</span></span>

<span data-ttu-id="0e0df-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0e0df-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e0df-111">属性</span><span class="sxs-lookup"><span data-stu-id="0e0df-111">Attributes</span></span>

|<span data-ttu-id="0e0df-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="0e0df-112">**Attribute**</span></span>|<span data-ttu-id="0e0df-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e0df-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e0df-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0e0df-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0e0df-115">描述[FindFolder 操作](findfolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="0e0df-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="0e0df-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="0e0df-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0e0df-117">-成功</span><span class="sxs-lookup"><span data-stu-id="0e0df-117">-  Success</span></span>  <br/><span data-ttu-id="0e0df-118">-警告</span><span class="sxs-lookup"><span data-stu-id="0e0df-118">-  Warning</span></span>  <br/><span data-ttu-id="0e0df-119">-错误</span><span class="sxs-lookup"><span data-stu-id="0e0df-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="0e0df-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="0e0df-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="0e0df-121">**值**</span><span class="sxs-lookup"><span data-stu-id="0e0df-121">**Value**</span></span>|<span data-ttu-id="0e0df-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e0df-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e0df-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="0e0df-123">**Success**</span></span> <br/> |<span data-ttu-id="0e0df-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="0e0df-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0e0df-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0e0df-125">**Warning**</span></span> <br/> | <span data-ttu-id="0e0df-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="0e0df-126">Describes a request that was not processed.</span></span> <span data-ttu-id="0e0df-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="0e0df-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0e0df-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="0e0df-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="0e0df-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="0e0df-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="0e0df-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="0e0df-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="0e0df-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="0e0df-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="0e0df-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="0e0df-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="0e0df-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="0e0df-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="0e0df-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="0e0df-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="0e0df-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="0e0df-135">**Error**</span></span> <br/> | <span data-ttu-id="0e0df-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="0e0df-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="0e0df-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="0e0df-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="0e0df-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="0e0df-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0e0df-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="0e0df-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0e0df-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="0e0df-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="0e0df-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="0e0df-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0e0df-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="0e0df-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="0e0df-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="0e0df-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="0e0df-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="0e0df-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0e0df-145">子元素</span><span class="sxs-lookup"><span data-stu-id="0e0df-145">Child elements</span></span>

|<span data-ttu-id="0e0df-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="0e0df-146">**Element**</span></span>|<span data-ttu-id="0e0df-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e0df-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e0df-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="0e0df-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0e0df-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0e0df-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0e0df-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0e0df-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0e0df-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0e0df-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0e0df-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0e0df-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0e0df-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0e0df-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0e0df-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="0e0df-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0e0df-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0e0df-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0e0df-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0e0df-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0e0df-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="0e0df-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="0e0df-158">[FindFolder 操作](findfolder-operation.md)期间包含单个根文件夹的搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="0e0df-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0e0df-159">父元素</span><span class="sxs-lookup"><span data-stu-id="0e0df-159">Parent elements</span></span>

|<span data-ttu-id="0e0df-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="0e0df-160">**Element**</span></span>|<span data-ttu-id="0e0df-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e0df-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e0df-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0e0df-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0e0df-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0e0df-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e0df-164">备注</span><span class="sxs-lookup"><span data-stu-id="0e0df-164">Remarks</span></span>

<span data-ttu-id="0e0df-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0e0df-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e0df-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="0e0df-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e0df-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="0e0df-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0e0df-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="0e0df-168">Schema name</span></span>  <br/> |<span data-ttu-id="0e0df-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="0e0df-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0e0df-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="0e0df-170">Validation file</span></span>  <br/> |<span data-ttu-id="0e0df-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0e0df-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e0df-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="0e0df-172">Can be empty</span></span>  <br/> |<span data-ttu-id="0e0df-173">False</span><span class="sxs-lookup"><span data-stu-id="0e0df-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e0df-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0e0df-174">See also</span></span>

- [<span data-ttu-id="0e0df-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="0e0df-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="0e0df-176">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="0e0df-176">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

