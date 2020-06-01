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
description: ResponseMessage 元素提供有关请求中单个实体的响应状态的描述性信息。
ms.openlocfilehash: a7f4240b1e988cb69d67118c6db58db0d7babba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467156"
---
# <a name="responsemessage"></a><span data-ttu-id="f9111-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f9111-103">ResponseMessage</span></span>

<span data-ttu-id="f9111-104">**ResponseMessage**元素提供有关请求中单个实体的响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="f9111-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="f9111-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9111-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f9111-106">Attributes and elements</span></span>

<span data-ttu-id="f9111-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f9111-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9111-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9111-108">Attributes</span></span>

|<span data-ttu-id="f9111-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f9111-109">**Attribute**</span></span>|<span data-ttu-id="f9111-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9111-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9111-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f9111-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f9111-112">表示响应的状态。</span><span class="sxs-lookup"><span data-stu-id="f9111-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="f9111-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="f9111-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="f9111-114">-成功</span><span class="sxs-lookup"><span data-stu-id="f9111-114">-  Success</span></span>  <br/><span data-ttu-id="f9111-115">-警告</span><span class="sxs-lookup"><span data-stu-id="f9111-115">-  Warning</span></span>  <br/><span data-ttu-id="f9111-116">-错误</span><span class="sxs-lookup"><span data-stu-id="f9111-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f9111-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="f9111-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="f9111-118">**值**</span><span class="sxs-lookup"><span data-stu-id="f9111-118">**Value**</span></span>|<span data-ttu-id="f9111-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9111-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9111-120">成功</span><span class="sxs-lookup"><span data-stu-id="f9111-120">Success</span></span>  <br/> |<span data-ttu-id="f9111-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="f9111-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f9111-122">警告</span><span class="sxs-lookup"><span data-stu-id="f9111-122">Warning</span></span>  <br/> | <span data-ttu-id="f9111-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="f9111-123">Describes a request that was not processed.</span></span> <span data-ttu-id="f9111-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="f9111-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="f9111-125">以下是警告的一些可能的原因：</span><span class="sxs-lookup"><span data-stu-id="f9111-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="f9111-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f9111-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="f9111-127">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="f9111-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="f9111-128">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="f9111-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="f9111-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f9111-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="f9111-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="f9111-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="f9111-131">-超出配额。</span><span class="sxs-lookup"><span data-stu-id="f9111-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="f9111-132">错误</span><span class="sxs-lookup"><span data-stu-id="f9111-132">Error</span></span>  <br/> | <span data-ttu-id="f9111-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="f9111-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="f9111-134">以下是一些可能的错误原因：</span><span class="sxs-lookup"><span data-stu-id="f9111-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="f9111-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="f9111-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f9111-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="f9111-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="f9111-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="f9111-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="f9111-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="f9111-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="f9111-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="f9111-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f9111-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="f9111-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="f9111-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="f9111-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f9111-142">子元素</span><span class="sxs-lookup"><span data-stu-id="f9111-142">Child elements</span></span>

|<span data-ttu-id="f9111-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="f9111-143">**Element**</span></span>|<span data-ttu-id="f9111-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="f9111-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9111-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="f9111-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f9111-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="f9111-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f9111-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f9111-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f9111-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f9111-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f9111-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f9111-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f9111-150">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="f9111-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f9111-151">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="f9111-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f9111-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f9111-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f9111-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="f9111-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9111-154">父元素</span><span class="sxs-lookup"><span data-stu-id="f9111-154">Parent elements</span></span>

|<span data-ttu-id="f9111-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="f9111-155">**Element**</span></span>|<span data-ttu-id="f9111-156">**描述**</span><span class="sxs-lookup"><span data-stu-id="f9111-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9111-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f9111-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="f9111-158">包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="f9111-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="f9111-159">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="f9111-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="f9111-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f9111-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="f9111-161">包含请求的会议建议的响应信息和建议数据。</span><span class="sxs-lookup"><span data-stu-id="f9111-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="f9111-162">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="f9111-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="f9111-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="f9111-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="f9111-164">包含用户的响应结果和 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="f9111-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="f9111-165">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="f9111-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="f9111-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="f9111-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="f9111-167">包含尝试的[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)邮件的结果。</span><span class="sxs-lookup"><span data-stu-id="f9111-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="f9111-168">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="f9111-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9111-169">备注</span><span class="sxs-lookup"><span data-stu-id="f9111-169">Remarks</span></span>

<span data-ttu-id="f9111-170">**ResponseMessageType**类型在所有 Exchange Web 服务响应中是通用的。</span><span class="sxs-lookup"><span data-stu-id="f9111-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="f9111-171">**ResponseMessageType**类型由以下复杂类型扩展：</span><span class="sxs-lookup"><span data-stu-id="f9111-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="f9111-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="f9111-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f9111-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="f9111-187">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f9111-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="f9111-188">版本差异</span><span class="sxs-lookup"><span data-stu-id="f9111-188">Version differences</span></span>

<span data-ttu-id="f9111-189">**ApplyConversationActionResponseMessage**和**DeleteItemResponseMessageType**类型是在 Exchange build 15.00.0986.00 中引入的。</span><span class="sxs-lookup"><span data-stu-id="f9111-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f9111-190">元素信息</span><span class="sxs-lookup"><span data-stu-id="f9111-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9111-191">命名空间</span><span class="sxs-lookup"><span data-stu-id="f9111-191">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9111-192">架构名称</span><span class="sxs-lookup"><span data-stu-id="f9111-192">Schema Name</span></span>  <br/> |<span data-ttu-id="f9111-193">消息架构</span><span class="sxs-lookup"><span data-stu-id="f9111-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f9111-194">验证文件</span><span class="sxs-lookup"><span data-stu-id="f9111-194">Validation File</span></span>  <br/> |<span data-ttu-id="f9111-195">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f9111-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9111-196">可以为空</span><span class="sxs-lookup"><span data-stu-id="f9111-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9111-197">False</span><span class="sxs-lookup"><span data-stu-id="f9111-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9111-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9111-198">See also</span></span>

- [<span data-ttu-id="f9111-199">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="f9111-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f9111-200">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="f9111-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="f9111-201">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="f9111-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="f9111-202">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="f9111-202">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

