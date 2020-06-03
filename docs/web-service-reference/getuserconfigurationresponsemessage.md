---
title: GetUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: f75e29eb-ae98-46fd-8da2-1c76a57f5458
description: GetUserConfigurationResponseMessage 元素表示返回用户配置对象的响应。
ms.openlocfilehash: 6aefa2364bfce9c3f928aedc4c018ebb3f85d28b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457688"
---
# <a name="getuserconfigurationresponsemessage"></a><span data-ttu-id="007f3-103">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="007f3-103">GetUserConfigurationResponseMessage</span></span>

<span data-ttu-id="007f3-104">**GetUserConfigurationResponseMessage**元素表示返回用户配置对象的响应。</span><span class="sxs-lookup"><span data-stu-id="007f3-104">The **GetUserConfigurationResponseMessage** element represents a response that returns a user configuration object.</span></span> 
  
```xml
<GetUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <UserConfiguration/>
</GetUserConfigurationResponseMessage>
```

 <span data-ttu-id="007f3-105">**GetUserConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="007f3-105">**GetUserConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="007f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="007f3-106">Attributes and elements</span></span>

<span data-ttu-id="007f3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="007f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="007f3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="007f3-108">Attributes</span></span>

|<span data-ttu-id="007f3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="007f3-109">**Attribute**</span></span>|<span data-ttu-id="007f3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="007f3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="007f3-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="007f3-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="007f3-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="007f3-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="007f3-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="007f3-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="007f3-114">-成功</span><span class="sxs-lookup"><span data-stu-id="007f3-114">-  Success</span></span>  <br/><span data-ttu-id="007f3-115">-警告</span><span class="sxs-lookup"><span data-stu-id="007f3-115">-  Warning</span></span>  <br/><span data-ttu-id="007f3-116">-错误</span><span class="sxs-lookup"><span data-stu-id="007f3-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="007f3-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="007f3-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="007f3-118">**值**</span><span class="sxs-lookup"><span data-stu-id="007f3-118">**Value**</span></span>|<span data-ttu-id="007f3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="007f3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="007f3-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="007f3-120">**Success**</span></span> <br/> |<span data-ttu-id="007f3-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="007f3-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="007f3-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="007f3-122">**Warning**</span></span> <br/> | <span data-ttu-id="007f3-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="007f3-123">Describes a request that was not processed.</span></span> <span data-ttu-id="007f3-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="007f3-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="007f3-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="007f3-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="007f3-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="007f3-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="007f3-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="007f3-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="007f3-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="007f3-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="007f3-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="007f3-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="007f3-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="007f3-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="007f3-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="007f3-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="007f3-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="007f3-132">**Error**</span></span> <br/> | <span data-ttu-id="007f3-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="007f3-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="007f3-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="007f3-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="007f3-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="007f3-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="007f3-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="007f3-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="007f3-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="007f3-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="007f3-138">-上下文中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="007f3-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="007f3-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="007f3-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="007f3-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="007f3-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="007f3-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="007f3-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="007f3-142">子元素</span><span class="sxs-lookup"><span data-stu-id="007f3-142">Child elements</span></span>

|<span data-ttu-id="007f3-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="007f3-143">**Element**</span></span>|<span data-ttu-id="007f3-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="007f3-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="007f3-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="007f3-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="007f3-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="007f3-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="007f3-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="007f3-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="007f3-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="007f3-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="007f3-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="007f3-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="007f3-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="007f3-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="007f3-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="007f3-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="007f3-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="007f3-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="007f3-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="007f3-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="007f3-154">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="007f3-154">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="007f3-155">包含单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="007f3-155">Contains a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="007f3-156">父元素</span><span class="sxs-lookup"><span data-stu-id="007f3-156">Parent elements</span></span>

|<span data-ttu-id="007f3-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="007f3-157">**Element**</span></span>|<span data-ttu-id="007f3-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="007f3-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="007f3-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="007f3-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="007f3-160">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="007f3-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="007f3-161">文本值</span><span class="sxs-lookup"><span data-stu-id="007f3-161">Text value</span></span>

<span data-ttu-id="007f3-162">无。</span><span class="sxs-lookup"><span data-stu-id="007f3-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="007f3-163">说明</span><span class="sxs-lookup"><span data-stu-id="007f3-163">Remarks</span></span>

<span data-ttu-id="007f3-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="007f3-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="007f3-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="007f3-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="007f3-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="007f3-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="007f3-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="007f3-167">Schema Name</span></span>  <br/> |<span data-ttu-id="007f3-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="007f3-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="007f3-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="007f3-169">Validation File</span></span>  <br/> |<span data-ttu-id="007f3-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="007f3-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="007f3-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="007f3-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="007f3-172">False</span><span class="sxs-lookup"><span data-stu-id="007f3-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="007f3-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="007f3-173">See also</span></span>

- [<span data-ttu-id="007f3-174">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="007f3-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

