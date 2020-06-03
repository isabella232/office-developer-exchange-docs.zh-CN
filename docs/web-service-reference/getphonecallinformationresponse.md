---
title: GetPhoneCallInformationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformationResponse
api_type:
- schema
ms.assetid: 17f79875-46ec-4289-b974-b3c35af429cd
description: GetPhoneCallInformationResponse 元素定义对单个 GetPhoneCallInformation 请求的响应。
ms.openlocfilehash: 5bc060504ea734ec2d7e01707ef6bbdb0aa665d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457884"
---
# <a name="getphonecallinformationresponse"></a><span data-ttu-id="42fff-103">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="42fff-103">GetPhoneCallInformationResponse</span></span>

<span data-ttu-id="42fff-104">**GetPhoneCallInformationResponse**元素定义对单个 GetPhoneCallInformation 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="42fff-104">The **GetPhoneCallInformationResponse** element defines a response to a single GetPhoneCallInformation request.</span></span> 
  
```xml
<GetPhoneCallInformationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <PhoneCallInformation/>
</GetPhoneCallInformationResponse>
```

 <span data-ttu-id="42fff-105">**GetPhoneCallInformationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="42fff-105">**GetPhoneCallInformationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42fff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="42fff-106">Attributes and elements</span></span>

<span data-ttu-id="42fff-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="42fff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42fff-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="42fff-108">Attributes</span></span>

|<span data-ttu-id="42fff-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="42fff-109">**Attribute**</span></span>|<span data-ttu-id="42fff-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fff-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42fff-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="42fff-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="42fff-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="42fff-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="42fff-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="42fff-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="42fff-114">-成功</span><span class="sxs-lookup"><span data-stu-id="42fff-114">-  Success</span></span>  <br/><span data-ttu-id="42fff-115">-警告</span><span class="sxs-lookup"><span data-stu-id="42fff-115">-  Warning</span></span>  <br/><span data-ttu-id="42fff-116">-错误</span><span class="sxs-lookup"><span data-stu-id="42fff-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="42fff-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="42fff-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="42fff-118">**值**</span><span class="sxs-lookup"><span data-stu-id="42fff-118">**Value**</span></span>|<span data-ttu-id="42fff-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="42fff-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42fff-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="42fff-120">**Success**</span></span> <br/> |<span data-ttu-id="42fff-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="42fff-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="42fff-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="42fff-122">**Warning**</span></span> <br/> | <span data-ttu-id="42fff-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="42fff-123">Describes a request that was not processed.</span></span> <span data-ttu-id="42fff-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="42fff-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="42fff-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="42fff-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="42fff-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="42fff-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="42fff-127">-Active Directory 目录服务脱机。</span><span class="sxs-lookup"><span data-stu-id="42fff-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="42fff-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="42fff-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="42fff-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="42fff-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="42fff-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="42fff-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="42fff-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="42fff-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="42fff-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="42fff-132">**Error**</span></span> <br/> | <span data-ttu-id="42fff-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="42fff-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="42fff-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="42fff-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="42fff-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="42fff-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="42fff-136">-属性或元素越界</span><span class="sxs-lookup"><span data-stu-id="42fff-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="42fff-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="42fff-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="42fff-138">-Context 中的属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="42fff-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="42fff-139">-任何客户端的未经授权访问尝试</span><span class="sxs-lookup"><span data-stu-id="42fff-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="42fff-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="42fff-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="42fff-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="42fff-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="42fff-142">子元素</span><span class="sxs-lookup"><span data-stu-id="42fff-142">Child elements</span></span>

|<span data-ttu-id="42fff-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="42fff-143">**Element**</span></span>|<span data-ttu-id="42fff-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="42fff-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42fff-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="42fff-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="42fff-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="42fff-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="42fff-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="42fff-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="42fff-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="42fff-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="42fff-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="42fff-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="42fff-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="42fff-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="42fff-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="42fff-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="42fff-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="42fff-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="42fff-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="42fff-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="42fff-154">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="42fff-154">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="42fff-155">指定电话呼叫的状态信息。</span><span class="sxs-lookup"><span data-stu-id="42fff-155">Specifies the state information for a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42fff-156">父元素</span><span class="sxs-lookup"><span data-stu-id="42fff-156">Parent elements</span></span>

<span data-ttu-id="42fff-157">无。</span><span class="sxs-lookup"><span data-stu-id="42fff-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42fff-158">说明</span><span class="sxs-lookup"><span data-stu-id="42fff-158">Remarks</span></span>

<span data-ttu-id="42fff-159">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="42fff-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42fff-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="42fff-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42fff-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="42fff-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42fff-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="42fff-162">Schema Name</span></span>  <br/> |<span data-ttu-id="42fff-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="42fff-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42fff-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="42fff-164">Validation File</span></span>  <br/> |<span data-ttu-id="42fff-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="42fff-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42fff-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="42fff-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="42fff-167">False</span><span class="sxs-lookup"><span data-stu-id="42fff-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42fff-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42fff-168">See also</span></span>

- [<span data-ttu-id="42fff-169">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="42fff-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

