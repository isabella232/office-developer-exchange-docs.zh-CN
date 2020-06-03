---
title: ServiceConfigurationResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServiceConfigurationResponseMessageType
api_type:
- schema
ms.assetid: ccfb0578-c648-44c2-ac4d-7620d881363e
description: ServiceConfigurationResponseMessageType 元素包含服务配置设置。
ms.openlocfilehash: 4c84a49b2403343a1defd00696858489497d6214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44439103"
---
# <a name="serviceconfigurationresponsemessagetype"></a><span data-ttu-id="90770-103">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="90770-103">ServiceConfigurationResponseMessageType</span></span>

<span data-ttu-id="90770-104">**ServiceConfigurationResponseMessageType**元素包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="90770-104">The **ServiceConfigurationResponseMessageType** element contains service configuration settings.</span></span> 
  
```XML
<ServiceConfigurationResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTipsConfiguration/>
   <UnifiedMessagingConfiguration/>
   <ProtectionRulesConfiguration/>
</ServiceConfigurationResponseMessageType>
```

 <span data-ttu-id="90770-105">**ServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="90770-105">**ServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90770-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="90770-106">Attributes and elements</span></span>

<span data-ttu-id="90770-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="90770-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90770-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="90770-108">Attributes</span></span>

|<span data-ttu-id="90770-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="90770-109">**Attribute**</span></span>|<span data-ttu-id="90770-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="90770-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90770-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="90770-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="90770-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="90770-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="90770-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="90770-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="90770-114">-成功</span><span class="sxs-lookup"><span data-stu-id="90770-114">-  Success</span></span>  <br/><span data-ttu-id="90770-115">-警告</span><span class="sxs-lookup"><span data-stu-id="90770-115">-  Warning</span></span>  <br/><span data-ttu-id="90770-116">-错误</span><span class="sxs-lookup"><span data-stu-id="90770-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="90770-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="90770-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="90770-118">**值**</span><span class="sxs-lookup"><span data-stu-id="90770-118">**Value**</span></span>|<span data-ttu-id="90770-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="90770-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90770-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="90770-120">**Success**</span></span> <br/> |<span data-ttu-id="90770-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="90770-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="90770-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="90770-122">**Warning**</span></span> <br/> | <span data-ttu-id="90770-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="90770-123">Describes a request that was not processed.</span></span> <span data-ttu-id="90770-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="90770-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="90770-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="90770-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="90770-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="90770-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="90770-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="90770-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="90770-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="90770-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="90770-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="90770-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="90770-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="90770-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="90770-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="90770-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="90770-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="90770-132">**Error**</span></span> <br/> | <span data-ttu-id="90770-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="90770-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="90770-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="90770-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="90770-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="90770-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="90770-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="90770-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="90770-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="90770-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="90770-138">-上下文中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="90770-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="90770-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="90770-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="90770-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="90770-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="90770-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="90770-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="90770-142">子元素</span><span class="sxs-lookup"><span data-stu-id="90770-142">Child elements</span></span>

|<span data-ttu-id="90770-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="90770-143">**Element**</span></span>|<span data-ttu-id="90770-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="90770-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90770-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="90770-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="90770-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="90770-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="90770-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="90770-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="90770-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="90770-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="90770-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="90770-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="90770-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="90770-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="90770-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="90770-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="90770-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="90770-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="90770-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="90770-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="90770-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="90770-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="90770-155">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="90770-155">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="90770-156">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="90770-156">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="90770-157">包含统一消息服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="90770-157">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
|[<span data-ttu-id="90770-158">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="90770-158">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="90770-159">包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="90770-159">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90770-160">父元素</span><span class="sxs-lookup"><span data-stu-id="90770-160">Parent elements</span></span>

|<span data-ttu-id="90770-161">**元素**</span><span class="sxs-lookup"><span data-stu-id="90770-161">**Element**</span></span>|<span data-ttu-id="90770-162">**描述**</span><span class="sxs-lookup"><span data-stu-id="90770-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90770-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="90770-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="90770-164">包含一组服务配置响应消息。</span><span class="sxs-lookup"><span data-stu-id="90770-164">Contains an array of service configuration response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90770-165">文本值</span><span class="sxs-lookup"><span data-stu-id="90770-165">Text value</span></span>

<span data-ttu-id="90770-166">无。</span><span class="sxs-lookup"><span data-stu-id="90770-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90770-167">说明</span><span class="sxs-lookup"><span data-stu-id="90770-167">Remarks</span></span>

<span data-ttu-id="90770-168">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="90770-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90770-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="90770-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90770-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="90770-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90770-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="90770-171">Schema Name</span></span>  <br/> |<span data-ttu-id="90770-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="90770-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="90770-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="90770-173">Validation File</span></span>  <br/> |<span data-ttu-id="90770-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="90770-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90770-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="90770-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="90770-176">False</span><span class="sxs-lookup"><span data-stu-id="90770-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90770-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="90770-177">See also</span></span>

- [<span data-ttu-id="90770-178">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="90770-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

