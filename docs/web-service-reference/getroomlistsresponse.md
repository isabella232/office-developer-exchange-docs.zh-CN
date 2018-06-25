---
title: GetRoomListsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomListsResponse
api_type:
- schema
ms.assetid: 8c736f68-1026-496a-b12f-c169c078abd0
description: GetRoomListsResponse 元素定义来自 GetRoomLists 操作请求的响应。
ms.openlocfilehash: 8231435f7dc348a070852f57d6152550326b5df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754681"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="e6c65-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="e6c65-103">GetRoomListsResponse</span></span>

<span data-ttu-id="e6c65-104">**GetRoomListsResponse**元素定义来自[GetRoomLists 操作](getroomlists-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e6c65-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="e6c65-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e6c65-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="e6c65-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="e6c65-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="e6c65-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e6c65-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6c65-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-108">Attributes and elements</span></span>

<span data-ttu-id="e6c65-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6c65-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6c65-110">属性</span><span class="sxs-lookup"><span data-stu-id="e6c65-110">Attributes</span></span>

|<span data-ttu-id="e6c65-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="e6c65-111">**Attribute**</span></span>|<span data-ttu-id="e6c65-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6c65-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6c65-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e6c65-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e6c65-114">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="e6c65-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="e6c65-115">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="e6c65-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e6c65-116">-成功</span><span class="sxs-lookup"><span data-stu-id="e6c65-116">-  Success</span></span>  <br/><span data-ttu-id="e6c65-117">-警告</span><span class="sxs-lookup"><span data-stu-id="e6c65-117">-  Warning</span></span>  <br/><span data-ttu-id="e6c65-118">-错误</span><span class="sxs-lookup"><span data-stu-id="e6c65-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e6c65-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="e6c65-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="e6c65-120">**值**</span><span class="sxs-lookup"><span data-stu-id="e6c65-120">**Value**</span></span>|<span data-ttu-id="e6c65-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6c65-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6c65-122">**成功**</span><span class="sxs-lookup"><span data-stu-id="e6c65-122">**Success**</span></span> <br/> |<span data-ttu-id="e6c65-123">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="e6c65-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e6c65-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="e6c65-124">**Warning**</span></span> <br/> | <span data-ttu-id="e6c65-125">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="e6c65-125">Describes a request that was not processed.</span></span> <span data-ttu-id="e6c65-126">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="e6c65-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e6c65-127">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="e6c65-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="e6c65-128">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e6c65-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e6c65-129">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e6c65-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="e6c65-130">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="e6c65-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e6c65-131">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e6c65-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e6c65-132">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="e6c65-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="e6c65-133">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="e6c65-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e6c65-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="e6c65-134">**Error**</span></span> <br/> | <span data-ttu-id="e6c65-135">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="e6c65-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e6c65-136">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="e6c65-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e6c65-137">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e6c65-138">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="e6c65-139">-未知标记</span><span class="sxs-lookup"><span data-stu-id="e6c65-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="e6c65-140">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="e6c65-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="e6c65-141">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="e6c65-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e6c65-142">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="e6c65-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="e6c65-143">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="e6c65-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="e6c65-144">子元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-144">Child elements</span></span>

|<span data-ttu-id="e6c65-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6c65-145">**Element**</span></span>|<span data-ttu-id="e6c65-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6c65-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6c65-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="e6c65-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e6c65-148">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e6c65-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e6c65-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e6c65-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e6c65-150">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e6c65-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e6c65-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e6c65-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e6c65-152">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e6c65-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e6c65-153">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="e6c65-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e6c65-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e6c65-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e6c65-155">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e6c65-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e6c65-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="e6c65-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="e6c65-157">提供的电子邮件地址和表示的会议室列表的显示名称的列表。</span><span class="sxs-lookup"><span data-stu-id="e6c65-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6c65-158">父元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-158">Parent elements</span></span>

|<span data-ttu-id="e6c65-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6c65-159">**Element**</span></span>|<span data-ttu-id="e6c65-160">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6c65-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6c65-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e6c65-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e6c65-162">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e6c65-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e6c65-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6c65-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6c65-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6c65-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6c65-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6c65-165">Schema Name</span></span>  <br/> |<span data-ttu-id="e6c65-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="e6c65-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6c65-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6c65-167">Validation File</span></span>  <br/> |<span data-ttu-id="e6c65-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6c65-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6c65-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6c65-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6c65-170">False</span><span class="sxs-lookup"><span data-stu-id="e6c65-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6c65-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6c65-171">See also</span></span>

- [<span data-ttu-id="e6c65-172">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="e6c65-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="e6c65-173">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e6c65-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

