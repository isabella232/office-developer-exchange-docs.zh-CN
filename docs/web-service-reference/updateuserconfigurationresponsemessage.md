---
title: UpdateUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 27728e57-5a9b-4314-ad64-df7869098f62
description: UpdateUserConfigurationResponseMessage 元素包含单个 UpdateUserConfiguration 操作请求的状态和结果。
ms.openlocfilehash: 9c885c87f4b48df16e4097b9c4eafd7e9278c7b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468521"
---
# <a name="updateuserconfigurationresponsemessage"></a><span data-ttu-id="3bd6d-103">UpdateUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3bd6d-103">UpdateUserConfigurationResponseMessage</span></span>

<span data-ttu-id="3bd6d-104">**UpdateUserConfigurationResponseMessage**元素包含单个 UpdateUserConfiguration 操作请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-104">The **UpdateUserConfigurationResponseMessage** element contains the status and result of a single UpdateUserConfiguration operation request.</span></span> 
  
```xml
<UpdateUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateUserConfigurationResponseMessage>
```

 <span data-ttu-id="3bd6d-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bd6d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3bd6d-106">Attributes and elements</span></span>

<span data-ttu-id="3bd6d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bd6d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3bd6d-108">Attributes</span></span>

|<span data-ttu-id="3bd6d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-109">**Attribute**</span></span>|<span data-ttu-id="3bd6d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3bd6d-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3bd6d-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="3bd6d-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="3bd6d-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="3bd6d-114">-成功</span><span class="sxs-lookup"><span data-stu-id="3bd6d-114">-  Success</span></span>  <br/><span data-ttu-id="3bd6d-115">-警告</span><span class="sxs-lookup"><span data-stu-id="3bd6d-115">-  Warning</span></span>  <br/><span data-ttu-id="3bd6d-116">-错误</span><span class="sxs-lookup"><span data-stu-id="3bd6d-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="3bd6d-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="3bd6d-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="3bd6d-118">**值**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-118">**Value**</span></span>|<span data-ttu-id="3bd6d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3bd6d-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-120">**Success**</span></span> <br/> |<span data-ttu-id="3bd6d-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="3bd6d-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-122">**Warning**</span></span> <br/> | <span data-ttu-id="3bd6d-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-123">Describes a request that was not processed.</span></span> <span data-ttu-id="3bd6d-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3bd6d-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="3bd6d-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="3bd6d-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="3bd6d-127">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="3bd6d-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="3bd6d-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="3bd6d-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="3bd6d-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="3bd6d-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-132">**Error**</span></span> <br/> | <span data-ttu-id="3bd6d-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3bd6d-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="3bd6d-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3bd6d-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="3bd6d-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="3bd6d-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="3bd6d-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="3bd6d-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="3bd6d-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="3bd6d-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="3bd6d-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="3bd6d-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="3bd6d-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="3bd6d-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="3bd6d-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="3bd6d-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3bd6d-142">子元素</span><span class="sxs-lookup"><span data-stu-id="3bd6d-142">Child elements</span></span>

|<span data-ttu-id="3bd6d-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-143">**Element**</span></span>|<span data-ttu-id="3bd6d-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bd6d-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="3bd6d-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3bd6d-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3bd6d-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3bd6d-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3bd6d-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="3bd6d-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3bd6d-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3bd6d-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="3bd6d-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3bd6d-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3bd6d-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3bd6d-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bd6d-154">父元素</span><span class="sxs-lookup"><span data-stu-id="3bd6d-154">Parent elements</span></span>

|<span data-ttu-id="3bd6d-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-155">**Element**</span></span>|<span data-ttu-id="3bd6d-156">**描述**</span><span class="sxs-lookup"><span data-stu-id="3bd6d-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bd6d-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3bd6d-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3bd6d-158">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bd6d-159">备注</span><span class="sxs-lookup"><span data-stu-id="3bd6d-159">Remarks</span></span>

<span data-ttu-id="3bd6d-160">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3bd6d-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bd6d-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="3bd6d-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bd6d-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="3bd6d-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3bd6d-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="3bd6d-163">Schema Name</span></span>  <br/> |<span data-ttu-id="3bd6d-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="3bd6d-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3bd6d-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="3bd6d-165">Validation File</span></span>  <br/> |<span data-ttu-id="3bd6d-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3bd6d-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3bd6d-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="3bd6d-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bd6d-168">False</span><span class="sxs-lookup"><span data-stu-id="3bd6d-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bd6d-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3bd6d-169">See also</span></span>

- [<span data-ttu-id="3bd6d-170">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3bd6d-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

