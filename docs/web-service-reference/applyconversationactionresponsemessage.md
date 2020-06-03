---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: ApplyConversationActionResponseMessage 元素包含 ApplyConversationAction 操作请求的状态和结果。
ms.openlocfilehash: 377aee12d8cc7d6b4aff8d6fc2a6cb67b3bcd10b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464691"
---
# <a name="applyconversationactionresponsemessage"></a><span data-ttu-id="192d6-103">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="192d6-103">ApplyConversationActionResponseMessage</span></span>

<span data-ttu-id="192d6-104">**ApplyConversationActionResponseMessage**元素包含[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="192d6-104">The **ApplyConversationActionResponseMessage** element contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.</span></span>  
  
- [<span data-ttu-id="192d6-105">ApplyConversationActionResponse</span><span class="sxs-lookup"><span data-stu-id="192d6-105">ApplyConversationActionResponse</span></span>](applyconversationactionresponse.md)
- [<span data-ttu-id="192d6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="192d6-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="192d6-107">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="192d6-107">ApplyConversationActionResponseMessage</span></span>](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 <span data-ttu-id="192d6-108">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="192d6-108">**ApplyConversationActionResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="192d6-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="192d6-109">Attributes and elements</span></span>

<span data-ttu-id="192d6-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="192d6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="192d6-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="192d6-111">Attributes</span></span>

|<span data-ttu-id="192d6-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="192d6-112">**Attribute**</span></span>|<span data-ttu-id="192d6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="192d6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="192d6-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="192d6-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="192d6-115">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="192d6-115">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="192d6-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="192d6-116">The following values are valid for this attribute:</span></span><ul><li><span data-ttu-id="192d6-117">成功</span><span class="sxs-lookup"><span data-stu-id="192d6-117">Success</span></span></li><li><span data-ttu-id="192d6-118">警告</span><span class="sxs-lookup"><span data-stu-id="192d6-118">Warning</span></span></li><li><span data-ttu-id="192d6-119">错误</span><span class="sxs-lookup"><span data-stu-id="192d6-119">Error</span></span></li></ul> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="192d6-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="192d6-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="192d6-121">**值**</span><span class="sxs-lookup"><span data-stu-id="192d6-121">**Value**</span></span>|<span data-ttu-id="192d6-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="192d6-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="192d6-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="192d6-123">**Success**</span></span> <br/> |<span data-ttu-id="192d6-124">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="192d6-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="192d6-125">**警告**</span><span class="sxs-lookup"><span data-stu-id="192d6-125">**Warning**</span></span> <br/> | <span data-ttu-id="192d6-126">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="192d6-126">Describes a request that was not processed.</span></span> <span data-ttu-id="192d6-127">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="192d6-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="192d6-128">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="192d6-128">The following are examples of sources of warnings:</span></span><ul><li><span data-ttu-id="192d6-129">在批处理过程中，Exchange 存储处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="192d6-129">The Exchange store is offline during the batch.</span></span></li><li><span data-ttu-id="192d6-130">Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="192d6-130">Active Directory Domain Services (AD DS) is offline.</span></span></li><li><span data-ttu-id="192d6-131">邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="192d6-131">Mailboxes were moved.</span></span></li><li><span data-ttu-id="192d6-132">邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="192d6-132">The message database (MDB) is offline.</span></span></li><li><span data-ttu-id="192d6-133">密码已过期。</span><span class="sxs-lookup"><span data-stu-id="192d6-133">A password is expired.</span></span></li><li><span data-ttu-id="192d6-134">已超出配额。</span><span class="sxs-lookup"><span data-stu-id="192d6-134">A quota has been exceeded.</span></span></li></ul> |
|<span data-ttu-id="192d6-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="192d6-135">**Error**</span></span> <br/> | <span data-ttu-id="192d6-136">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="192d6-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="192d6-137">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="192d6-137">The following are examples of sources of errors:</span></span>  <ul><li><span data-ttu-id="192d6-138">无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="192d6-138">Invalid attributes or elements</span></span></li><li><span data-ttu-id="192d6-139">超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="192d6-139">Attributes or elements that are out of range</span></span></li><li><span data-ttu-id="192d6-140">未知标记</span><span class="sxs-lookup"><span data-stu-id="192d6-140">An unknown tag</span></span>  </li><li><span data-ttu-id="192d6-141">上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="192d6-141">An attribute or element that is not valid in the context</span></span></li><li><span data-ttu-id="192d6-142">任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="192d6-142">An unauthorized access attempt by any client</span></span></li><li><span data-ttu-id="192d6-143">响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="192d6-143">A server-side failure in response to a valid client-side call</span></span></li></ul><span data-ttu-id="192d6-144">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="192d6-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="192d6-145">子元素</span><span class="sxs-lookup"><span data-stu-id="192d6-145">Child elements</span></span>

|<span data-ttu-id="192d6-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="192d6-146">**Element**</span></span>|<span data-ttu-id="192d6-147">**描述**</span><span class="sxs-lookup"><span data-stu-id="192d6-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="192d6-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="192d6-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="192d6-149">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="192d6-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="192d6-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="192d6-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="192d6-151">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="192d6-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="192d6-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="192d6-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="192d6-153">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="192d6-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="192d6-154">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="192d6-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="192d6-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="192d6-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="192d6-156">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="192d6-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="192d6-157">父元素</span><span class="sxs-lookup"><span data-stu-id="192d6-157">Parent elements</span></span>

|<span data-ttu-id="192d6-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="192d6-158">**Element**</span></span>|<span data-ttu-id="192d6-159">**描述**</span><span class="sxs-lookup"><span data-stu-id="192d6-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="192d6-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="192d6-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="192d6-161">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="192d6-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="192d6-162">文本值</span><span class="sxs-lookup"><span data-stu-id="192d6-162">Text value</span></span>

<span data-ttu-id="192d6-163">无。</span><span class="sxs-lookup"><span data-stu-id="192d6-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="192d6-164">说明</span><span class="sxs-lookup"><span data-stu-id="192d6-164">Remarks</span></span>

<span data-ttu-id="192d6-165">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="192d6-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="192d6-166">版本差异</span><span class="sxs-lookup"><span data-stu-id="192d6-166">Version differences</span></span>

<span data-ttu-id="192d6-167">在从 build 15.00.0986.00 开始的 Exchange 版本中， **ApplyConversationActionResponseMessage**元素的类型为**ApplyConversationActionResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="192d6-167">In versions of Exchange starting with build 15.00.0986.00, the **ApplyConversationActionResponseMessage** element is of type **ApplyConversationActionResponseMessageType**.</span></span> <span data-ttu-id="192d6-168">在以前的版本中，元素的类型为**ResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="192d6-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="192d6-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="192d6-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="192d6-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="192d6-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="192d6-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="192d6-171">Schema Name</span></span>  <br/> |<span data-ttu-id="192d6-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="192d6-172">Message schema</span></span>  <br/> |
|<span data-ttu-id="192d6-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="192d6-173">Validation File</span></span>  <br/> |<span data-ttu-id="192d6-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="192d6-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="192d6-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="192d6-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="192d6-176">False</span><span class="sxs-lookup"><span data-stu-id="192d6-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="192d6-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="192d6-177">See also</span></span>

- [<span data-ttu-id="192d6-178">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="192d6-178">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="192d6-179">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="192d6-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

