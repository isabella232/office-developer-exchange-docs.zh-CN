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
description: SyncFolderHierarchyResponseMessage 元素包含单个 SyncFolderHierarchy 操作请求的状态和结果。
ms.openlocfilehash: fda0a37178f89ba0fd5ef860f8b009f335a11391
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465343"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="ca104-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ca104-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="ca104-104">**SyncFolderHierarchyResponseMessage**元素包含单个[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="ca104-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ca104-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="ca104-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="ca104-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ca104-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ca104-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ca104-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
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

 <span data-ttu-id="ca104-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ca104-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca104-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ca104-109">Attributes and elements</span></span>

<span data-ttu-id="ca104-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ca104-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca104-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="ca104-111">Attributes</span></span>

|<span data-ttu-id="ca104-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="ca104-112">**Attribute**</span></span>|<span data-ttu-id="ca104-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca104-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca104-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ca104-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ca104-115">描述[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="ca104-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ca104-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="ca104-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="ca104-117">-成功</span><span class="sxs-lookup"><span data-stu-id="ca104-117">-  Success</span></span>  <br/><span data-ttu-id="ca104-118">-警告</span><span class="sxs-lookup"><span data-stu-id="ca104-118">-  Warning</span></span>  <br/><span data-ttu-id="ca104-119">-错误</span><span class="sxs-lookup"><span data-stu-id="ca104-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ca104-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="ca104-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ca104-121">**值**</span><span class="sxs-lookup"><span data-stu-id="ca104-121">**Value**</span></span>|<span data-ttu-id="ca104-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca104-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca104-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="ca104-123">**Success**</span></span> <br/> |<span data-ttu-id="ca104-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="ca104-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ca104-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="ca104-125">**Warning**</span></span> <br/> | <span data-ttu-id="ca104-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="ca104-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ca104-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="ca104-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ca104-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="ca104-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ca104-129">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ca104-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ca104-130">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ca104-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ca104-131">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="ca104-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ca104-132">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ca104-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ca104-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="ca104-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="ca104-134">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="ca104-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ca104-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="ca104-135">**Error**</span></span> <br/> | <span data-ttu-id="ca104-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="ca104-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ca104-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="ca104-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ca104-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="ca104-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ca104-139">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="ca104-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ca104-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="ca104-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="ca104-141">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="ca104-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ca104-142">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="ca104-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ca104-143">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="ca104-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ca104-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="ca104-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca104-145">子元素</span><span class="sxs-lookup"><span data-stu-id="ca104-145">Child elements</span></span>

|<span data-ttu-id="ca104-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="ca104-146">**Element**</span></span>|<span data-ttu-id="ca104-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="ca104-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca104-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ca104-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ca104-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="ca104-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ca104-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ca104-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ca104-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="ca104-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ca104-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ca104-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ca104-153">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="ca104-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ca104-154">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="ca104-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ca104-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ca104-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ca104-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="ca104-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ca104-157">SyncState</span><span class="sxs-lookup"><span data-stu-id="ca104-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ca104-158">包含在每次成功请求后更新的、base64 编码的格式的同步数据。</span><span class="sxs-lookup"><span data-stu-id="ca104-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="ca104-159">这用于标识同步状态。</span><span class="sxs-lookup"><span data-stu-id="ca104-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="ca104-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="ca104-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="ca104-161">指示是否已在响应中包含要同步的最后一个项目。</span><span class="sxs-lookup"><span data-stu-id="ca104-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="ca104-162">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="ca104-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="ca104-163">包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="ca104-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ca104-164">父元素</span><span class="sxs-lookup"><span data-stu-id="ca104-164">Parent elements</span></span>

|<span data-ttu-id="ca104-165">**元素**</span><span class="sxs-lookup"><span data-stu-id="ca104-165">**Element**</span></span>|<span data-ttu-id="ca104-166">**描述**</span><span class="sxs-lookup"><span data-stu-id="ca104-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca104-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ca104-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ca104-168">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ca104-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca104-169">备注</span><span class="sxs-lookup"><span data-stu-id="ca104-169">Remarks</span></span>

<span data-ttu-id="ca104-170">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ca104-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca104-171">元素信息</span><span class="sxs-lookup"><span data-stu-id="ca104-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca104-172">命名空间</span><span class="sxs-lookup"><span data-stu-id="ca104-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ca104-173">架构名称</span><span class="sxs-lookup"><span data-stu-id="ca104-173">Schema Name</span></span>  <br/> |<span data-ttu-id="ca104-174">消息架构</span><span class="sxs-lookup"><span data-stu-id="ca104-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ca104-175">验证文件</span><span class="sxs-lookup"><span data-stu-id="ca104-175">Validation File</span></span>  <br/> |<span data-ttu-id="ca104-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ca104-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ca104-177">可以为空</span><span class="sxs-lookup"><span data-stu-id="ca104-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca104-178">False</span><span class="sxs-lookup"><span data-stu-id="ca104-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca104-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca104-179">See also</span></span>

- [<span data-ttu-id="ca104-180">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="ca104-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="ca104-181">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ca104-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

