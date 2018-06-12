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
description: UpdateItemResponseMessage 元素包含状态和单个 UpdateItem 操作请求的结果。
ms.openlocfilehash: c971657813784e68a01539899e8fabea67847325
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838410"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="553f8-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="553f8-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="553f8-104">**UpdateItemResponseMessage**元素包含状态和的单个结果[UpdateItem 操作](updateitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="553f8-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="553f8-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="553f8-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="553f8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="553f8-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="553f8-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="553f8-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
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

 <span data-ttu-id="553f8-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="553f8-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="553f8-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="553f8-109">Attributes and elements</span></span>

<span data-ttu-id="553f8-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="553f8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="553f8-111">属性</span><span class="sxs-lookup"><span data-stu-id="553f8-111">Attributes</span></span>

|<span data-ttu-id="553f8-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="553f8-112">**Attribute**</span></span>|<span data-ttu-id="553f8-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="553f8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="553f8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="553f8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="553f8-115">介绍[UpdateItem 操作](updateitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="553f8-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="553f8-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="553f8-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="553f8-117">-成功</span><span class="sxs-lookup"><span data-stu-id="553f8-117">-  Success</span></span>  <br/><span data-ttu-id="553f8-118">-警告</span><span class="sxs-lookup"><span data-stu-id="553f8-118">-  Warning</span></span>  <br/><span data-ttu-id="553f8-119">-错误</span><span class="sxs-lookup"><span data-stu-id="553f8-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="553f8-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="553f8-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="553f8-121">**值**</span><span class="sxs-lookup"><span data-stu-id="553f8-121">**Value**</span></span>|<span data-ttu-id="553f8-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="553f8-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="553f8-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="553f8-123">**Success**</span></span> <br/> |<span data-ttu-id="553f8-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="553f8-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="553f8-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="553f8-125">**Warning**</span></span> <br/> | <span data-ttu-id="553f8-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="553f8-126">Describes a request that was not processed.</span></span> <span data-ttu-id="553f8-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="553f8-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="553f8-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="553f8-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="553f8-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="553f8-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="553f8-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="553f8-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="553f8-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="553f8-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="553f8-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="553f8-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="553f8-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="553f8-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="553f8-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="553f8-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="553f8-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="553f8-135">**Error**</span></span> <br/> | <span data-ttu-id="553f8-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="553f8-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="553f8-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="553f8-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="553f8-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="553f8-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="553f8-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="553f8-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="553f8-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="553f8-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="553f8-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="553f8-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="553f8-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="553f8-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="553f8-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="553f8-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="553f8-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="553f8-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="553f8-145">子元素</span><span class="sxs-lookup"><span data-stu-id="553f8-145">Child elements</span></span>

|<span data-ttu-id="553f8-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="553f8-146">**Element**</span></span>|<span data-ttu-id="553f8-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="553f8-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="553f8-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="553f8-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="553f8-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="553f8-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="553f8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="553f8-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="553f8-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="553f8-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="553f8-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="553f8-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="553f8-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="553f8-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="553f8-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="553f8-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="553f8-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="553f8-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="553f8-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="553f8-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="553f8-157">Items</span><span class="sxs-lookup"><span data-stu-id="553f8-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="553f8-158">包含更新项的数组。</span><span class="sxs-lookup"><span data-stu-id="553f8-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="553f8-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="553f8-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="553f8-160">包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突的数量。</span><span class="sxs-lookup"><span data-stu-id="553f8-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="553f8-161">父元素</span><span class="sxs-lookup"><span data-stu-id="553f8-161">Parent elements</span></span>

|<span data-ttu-id="553f8-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="553f8-162">**Element**</span></span>|<span data-ttu-id="553f8-163">**说明**</span><span class="sxs-lookup"><span data-stu-id="553f8-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="553f8-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="553f8-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="553f8-165">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="553f8-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="553f8-166">备注</span><span class="sxs-lookup"><span data-stu-id="553f8-166">Remarks</span></span>

<span data-ttu-id="553f8-167">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="553f8-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="553f8-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="553f8-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="553f8-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="553f8-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="553f8-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="553f8-170">Schema Name</span></span>  <br/> |<span data-ttu-id="553f8-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="553f8-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="553f8-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="553f8-172">Validation File</span></span>  <br/> |<span data-ttu-id="553f8-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="553f8-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="553f8-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="553f8-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="553f8-175">False</span><span class="sxs-lookup"><span data-stu-id="553f8-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="553f8-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="553f8-176">See also</span></span>

- [<span data-ttu-id="553f8-177">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="553f8-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="553f8-178">更新联系人</span><span class="sxs-lookup"><span data-stu-id="553f8-178">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="553f8-179">更新任务</span><span class="sxs-lookup"><span data-stu-id="553f8-179">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

