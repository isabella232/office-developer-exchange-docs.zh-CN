---
title: GetRoomsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomsResponse
api_type:
- schema
ms.assetid: a8c85f65-bb63-4e7a-b0ca-7c9a04560a58
description: GetRoomsResponse 元素定义对 GetRooms 操作请求的响应。
ms.openlocfilehash: 661e143a9edd30f12ab83fb0666e2832422e280a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458584"
---
# <a name="getroomsresponse"></a><span data-ttu-id="2dc0e-103">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="2dc0e-103">GetRoomsResponse</span></span>

<span data-ttu-id="2dc0e-104">**GetRoomsResponse**元素定义对[GetRooms 操作](getrooms-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-104">The **GetRoomsResponse** element defines a response to a [GetRooms operation](getrooms-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2dc0e-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2dc0e-105">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="2dc0e-106">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="2dc0e-106">GetRoomsResponse</span></span>](getroomsresponse.md)
  
```XML
<GetRoomsResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Rooms/>
</GetRoomsResponse>
```

 <span data-ttu-id="2dc0e-107">**GetRoomsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-107">**GetRoomsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dc0e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2dc0e-108">Attributes and elements</span></span>

<span data-ttu-id="2dc0e-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dc0e-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="2dc0e-110">Attributes</span></span>

|<span data-ttu-id="2dc0e-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-111">**Attribute**</span></span>|<span data-ttu-id="2dc0e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dc0e-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2dc0e-114">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="2dc0e-115">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="2dc0e-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2dc0e-116">-成功</span><span class="sxs-lookup"><span data-stu-id="2dc0e-116">-  Success</span></span>  <br/><span data-ttu-id="2dc0e-117">-警告</span><span class="sxs-lookup"><span data-stu-id="2dc0e-117">-  Warning</span></span>  <br/><span data-ttu-id="2dc0e-118">-错误</span><span class="sxs-lookup"><span data-stu-id="2dc0e-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2dc0e-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="2dc0e-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="2dc0e-120">**值**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-120">**Value**</span></span>|<span data-ttu-id="2dc0e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dc0e-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-122">**Success**</span></span> <br/> |<span data-ttu-id="2dc0e-123">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2dc0e-124">**警告**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-124">**Warning**</span></span> <br/> | <span data-ttu-id="2dc0e-125">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-125">Describes a request that was not processed.</span></span> <span data-ttu-id="2dc0e-126">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2dc0e-127">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="2dc0e-127">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="2dc0e-128">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2dc0e-129">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2dc0e-130">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="2dc0e-131">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2dc0e-132">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="2dc0e-133">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="2dc0e-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-134">**Error**</span></span> <br/> | <span data-ttu-id="2dc0e-135">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2dc0e-136">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="2dc0e-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2dc0e-137">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="2dc0e-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2dc0e-138">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="2dc0e-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="2dc0e-139">-未知标记</span><span class="sxs-lookup"><span data-stu-id="2dc0e-139">-  An unknown tag</span></span>  <br/><span data-ttu-id="2dc0e-140">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="2dc0e-140">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2dc0e-141">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="2dc0e-141">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2dc0e-142">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="2dc0e-142">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2dc0e-143">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2dc0e-144">子元素</span><span class="sxs-lookup"><span data-stu-id="2dc0e-144">Child elements</span></span>

|<span data-ttu-id="2dc0e-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-145">**Element**</span></span>|<span data-ttu-id="2dc0e-146">**描述**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dc0e-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="2dc0e-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2dc0e-148">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2dc0e-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2dc0e-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2dc0e-150">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2dc0e-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2dc0e-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2dc0e-152">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="2dc0e-153">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2dc0e-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2dc0e-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2dc0e-155">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2dc0e-156">所属</span><span class="sxs-lookup"><span data-stu-id="2dc0e-156">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="2dc0e-157">提供表示会议室的电子邮件地址和显示名称的列表。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-157">Provides a list of email addresses and display names that represent meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2dc0e-158">父元素</span><span class="sxs-lookup"><span data-stu-id="2dc0e-158">Parent elements</span></span>

|<span data-ttu-id="2dc0e-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-159">**Element**</span></span>|<span data-ttu-id="2dc0e-160">**描述**</span><span class="sxs-lookup"><span data-stu-id="2dc0e-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dc0e-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2dc0e-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2dc0e-162">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dc0e-163">说明</span><span class="sxs-lookup"><span data-stu-id="2dc0e-163">Remarks</span></span>

<span data-ttu-id="2dc0e-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2dc0e-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dc0e-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="2dc0e-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dc0e-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="2dc0e-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2dc0e-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="2dc0e-167">Schema Name</span></span>  <br/> |<span data-ttu-id="2dc0e-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="2dc0e-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2dc0e-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="2dc0e-169">Validation File</span></span>  <br/> |<span data-ttu-id="2dc0e-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2dc0e-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2dc0e-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="2dc0e-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="2dc0e-172">False</span><span class="sxs-lookup"><span data-stu-id="2dc0e-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2dc0e-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2dc0e-173">See also</span></span>

- [<span data-ttu-id="2dc0e-174">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="2dc0e-174">GetRooms operation</span></span>](getrooms-operation.md)
- [<span data-ttu-id="2dc0e-175">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2dc0e-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

