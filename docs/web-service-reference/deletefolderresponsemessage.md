---
title: DeleteFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponseMessage
api_type:
- schema
ms.assetid: de4c63ff-80b2-40c2-bc06-ef0c23beacd4
description: DeleteFolderResponseMessage 元素包含状态和单个 DeleteFolder 操作请求的结果。
ms.openlocfilehash: 5601fe2e48ad002e0fab60d812e7d70c7398f3ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753806"
---
# <a name="deletefolderresponsemessage"></a><span data-ttu-id="fbd9a-103">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fbd9a-103">DeleteFolderResponseMessage</span></span>

<span data-ttu-id="fbd9a-104">**DeleteFolderResponseMessage**元素包含状态和的单个结果[DeleteFolder 操作](deletefolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-104">The **DeleteFolderResponseMessage** element contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="fbd9a-105">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="fbd9a-105">DeleteFolderResponse</span></span>](deletefolderresponse.md)  
- [<span data-ttu-id="fbd9a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fbd9a-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="fbd9a-107">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fbd9a-107">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 <span data-ttu-id="fbd9a-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbd9a-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-109">Attributes and elements</span></span>

<span data-ttu-id="fbd9a-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbd9a-111">属性</span><span class="sxs-lookup"><span data-stu-id="fbd9a-111">Attributes</span></span>

|<span data-ttu-id="fbd9a-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-112">**Attribute**</span></span>|<span data-ttu-id="fbd9a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbd9a-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fbd9a-115">描述[DeleteFolder 操作](deletefolder-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-115">Describes the status of a [DeleteFolder operation](deletefolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="fbd9a-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="fbd9a-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="fbd9a-117">-成功</span><span class="sxs-lookup"><span data-stu-id="fbd9a-117">-  Success</span></span>  <br/><span data-ttu-id="fbd9a-118">-警告</span><span class="sxs-lookup"><span data-stu-id="fbd9a-118">-  Warning</span></span>  <br/><span data-ttu-id="fbd9a-119">-错误</span><span class="sxs-lookup"><span data-stu-id="fbd9a-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="fbd9a-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="fbd9a-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="fbd9a-121">**值**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-121">**Value**</span></span>|<span data-ttu-id="fbd9a-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbd9a-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-123">**Success**</span></span> <br/> |<span data-ttu-id="fbd9a-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fbd9a-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-125">**Warning**</span></span> <br/> | <span data-ttu-id="fbd9a-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-126">Describes a request that was not processed.</span></span> <span data-ttu-id="fbd9a-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="fbd9a-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="fbd9a-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="fbd9a-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-129">- The Exchange store goes offline during the batch.</span></span><br/><span data-ttu-id="fbd9a-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-130">- Active Directory Domain Services (AD DS) goes offline.</span></span><br/><span data-ttu-id="fbd9a-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="fbd9a-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-132">- The message database (MDB) goes offline.</span></span><br/><span data-ttu-id="fbd9a-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-133">- A password is expired.</span></span><br/><span data-ttu-id="fbd9a-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-134">- A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="fbd9a-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-135">**Error**</span></span> <br/> | <span data-ttu-id="fbd9a-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="fbd9a-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="fbd9a-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="fbd9a-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="fbd9a-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="fbd9a-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="fbd9a-140">- Unknown tag</span></span><br/><span data-ttu-id="fbd9a-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="fbd9a-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="fbd9a-142">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="fbd9a-142">- Unauthorized access attempt by any client</span></span><br/><span data-ttu-id="fbd9a-143">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="fbd9a-143">- Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="fbd9a-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbd9a-145">子元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-145">Child elements</span></span>

|<span data-ttu-id="fbd9a-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-146">**Element**</span></span>|<span data-ttu-id="fbd9a-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd9a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="fbd9a-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fbd9a-149">响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fbd9a-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fbd9a-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fbd9a-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="fbd9a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fbd9a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fbd9a-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="fbd9a-154">它包含 0 的值。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fbd9a-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fbd9a-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fbd9a-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbd9a-157">父元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-157">Parent elements</span></span>

|<span data-ttu-id="fbd9a-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-158">**Element**</span></span>|<span data-ttu-id="fbd9a-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd9a-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd9a-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fbd9a-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fbd9a-161">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbd9a-162">注解</span><span class="sxs-lookup"><span data-stu-id="fbd9a-162">Remarks</span></span>

<span data-ttu-id="fbd9a-163">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fbd9a-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbd9a-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="fbd9a-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbd9a-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="fbd9a-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fbd9a-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="fbd9a-166">Schema Name</span></span>  <br/> |<span data-ttu-id="fbd9a-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="fbd9a-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fbd9a-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="fbd9a-168">Validation File</span></span>  <br/> |<span data-ttu-id="fbd9a-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fbd9a-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fbd9a-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="fbd9a-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbd9a-171">False</span><span class="sxs-lookup"><span data-stu-id="fbd9a-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbd9a-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fbd9a-172">See also</span></span>

- [<span data-ttu-id="fbd9a-173">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="fbd9a-173">DeleteFolder operation</span></span>](deletefolder-operation.md)
- [<span data-ttu-id="fbd9a-174">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="fbd9a-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="fbd9a-175">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fbd9a-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="fbd9a-176">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="fbd9a-176">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

