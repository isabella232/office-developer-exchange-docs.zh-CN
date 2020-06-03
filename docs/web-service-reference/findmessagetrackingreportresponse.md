---
title: FindMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReportResponse
api_type:
- schema
ms.assetid: ed4265dc-0e79-4b34-8bf4-88a94875629d
description: FindMessageTrackingReportResponse 元素包含单个 FindMessageTrackingReport 操作请求的状态和结果。
ms.openlocfilehash: a72ae3b20f2cae3d37a90da36b816e6f3265c716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462913"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="e2dcb-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="e2dcb-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="e2dcb-104">**FindMessageTrackingReportResponse**元素包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
```xml
<FindMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Diagnostics/>
   <MessageTrackingSearchResults/>
   <Errors/>
   <Properties/>
</FindMessageTrackingReportResponse>
```

 <span data-ttu-id="e2dcb-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2dcb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-106">Attributes and elements</span></span>

<span data-ttu-id="e2dcb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2dcb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e2dcb-108">Attributes</span></span>

|<span data-ttu-id="e2dcb-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-109">**Attribute**</span></span>|<span data-ttu-id="e2dcb-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2dcb-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e2dcb-112">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="e2dcb-113">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="e2dcb-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e2dcb-114">-成功</span><span class="sxs-lookup"><span data-stu-id="e2dcb-114">-  Success</span></span>  <br/><span data-ttu-id="e2dcb-115">-警告</span><span class="sxs-lookup"><span data-stu-id="e2dcb-115">-  Warning</span></span>  <br/><span data-ttu-id="e2dcb-116">-错误</span><span class="sxs-lookup"><span data-stu-id="e2dcb-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e2dcb-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="e2dcb-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="e2dcb-118">**值**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-118">**Value**</span></span>|<span data-ttu-id="e2dcb-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2dcb-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-120">**Success**</span></span> <br/> |<span data-ttu-id="e2dcb-121">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e2dcb-122">**警告**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-122">**Warning**</span></span> <br/> | <span data-ttu-id="e2dcb-123">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-123">Describes a request that was not processed.</span></span> <span data-ttu-id="e2dcb-124">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e2dcb-125">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="e2dcb-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="e2dcb-126">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e2dcb-127">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e2dcb-128">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e2dcb-129">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e2dcb-130">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="e2dcb-131">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e2dcb-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-132">**Error**</span></span> <br/> | <span data-ttu-id="e2dcb-133">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e2dcb-134">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="e2dcb-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e2dcb-135">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="e2dcb-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e2dcb-136">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="e2dcb-137">-未知标记</span><span class="sxs-lookup"><span data-stu-id="e2dcb-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="e2dcb-138">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e2dcb-139">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="e2dcb-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e2dcb-140">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="e2dcb-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="e2dcb-141">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2dcb-142">子元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-142">Child elements</span></span>

|<span data-ttu-id="e2dcb-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-143">**Element**</span></span>|<span data-ttu-id="e2dcb-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="e2dcb-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2dcb-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="e2dcb-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e2dcb-146">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2dcb-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e2dcb-148">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e2dcb-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e2dcb-150">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e2dcb-151">此元素包含值0。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e2dcb-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e2dcb-153">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-154">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="e2dcb-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="e2dcb-155">包含将用于生成数据中心中的跟踪功能的各种统计报告的信息。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="e2dcb-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="e2dcb-157">包含与搜索要求相匹配的邮件的和数组。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="e2dcb-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="e2dcb-159">包含为获取搜索结果而执行的搜索的范围。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-160">错误</span><span class="sxs-lookup"><span data-stu-id="e2dcb-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e2dcb-161">包含用于存储通过 Web 服务返回的错误的属性包。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="e2dcb-162">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="e2dcb-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="e2dcb-163">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2dcb-164">父元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-164">Parent elements</span></span>

<span data-ttu-id="e2dcb-165">无。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e2dcb-166">文本值</span><span class="sxs-lookup"><span data-stu-id="e2dcb-166">Text value</span></span>

<span data-ttu-id="e2dcb-167">无。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2dcb-168">说明</span><span class="sxs-lookup"><span data-stu-id="e2dcb-168">Remarks</span></span>

<span data-ttu-id="e2dcb-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e2dcb-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2dcb-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="e2dcb-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2dcb-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="e2dcb-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e2dcb-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="e2dcb-172">Schema Name</span></span>  <br/> |<span data-ttu-id="e2dcb-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="e2dcb-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e2dcb-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="e2dcb-174">Validation File</span></span>  <br/> |<span data-ttu-id="e2dcb-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e2dcb-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2dcb-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="e2dcb-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2dcb-177">False</span><span class="sxs-lookup"><span data-stu-id="e2dcb-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2dcb-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2dcb-178">See also</span></span>

- [<span data-ttu-id="e2dcb-179">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="e2dcb-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="e2dcb-180">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e2dcb-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

