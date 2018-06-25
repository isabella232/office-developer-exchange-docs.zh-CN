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
description: UpdateFolderResponseMessage 元素包含状态和更新的 UpdateFolder 操作请求 FolderChange 元素定义的结果。
ms.openlocfilehash: 4cd00232bcc233f6534d844418f523c248ce54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838388"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="706c3-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="706c3-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="706c3-104">**UpdateFolderResponseMessage**元素包含状态和更新的[UpdateFolder 操作](updatefolder-operation.md)请求[FolderChange](folderchange.md)元素定义的结果。</span><span class="sxs-lookup"><span data-stu-id="706c3-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="706c3-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="706c3-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="706c3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="706c3-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="706c3-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="706c3-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="706c3-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="706c3-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="706c3-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="706c3-109">Attributes and elements</span></span>

<span data-ttu-id="706c3-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="706c3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="706c3-111">属性</span><span class="sxs-lookup"><span data-stu-id="706c3-111">Attributes</span></span>

|<span data-ttu-id="706c3-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="706c3-112">**Attribute**</span></span>|<span data-ttu-id="706c3-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="706c3-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="706c3-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="706c3-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="706c3-115">介绍[UpdateFolder 操作](updatefolder-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="706c3-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="706c3-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="706c3-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="706c3-117">-成功</span><span class="sxs-lookup"><span data-stu-id="706c3-117">-  Success</span></span>  <br/><span data-ttu-id="706c3-118">-警告</span><span class="sxs-lookup"><span data-stu-id="706c3-118">-  Warning</span></span>  <br/><span data-ttu-id="706c3-119">-错误</span><span class="sxs-lookup"><span data-stu-id="706c3-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="706c3-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="706c3-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="706c3-121">**值**</span><span class="sxs-lookup"><span data-stu-id="706c3-121">**Value**</span></span>|<span data-ttu-id="706c3-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="706c3-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="706c3-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="706c3-123">**Success**</span></span> <br/> |<span data-ttu-id="706c3-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="706c3-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="706c3-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="706c3-125">**Warning**</span></span> <br/> | <span data-ttu-id="706c3-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="706c3-126">Describes a request that was not processed.</span></span> <span data-ttu-id="706c3-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="706c3-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="706c3-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="706c3-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="706c3-129">-在 Exchange 存储处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="706c3-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="706c3-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="706c3-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="706c3-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="706c3-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="706c3-132">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="706c3-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="706c3-133">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="706c3-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="706c3-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="706c3-134">**Error**</span></span> <br/> | <span data-ttu-id="706c3-135">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="706c3-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="706c3-136">下面是个错误的源的示例：</span><span class="sxs-lookup"><span data-stu-id="706c3-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="706c3-137">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="706c3-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="706c3-138">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="706c3-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="706c3-139">-未知标记</span><span class="sxs-lookup"><span data-stu-id="706c3-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="706c3-140">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="706c3-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="706c3-141">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="706c3-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="706c3-142">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="706c3-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="706c3-143">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="706c3-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="706c3-144">子元素</span><span class="sxs-lookup"><span data-stu-id="706c3-144">Child elements</span></span>

|<span data-ttu-id="706c3-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="706c3-145">**Element**</span></span>|<span data-ttu-id="706c3-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="706c3-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="706c3-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="706c3-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="706c3-148">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="706c3-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="706c3-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="706c3-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="706c3-150">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="706c3-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="706c3-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="706c3-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="706c3-152">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="706c3-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="706c3-153">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="706c3-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="706c3-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="706c3-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="706c3-155">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="706c3-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="706c3-156">Folders</span><span class="sxs-lookup"><span data-stu-id="706c3-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="706c3-157">包含文件夹在文件夹操作中使用的数组。</span><span class="sxs-lookup"><span data-stu-id="706c3-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="706c3-158">父元素</span><span class="sxs-lookup"><span data-stu-id="706c3-158">Parent elements</span></span>

|<span data-ttu-id="706c3-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="706c3-159">**Element**</span></span>|<span data-ttu-id="706c3-160">**说明**</span><span class="sxs-lookup"><span data-stu-id="706c3-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="706c3-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="706c3-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="706c3-162">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="706c3-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="706c3-163">注解</span><span class="sxs-lookup"><span data-stu-id="706c3-163">Remarks</span></span>

<span data-ttu-id="706c3-164">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="706c3-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="706c3-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="706c3-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="706c3-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="706c3-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="706c3-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="706c3-167">Schema Name</span></span>  <br/> |<span data-ttu-id="706c3-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="706c3-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="706c3-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="706c3-169">Validation File</span></span>  <br/> |<span data-ttu-id="706c3-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="706c3-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="706c3-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="706c3-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="706c3-172">False</span><span class="sxs-lookup"><span data-stu-id="706c3-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="706c3-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="706c3-173">See also</span></span>

- [<span data-ttu-id="706c3-174">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="706c3-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

