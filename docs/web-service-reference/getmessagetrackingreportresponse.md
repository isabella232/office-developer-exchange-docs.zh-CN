---
title: GetMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReportResponse
api_type:
- schema
ms.assetid: 41177894-2008-44a6-86f8-bc34c0a48e36
description: GetMessageTrackingReportResponse 元素包含 GetMessageTrackingReport 操作的响应。
ms.openlocfilehash: 15e1f5c91c07dbaad224fb0cd3bc89f444a18087
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460566"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="52796-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="52796-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="52796-104">**GetMessageTrackingReportResponse**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="52796-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
```xml
<GetMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MessageTrackingReport/>
   <Diagnostics/>
   <Errors/>
   <Properties/>
</GetMessageTrackingReportResponse>
```

 <span data-ttu-id="52796-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="52796-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52796-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52796-106">Attributes and elements</span></span>

<span data-ttu-id="52796-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52796-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52796-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="52796-108">Attributes</span></span>

|<span data-ttu-id="52796-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="52796-109">**Attribute**</span></span>|<span data-ttu-id="52796-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="52796-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52796-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="52796-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="52796-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="52796-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="52796-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="52796-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="52796-114">-成功</span><span class="sxs-lookup"><span data-stu-id="52796-114">-  Success</span></span>  <br/><span data-ttu-id="52796-115">-警告</span><span class="sxs-lookup"><span data-stu-id="52796-115">-  Warning</span></span>  <br/><span data-ttu-id="52796-116">-错误</span><span class="sxs-lookup"><span data-stu-id="52796-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="52796-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="52796-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="52796-118">**值**</span><span class="sxs-lookup"><span data-stu-id="52796-118">**Value**</span></span>|<span data-ttu-id="52796-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="52796-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52796-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="52796-120">**Success**</span></span> <br/> |<span data-ttu-id="52796-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="52796-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="52796-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="52796-122">**Warning**</span></span> <br/> | <span data-ttu-id="52796-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="52796-123">Describes a request that was not processed.</span></span> <span data-ttu-id="52796-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="52796-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="52796-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="52796-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="52796-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="52796-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="52796-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="52796-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="52796-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="52796-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="52796-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="52796-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="52796-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="52796-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="52796-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="52796-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="52796-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="52796-132">**Error**</span></span> <br/> | <span data-ttu-id="52796-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="52796-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="52796-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="52796-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="52796-135">无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="52796-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="52796-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="52796-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="52796-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="52796-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="52796-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="52796-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="52796-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="52796-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="52796-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="52796-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="52796-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="52796-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52796-142">子元素</span><span class="sxs-lookup"><span data-stu-id="52796-142">Child elements</span></span>

|<span data-ttu-id="52796-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="52796-143">**Element**</span></span>|<span data-ttu-id="52796-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="52796-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52796-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="52796-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="52796-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="52796-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="52796-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="52796-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="52796-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="52796-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="52796-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="52796-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="52796-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="52796-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="52796-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="52796-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="52796-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="52796-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="52796-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="52796-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="52796-154">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="52796-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="52796-155">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="52796-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="52796-156">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="52796-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="52796-157">提供用于在数据中心中进行报告的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="52796-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="52796-158">错误</span><span class="sxs-lookup"><span data-stu-id="52796-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="52796-159">包含用于存储通过 Web 服务返回的错误的属性包。</span><span class="sxs-lookup"><span data-stu-id="52796-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="52796-160">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="52796-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="52796-161">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="52796-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52796-162">父元素</span><span class="sxs-lookup"><span data-stu-id="52796-162">Parent elements</span></span>

<span data-ttu-id="52796-163">无。</span><span class="sxs-lookup"><span data-stu-id="52796-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="52796-164">文本值</span><span class="sxs-lookup"><span data-stu-id="52796-164">Text value</span></span>

<span data-ttu-id="52796-165">无。</span><span class="sxs-lookup"><span data-stu-id="52796-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52796-166">说明</span><span class="sxs-lookup"><span data-stu-id="52796-166">Remarks</span></span>

<span data-ttu-id="52796-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52796-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52796-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="52796-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52796-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="52796-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52796-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="52796-170">Schema Name</span></span>  <br/> |<span data-ttu-id="52796-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="52796-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52796-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="52796-172">Validation File</span></span>  <br/> |<span data-ttu-id="52796-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52796-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52796-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="52796-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="52796-175">False</span><span class="sxs-lookup"><span data-stu-id="52796-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52796-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52796-176">See also</span></span>

- [<span data-ttu-id="52796-177">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="52796-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="52796-178">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52796-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

