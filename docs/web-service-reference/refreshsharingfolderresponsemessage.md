---
title: RefreshSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponseMessage
api_type:
- schema
ms.assetid: 53ee65bd-cf75-4e04-9b27-eff1b040ae82
description: RefreshSharingFolderResponseMessage 元素包含状态和单个 RefreshSharingFolder 操作请求的结果。
ms.openlocfilehash: 9dbb66c294439f33a9307d51c03dd1cd127e95e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827052"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="c6c9c-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c6c9c-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="c6c9c-104">**RefreshSharingFolderResponseMessage**元素包含状态和的单个结果[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="c6c9c-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6c9c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-106">Attributes and elements</span></span>

<span data-ttu-id="c6c9c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6c9c-108">属性</span><span class="sxs-lookup"><span data-stu-id="c6c9c-108">Attributes</span></span>

|<span data-ttu-id="c6c9c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-109">**Attribute**</span></span>|<span data-ttu-id="c6c9c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6c9c-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c6c9c-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="c6c9c-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="c6c9c-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="c6c9c-114">-成功</span><span class="sxs-lookup"><span data-stu-id="c6c9c-114">-  Success</span></span>  <br/><span data-ttu-id="c6c9c-115">-警告</span><span class="sxs-lookup"><span data-stu-id="c6c9c-115">-  Warning</span></span>  <br/><span data-ttu-id="c6c9c-116">-错误</span><span class="sxs-lookup"><span data-stu-id="c6c9c-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c6c9c-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="c6c9c-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="c6c9c-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-118">**Value**</span></span>|<span data-ttu-id="c6c9c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6c9c-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-120">**Success**</span></span> <br/> |<span data-ttu-id="c6c9c-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c6c9c-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-122">**Warning**</span></span> <br/> | <span data-ttu-id="c6c9c-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c6c9c-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c6c9c-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="c6c9c-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="c6c9c-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c6c9c-127">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="c6c9c-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="c6c9c-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c6c9c-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c6c9c-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="c6c9c-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-132">**Error**</span></span> <br/> | <span data-ttu-id="c6c9c-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="c6c9c-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="c6c9c-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c6c9c-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c6c9c-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="c6c9c-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c6c9c-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="c6c9c-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="c6c9c-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="c6c9c-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="c6c9c-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c6c9c-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="c6c9c-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="c6c9c-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6c9c-142">子元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-142">Child elements</span></span>

|<span data-ttu-id="c6c9c-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-143">**Element**</span></span>|<span data-ttu-id="c6c9c-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6c9c-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c6c9c-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c6c9c-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c6c9c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c6c9c-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c6c9c-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c6c9c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c6c9c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c6c9c-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="c6c9c-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c6c9c-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c6c9c-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c6c9c-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6c9c-154">父元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-154">Parent elements</span></span>

|<span data-ttu-id="c6c9c-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-155">**Element**</span></span>|<span data-ttu-id="c6c9c-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6c9c-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6c9c-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c6c9c-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c6c9c-158">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6c9c-159">备注</span><span class="sxs-lookup"><span data-stu-id="c6c9c-159">Remarks</span></span>

<span data-ttu-id="c6c9c-160">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="c6c9c-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6c9c-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6c9c-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6c9c-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6c9c-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6c9c-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6c9c-163">Schema Name</span></span>  <br/> |<span data-ttu-id="c6c9c-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="c6c9c-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c6c9c-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6c9c-165">Validation File</span></span>  <br/> |<span data-ttu-id="c6c9c-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c6c9c-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6c9c-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6c9c-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6c9c-168">False</span><span class="sxs-lookup"><span data-stu-id="c6c9c-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6c9c-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6c9c-169">See also</span></span>

- [<span data-ttu-id="c6c9c-170">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="c6c9c-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="c6c9c-171">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6c9c-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

