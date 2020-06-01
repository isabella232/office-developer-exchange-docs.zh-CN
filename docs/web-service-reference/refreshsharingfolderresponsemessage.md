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
description: RefreshSharingFolderResponseMessage 元素包含单个 RefreshSharingFolder 操作请求的状态和结果。
ms.openlocfilehash: f2cc357298d523b418d2c45598639627c5a63252
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468668"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="0408b-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0408b-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="0408b-104">**RefreshSharingFolderResponseMessage**元素包含单个[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="0408b-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="0408b-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0408b-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0408b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0408b-106">Attributes and elements</span></span>

<span data-ttu-id="0408b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0408b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0408b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0408b-108">Attributes</span></span>

|<span data-ttu-id="0408b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0408b-109">**Attribute**</span></span>|<span data-ttu-id="0408b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0408b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0408b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0408b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0408b-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="0408b-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="0408b-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="0408b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0408b-114">-成功</span><span class="sxs-lookup"><span data-stu-id="0408b-114">-  Success</span></span>  <br/><span data-ttu-id="0408b-115">-警告</span><span class="sxs-lookup"><span data-stu-id="0408b-115">-  Warning</span></span>  <br/><span data-ttu-id="0408b-116">-错误</span><span class="sxs-lookup"><span data-stu-id="0408b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="0408b-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="0408b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="0408b-118">**值**</span><span class="sxs-lookup"><span data-stu-id="0408b-118">**Value**</span></span>|<span data-ttu-id="0408b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0408b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0408b-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="0408b-120">**Success**</span></span> <br/> |<span data-ttu-id="0408b-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="0408b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0408b-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="0408b-122">**Warning**</span></span> <br/> | <span data-ttu-id="0408b-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="0408b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="0408b-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="0408b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0408b-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="0408b-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="0408b-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0408b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0408b-127">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="0408b-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="0408b-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="0408b-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="0408b-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0408b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0408b-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="0408b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="0408b-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="0408b-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="0408b-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="0408b-132">**Error**</span></span> <br/> | <span data-ttu-id="0408b-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="0408b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="0408b-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="0408b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0408b-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="0408b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0408b-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="0408b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0408b-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="0408b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="0408b-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="0408b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0408b-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="0408b-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="0408b-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="0408b-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="0408b-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="0408b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0408b-142">子元素</span><span class="sxs-lookup"><span data-stu-id="0408b-142">Child elements</span></span>

|<span data-ttu-id="0408b-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="0408b-143">**Element**</span></span>|<span data-ttu-id="0408b-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="0408b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0408b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="0408b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0408b-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0408b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0408b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0408b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0408b-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0408b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0408b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0408b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0408b-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0408b-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="0408b-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="0408b-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0408b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0408b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0408b-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0408b-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0408b-154">父元素</span><span class="sxs-lookup"><span data-stu-id="0408b-154">Parent elements</span></span>

|<span data-ttu-id="0408b-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="0408b-155">**Element**</span></span>|<span data-ttu-id="0408b-156">**描述**</span><span class="sxs-lookup"><span data-stu-id="0408b-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0408b-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0408b-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0408b-158">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0408b-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0408b-159">说明</span><span class="sxs-lookup"><span data-stu-id="0408b-159">Remarks</span></span>

<span data-ttu-id="0408b-160">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="0408b-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0408b-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="0408b-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0408b-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="0408b-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0408b-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="0408b-163">Schema Name</span></span>  <br/> |<span data-ttu-id="0408b-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="0408b-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0408b-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="0408b-165">Validation File</span></span>  <br/> |<span data-ttu-id="0408b-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0408b-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0408b-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="0408b-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="0408b-168">False</span><span class="sxs-lookup"><span data-stu-id="0408b-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0408b-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0408b-169">See also</span></span>

- [<span data-ttu-id="0408b-170">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0408b-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="0408b-171">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0408b-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

