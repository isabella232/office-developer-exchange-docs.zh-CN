---
title: UpdateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItemResponseMessage
api_type:
- schema
ms.assetid: dc585b05-5afc-4c74-8763-5a54f9a650ec
description: UpdateItemResponseMessage 元素包含单个 UpdateItem 操作请求的状态和结果。
ms.openlocfilehash: ef25dcf26e06f199587cef885d8cbc9e93b52bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457940"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="1a291-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1a291-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="1a291-104">**UpdateItemResponseMessage**元素包含单个[UpdateItem 操作](updateitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1a291-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="1a291-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="1a291-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="1a291-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a291-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="1a291-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1a291-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
```xml
<UpdateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <ConflictResults/>
</UpdateItemResponseMessage>
```

 <span data-ttu-id="1a291-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1a291-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a291-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a291-109">Attributes and elements</span></span>

<span data-ttu-id="1a291-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a291-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a291-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="1a291-111">Attributes</span></span>

|<span data-ttu-id="1a291-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="1a291-112">**Attribute**</span></span>|<span data-ttu-id="1a291-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a291-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a291-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1a291-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1a291-115">描述[UpdateItem 操作](updateitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="1a291-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="1a291-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="1a291-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1a291-117">-成功</span><span class="sxs-lookup"><span data-stu-id="1a291-117">-  Success</span></span>  <br/><span data-ttu-id="1a291-118">-警告</span><span class="sxs-lookup"><span data-stu-id="1a291-118">-  Warning</span></span>  <br/><span data-ttu-id="1a291-119">-错误</span><span class="sxs-lookup"><span data-stu-id="1a291-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1a291-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="1a291-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="1a291-121">**值**</span><span class="sxs-lookup"><span data-stu-id="1a291-121">**Value**</span></span>|<span data-ttu-id="1a291-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a291-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a291-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="1a291-123">**Success**</span></span> <br/> |<span data-ttu-id="1a291-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="1a291-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1a291-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="1a291-125">**Warning**</span></span> <br/> | <span data-ttu-id="1a291-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="1a291-126">Describes a request that was not processed.</span></span> <span data-ttu-id="1a291-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="1a291-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1a291-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="1a291-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1a291-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1a291-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1a291-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1a291-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1a291-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="1a291-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="1a291-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1a291-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1a291-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="1a291-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="1a291-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="1a291-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="1a291-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="1a291-135">**Error**</span></span> <br/> | <span data-ttu-id="1a291-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="1a291-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1a291-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="1a291-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1a291-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1a291-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1a291-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="1a291-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1a291-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="1a291-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="1a291-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1a291-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1a291-142">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="1a291-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1a291-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="1a291-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1a291-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="1a291-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1a291-145">子元素</span><span class="sxs-lookup"><span data-stu-id="1a291-145">Child elements</span></span>

|<span data-ttu-id="1a291-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a291-146">**Element**</span></span>|<span data-ttu-id="1a291-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="1a291-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a291-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="1a291-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1a291-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="1a291-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1a291-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1a291-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1a291-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="1a291-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1a291-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1a291-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1a291-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="1a291-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1a291-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="1a291-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1a291-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1a291-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1a291-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="1a291-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1a291-157">Items</span><span class="sxs-lookup"><span data-stu-id="1a291-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="1a291-158">包含已更新项的数组。</span><span class="sxs-lookup"><span data-stu-id="1a291-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="1a291-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="1a291-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="1a291-160">包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。</span><span class="sxs-lookup"><span data-stu-id="1a291-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a291-161">父元素</span><span class="sxs-lookup"><span data-stu-id="1a291-161">Parent elements</span></span>

|<span data-ttu-id="1a291-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a291-162">**Element**</span></span>|<span data-ttu-id="1a291-163">**描述**</span><span class="sxs-lookup"><span data-stu-id="1a291-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a291-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a291-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1a291-165">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="1a291-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a291-166">备注</span><span class="sxs-lookup"><span data-stu-id="1a291-166">Remarks</span></span>

<span data-ttu-id="1a291-167">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1a291-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a291-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a291-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a291-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a291-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a291-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a291-170">Schema Name</span></span>  <br/> |<span data-ttu-id="1a291-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="1a291-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1a291-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a291-172">Validation File</span></span>  <br/> |<span data-ttu-id="1a291-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1a291-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a291-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a291-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a291-175">False</span><span class="sxs-lookup"><span data-stu-id="1a291-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a291-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a291-176">See also</span></span>

- [<span data-ttu-id="1a291-177">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="1a291-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="1a291-178">更新联系人</span><span class="sxs-lookup"><span data-stu-id="1a291-178">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="1a291-179">更新任务</span><span class="sxs-lookup"><span data-stu-id="1a291-179">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

