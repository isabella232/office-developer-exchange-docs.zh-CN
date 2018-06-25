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
ms.openlocfilehash: 5a03d63198cd00997b8975b18a5ae0eb5fca1af2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754663"
---
# <a name="getphonecallinformationresponse"></a><span data-ttu-id="bb4f8-103">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="bb4f8-103">GetPhoneCallInformationResponse</span></span>

<span data-ttu-id="bb4f8-104">**GetPhoneCallInformationResponse**元素定义对单个 GetPhoneCallInformation 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-104">The **GetPhoneCallInformationResponse** element defines a response to a single GetPhoneCallInformation request.</span></span> 
  
```xml
<GetPhoneCallInformationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <PhoneCallInformation/>
</GetPhoneCallInformationResponse>
```

 <span data-ttu-id="bb4f8-105">**GetPhoneCallInformationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-105">**GetPhoneCallInformationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb4f8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-106">Attributes and elements</span></span>

<span data-ttu-id="bb4f8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb4f8-108">属性</span><span class="sxs-lookup"><span data-stu-id="bb4f8-108">Attributes</span></span>

|<span data-ttu-id="bb4f8-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-109">**Attribute**</span></span>|<span data-ttu-id="bb4f8-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb4f8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bb4f8-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="bb4f8-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="bb4f8-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="bb4f8-114">-成功</span><span class="sxs-lookup"><span data-stu-id="bb4f8-114">-  Success</span></span>  <br/><span data-ttu-id="bb4f8-115">-警告</span><span class="sxs-lookup"><span data-stu-id="bb4f8-115">-  Warning</span></span>  <br/><span data-ttu-id="bb4f8-116">-错误</span><span class="sxs-lookup"><span data-stu-id="bb4f8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="bb4f8-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="bb4f8-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="bb4f8-118">**值**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-118">**Value**</span></span>|<span data-ttu-id="bb4f8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb4f8-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-120">**Success**</span></span> <br/> |<span data-ttu-id="bb4f8-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bb4f8-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-122">**Warning**</span></span> <br/> | <span data-ttu-id="bb4f8-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="bb4f8-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="bb4f8-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="bb4f8-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="bb4f8-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="bb4f8-127">-Active Directory 目录服务处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="bb4f8-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="bb4f8-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="bb4f8-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="bb4f8-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="bb4f8-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-132">**Error**</span></span> <br/> | <span data-ttu-id="bb4f8-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="bb4f8-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="bb4f8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bb4f8-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bb4f8-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="bb4f8-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="bb4f8-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="bb4f8-138">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="bb4f8-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="bb4f8-139">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="bb4f8-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bb4f8-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="bb4f8-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="bb4f8-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb4f8-142">子元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-142">Child elements</span></span>

|<span data-ttu-id="bb4f8-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-143">**Element**</span></span>|<span data-ttu-id="bb4f8-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb4f8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb4f8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="bb4f8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bb4f8-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bb4f8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bb4f8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bb4f8-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="bb4f8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bb4f8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bb4f8-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="bb4f8-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bb4f8-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bb4f8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bb4f8-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bb4f8-154">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="bb4f8-154">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="bb4f8-155">指定的电话的状态信息。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-155">Specifies the state information for a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb4f8-156">父元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-156">Parent elements</span></span>

<span data-ttu-id="bb4f8-157">无。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb4f8-158">注解</span><span class="sxs-lookup"><span data-stu-id="bb4f8-158">Remarks</span></span>

<span data-ttu-id="bb4f8-159">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bb4f8-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb4f8-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="bb4f8-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb4f8-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="bb4f8-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb4f8-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="bb4f8-162">Schema Name</span></span>  <br/> |<span data-ttu-id="bb4f8-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="bb4f8-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb4f8-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="bb4f8-164">Validation File</span></span>  <br/> |<span data-ttu-id="bb4f8-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bb4f8-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb4f8-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="bb4f8-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb4f8-167">False</span><span class="sxs-lookup"><span data-stu-id="bb4f8-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb4f8-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb4f8-168">See also</span></span>

- [<span data-ttu-id="bb4f8-169">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bb4f8-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

