---
title: RefreshSharingFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponse
api_type:
- schema
ms.assetid: 951ab681-f2d5-4f10-933e-ff199685ff8e
description: RefreshSharingFolderResponse 元素定义 RefreshSharingFolder 操作请求的响应。
ms.openlocfilehash: 4ef7a63b2153c6106dae988439f499046689c2b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827048"
---
# <a name="refreshsharingfolderresponse"></a><span data-ttu-id="c0845-103">RefreshSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="c0845-103">RefreshSharingFolderResponse</span></span>

<span data-ttu-id="c0845-104">**RefreshSharingFolderResponse**元素定义[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c0845-104">The **RefreshSharingFolderResponse** element defines a response to a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponse>
```

 <span data-ttu-id="c0845-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c0845-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0845-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0845-106">Attributes and elements</span></span>

<span data-ttu-id="c0845-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0845-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0845-108">属性</span><span class="sxs-lookup"><span data-stu-id="c0845-108">Attributes</span></span>

|<span data-ttu-id="c0845-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c0845-109">**Attribute**</span></span>|<span data-ttu-id="c0845-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0845-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0845-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c0845-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c0845-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="c0845-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="c0845-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="c0845-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="c0845-114">-成功</span><span class="sxs-lookup"><span data-stu-id="c0845-114">-  Success</span></span>  <br/><span data-ttu-id="c0845-115">-警告</span><span class="sxs-lookup"><span data-stu-id="c0845-115">-  Warning</span></span>  <br/><span data-ttu-id="c0845-116">-错误</span><span class="sxs-lookup"><span data-stu-id="c0845-116">-  Error</span></span>  <br/>- |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c0845-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="c0845-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="c0845-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c0845-118">**Value**</span></span>|<span data-ttu-id="c0845-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0845-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0845-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="c0845-120">**Success**</span></span> <br/> |<span data-ttu-id="c0845-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="c0845-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c0845-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="c0845-122">**Warning**</span></span> <br/> | <span data-ttu-id="c0845-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="c0845-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c0845-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="c0845-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="c0845-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="c0845-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="c0845-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c0845-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c0845-127">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c0845-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="c0845-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="c0845-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="c0845-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="c0845-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c0845-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="c0845-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c0845-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="c0845-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="c0845-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c0845-132">**Error**</span></span> <br/> | <span data-ttu-id="c0845-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="c0845-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="c0845-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="c0845-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c0845-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="c0845-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c0845-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="c0845-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="c0845-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="c0845-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="c0845-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="c0845-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="c0845-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="c0845-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c0845-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="c0845-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="c0845-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="c0845-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0845-142">子元素</span><span class="sxs-lookup"><span data-stu-id="c0845-142">Child elements</span></span>

|<span data-ttu-id="c0845-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0845-143">**Element**</span></span>|<span data-ttu-id="c0845-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0845-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0845-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c0845-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c0845-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c0845-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c0845-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c0845-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c0845-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="c0845-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c0845-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c0845-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c0845-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c0845-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="c0845-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="c0845-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c0845-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c0845-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c0845-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c0845-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0845-154">父元素</span><span class="sxs-lookup"><span data-stu-id="c0845-154">Parent elements</span></span>

<span data-ttu-id="c0845-155">无。</span><span class="sxs-lookup"><span data-stu-id="c0845-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0845-156">备注</span><span class="sxs-lookup"><span data-stu-id="c0845-156">Remarks</span></span>

<span data-ttu-id="c0845-157">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="c0845-157">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0845-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0845-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0845-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0845-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0845-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0845-160">Schema Name</span></span>  <br/> |<span data-ttu-id="c0845-161">消息架构</span><span class="sxs-lookup"><span data-stu-id="c0845-161">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0845-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0845-162">Validation File</span></span>  <br/> |<span data-ttu-id="c0845-163">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0845-163">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0845-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0845-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0845-165">False</span><span class="sxs-lookup"><span data-stu-id="c0845-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0845-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0845-166">See also</span></span>

- [<span data-ttu-id="c0845-167">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="c0845-167">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="c0845-168">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0845-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

