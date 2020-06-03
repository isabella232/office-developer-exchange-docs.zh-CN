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
description: FindFolderResponseMessage 元素包含单个 FindFolder 操作请求的状态和结果。
ms.openlocfilehash: 318a09e371043252d43a5197211e9623f34229fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462561"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="67a32-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="67a32-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="67a32-104">**FindFolderResponseMessage**元素包含单个[FindFolder 操作](findfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="67a32-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="67a32-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="67a32-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="67a32-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="67a32-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="67a32-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="67a32-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="67a32-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="67a32-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67a32-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67a32-109">Attributes and elements</span></span>

<span data-ttu-id="67a32-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67a32-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67a32-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="67a32-111">Attributes</span></span>

|<span data-ttu-id="67a32-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="67a32-112">**Attribute**</span></span>|<span data-ttu-id="67a32-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="67a32-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67a32-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="67a32-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="67a32-115">描述[FindFolder 操作](findfolder-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="67a32-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="67a32-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="67a32-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="67a32-117">-成功</span><span class="sxs-lookup"><span data-stu-id="67a32-117">-  Success</span></span>  <br/><span data-ttu-id="67a32-118">-警告</span><span class="sxs-lookup"><span data-stu-id="67a32-118">-  Warning</span></span>  <br/><span data-ttu-id="67a32-119">-错误</span><span class="sxs-lookup"><span data-stu-id="67a32-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="67a32-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="67a32-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="67a32-121">**值**</span><span class="sxs-lookup"><span data-stu-id="67a32-121">**Value**</span></span>|<span data-ttu-id="67a32-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="67a32-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67a32-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="67a32-123">**Success**</span></span> <br/> |<span data-ttu-id="67a32-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="67a32-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="67a32-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="67a32-125">**Warning**</span></span> <br/> | <span data-ttu-id="67a32-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="67a32-126">Describes a request that was not processed.</span></span> <span data-ttu-id="67a32-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="67a32-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="67a32-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="67a32-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="67a32-129">-Exchange 存储在批处理过程中脱机。</span><span class="sxs-lookup"><span data-stu-id="67a32-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="67a32-130">-Active Directory 域服务（AD DS）脱机。</span><span class="sxs-lookup"><span data-stu-id="67a32-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="67a32-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="67a32-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="67a32-132">-邮件数据库（MDB）脱机。</span><span class="sxs-lookup"><span data-stu-id="67a32-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="67a32-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="67a32-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="67a32-134">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="67a32-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="67a32-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="67a32-135">**Error**</span></span> <br/> | <span data-ttu-id="67a32-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="67a32-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="67a32-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="67a32-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="67a32-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="67a32-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="67a32-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="67a32-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="67a32-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="67a32-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="67a32-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="67a32-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="67a32-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="67a32-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="67a32-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="67a32-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="67a32-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="67a32-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67a32-145">子元素</span><span class="sxs-lookup"><span data-stu-id="67a32-145">Child elements</span></span>

|<span data-ttu-id="67a32-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="67a32-146">**Element**</span></span>|<span data-ttu-id="67a32-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="67a32-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67a32-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="67a32-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="67a32-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="67a32-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="67a32-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="67a32-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="67a32-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="67a32-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="67a32-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="67a32-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="67a32-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="67a32-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="67a32-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="67a32-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="67a32-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="67a32-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="67a32-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="67a32-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="67a32-157">RootFolder （FindFolderResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="67a32-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="67a32-158">包含在[FindFolder 操作](findfolder-operation.md)过程中搜索单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="67a32-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67a32-159">父元素</span><span class="sxs-lookup"><span data-stu-id="67a32-159">Parent elements</span></span>

|<span data-ttu-id="67a32-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="67a32-160">**Element**</span></span>|<span data-ttu-id="67a32-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="67a32-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67a32-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="67a32-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="67a32-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="67a32-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67a32-164">备注</span><span class="sxs-lookup"><span data-stu-id="67a32-164">Remarks</span></span>

<span data-ttu-id="67a32-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67a32-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67a32-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="67a32-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67a32-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="67a32-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67a32-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="67a32-168">Schema name</span></span>  <br/> |<span data-ttu-id="67a32-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="67a32-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="67a32-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="67a32-170">Validation file</span></span>  <br/> |<span data-ttu-id="67a32-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="67a32-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67a32-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="67a32-172">Can be empty</span></span>  <br/> |<span data-ttu-id="67a32-173">False</span><span class="sxs-lookup"><span data-stu-id="67a32-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67a32-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67a32-174">See also</span></span>

- [<span data-ttu-id="67a32-175">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="67a32-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="67a32-176">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="67a32-176">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

