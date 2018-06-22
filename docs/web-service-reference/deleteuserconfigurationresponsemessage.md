---
title: DeleteUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 543b1743-7e1c-4acb-93bd-34532e7fe79b
description: DeleteUserConfigurationResponseMessage 元素包含状态和单个 DeleteUserConfiguration 请求的结果。
ms.openlocfilehash: 3e07917688ad1f25f7ca3fa06d6db51cf9905503
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753826"
---
# <a name="deleteuserconfigurationresponsemessage"></a><span data-ttu-id="ed65b-103">DeleteUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ed65b-103">DeleteUserConfigurationResponseMessage</span></span>

<span data-ttu-id="ed65b-104">**DeleteUserConfigurationResponseMessage**元素包含状态和单个**DeleteUserConfiguration**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="ed65b-104">The **DeleteUserConfigurationResponseMessage** element contains the status and result of a single **DeleteUserConfiguration** request.</span></span> 
  
```xml
<DeleteUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteUserConfigurationResponseMessage>
```

 <span data-ttu-id="ed65b-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ed65b-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed65b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-106">Attributes and elements</span></span>

<span data-ttu-id="ed65b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed65b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed65b-108">属性</span><span class="sxs-lookup"><span data-stu-id="ed65b-108">Attributes</span></span>

|<span data-ttu-id="ed65b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ed65b-109">**Attribute**</span></span>|<span data-ttu-id="ed65b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed65b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed65b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ed65b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ed65b-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="ed65b-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="ed65b-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="ed65b-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="ed65b-114">-成功</span><span class="sxs-lookup"><span data-stu-id="ed65b-114">-  Success</span></span>  <br/><span data-ttu-id="ed65b-115">-警告</span><span class="sxs-lookup"><span data-stu-id="ed65b-115">-  Warning</span></span>  <br/><span data-ttu-id="ed65b-116">-错误</span><span class="sxs-lookup"><span data-stu-id="ed65b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ed65b-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="ed65b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ed65b-118">**值**</span><span class="sxs-lookup"><span data-stu-id="ed65b-118">**Value**</span></span>|<span data-ttu-id="ed65b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed65b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed65b-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="ed65b-120">**Success**</span></span> <br/> |<span data-ttu-id="ed65b-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="ed65b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ed65b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ed65b-122">**Warning**</span></span> <br/> | <span data-ttu-id="ed65b-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="ed65b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ed65b-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="ed65b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="ed65b-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="ed65b-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="ed65b-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ed65b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ed65b-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ed65b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ed65b-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="ed65b-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ed65b-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ed65b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ed65b-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="ed65b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ed65b-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="ed65b-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ed65b-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ed65b-132">**Error**</span></span> <br/> | <span data-ttu-id="ed65b-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="ed65b-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="ed65b-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="ed65b-134">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="ed65b-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ed65b-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ed65b-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="ed65b-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ed65b-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ed65b-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="ed65b-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ed65b-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="ed65b-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="ed65b-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="ed65b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed65b-142">子元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-142">Child elements</span></span>

|<span data-ttu-id="ed65b-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed65b-143">**Element**</span></span>|<span data-ttu-id="ed65b-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed65b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed65b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ed65b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ed65b-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="ed65b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ed65b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ed65b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ed65b-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="ed65b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ed65b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ed65b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ed65b-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="ed65b-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ed65b-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="ed65b-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ed65b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ed65b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ed65b-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="ed65b-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed65b-154">父元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-154">Parent elements</span></span>

|<span data-ttu-id="ed65b-155">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed65b-155">**Element**</span></span>|<span data-ttu-id="ed65b-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed65b-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed65b-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ed65b-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ed65b-158">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ed65b-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed65b-159">文本值</span><span class="sxs-lookup"><span data-stu-id="ed65b-159">Text value</span></span>

<span data-ttu-id="ed65b-160">无。</span><span class="sxs-lookup"><span data-stu-id="ed65b-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed65b-161">备注</span><span class="sxs-lookup"><span data-stu-id="ed65b-161">Remarks</span></span>

<span data-ttu-id="ed65b-162">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ed65b-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed65b-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="ed65b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed65b-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="ed65b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed65b-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="ed65b-165">Schema Name</span></span>  <br/> |<span data-ttu-id="ed65b-166">消息架构</span><span class="sxs-lookup"><span data-stu-id="ed65b-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed65b-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="ed65b-167">Validation File</span></span>  <br/> |<span data-ttu-id="ed65b-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed65b-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed65b-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="ed65b-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed65b-170">False</span><span class="sxs-lookup"><span data-stu-id="ed65b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed65b-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed65b-171">See also</span></span>

- [<span data-ttu-id="ed65b-172">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ed65b-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

