---
title: SyncFolderHierarchyResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponseMessage
api_type:
- schema
ms.assetid: ab96c649-1005-401c-9d1c-9917f0b19a60
description: SyncFolderHierarchyResponseMessage 元素包含状态和单个 SyncFolderHierarchy 操作请求的结果。
ms.openlocfilehash: e4141299b128ffb7f67c55bbb09390b77a79e043
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838173"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="df28b-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="df28b-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="df28b-104">**SyncFolderHierarchyResponseMessage**元素包含状态和的单个结果[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="df28b-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="df28b-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="df28b-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="df28b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="df28b-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="df28b-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="df28b-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
```xml
<SyncFolderHierarchyResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastFolderInRange/>
   <Changes/>
</SyncFolderHierarchyResponseMessage>
```

 <span data-ttu-id="df28b-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="df28b-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df28b-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="df28b-109">Attributes and elements</span></span>

<span data-ttu-id="df28b-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="df28b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df28b-111">属性</span><span class="sxs-lookup"><span data-stu-id="df28b-111">Attributes</span></span>

|<span data-ttu-id="df28b-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="df28b-112">**Attribute**</span></span>|<span data-ttu-id="df28b-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="df28b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df28b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="df28b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="df28b-115">描述[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="df28b-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="df28b-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="df28b-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="df28b-117">-成功</span><span class="sxs-lookup"><span data-stu-id="df28b-117">-  Success</span></span>  <br/><span data-ttu-id="df28b-118">-警告</span><span class="sxs-lookup"><span data-stu-id="df28b-118">-  Warning</span></span>  <br/><span data-ttu-id="df28b-119">-错误</span><span class="sxs-lookup"><span data-stu-id="df28b-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="df28b-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="df28b-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="df28b-121">**值**</span><span class="sxs-lookup"><span data-stu-id="df28b-121">**Value**</span></span>|<span data-ttu-id="df28b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="df28b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df28b-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="df28b-123">**Success**</span></span> <br/> |<span data-ttu-id="df28b-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="df28b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="df28b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="df28b-125">**Warning**</span></span> <br/> | <span data-ttu-id="df28b-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="df28b-126">Describes a request that was not processed.</span></span> <span data-ttu-id="df28b-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="df28b-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="df28b-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="df28b-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="df28b-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="df28b-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="df28b-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="df28b-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="df28b-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="df28b-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="df28b-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="df28b-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="df28b-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="df28b-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="df28b-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="df28b-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="df28b-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="df28b-135">**Error**</span></span> <br/> | <span data-ttu-id="df28b-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="df28b-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="df28b-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="df28b-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="df28b-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="df28b-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="df28b-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="df28b-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="df28b-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="df28b-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="df28b-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="df28b-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="df28b-142">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="df28b-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="df28b-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="df28b-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="df28b-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="df28b-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df28b-145">子元素</span><span class="sxs-lookup"><span data-stu-id="df28b-145">Child elements</span></span>

|<span data-ttu-id="df28b-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="df28b-146">**Element**</span></span>|<span data-ttu-id="df28b-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="df28b-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df28b-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="df28b-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="df28b-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="df28b-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="df28b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="df28b-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="df28b-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="df28b-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="df28b-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="df28b-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="df28b-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="df28b-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="df28b-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="df28b-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="df28b-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="df28b-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="df28b-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="df28b-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="df28b-157">SyncState</span><span class="sxs-lookup"><span data-stu-id="df28b-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="df28b-158">包含 base64 编码的同步数据的每个请求成功后都会更新窗体。</span><span class="sxs-lookup"><span data-stu-id="df28b-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="df28b-159">这用于标识的同步状态。</span><span class="sxs-lookup"><span data-stu-id="df28b-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="df28b-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="df28b-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="df28b-161">指示是否在响应中包含的最后一项进行同步。</span><span class="sxs-lookup"><span data-stu-id="df28b-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="df28b-162">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="df28b-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="df28b-163">包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="df28b-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df28b-164">父元素</span><span class="sxs-lookup"><span data-stu-id="df28b-164">Parent elements</span></span>

|<span data-ttu-id="df28b-165">**元素**</span><span class="sxs-lookup"><span data-stu-id="df28b-165">**Element**</span></span>|<span data-ttu-id="df28b-166">**说明**</span><span class="sxs-lookup"><span data-stu-id="df28b-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df28b-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="df28b-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="df28b-168">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="df28b-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df28b-169">注解</span><span class="sxs-lookup"><span data-stu-id="df28b-169">Remarks</span></span>

<span data-ttu-id="df28b-170">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="df28b-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df28b-171">元素信息</span><span class="sxs-lookup"><span data-stu-id="df28b-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df28b-172">命名空间</span><span class="sxs-lookup"><span data-stu-id="df28b-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="df28b-173">架构名称</span><span class="sxs-lookup"><span data-stu-id="df28b-173">Schema Name</span></span>  <br/> |<span data-ttu-id="df28b-174">消息架构</span><span class="sxs-lookup"><span data-stu-id="df28b-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="df28b-175">验证文件</span><span class="sxs-lookup"><span data-stu-id="df28b-175">Validation File</span></span>  <br/> |<span data-ttu-id="df28b-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="df28b-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="df28b-177">可以为空</span><span class="sxs-lookup"><span data-stu-id="df28b-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="df28b-178">False</span><span class="sxs-lookup"><span data-stu-id="df28b-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df28b-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df28b-179">See also</span></span>

- [<span data-ttu-id="df28b-180">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="df28b-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="df28b-181">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="df28b-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

