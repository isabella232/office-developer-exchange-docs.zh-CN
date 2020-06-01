---
title: CreateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolderResponseMessage
api_type:
- schema
ms.assetid: 1301dd15-b008-4fd9-8c89-b15a20b186e2
description: CreateFolderResponseMessage 元素包含单个 CreateFolder 操作请求的状态和结果。
ms.openlocfilehash: 386dd2aa4e114d8382d5c83a3d6da70b1ccbbada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457527"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="05269-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="05269-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="05269-104">**CreateFolderResponseMessage**元素包含单个[CreateFolder 操作](createfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="05269-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="05269-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="05269-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="05269-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="05269-106">Attributes and elements</span></span>

<span data-ttu-id="05269-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05269-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05269-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="05269-108">Attributes</span></span>

|<span data-ttu-id="05269-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="05269-109">**Attribute**</span></span>|<span data-ttu-id="05269-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="05269-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05269-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="05269-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="05269-112">描述[CreateFolder 操作](createfolder-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="05269-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="05269-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="05269-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="05269-114">-成功</span><span class="sxs-lookup"><span data-stu-id="05269-114">-  Success</span></span>  <br/><span data-ttu-id="05269-115">-警告</span><span class="sxs-lookup"><span data-stu-id="05269-115">-  Warning</span></span>  <br/><span data-ttu-id="05269-116">-错误</span><span class="sxs-lookup"><span data-stu-id="05269-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="05269-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="05269-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="05269-118">**值**</span><span class="sxs-lookup"><span data-stu-id="05269-118">**Value**</span></span>|<span data-ttu-id="05269-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="05269-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05269-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="05269-120">**Success**</span></span> <br/> |<span data-ttu-id="05269-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="05269-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="05269-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="05269-122">**Warning**</span></span> <br/> | <span data-ttu-id="05269-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="05269-123">Describes a request that was not processed.</span></span> <span data-ttu-id="05269-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="05269-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="05269-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="05269-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="05269-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="05269-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="05269-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="05269-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="05269-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="05269-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="05269-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="05269-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="05269-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="05269-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="05269-131">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="05269-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="05269-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="05269-132">**Error**</span></span> <br/> | <span data-ttu-id="05269-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="05269-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="05269-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="05269-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="05269-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="05269-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="05269-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="05269-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="05269-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="05269-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="05269-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="05269-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="05269-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="05269-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="05269-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="05269-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="05269-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="05269-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05269-142">子元素</span><span class="sxs-lookup"><span data-stu-id="05269-142">Child elements</span></span>

|<span data-ttu-id="05269-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="05269-143">**Element**</span></span>|<span data-ttu-id="05269-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="05269-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05269-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="05269-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="05269-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="05269-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="05269-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="05269-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="05269-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="05269-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="05269-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="05269-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="05269-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="05269-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="05269-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="05269-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="05269-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="05269-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="05269-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="05269-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="05269-154">Folders</span><span class="sxs-lookup"><span data-stu-id="05269-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="05269-155">包含已创建的文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="05269-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05269-156">父元素</span><span class="sxs-lookup"><span data-stu-id="05269-156">Parent elements</span></span>

|<span data-ttu-id="05269-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="05269-157">**Element**</span></span>|<span data-ttu-id="05269-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="05269-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05269-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="05269-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="05269-160">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="05269-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05269-161">备注</span><span class="sxs-lookup"><span data-stu-id="05269-161">Remarks</span></span>

<span data-ttu-id="05269-162">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="05269-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05269-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="05269-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05269-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="05269-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="05269-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="05269-165">Schema Name</span></span>  <br/> |<span data-ttu-id="05269-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="05269-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="05269-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="05269-167">Validation File</span></span>  <br/> |<span data-ttu-id="05269-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="05269-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05269-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="05269-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="05269-170">False</span><span class="sxs-lookup"><span data-stu-id="05269-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05269-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05269-171">See also</span></span>

- [<span data-ttu-id="05269-172">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="05269-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="05269-173">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="05269-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="05269-174">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="05269-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

