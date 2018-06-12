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
description: FindMessageTrackingReportResponse 元素包含状态和单个 FindMessageTrackingReport 操作请求的结果。
ms.openlocfilehash: fa381f500eac9a46b11aea8c813f1ffc625a3bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754356"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="2366a-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="2366a-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="2366a-104">**FindMessageTrackingReportResponse**元素包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="2366a-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="2366a-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2366a-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2366a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2366a-106">Attributes and elements</span></span>

<span data-ttu-id="2366a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2366a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2366a-108">属性</span><span class="sxs-lookup"><span data-stu-id="2366a-108">Attributes</span></span>

|<span data-ttu-id="2366a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2366a-109">**Attribute**</span></span>|<span data-ttu-id="2366a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2366a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2366a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2366a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2366a-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="2366a-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="2366a-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="2366a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2366a-114">-成功</span><span class="sxs-lookup"><span data-stu-id="2366a-114">-  Success</span></span>  <br/><span data-ttu-id="2366a-115">-警告</span><span class="sxs-lookup"><span data-stu-id="2366a-115">-  Warning</span></span>  <br/><span data-ttu-id="2366a-116">-错误</span><span class="sxs-lookup"><span data-stu-id="2366a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2366a-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="2366a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="2366a-118">**值**</span><span class="sxs-lookup"><span data-stu-id="2366a-118">**Value**</span></span>|<span data-ttu-id="2366a-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="2366a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2366a-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="2366a-120">**Success**</span></span> <br/> |<span data-ttu-id="2366a-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="2366a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2366a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2366a-122">**Warning**</span></span> <br/> | <span data-ttu-id="2366a-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="2366a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="2366a-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="2366a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2366a-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="2366a-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="2366a-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2366a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2366a-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2366a-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2366a-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="2366a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="2366a-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="2366a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2366a-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="2366a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="2366a-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="2366a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="2366a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="2366a-132">**Error**</span></span> <br/> | <span data-ttu-id="2366a-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="2366a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2366a-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="2366a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2366a-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="2366a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2366a-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="2366a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="2366a-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="2366a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="2366a-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="2366a-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2366a-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="2366a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2366a-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="2366a-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2366a-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="2366a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2366a-142">子元素</span><span class="sxs-lookup"><span data-stu-id="2366a-142">Child elements</span></span>

|<span data-ttu-id="2366a-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="2366a-143">**Element**</span></span>|<span data-ttu-id="2366a-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="2366a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2366a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="2366a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2366a-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="2366a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2366a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2366a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2366a-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2366a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2366a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2366a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2366a-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="2366a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="2366a-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="2366a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2366a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2366a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2366a-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="2366a-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2366a-154">诊断</span><span class="sxs-lookup"><span data-stu-id="2366a-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="2366a-155">包含用于生成数据中心中的跟踪功能的各种统计报告的信息。</span><span class="sxs-lookup"><span data-stu-id="2366a-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="2366a-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="2366a-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="2366a-157">包含和匹配的搜索要求的邮件的数组。</span><span class="sxs-lookup"><span data-stu-id="2366a-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="2366a-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="2366a-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="2366a-159">包含执行从中获取搜索结果的搜索范围。</span><span class="sxs-lookup"><span data-stu-id="2366a-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="2366a-160">错误</span><span class="sxs-lookup"><span data-stu-id="2366a-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2366a-161">包含用于存储通过 Web 服务返回的错误的属性包。</span><span class="sxs-lookup"><span data-stu-id="2366a-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="2366a-162">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="2366a-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="2366a-163">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="2366a-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2366a-164">父元素</span><span class="sxs-lookup"><span data-stu-id="2366a-164">Parent elements</span></span>

<span data-ttu-id="2366a-165">无。</span><span class="sxs-lookup"><span data-stu-id="2366a-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2366a-166">文本值</span><span class="sxs-lookup"><span data-stu-id="2366a-166">Text value</span></span>

<span data-ttu-id="2366a-167">无。</span><span class="sxs-lookup"><span data-stu-id="2366a-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2366a-168">备注</span><span class="sxs-lookup"><span data-stu-id="2366a-168">Remarks</span></span>

<span data-ttu-id="2366a-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2366a-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2366a-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="2366a-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2366a-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="2366a-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2366a-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="2366a-172">Schema Name</span></span>  <br/> |<span data-ttu-id="2366a-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="2366a-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2366a-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="2366a-174">Validation File</span></span>  <br/> |<span data-ttu-id="2366a-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2366a-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2366a-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="2366a-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="2366a-177">False</span><span class="sxs-lookup"><span data-stu-id="2366a-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2366a-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2366a-178">See also</span></span>

- [<span data-ttu-id="2366a-179">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="2366a-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="2366a-180">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2366a-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

