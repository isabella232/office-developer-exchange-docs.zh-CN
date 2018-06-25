---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: SyncFolderItemsResponseMessage 元素包含状态和单个 SyncFolderItems 操作请求的结果。
ms.openlocfilehash: 9bb32232143df56ad9de93480e10a5941e68025a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838180"
---
# <a name="syncfolderitemsresponsemessage"></a><span data-ttu-id="a31a5-103">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a31a5-103">SyncFolderItemsResponseMessage</span></span>

<span data-ttu-id="a31a5-104">**SyncFolderItemsResponseMessage**元素包含状态和的单个结果[SyncFolderItems 操作](syncfolderitems-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a31a5-104">The **SyncFolderItemsResponseMessage** element contains the status and result of a single [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span> 
  
- [<span data-ttu-id="a31a5-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="a31a5-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="a31a5-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a31a5-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="a31a5-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a31a5-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 <span data-ttu-id="a31a5-108">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a31a5-108">**SyncFolderItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a31a5-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-109">Attributes and elements</span></span>

<span data-ttu-id="a31a5-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a31a5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a31a5-111">属性</span><span class="sxs-lookup"><span data-stu-id="a31a5-111">Attributes</span></span>

|<span data-ttu-id="a31a5-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="a31a5-112">**Attribute**</span></span>|<span data-ttu-id="a31a5-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="a31a5-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a31a5-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a31a5-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a31a5-115">描述[SyncFolderItems 操作](syncfolderitems-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="a31a5-115">Describes the status of a [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> <br/><br/><span data-ttu-id="a31a5-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="a31a5-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="a31a5-117">-成功</span><span class="sxs-lookup"><span data-stu-id="a31a5-117">-  Success</span></span>  <br/><span data-ttu-id="a31a5-118">-警告</span><span class="sxs-lookup"><span data-stu-id="a31a5-118">-  Warning</span></span>  <br/><span data-ttu-id="a31a5-119">-错误</span><span class="sxs-lookup"><span data-stu-id="a31a5-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="a31a5-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="a31a5-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="a31a5-121">**值**</span><span class="sxs-lookup"><span data-stu-id="a31a5-121">**Value**</span></span>|<span data-ttu-id="a31a5-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="a31a5-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a31a5-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="a31a5-123">**Success**</span></span> <br/> |<span data-ttu-id="a31a5-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="a31a5-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a31a5-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="a31a5-125">**Warning**</span></span> <br/> | <span data-ttu-id="a31a5-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="a31a5-126">Describes a request that was not processed.</span></span> <span data-ttu-id="a31a5-127">如果处理请求中的项目时出错，因此无法处理后续项目，可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="a31a5-127">A warning may be returned if an error occurred while processing an item in the request and subsequent items cannot be processed.</span></span> <br/><br/><span data-ttu-id="a31a5-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="a31a5-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="a31a5-129">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="a31a5-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="a31a5-130">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="a31a5-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="a31a5-131">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="a31a5-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="a31a5-132">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="a31a5-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="a31a5-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="a31a5-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="a31a5-134">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="a31a5-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="a31a5-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="a31a5-135">**Error**</span></span> <br/> | <span data-ttu-id="a31a5-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="a31a5-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="a31a5-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="a31a5-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a31a5-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a31a5-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="a31a5-140">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="a31a5-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="a31a5-141">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="a31a5-142">-任何未经授权的访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="a31a5-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a31a5-143">的有效的客户端的呼叫的响应中任何服务器端故障</span><span class="sxs-lookup"><span data-stu-id="a31a5-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="a31a5-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="a31a5-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a31a5-145">子元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-145">Child elements</span></span>

|<span data-ttu-id="a31a5-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="a31a5-146">**Element**</span></span>|<span data-ttu-id="a31a5-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="a31a5-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a31a5-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="a31a5-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a31a5-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="a31a5-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a31a5-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a31a5-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a31a5-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a31a5-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a31a5-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="a31a5-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="a31a5-154">它包含 0 的值。</span><span class="sxs-lookup"><span data-stu-id="a31a5-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a31a5-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a31a5-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="a31a5-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-157">SyncState</span><span class="sxs-lookup"><span data-stu-id="a31a5-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a31a5-158">包含 base64 编码的同步数据的每个请求成功后都会更新窗体。</span><span class="sxs-lookup"><span data-stu-id="a31a5-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="a31a5-159">这用于标识的同步状态。</span><span class="sxs-lookup"><span data-stu-id="a31a5-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-160">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="a31a5-160">IncludesLastItemInRange</span></span>](includeslastiteminrange.md) <br/> |<span data-ttu-id="a31a5-161">指示是否在响应中包含的最后一项进行同步。</span><span class="sxs-lookup"><span data-stu-id="a31a5-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="a31a5-162">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="a31a5-162">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="a31a5-163">包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="a31a5-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a31a5-164">父元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-164">Parent elements</span></span>

|<span data-ttu-id="a31a5-165">**元素**</span><span class="sxs-lookup"><span data-stu-id="a31a5-165">**Element**</span></span>|<span data-ttu-id="a31a5-166">**说明**</span><span class="sxs-lookup"><span data-stu-id="a31a5-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a31a5-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a31a5-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a31a5-168">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="a31a5-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a31a5-169">备注</span><span class="sxs-lookup"><span data-stu-id="a31a5-169">Remarks</span></span>

<span data-ttu-id="a31a5-170">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a31a5-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a31a5-171">元素信息</span><span class="sxs-lookup"><span data-stu-id="a31a5-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a31a5-172">命名空间</span><span class="sxs-lookup"><span data-stu-id="a31a5-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a31a5-173">架构名称</span><span class="sxs-lookup"><span data-stu-id="a31a5-173">Schema Name</span></span>  <br/> |<span data-ttu-id="a31a5-174">消息架构</span><span class="sxs-lookup"><span data-stu-id="a31a5-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a31a5-175">验证文件</span><span class="sxs-lookup"><span data-stu-id="a31a5-175">Validation File</span></span>  <br/> |<span data-ttu-id="a31a5-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a31a5-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a31a5-177">可以为空</span><span class="sxs-lookup"><span data-stu-id="a31a5-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="a31a5-178">False</span><span class="sxs-lookup"><span data-stu-id="a31a5-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a31a5-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a31a5-179">See also</span></span>

- [<span data-ttu-id="a31a5-180">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="a31a5-180">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="a31a5-181">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a31a5-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

