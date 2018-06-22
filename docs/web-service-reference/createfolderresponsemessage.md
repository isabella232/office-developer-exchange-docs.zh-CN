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
description: CreateFolderResponseMessage 元素包含状态和单个 CreateFolder 操作请求的结果。
ms.openlocfilehash: c587cca1f935b295a0ed30ab2210de40af28d06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753652"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="14d0f-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="14d0f-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="14d0f-104">**CreateFolderResponseMessage**元素包含状态和的单个结果[CreateFolder 操作](createfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="14d0f-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="14d0f-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="14d0f-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="14d0f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-106">Attributes and elements</span></span>

<span data-ttu-id="14d0f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14d0f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14d0f-108">属性</span><span class="sxs-lookup"><span data-stu-id="14d0f-108">Attributes</span></span>

|<span data-ttu-id="14d0f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="14d0f-109">**Attribute**</span></span>|<span data-ttu-id="14d0f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="14d0f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14d0f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="14d0f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="14d0f-112">描述[CreateFolder 操作](createfolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="14d0f-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="14d0f-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="14d0f-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="14d0f-114">-成功</span><span class="sxs-lookup"><span data-stu-id="14d0f-114">-  Success</span></span>  <br/><span data-ttu-id="14d0f-115">-警告</span><span class="sxs-lookup"><span data-stu-id="14d0f-115">-  Warning</span></span>  <br/><span data-ttu-id="14d0f-116">-错误</span><span class="sxs-lookup"><span data-stu-id="14d0f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="14d0f-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="14d0f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="14d0f-118">**值**</span><span class="sxs-lookup"><span data-stu-id="14d0f-118">**Value**</span></span>|<span data-ttu-id="14d0f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="14d0f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14d0f-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="14d0f-120">**Success**</span></span> <br/> |<span data-ttu-id="14d0f-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="14d0f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="14d0f-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="14d0f-122">**Warning**</span></span> <br/> | <span data-ttu-id="14d0f-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="14d0f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="14d0f-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="14d0f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="14d0f-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="14d0f-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="14d0f-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="14d0f-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="14d0f-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="14d0f-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="14d0f-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="14d0f-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="14d0f-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="14d0f-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="14d0f-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="14d0f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="14d0f-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="14d0f-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="14d0f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="14d0f-132">**Error**</span></span> <br/> | <span data-ttu-id="14d0f-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="14d0f-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="14d0f-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="14d0f-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="14d0f-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="14d0f-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="14d0f-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="14d0f-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="14d0f-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="14d0f-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="14d0f-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="14d0f-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="14d0f-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="14d0f-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="14d0f-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="14d0f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="14d0f-142">子元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-142">Child elements</span></span>

|<span data-ttu-id="14d0f-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="14d0f-143">**Element**</span></span>|<span data-ttu-id="14d0f-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="14d0f-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14d0f-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="14d0f-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="14d0f-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="14d0f-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="14d0f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="14d0f-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="14d0f-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="14d0f-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="14d0f-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="14d0f-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="14d0f-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="14d0f-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="14d0f-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="14d0f-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="14d0f-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="14d0f-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="14d0f-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="14d0f-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="14d0f-154">Folders</span><span class="sxs-lookup"><span data-stu-id="14d0f-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="14d0f-155">包含数组的创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="14d0f-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="14d0f-156">父元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-156">Parent elements</span></span>

|<span data-ttu-id="14d0f-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="14d0f-157">**Element**</span></span>|<span data-ttu-id="14d0f-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="14d0f-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14d0f-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="14d0f-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="14d0f-160">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="14d0f-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14d0f-161">备注</span><span class="sxs-lookup"><span data-stu-id="14d0f-161">Remarks</span></span>

<span data-ttu-id="14d0f-162">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14d0f-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14d0f-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="14d0f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14d0f-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="14d0f-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="14d0f-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="14d0f-165">Schema Name</span></span>  <br/> |<span data-ttu-id="14d0f-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="14d0f-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="14d0f-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="14d0f-167">Validation File</span></span>  <br/> |<span data-ttu-id="14d0f-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="14d0f-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14d0f-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="14d0f-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="14d0f-170">False</span><span class="sxs-lookup"><span data-stu-id="14d0f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14d0f-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14d0f-171">See also</span></span>

- [<span data-ttu-id="14d0f-172">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="14d0f-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="14d0f-173">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="14d0f-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="14d0f-174">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="14d0f-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

