---
title: UpdateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolderResponseMessage
api_type:
- schema
ms.assetid: 914bb683-49ee-44a2-b59d-ef560244dfb8
description: UpdateFolderResponseMessage 元素包含 UpdateFolder 操作请求的 FolderChange 元素定义的更新的状态和结果。
ms.openlocfilehash: bbe01583072e6203e099d440f2a171012f51e7df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466582"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="94c02-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94c02-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="94c02-104">**UpdateFolderResponseMessage**元素包含[UpdateFolder 操作](updatefolder-operation.md)请求的[FolderChange](folderchange.md)元素定义的更新的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="94c02-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="94c02-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="94c02-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="94c02-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94c02-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="94c02-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94c02-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="94c02-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="94c02-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94c02-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="94c02-109">Attributes and elements</span></span>

<span data-ttu-id="94c02-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="94c02-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94c02-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="94c02-111">Attributes</span></span>

|<span data-ttu-id="94c02-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="94c02-112">**Attribute**</span></span>|<span data-ttu-id="94c02-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="94c02-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94c02-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="94c02-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="94c02-115">描述[UpdateFolder 操作](updatefolder-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="94c02-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="94c02-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="94c02-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="94c02-117">-成功</span><span class="sxs-lookup"><span data-stu-id="94c02-117">-  Success</span></span>  <br/><span data-ttu-id="94c02-118">-警告</span><span class="sxs-lookup"><span data-stu-id="94c02-118">-  Warning</span></span>  <br/><span data-ttu-id="94c02-119">-错误</span><span class="sxs-lookup"><span data-stu-id="94c02-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="94c02-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="94c02-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="94c02-121">**值**</span><span class="sxs-lookup"><span data-stu-id="94c02-121">**Value**</span></span>|<span data-ttu-id="94c02-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="94c02-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94c02-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="94c02-123">**Success**</span></span> <br/> |<span data-ttu-id="94c02-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="94c02-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="94c02-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="94c02-125">**Warning**</span></span> <br/> | <span data-ttu-id="94c02-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="94c02-126">Describes a request that was not processed.</span></span> <span data-ttu-id="94c02-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="94c02-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="94c02-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="94c02-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="94c02-129">-Exchange 存储处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="94c02-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="94c02-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="94c02-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="94c02-131">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="94c02-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="94c02-132">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="94c02-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="94c02-133">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="94c02-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="94c02-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="94c02-134">**Error**</span></span> <br/> | <span data-ttu-id="94c02-135">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="94c02-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="94c02-136">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="94c02-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="94c02-137">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="94c02-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="94c02-138">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="94c02-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="94c02-139">-未知标记</span><span class="sxs-lookup"><span data-stu-id="94c02-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="94c02-140">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="94c02-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="94c02-141">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="94c02-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="94c02-142">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="94c02-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="94c02-143">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="94c02-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94c02-144">子元素</span><span class="sxs-lookup"><span data-stu-id="94c02-144">Child elements</span></span>

|<span data-ttu-id="94c02-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="94c02-145">**Element**</span></span>|<span data-ttu-id="94c02-146">**描述**</span><span class="sxs-lookup"><span data-stu-id="94c02-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94c02-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="94c02-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="94c02-148">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="94c02-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="94c02-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="94c02-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="94c02-150">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="94c02-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="94c02-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="94c02-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="94c02-152">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="94c02-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="94c02-153">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="94c02-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="94c02-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="94c02-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="94c02-155">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="94c02-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="94c02-156">Folders</span><span class="sxs-lookup"><span data-stu-id="94c02-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="94c02-157">包含文件夹在文件夹操作中使用的数组。</span><span class="sxs-lookup"><span data-stu-id="94c02-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94c02-158">父元素</span><span class="sxs-lookup"><span data-stu-id="94c02-158">Parent elements</span></span>

|<span data-ttu-id="94c02-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="94c02-159">**Element**</span></span>|<span data-ttu-id="94c02-160">**描述**</span><span class="sxs-lookup"><span data-stu-id="94c02-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94c02-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94c02-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="94c02-162">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="94c02-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94c02-163">备注</span><span class="sxs-lookup"><span data-stu-id="94c02-163">Remarks</span></span>

<span data-ttu-id="94c02-164">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="94c02-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94c02-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="94c02-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94c02-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="94c02-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94c02-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="94c02-167">Schema Name</span></span>  <br/> |<span data-ttu-id="94c02-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="94c02-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="94c02-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="94c02-169">Validation File</span></span>  <br/> |<span data-ttu-id="94c02-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="94c02-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94c02-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="94c02-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="94c02-172">False</span><span class="sxs-lookup"><span data-stu-id="94c02-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94c02-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94c02-173">See also</span></span>

- [<span data-ttu-id="94c02-174">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="94c02-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

