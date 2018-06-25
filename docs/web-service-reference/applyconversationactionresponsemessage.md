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
description: ApplyConversationActionResponseMessage 元素包含状态和 ApplyConversationAction 操作请求的结果。
ms.openlocfilehash: d8c5571cfc9c2ea6aaf09cb26a0e47e4abfc3f40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753240"
---
# <a name="applyconversationactionresponsemessage"></a><span data-ttu-id="0db0d-103">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0db0d-103">ApplyConversationActionResponseMessage</span></span>

<span data-ttu-id="0db0d-104">**ApplyConversationActionResponseMessage**元素包含状态和[ApplyConversationAction 操作](applyconversationaction-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="0db0d-104">The **ApplyConversationActionResponseMessage** element contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.</span></span>  
  
- [<span data-ttu-id="0db0d-105">ApplyConversationActionResponse</span><span class="sxs-lookup"><span data-stu-id="0db0d-105">ApplyConversationActionResponse</span></span>](applyconversationactionresponse.md)
- [<span data-ttu-id="0db0d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0db0d-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="0db0d-107">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0db0d-107">ApplyConversationActionResponseMessage</span></span>](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 <span data-ttu-id="0db0d-108">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0db0d-108">**ApplyConversationActionResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0db0d-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-109">Attributes and elements</span></span>

<span data-ttu-id="0db0d-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0db0d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0db0d-111">属性</span><span class="sxs-lookup"><span data-stu-id="0db0d-111">Attributes</span></span>

|<span data-ttu-id="0db0d-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="0db0d-112">**Attribute**</span></span>|<span data-ttu-id="0db0d-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0db0d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0db0d-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0db0d-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0db0d-115">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="0db0d-115">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="0db0d-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="0db0d-116">The following values are valid for this attribute:</span></span><ul><li><span data-ttu-id="0db0d-117">成功</span><span class="sxs-lookup"><span data-stu-id="0db0d-117">Success</span></span></li><li><span data-ttu-id="0db0d-118">警告</span><span class="sxs-lookup"><span data-stu-id="0db0d-118">Warning</span></span></li><li><span data-ttu-id="0db0d-119">错误</span><span class="sxs-lookup"><span data-stu-id="0db0d-119">Error</span></span></li></ul> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="0db0d-120">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="0db0d-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="0db0d-121">**值**</span><span class="sxs-lookup"><span data-stu-id="0db0d-121">**Value**</span></span>|<span data-ttu-id="0db0d-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="0db0d-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0db0d-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="0db0d-123">**Success**</span></span> <br/> |<span data-ttu-id="0db0d-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="0db0d-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0db0d-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0db0d-125">**Warning**</span></span> <br/> | <span data-ttu-id="0db0d-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="0db0d-126">Describes a request that was not processed.</span></span> <span data-ttu-id="0db0d-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="0db0d-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="0db0d-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="0db0d-128">The following are examples of sources of warnings:</span></span><ul><li><span data-ttu-id="0db0d-129">在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0db0d-129">The Exchange store is offline during the batch.</span></span></li><li><span data-ttu-id="0db0d-130">Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0db0d-130">Active Directory Domain Services (AD DS) is offline.</span></span></li><li><span data-ttu-id="0db0d-131">邮箱移动。</span><span class="sxs-lookup"><span data-stu-id="0db0d-131">Mailboxes were moved.</span></span></li><li><span data-ttu-id="0db0d-132">邮件数据库 (MDB) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="0db0d-132">The message database (MDB) is offline.</span></span></li><li><span data-ttu-id="0db0d-133">密码已过期。</span><span class="sxs-lookup"><span data-stu-id="0db0d-133">A password is expired.</span></span></li><li><span data-ttu-id="0db0d-134">已超出配额。</span><span class="sxs-lookup"><span data-stu-id="0db0d-134">A quota has been exceeded.</span></span></li></ul> |
|<span data-ttu-id="0db0d-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="0db0d-135">**Error**</span></span> <br/> | <span data-ttu-id="0db0d-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="0db0d-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="0db0d-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="0db0d-137">The following are examples of sources of errors:</span></span>  <ul><li><span data-ttu-id="0db0d-138">无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-138">Invalid attributes or elements</span></span></li><li><span data-ttu-id="0db0d-139">超出范围元素或属性</span><span class="sxs-lookup"><span data-stu-id="0db0d-139">Attributes or elements that are out of range</span></span></li><li><span data-ttu-id="0db0d-140">未知的标记</span><span class="sxs-lookup"><span data-stu-id="0db0d-140">An unknown tag</span></span>  </li><li><span data-ttu-id="0db0d-141">属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-141">An attribute or element that is not valid in the context</span></span></li><li><span data-ttu-id="0db0d-142">由任何客户端的未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="0db0d-142">An unauthorized access attempt by any client</span></span></li><li><span data-ttu-id="0db0d-143">服务器端失败响应有效的客户端调用</span><span class="sxs-lookup"><span data-stu-id="0db0d-143">A server-side failure in response to a valid client-side call</span></span></li></ul><span data-ttu-id="0db0d-144">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="0db0d-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0db0d-145">子元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-145">Child elements</span></span>

|<span data-ttu-id="0db0d-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="0db0d-146">**Element**</span></span>|<span data-ttu-id="0db0d-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="0db0d-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0db0d-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="0db0d-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0db0d-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0db0d-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0db0d-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0db0d-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0db0d-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0db0d-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0db0d-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0db0d-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0db0d-153">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0db0d-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="0db0d-154">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="0db0d-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0db0d-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0db0d-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0db0d-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0db0d-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0db0d-157">父元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-157">Parent elements</span></span>

|<span data-ttu-id="0db0d-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="0db0d-158">**Element**</span></span>|<span data-ttu-id="0db0d-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="0db0d-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0db0d-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0db0d-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0db0d-161">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0db0d-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0db0d-162">文本值</span><span class="sxs-lookup"><span data-stu-id="0db0d-162">Text value</span></span>

<span data-ttu-id="0db0d-163">无。</span><span class="sxs-lookup"><span data-stu-id="0db0d-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0db0d-164">备注</span><span class="sxs-lookup"><span data-stu-id="0db0d-164">Remarks</span></span>

<span data-ttu-id="0db0d-165">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0db0d-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="0db0d-166">版本差异</span><span class="sxs-lookup"><span data-stu-id="0db0d-166">Version differences</span></span>

<span data-ttu-id="0db0d-167">在版本的 Exchange 开头生成 15.00.0986.00， **ApplyConversationActionResponseMessage**元素是类型**ApplyConversationActionResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="0db0d-167">In versions of Exchange starting with build 15.00.0986.00, the **ApplyConversationActionResponseMessage** element is of type **ApplyConversationActionResponseMessageType**.</span></span> <span data-ttu-id="0db0d-168">在早期版本，该元素是类型**ResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="0db0d-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0db0d-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="0db0d-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0db0d-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="0db0d-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0db0d-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="0db0d-171">Schema Name</span></span>  <br/> |<span data-ttu-id="0db0d-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="0db0d-172">Message schema</span></span>  <br/> |
|<span data-ttu-id="0db0d-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="0db0d-173">Validation File</span></span>  <br/> |<span data-ttu-id="0db0d-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0db0d-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0db0d-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="0db0d-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="0db0d-176">False</span><span class="sxs-lookup"><span data-stu-id="0db0d-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0db0d-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0db0d-177">See also</span></span>

- [<span data-ttu-id="0db0d-178">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="0db0d-178">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="0db0d-179">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0db0d-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

