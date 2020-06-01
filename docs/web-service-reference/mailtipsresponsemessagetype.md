---
title: MailTipsResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: MailTipsResponseMessageType 元素表示邮件提示设置。
ms.openlocfilehash: 5244f26ef927a817a9087c299fd1124acb828aa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454034"
---
# <a name="mailtipsresponsemessagetype"></a><span data-ttu-id="f036a-103">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="f036a-103">MailTipsResponseMessageType</span></span>

<span data-ttu-id="f036a-104">**MailTipsResponseMessageType**元素表示邮件提示设置。</span><span class="sxs-lookup"><span data-stu-id="f036a-104">The **MailTipsResponseMessageType** element represents mail tips settings.</span></span> 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 <span data-ttu-id="f036a-105">**MailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f036a-105">**MailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f036a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f036a-106">Attributes and elements</span></span>

<span data-ttu-id="f036a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f036a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f036a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f036a-108">Attributes</span></span>

|<span data-ttu-id="f036a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f036a-109">**Attribute**</span></span>|<span data-ttu-id="f036a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f036a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f036a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f036a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f036a-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="f036a-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="f036a-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="f036a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="f036a-114">-成功</span><span class="sxs-lookup"><span data-stu-id="f036a-114">-  Success</span></span>  <br/><span data-ttu-id="f036a-115">-警告</span><span class="sxs-lookup"><span data-stu-id="f036a-115">-  Warning</span></span>  <br/><span data-ttu-id="f036a-116">-错误</span><span class="sxs-lookup"><span data-stu-id="f036a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f036a-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="f036a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="f036a-118">**值**</span><span class="sxs-lookup"><span data-stu-id="f036a-118">**Value**</span></span>|<span data-ttu-id="f036a-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f036a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f036a-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="f036a-120">**Success**</span></span> <br/> |<span data-ttu-id="f036a-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="f036a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f036a-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="f036a-122">**Warning**</span></span> <br/> | <span data-ttu-id="f036a-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="f036a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="f036a-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="f036a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="f036a-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="f036a-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="f036a-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f036a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="f036a-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f036a-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="f036a-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="f036a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="f036a-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="f036a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="f036a-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="f036a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="f036a-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="f036a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="f036a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="f036a-132">**Error**</span></span> <br/> | <span data-ttu-id="f036a-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="f036a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="f036a-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="f036a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f036a-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="f036a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f036a-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="f036a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="f036a-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="f036a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="f036a-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="f036a-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="f036a-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="f036a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f036a-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="f036a-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="f036a-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="f036a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f036a-142">子元素</span><span class="sxs-lookup"><span data-stu-id="f036a-142">Child elements</span></span>

|<span data-ttu-id="f036a-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="f036a-143">**Element**</span></span>|<span data-ttu-id="f036a-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="f036a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f036a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="f036a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f036a-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="f036a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f036a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f036a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f036a-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f036a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f036a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f036a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f036a-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="f036a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="f036a-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="f036a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f036a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f036a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f036a-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="f036a-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f036a-154">邮件提示</span><span class="sxs-lookup"><span data-stu-id="f036a-154">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="f036a-155">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="f036a-155">Represents values for various types of mail tips.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f036a-156">父元素</span><span class="sxs-lookup"><span data-stu-id="f036a-156">Parent elements</span></span>

|<span data-ttu-id="f036a-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="f036a-157">**Element**</span></span>|<span data-ttu-id="f036a-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="f036a-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f036a-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="f036a-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="f036a-160">表示邮件提示响应邮件的列表。</span><span class="sxs-lookup"><span data-stu-id="f036a-160">Represents a list of mail tips response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f036a-161">文本值</span><span class="sxs-lookup"><span data-stu-id="f036a-161">Text value</span></span>

<span data-ttu-id="f036a-162">无。</span><span class="sxs-lookup"><span data-stu-id="f036a-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f036a-163">说明</span><span class="sxs-lookup"><span data-stu-id="f036a-163">Remarks</span></span>

<span data-ttu-id="f036a-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f036a-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f036a-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="f036a-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f036a-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="f036a-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f036a-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="f036a-167">Schema Name</span></span>  <br/> |<span data-ttu-id="f036a-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="f036a-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f036a-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="f036a-169">Validation File</span></span>  <br/> |<span data-ttu-id="f036a-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f036a-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f036a-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="f036a-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="f036a-172">False</span><span class="sxs-lookup"><span data-stu-id="f036a-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f036a-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f036a-173">See also</span></span>

- [<span data-ttu-id="f036a-174">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f036a-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

