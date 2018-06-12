---
title: MoveFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolderResponseMessage
api_type:
- schema
ms.assetid: 54917251-96af-44c2-ae90-d545f0a16e2e
description: MoveFolderResponseMessage 元素包含状态和单个 MoveFolder 操作请求的结果。
ms.openlocfilehash: 777520bf6a093882da95a7bfd466b66acdab957c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826496"
---
# <a name="movefolderresponsemessage"></a><span data-ttu-id="7e0a0-103">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7e0a0-103">MoveFolderResponseMessage</span></span>

<span data-ttu-id="7e0a0-104">**MoveFolderResponseMessage**元素包含状态和的单个结果[MoveFolder 操作](movefolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-104">The **MoveFolderResponseMessage** element contains the status and result of a single [MoveFolder operation](movefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="7e0a0-105">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="7e0a0-105">MoveFolderResponse</span></span>](movefolderresponse.md)
- [<span data-ttu-id="7e0a0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7e0a0-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="7e0a0-107">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7e0a0-107">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
  
```xml
<MoveFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</MoveFolderResponseMessage>
```

 <span data-ttu-id="7e0a0-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e0a0-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e0a0-109">Attributes and elements</span></span>

<span data-ttu-id="7e0a0-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e0a0-111">属性</span><span class="sxs-lookup"><span data-stu-id="7e0a0-111">Attributes</span></span>

|<span data-ttu-id="7e0a0-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-112">**Attribute**</span></span>|<span data-ttu-id="7e0a0-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e0a0-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7e0a0-115">描述[MoveFolder 操作](movefolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-115">Describes the status of a [MoveFolder operation](movefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="7e0a0-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="7e0a0-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="7e0a0-117">-成功</span><span class="sxs-lookup"><span data-stu-id="7e0a0-117">-  Success</span></span>  <br/><span data-ttu-id="7e0a0-118">-警告</span><span class="sxs-lookup"><span data-stu-id="7e0a0-118">-  Warning</span></span>  <br/><span data-ttu-id="7e0a0-119">-错误</span><span class="sxs-lookup"><span data-stu-id="7e0a0-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="7e0a0-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="7e0a0-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="7e0a0-121">**值**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-121">**Value**</span></span>|<span data-ttu-id="7e0a0-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e0a0-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-123">**Success**</span></span> <br/> |<span data-ttu-id="7e0a0-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7e0a0-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-125">**Warning**</span></span> <br/> | <span data-ttu-id="7e0a0-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-126">Describes a request that was not processed.</span></span> <span data-ttu-id="7e0a0-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="7e0a0-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="7e0a0-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7e0a0-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7e0a0-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7e0a0-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="7e0a0-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7e0a0-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="7e0a0-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="7e0a0-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-135">**Error**</span></span> <br/> | <span data-ttu-id="7e0a0-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7e0a0-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="7e0a0-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7e0a0-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="7e0a0-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7e0a0-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="7e0a0-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="7e0a0-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="7e0a0-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="7e0a0-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="7e0a0-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="7e0a0-142">-任何未经授权的访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="7e0a0-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7e0a0-143">的有效的客户端的呼叫的响应中任何服务器端故障</span><span class="sxs-lookup"><span data-stu-id="7e0a0-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="7e0a0-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e0a0-145">子元素</span><span class="sxs-lookup"><span data-stu-id="7e0a0-145">Child elements</span></span>

|<span data-ttu-id="7e0a0-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-146">**Element**</span></span>|<span data-ttu-id="7e0a0-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e0a0-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="7e0a0-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7e0a0-149">响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7e0a0-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7e0a0-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7e0a0-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7e0a0-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7e0a0-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7e0a0-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="7e0a0-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7e0a0-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7e0a0-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7e0a0-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7e0a0-157">Folders</span><span class="sxs-lookup"><span data-stu-id="7e0a0-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7e0a0-158">包含数组移动文件夹。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-158">Contains an array of moved folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e0a0-159">父元素</span><span class="sxs-lookup"><span data-stu-id="7e0a0-159">Parent elements</span></span>

|<span data-ttu-id="7e0a0-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-160">**Element**</span></span>|<span data-ttu-id="7e0a0-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e0a0-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e0a0-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7e0a0-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7e0a0-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e0a0-164">备注</span><span class="sxs-lookup"><span data-stu-id="7e0a0-164">Remarks</span></span>

<span data-ttu-id="7e0a0-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e0a0-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e0a0-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e0a0-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e0a0-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e0a0-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e0a0-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e0a0-168">Schema Name</span></span>  <br/> |<span data-ttu-id="7e0a0-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="7e0a0-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e0a0-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e0a0-170">Validation File</span></span>  <br/> |<span data-ttu-id="7e0a0-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e0a0-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e0a0-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e0a0-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e0a0-173">False</span><span class="sxs-lookup"><span data-stu-id="7e0a0-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e0a0-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e0a0-174">See also</span></span>

- [<span data-ttu-id="7e0a0-175">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="7e0a0-175">MoveFolder</span></span>](movefolder.md)
- [<span data-ttu-id="7e0a0-176">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="7e0a0-176">MoveFolder operation</span></span>](movefolder-operation.md)

