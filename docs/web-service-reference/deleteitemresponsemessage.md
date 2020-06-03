---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: DeleteItemResponseMessage 元素包含单个 DeleteItem 操作请求的状态和结果。
ms.openlocfilehash: 78e3efc6a9e9e6629d7efe7f2dc294e0a731005a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526926"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="e70df-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e70df-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="e70df-104">**DeleteItemResponseMessage**元素包含单个[DeleteItem 操作](deleteitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e70df-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="e70df-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="e70df-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="e70df-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e70df-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="e70df-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e70df-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="e70df-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e70df-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e70df-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e70df-109">Attributes and elements</span></span>

<span data-ttu-id="e70df-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e70df-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e70df-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="e70df-111">Attributes</span></span>

|<span data-ttu-id="e70df-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="e70df-112">**Attribute**</span></span>|<span data-ttu-id="e70df-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="e70df-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e70df-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e70df-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e70df-115">描述[DeleteItem 操作](deleteitem-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="e70df-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="e70df-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="e70df-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="e70df-117">-成功</span><span class="sxs-lookup"><span data-stu-id="e70df-117">- Success</span></span>  <br/><span data-ttu-id="e70df-118">-警告</span><span class="sxs-lookup"><span data-stu-id="e70df-118">-  Warning</span></span>  <br/><span data-ttu-id="e70df-119">-错误</span><span class="sxs-lookup"><span data-stu-id="e70df-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="e70df-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="e70df-120">ResponseClass attribute</span></span>

|<span data-ttu-id="e70df-121">**值**</span><span class="sxs-lookup"><span data-stu-id="e70df-121">**Value**</span></span>|<span data-ttu-id="e70df-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="e70df-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e70df-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="e70df-123">**Success**</span></span> <br/> |<span data-ttu-id="e70df-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="e70df-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e70df-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="e70df-125">**Warning**</span></span> <br/> | <span data-ttu-id="e70df-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="e70df-126">Describes a request that was not processed.</span></span> <span data-ttu-id="e70df-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="e70df-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="e70df-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="e70df-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="e70df-129">-Exchange 存储在批处理过程中脱机。</span><span class="sxs-lookup"><span data-stu-id="e70df-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="e70df-130">-Active Directory 域服务（AD DS）脱机。</span><span class="sxs-lookup"><span data-stu-id="e70df-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="e70df-131">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="e70df-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="e70df-132">-邮件数据库（MDB）脱机。</span><span class="sxs-lookup"><span data-stu-id="e70df-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="e70df-133">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="e70df-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="e70df-134">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="e70df-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="e70df-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="e70df-135">**Error**</span></span> <br/> | <span data-ttu-id="e70df-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="e70df-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="e70df-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="e70df-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="e70df-138">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="e70df-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e70df-139">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="e70df-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="e70df-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="e70df-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="e70df-141">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="e70df-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="e70df-142">-客户端尝试将错误日志记录级别设置为管理员允许的最高级别以上</span><span class="sxs-lookup"><span data-stu-id="e70df-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="e70df-143">-客户端尝试将严重级别故障级别设置为低于管理员指定的默认级别</span><span class="sxs-lookup"><span data-stu-id="e70df-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="e70df-144">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="e70df-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e70df-145">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="e70df-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="e70df-146">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="e70df-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e70df-147">子元素</span><span class="sxs-lookup"><span data-stu-id="e70df-147">Child elements</span></span>

|<span data-ttu-id="e70df-148">**元素**</span><span class="sxs-lookup"><span data-stu-id="e70df-148">**Element**</span></span>|<span data-ttu-id="e70df-149">**描述**</span><span class="sxs-lookup"><span data-stu-id="e70df-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e70df-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="e70df-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e70df-151">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e70df-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e70df-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e70df-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e70df-153">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e70df-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e70df-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e70df-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e70df-155">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e70df-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="e70df-156">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="e70df-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e70df-157">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e70df-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e70df-158">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e70df-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e70df-159">父元素</span><span class="sxs-lookup"><span data-stu-id="e70df-159">Parent elements</span></span>

|<span data-ttu-id="e70df-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="e70df-160">**Element**</span></span>|<span data-ttu-id="e70df-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="e70df-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e70df-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e70df-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e70df-163">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e70df-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e70df-164">备注</span><span class="sxs-lookup"><span data-stu-id="e70df-164">Remarks</span></span>

<span data-ttu-id="e70df-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e70df-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="e70df-166">版本差异</span><span class="sxs-lookup"><span data-stu-id="e70df-166">Version differences</span></span>

<span data-ttu-id="e70df-167">在从 build 15.00.0986.00 开始的 Exchange 版本中， **DeleteItemResponseMessage**元素的类型为**DeleteItemResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="e70df-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="e70df-168">在以前的版本中，元素的类型为**ResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="e70df-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e70df-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="e70df-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e70df-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="e70df-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e70df-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="e70df-171">Schema Name</span></span>  <br/> |<span data-ttu-id="e70df-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="e70df-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e70df-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="e70df-173">Validation File</span></span>  <br/> |<span data-ttu-id="e70df-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e70df-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e70df-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="e70df-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="e70df-176">False</span><span class="sxs-lookup"><span data-stu-id="e70df-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e70df-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e70df-177">See also</span></span>

- [<span data-ttu-id="e70df-178">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="e70df-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="e70df-179">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="e70df-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="e70df-180">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e70df-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e70df-181">删除项目（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="e70df-181">Deleting Items (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

