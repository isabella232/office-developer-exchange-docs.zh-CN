---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: ResponseMessage 元素提供了有关单个实体中请求的响应状态的描述性信息。
ms.openlocfilehash: 69f1f6f12d10044045b72dd644536e742c479b9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827191"
---
# <a name="responsemessage"></a><span data-ttu-id="eee8b-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="eee8b-103">ResponseMessage</span></span>

<span data-ttu-id="eee8b-104">**ResponseMessage**元素提供了有关单个实体中请求的响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="eee8b-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="eee8b-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eee8b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eee8b-106">Attributes and elements</span></span>

<span data-ttu-id="eee8b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eee8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eee8b-108">属性</span><span class="sxs-lookup"><span data-stu-id="eee8b-108">Attributes</span></span>

|<span data-ttu-id="eee8b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="eee8b-109">**Attribute**</span></span>|<span data-ttu-id="eee8b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="eee8b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eee8b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="eee8b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="eee8b-112">表示响应的状态。</span><span class="sxs-lookup"><span data-stu-id="eee8b-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="eee8b-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="eee8b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="eee8b-114">-成功</span><span class="sxs-lookup"><span data-stu-id="eee8b-114">-  Success</span></span>  <br/><span data-ttu-id="eee8b-115">-警告</span><span class="sxs-lookup"><span data-stu-id="eee8b-115">-  Warning</span></span>  <br/><span data-ttu-id="eee8b-116">-错误</span><span class="sxs-lookup"><span data-stu-id="eee8b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="eee8b-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="eee8b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="eee8b-118">**值**</span><span class="sxs-lookup"><span data-stu-id="eee8b-118">**Value**</span></span>|<span data-ttu-id="eee8b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="eee8b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eee8b-120">成功</span><span class="sxs-lookup"><span data-stu-id="eee8b-120">Success</span></span>  <br/> |<span data-ttu-id="eee8b-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="eee8b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="eee8b-122">警告</span><span class="sxs-lookup"><span data-stu-id="eee8b-122">Warning</span></span>  <br/> | <span data-ttu-id="eee8b-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="eee8b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="eee8b-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="eee8b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="eee8b-125">警告的一些可能原因如下：</span><span class="sxs-lookup"><span data-stu-id="eee8b-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="eee8b-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eee8b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="eee8b-127">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eee8b-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="eee8b-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="eee8b-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="eee8b-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="eee8b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="eee8b-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="eee8b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="eee8b-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="eee8b-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="eee8b-132">错误</span><span class="sxs-lookup"><span data-stu-id="eee8b-132">Error</span></span>  <br/> | <span data-ttu-id="eee8b-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="eee8b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="eee8b-134">错误的一些可能原因如下：</span><span class="sxs-lookup"><span data-stu-id="eee8b-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="eee8b-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="eee8b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="eee8b-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="eee8b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="eee8b-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="eee8b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="eee8b-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="eee8b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="eee8b-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="eee8b-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="eee8b-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="eee8b-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="eee8b-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="eee8b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eee8b-142">子元素</span><span class="sxs-lookup"><span data-stu-id="eee8b-142">Child elements</span></span>

|<span data-ttu-id="eee8b-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="eee8b-143">**Element**</span></span>|<span data-ttu-id="eee8b-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="eee8b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eee8b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="eee8b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="eee8b-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="eee8b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="eee8b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eee8b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="eee8b-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="eee8b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="eee8b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="eee8b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="eee8b-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="eee8b-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="eee8b-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="eee8b-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="eee8b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="eee8b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="eee8b-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="eee8b-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eee8b-154">父元素</span><span class="sxs-lookup"><span data-stu-id="eee8b-154">Parent elements</span></span>

|<span data-ttu-id="eee8b-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="eee8b-155">**Element**</span></span>|<span data-ttu-id="eee8b-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="eee8b-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eee8b-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="eee8b-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="eee8b-158">包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="eee8b-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="eee8b-159">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="eee8b-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="eee8b-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="eee8b-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="eee8b-161">包含用于请求会议建议的响应的信息和建议数据。</span><span class="sxs-lookup"><span data-stu-id="eee8b-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="eee8b-162">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="eee8b-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="eee8b-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="eee8b-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="eee8b-164">包含响应结果和用户的 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="eee8b-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="eee8b-165">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="eee8b-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="eee8b-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="eee8b-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="eee8b-167">包含结果的尝试的[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)消息。</span><span class="sxs-lookup"><span data-stu-id="eee8b-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="eee8b-168">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="eee8b-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eee8b-169">注解</span><span class="sxs-lookup"><span data-stu-id="eee8b-169">Remarks</span></span>

<span data-ttu-id="eee8b-170">适用于所有 Exchange Web 服务响应**ResponseMessageType**类型。</span><span class="sxs-lookup"><span data-stu-id="eee8b-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="eee8b-171">**ResponseMessageType**类型是由下列复杂类型扩展：</span><span class="sxs-lookup"><span data-stu-id="eee8b-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="eee8b-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="eee8b-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="eee8b-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="eee8b-187">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eee8b-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="eee8b-188">版本差异</span><span class="sxs-lookup"><span data-stu-id="eee8b-188">Version differences</span></span>

<span data-ttu-id="eee8b-189">**ApplyConversationActionResponseMessage**和**DeleteItemResponseMessageType**类型是 Exchange 生成 15.00.0986.00 中引入的。</span><span class="sxs-lookup"><span data-stu-id="eee8b-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="eee8b-190">元素信息</span><span class="sxs-lookup"><span data-stu-id="eee8b-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eee8b-191">命名空间</span><span class="sxs-lookup"><span data-stu-id="eee8b-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eee8b-192">架构名称</span><span class="sxs-lookup"><span data-stu-id="eee8b-192">Schema Name</span></span>  <br/> |<span data-ttu-id="eee8b-193">消息架构</span><span class="sxs-lookup"><span data-stu-id="eee8b-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eee8b-194">验证文件</span><span class="sxs-lookup"><span data-stu-id="eee8b-194">Validation File</span></span>  <br/> |<span data-ttu-id="eee8b-195">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eee8b-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eee8b-196">可以为空</span><span class="sxs-lookup"><span data-stu-id="eee8b-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="eee8b-197">False</span><span class="sxs-lookup"><span data-stu-id="eee8b-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eee8b-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eee8b-198">See also</span></span>

- [<span data-ttu-id="eee8b-199">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="eee8b-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="eee8b-200">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="eee8b-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="eee8b-201">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="eee8b-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="eee8b-202">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="eee8b-202">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

