---
title: FindConversationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversationResponse
api_type:
- schema
ms.assetid: a689e29d-5f3d-4deb-81ee-8b6cc60f6dea
description: FindConversationResponse 元素定义 FindConversation 操作请求的响应。
ms.openlocfilehash: 5754ea7540fa6daac8cd725386ca213d5bf05c8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754325"
---
# <a name="findconversationresponse"></a><span data-ttu-id="f8f1d-103">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="f8f1d-103">FindConversationResponse</span></span>

<span data-ttu-id="f8f1d-104">**FindConversationResponse**元素定义[FindConversation 操作](findconversation-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-104">The **FindConversationResponse** element defines a response to a [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
[<span data-ttu-id="f8f1d-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="f8f1d-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 <span data-ttu-id="f8f1d-106">**FindConversationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-106">**FindConversationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8f1d-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-107">Attributes and elements</span></span>

<span data-ttu-id="f8f1d-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8f1d-109">属性</span><span class="sxs-lookup"><span data-stu-id="f8f1d-109">Attributes</span></span>

|<span data-ttu-id="f8f1d-110">**属性**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-110">**Attribute**</span></span>|<span data-ttu-id="f8f1d-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8f1d-112">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-112">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f8f1d-113">描述[FindConversation 操作](findconversation-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-113">Describes the status of a [FindConversation operation](findconversation-operation.md) response.</span></span> <br/><br/><span data-ttu-id="f8f1d-114">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="f8f1d-114">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="f8f1d-115">-成功</span><span class="sxs-lookup"><span data-stu-id="f8f1d-115">-  Success</span></span>  <br/><span data-ttu-id="f8f1d-116">-警告</span><span class="sxs-lookup"><span data-stu-id="f8f1d-116">-  Warning</span></span>  <br/><span data-ttu-id="f8f1d-117">-错误</span><span class="sxs-lookup"><span data-stu-id="f8f1d-117">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f8f1d-118">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="f8f1d-118">ResponseClass attribute values</span></span>

|<span data-ttu-id="f8f1d-119">**值**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-119">**Value**</span></span>|<span data-ttu-id="f8f1d-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8f1d-121">**成功**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-121">**Success**</span></span> <br/> |<span data-ttu-id="f8f1d-122">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-122">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f8f1d-123">**Warning**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-123">**Warning**</span></span> <br/> | <span data-ttu-id="f8f1d-124">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-124">Describes a request that was not processed.</span></span> <span data-ttu-id="f8f1d-125">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-125">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="f8f1d-126">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="f8f1d-126">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="f8f1d-127">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-127">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="f8f1d-128">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-128">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="f8f1d-129">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-129">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="f8f1d-130">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-130">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="f8f1d-131">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-131">-  A password is expired.</span></span>  <br/><span data-ttu-id="f8f1d-132">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-132">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="f8f1d-133">**Error**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-133">**Error**</span></span> <br/> | <span data-ttu-id="f8f1d-134">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-134">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="f8f1d-135">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="f8f1d-135">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f8f1d-136">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-136">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f8f1d-137">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-137">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="f8f1d-138">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="f8f1d-138">-  An unknown tag</span></span>  <br/><span data-ttu-id="f8f1d-139">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-139">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="f8f1d-140">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="f8f1d-140">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f8f1d-141">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="f8f1d-141">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="f8f1d-142">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-142">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8f1d-143">子元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-143">Child elements</span></span>

|<span data-ttu-id="f8f1d-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-144">**Element**</span></span>|<span data-ttu-id="f8f1d-145">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8f1d-146">Conversations</span><span class="sxs-lookup"><span data-stu-id="f8f1d-146">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f8f1d-147">包含数组的对话。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-147">Contains an array of conversations.</span></span>  <br/> |
|[<span data-ttu-id="f8f1d-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f8f1d-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f8f1d-149">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f8f1d-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f8f1d-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f8f1d-151">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f8f1d-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f8f1d-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f8f1d-153">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f8f1d-154">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f8f1d-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f8f1d-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f8f1d-156">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8f1d-157">父元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-157">Parent elements</span></span>

<span data-ttu-id="f8f1d-158">无。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-158">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f8f1d-159">文本值</span><span class="sxs-lookup"><span data-stu-id="f8f1d-159">Text value</span></span>

<span data-ttu-id="f8f1d-160">无。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8f1d-161">备注</span><span class="sxs-lookup"><span data-stu-id="f8f1d-161">Remarks</span></span>

<span data-ttu-id="f8f1d-162">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f8f1d-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8f1d-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="f8f1d-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8f1d-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="f8f1d-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f8f1d-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="f8f1d-165">Schema name</span></span>  <br/> |<span data-ttu-id="f8f1d-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="f8f1d-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f8f1d-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="f8f1d-167">Validation file</span></span>  <br/> |<span data-ttu-id="f8f1d-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f8f1d-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f8f1d-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="f8f1d-169">Can be empty</span></span>  <br/> |<span data-ttu-id="f8f1d-170">False</span><span class="sxs-lookup"><span data-stu-id="f8f1d-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8f1d-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8f1d-171">See also</span></span>

- [<span data-ttu-id="f8f1d-172">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="f8f1d-172">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="f8f1d-173">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f8f1d-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="f8f1d-174">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="f8f1d-174">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

