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
ms.openlocfilehash: b6d7c2baa2861309d72bcbf880eaed2ad0989175
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462941"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="1a4e9-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="1a4e9-103">GetRoomListsResponse</span></span>

<span data-ttu-id="1a4e9-104">**GetRoomListsResponse**元素定义来自[GetRoomLists 操作](getroomlists-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="1a4e9-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a4e9-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="1a4e9-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="1a4e9-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="1a4e9-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a4e9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a4e9-108">Attributes and elements</span></span>

<span data-ttu-id="1a4e9-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a4e9-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="1a4e9-110">Attributes</span></span>

|<span data-ttu-id="1a4e9-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-111">**Attribute**</span></span>|<span data-ttu-id="1a4e9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a4e9-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1a4e9-114">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="1a4e9-115">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="1a4e9-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1a4e9-116">-成功</span><span class="sxs-lookup"><span data-stu-id="1a4e9-116">-  Success</span></span>  <br/><span data-ttu-id="1a4e9-117">-警告</span><span class="sxs-lookup"><span data-stu-id="1a4e9-117">-  Warning</span></span>  <br/><span data-ttu-id="1a4e9-118">-错误</span><span class="sxs-lookup"><span data-stu-id="1a4e9-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1a4e9-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="1a4e9-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="1a4e9-120">**值**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-120">**Value**</span></span>|<span data-ttu-id="1a4e9-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a4e9-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-122">**Success**</span></span> <br/> |<span data-ttu-id="1a4e9-123">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1a4e9-124">**警告**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-124">**Warning**</span></span> <br/> | <span data-ttu-id="1a4e9-125">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-125">Describes a request that was not processed.</span></span> <span data-ttu-id="1a4e9-126">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1a4e9-127">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="1a4e9-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1a4e9-128">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1a4e9-129">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="1a4e9-130">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1a4e9-131">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1a4e9-132">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="1a4e9-133">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1a4e9-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-134">**Error**</span></span> <br/> | <span data-ttu-id="1a4e9-135">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1a4e9-136">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="1a4e9-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1a4e9-137">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1a4e9-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1a4e9-138">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="1a4e9-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1a4e9-139">-未知标记</span><span class="sxs-lookup"><span data-stu-id="1a4e9-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="1a4e9-140">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="1a4e9-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1a4e9-141">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="1a4e9-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1a4e9-142">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="1a4e9-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1a4e9-143">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="1a4e9-144">子元素</span><span class="sxs-lookup"><span data-stu-id="1a4e9-144">Child elements</span></span>

|<span data-ttu-id="1a4e9-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-145">**Element**</span></span>|<span data-ttu-id="1a4e9-146">**描述**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a4e9-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="1a4e9-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1a4e9-148">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1a4e9-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1a4e9-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1a4e9-150">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1a4e9-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1a4e9-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1a4e9-152">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1a4e9-153">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1a4e9-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1a4e9-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1a4e9-155">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1a4e9-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="1a4e9-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="1a4e9-157">提供表示会议室列表的电子邮件地址和显示名称的列表。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a4e9-158">父元素</span><span class="sxs-lookup"><span data-stu-id="1a4e9-158">Parent elements</span></span>

|<span data-ttu-id="1a4e9-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-159">**Element**</span></span>|<span data-ttu-id="1a4e9-160">**描述**</span><span class="sxs-lookup"><span data-stu-id="1a4e9-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a4e9-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a4e9-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1a4e9-162">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="1a4e9-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="1a4e9-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a4e9-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a4e9-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a4e9-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a4e9-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a4e9-165">Schema Name</span></span>  <br/> |<span data-ttu-id="1a4e9-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="1a4e9-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1a4e9-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a4e9-167">Validation File</span></span>  <br/> |<span data-ttu-id="1a4e9-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1a4e9-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a4e9-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a4e9-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a4e9-170">False</span><span class="sxs-lookup"><span data-stu-id="1a4e9-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a4e9-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a4e9-171">See also</span></span>

- [<span data-ttu-id="1a4e9-172">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="1a4e9-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="1a4e9-173">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1a4e9-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

