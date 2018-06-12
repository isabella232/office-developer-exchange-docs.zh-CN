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
description: GetRoomsResponse 元素定义 GetRooms 操作请求的响应。
ms.openlocfilehash: 7399ab910a99b39757eb752b11a4771ba81be46a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754675"
---
# <a name="getroomsresponse"></a><span data-ttu-id="33b57-103">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="33b57-103">GetRoomsResponse</span></span>

<span data-ttu-id="33b57-104">**GetRoomsResponse**元素定义[GetRooms 操作](getrooms-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="33b57-104">The **GetRoomsResponse** element defines a response to a [GetRooms operation](getrooms-operation.md) request.</span></span> 
  
- [<span data-ttu-id="33b57-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33b57-105">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="33b57-106">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="33b57-106">GetRoomsResponse</span></span>](getroomsresponse.md)
  
```XML
<GetRoomsResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Rooms/>
</GetRoomsResponse>
```

 <span data-ttu-id="33b57-107">**GetRoomsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="33b57-107">**GetRoomsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33b57-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="33b57-108">Attributes and elements</span></span>

<span data-ttu-id="33b57-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33b57-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33b57-110">属性</span><span class="sxs-lookup"><span data-stu-id="33b57-110">Attributes</span></span>

|<span data-ttu-id="33b57-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="33b57-111">**Attribute**</span></span>|<span data-ttu-id="33b57-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="33b57-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33b57-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="33b57-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="33b57-114">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="33b57-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="33b57-115">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="33b57-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="33b57-116">-成功</span><span class="sxs-lookup"><span data-stu-id="33b57-116">-  Success</span></span>  <br/><span data-ttu-id="33b57-117">-警告</span><span class="sxs-lookup"><span data-stu-id="33b57-117">-  Warning</span></span>  <br/><span data-ttu-id="33b57-118">-错误</span><span class="sxs-lookup"><span data-stu-id="33b57-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="33b57-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="33b57-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="33b57-120">**值**</span><span class="sxs-lookup"><span data-stu-id="33b57-120">**Value**</span></span>|<span data-ttu-id="33b57-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="33b57-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33b57-122">**成功**</span><span class="sxs-lookup"><span data-stu-id="33b57-122">**Success**</span></span> <br/> |<span data-ttu-id="33b57-123">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="33b57-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="33b57-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="33b57-124">**Warning**</span></span> <br/> | <span data-ttu-id="33b57-125">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="33b57-125">Describes a request that was not processed.</span></span> <span data-ttu-id="33b57-126">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="33b57-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="33b57-127">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="33b57-127">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="33b57-128">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33b57-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="33b57-129">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33b57-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="33b57-130">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="33b57-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="33b57-131">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33b57-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="33b57-132">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="33b57-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="33b57-133">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="33b57-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="33b57-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="33b57-134">**Error**</span></span> <br/> | <span data-ttu-id="33b57-135">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="33b57-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="33b57-136">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="33b57-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="33b57-137">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="33b57-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="33b57-138">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="33b57-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="33b57-139">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="33b57-139">-  An unknown tag</span></span>  <br/><span data-ttu-id="33b57-140">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="33b57-140">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="33b57-141">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="33b57-141">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="33b57-142">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="33b57-142">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="33b57-143">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="33b57-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="33b57-144">子元素</span><span class="sxs-lookup"><span data-stu-id="33b57-144">Child elements</span></span>

|<span data-ttu-id="33b57-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="33b57-145">**Element**</span></span>|<span data-ttu-id="33b57-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="33b57-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33b57-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="33b57-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="33b57-148">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="33b57-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="33b57-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="33b57-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="33b57-150">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="33b57-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="33b57-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="33b57-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="33b57-152">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="33b57-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="33b57-153">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="33b57-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="33b57-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="33b57-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="33b57-155">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="33b57-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="33b57-156">聊天室</span><span class="sxs-lookup"><span data-stu-id="33b57-156">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="33b57-157">提供的电子邮件地址和表示会议室的显示名称的列表。</span><span class="sxs-lookup"><span data-stu-id="33b57-157">Provides a list of email addresses and display names that represent meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33b57-158">父元素</span><span class="sxs-lookup"><span data-stu-id="33b57-158">Parent elements</span></span>

|<span data-ttu-id="33b57-159">**元素**</span><span class="sxs-lookup"><span data-stu-id="33b57-159">**Element**</span></span>|<span data-ttu-id="33b57-160">**说明**</span><span class="sxs-lookup"><span data-stu-id="33b57-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33b57-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33b57-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="33b57-162">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="33b57-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33b57-163">备注</span><span class="sxs-lookup"><span data-stu-id="33b57-163">Remarks</span></span>

<span data-ttu-id="33b57-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="33b57-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33b57-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="33b57-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33b57-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="33b57-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="33b57-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="33b57-167">Schema Name</span></span>  <br/> |<span data-ttu-id="33b57-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="33b57-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="33b57-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="33b57-169">Validation File</span></span>  <br/> |<span data-ttu-id="33b57-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="33b57-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="33b57-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="33b57-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="33b57-172">False</span><span class="sxs-lookup"><span data-stu-id="33b57-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33b57-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33b57-173">See also</span></span>

- [<span data-ttu-id="33b57-174">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="33b57-174">GetRooms operation</span></span>](getrooms-operation.md)
- [<span data-ttu-id="33b57-175">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="33b57-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

