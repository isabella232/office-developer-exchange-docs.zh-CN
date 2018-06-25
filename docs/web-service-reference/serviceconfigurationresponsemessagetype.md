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
ms.openlocfilehash: fb7841f346083017319cece4479fea8bbfb6de17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827393"
---
# <a name="serviceconfigurationresponsemessagetype"></a><span data-ttu-id="28d03-103">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="28d03-103">ServiceConfigurationResponseMessageType</span></span>

<span data-ttu-id="28d03-104">**ServiceConfigurationResponseMessageType**元素包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="28d03-104">The **ServiceConfigurationResponseMessageType** element contains service configuration settings.</span></span> 
  
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

 <span data-ttu-id="28d03-105">**ServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="28d03-105">**ServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28d03-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="28d03-106">Attributes and elements</span></span>

<span data-ttu-id="28d03-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="28d03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28d03-108">属性</span><span class="sxs-lookup"><span data-stu-id="28d03-108">Attributes</span></span>

|<span data-ttu-id="28d03-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="28d03-109">**Attribute**</span></span>|<span data-ttu-id="28d03-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="28d03-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28d03-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="28d03-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="28d03-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="28d03-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="28d03-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="28d03-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="28d03-114">-成功</span><span class="sxs-lookup"><span data-stu-id="28d03-114">-  Success</span></span>  <br/><span data-ttu-id="28d03-115">-警告</span><span class="sxs-lookup"><span data-stu-id="28d03-115">-  Warning</span></span>  <br/><span data-ttu-id="28d03-116">-错误</span><span class="sxs-lookup"><span data-stu-id="28d03-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="28d03-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="28d03-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="28d03-118">**值**</span><span class="sxs-lookup"><span data-stu-id="28d03-118">**Value**</span></span>|<span data-ttu-id="28d03-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="28d03-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28d03-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="28d03-120">**Success**</span></span> <br/> |<span data-ttu-id="28d03-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="28d03-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="28d03-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="28d03-122">**Warning**</span></span> <br/> | <span data-ttu-id="28d03-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="28d03-123">Describes a request that was not processed.</span></span> <span data-ttu-id="28d03-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="28d03-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="28d03-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="28d03-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="28d03-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="28d03-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="28d03-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="28d03-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="28d03-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28d03-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="28d03-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="28d03-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="28d03-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="28d03-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="28d03-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="28d03-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="28d03-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="28d03-132">**Error**</span></span> <br/> | <span data-ttu-id="28d03-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="28d03-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="28d03-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="28d03-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="28d03-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="28d03-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="28d03-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="28d03-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="28d03-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="28d03-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="28d03-138">-属性或元素不是有效的上下文中</span><span class="sxs-lookup"><span data-stu-id="28d03-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="28d03-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="28d03-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="28d03-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="28d03-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="28d03-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="28d03-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28d03-142">子元素</span><span class="sxs-lookup"><span data-stu-id="28d03-142">Child elements</span></span>

|<span data-ttu-id="28d03-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="28d03-143">**Element**</span></span>|<span data-ttu-id="28d03-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="28d03-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28d03-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="28d03-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="28d03-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="28d03-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="28d03-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="28d03-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="28d03-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="28d03-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="28d03-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="28d03-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="28d03-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="28d03-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="28d03-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="28d03-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="28d03-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="28d03-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="28d03-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="28d03-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="28d03-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="28d03-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="28d03-155">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="28d03-155">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="28d03-156">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d03-156">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="28d03-157">包含服务统一消息服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="28d03-157">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
|[<span data-ttu-id="28d03-158">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d03-158">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="28d03-159">包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="28d03-159">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28d03-160">父元素</span><span class="sxs-lookup"><span data-stu-id="28d03-160">Parent elements</span></span>

|<span data-ttu-id="28d03-161">**元素**</span><span class="sxs-lookup"><span data-stu-id="28d03-161">**Element**</span></span>|<span data-ttu-id="28d03-162">**说明**</span><span class="sxs-lookup"><span data-stu-id="28d03-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28d03-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="28d03-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="28d03-164">包含服务配置响应消息的数组。</span><span class="sxs-lookup"><span data-stu-id="28d03-164">Contains an array of service configuration response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28d03-165">文本值</span><span class="sxs-lookup"><span data-stu-id="28d03-165">Text value</span></span>

<span data-ttu-id="28d03-166">无。</span><span class="sxs-lookup"><span data-stu-id="28d03-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28d03-167">备注</span><span class="sxs-lookup"><span data-stu-id="28d03-167">Remarks</span></span>

<span data-ttu-id="28d03-168">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="28d03-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28d03-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="28d03-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28d03-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="28d03-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28d03-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="28d03-171">Schema Name</span></span>  <br/> |<span data-ttu-id="28d03-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="28d03-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28d03-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="28d03-173">Validation File</span></span>  <br/> |<span data-ttu-id="28d03-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28d03-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28d03-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="28d03-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="28d03-176">False</span><span class="sxs-lookup"><span data-stu-id="28d03-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28d03-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28d03-177">See also</span></span>

- [<span data-ttu-id="28d03-178">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="28d03-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

