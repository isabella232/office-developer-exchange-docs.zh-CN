---
title: FindItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItemResponseMessage
api_type:
- schema
ms.assetid: fb2cd399-8a04-4f26-9091-993134ed1d15
description: FindItemResponseMessage 元素包含状态和单个 FindItem 操作请求的结果。
ms.openlocfilehash: 0a4bfb3ba8d85b0bff0d03f043be865ce7276229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754346"
---
# <a name="finditemresponsemessage"></a><span data-ttu-id="2d490-103">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2d490-103">FindItemResponseMessage</span></span>

<span data-ttu-id="2d490-104">**FindItemResponseMessage**元素包含状态和的单个结果[FindItem 操作](finditem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="2d490-104">The **FindItemResponseMessage** element contains the status and result of a single [FindItem operation](finditem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2d490-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="2d490-105">FindItemResponse</span></span>](finditemresponse.md) 
- [<span data-ttu-id="2d490-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2d490-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="2d490-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2d490-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
```xml
<FindItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindItemResponseMessage>
```

 <span data-ttu-id="2d490-108">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2d490-108">**FindItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d490-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d490-109">Attributes and elements</span></span>

<span data-ttu-id="2d490-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d490-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d490-111">属性</span><span class="sxs-lookup"><span data-stu-id="2d490-111">Attributes</span></span>

|<span data-ttu-id="2d490-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="2d490-112">**Attribute**</span></span>|<span data-ttu-id="2d490-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d490-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d490-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2d490-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2d490-115">描述[FindItem 操作](finditem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="2d490-115">Describes the status of a [FindItem operation](finditem-operation.md) response.</span></span><br/><br/> <span data-ttu-id="2d490-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="2d490-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="2d490-117">-成功</span><span class="sxs-lookup"><span data-stu-id="2d490-117">-  Success</span></span>  <br/><span data-ttu-id="2d490-118">-警告</span><span class="sxs-lookup"><span data-stu-id="2d490-118">-  Warning</span></span>  <br/><span data-ttu-id="2d490-119">-错误</span><span class="sxs-lookup"><span data-stu-id="2d490-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2d490-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="2d490-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="2d490-121">**值**</span><span class="sxs-lookup"><span data-stu-id="2d490-121">**Value**</span></span>|<span data-ttu-id="2d490-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d490-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d490-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="2d490-123">**Success**</span></span> <br/> |<span data-ttu-id="2d490-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="2d490-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2d490-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2d490-125">**Warning**</span></span> <br/> | <span data-ttu-id="2d490-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="2d490-126">Describes a request that was not processed.</span></span> <span data-ttu-id="2d490-127">可能返回一条警告，如果处理请求中的项目处理和无法处理后续项时出错。</span><span class="sxs-lookup"><span data-stu-id="2d490-127">A warning may be returned if an error occurred while processing an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2d490-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="2d490-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="2d490-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="2d490-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="2d490-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="2d490-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="2d490-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="2d490-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="2d490-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="2d490-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="2d490-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="2d490-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="2d490-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="2d490-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="2d490-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="2d490-135">**Error**</span></span> <br/> | <span data-ttu-id="2d490-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="2d490-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2d490-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="2d490-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2d490-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="2d490-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2d490-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="2d490-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="2d490-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="2d490-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="2d490-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="2d490-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2d490-142">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="2d490-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2d490-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="2d490-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2d490-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="2d490-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2d490-145">子元素</span><span class="sxs-lookup"><span data-stu-id="2d490-145">Child elements</span></span>

|<span data-ttu-id="2d490-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d490-146">**Element**</span></span>|<span data-ttu-id="2d490-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d490-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d490-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="2d490-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2d490-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="2d490-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2d490-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2d490-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2d490-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2d490-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2d490-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2d490-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2d490-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="2d490-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2d490-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="2d490-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2d490-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2d490-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2d490-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="2d490-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2d490-157">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="2d490-157">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="2d490-158">[FindItem 操作](finditem-operation.md)期间包含单个根文件夹的搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="2d490-158">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d490-159">父元素</span><span class="sxs-lookup"><span data-stu-id="2d490-159">Parent elements</span></span>

|<span data-ttu-id="2d490-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d490-160">**Element**</span></span>|<span data-ttu-id="2d490-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d490-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d490-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2d490-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2d490-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2d490-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d490-164">注解</span><span class="sxs-lookup"><span data-stu-id="2d490-164">Remarks</span></span>

<span data-ttu-id="2d490-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d490-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d490-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d490-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d490-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d490-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d490-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d490-168">Schema name</span></span>  <br/> |<span data-ttu-id="2d490-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="2d490-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d490-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d490-170">Validation file</span></span>  <br/> |<span data-ttu-id="2d490-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d490-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d490-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d490-172">Can be empty</span></span>  <br/> |<span data-ttu-id="2d490-173">False</span><span class="sxs-lookup"><span data-stu-id="2d490-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d490-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d490-174">See also</span></span>

- [<span data-ttu-id="2d490-175">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="2d490-175">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="2d490-176">查找项目</span><span class="sxs-lookup"><span data-stu-id="2d490-176">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

