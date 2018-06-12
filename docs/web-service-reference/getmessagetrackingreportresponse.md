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
ms.openlocfilehash: bdb8b97e57f92a32cbdc498d09297920366b58bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754620"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="4ec75-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="4ec75-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="4ec75-104">**GetMessageTrackingReportResponse**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="4ec75-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
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

 <span data-ttu-id="4ec75-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4ec75-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ec75-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-106">Attributes and elements</span></span>

<span data-ttu-id="4ec75-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4ec75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ec75-108">属性</span><span class="sxs-lookup"><span data-stu-id="4ec75-108">Attributes</span></span>

|<span data-ttu-id="4ec75-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4ec75-109">**Attribute**</span></span>|<span data-ttu-id="4ec75-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ec75-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ec75-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4ec75-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4ec75-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="4ec75-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="4ec75-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="4ec75-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="4ec75-114">-成功</span><span class="sxs-lookup"><span data-stu-id="4ec75-114">-  Success</span></span>  <br/><span data-ttu-id="4ec75-115">-警告</span><span class="sxs-lookup"><span data-stu-id="4ec75-115">-  Warning</span></span>  <br/><span data-ttu-id="4ec75-116">-错误</span><span class="sxs-lookup"><span data-stu-id="4ec75-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4ec75-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="4ec75-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="4ec75-118">**值**</span><span class="sxs-lookup"><span data-stu-id="4ec75-118">**Value**</span></span>|<span data-ttu-id="4ec75-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ec75-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ec75-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="4ec75-120">**Success**</span></span> <br/> |<span data-ttu-id="4ec75-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="4ec75-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4ec75-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4ec75-122">**Warning**</span></span> <br/> | <span data-ttu-id="4ec75-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="4ec75-123">Describes a request that was not processed.</span></span> <span data-ttu-id="4ec75-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="4ec75-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="4ec75-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="4ec75-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="4ec75-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4ec75-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4ec75-127">-Active Directory 域服务 (AD DS) 于处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4ec75-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4ec75-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="4ec75-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="4ec75-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="4ec75-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4ec75-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="4ec75-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="4ec75-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="4ec75-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="4ec75-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="4ec75-132">**Error**</span></span> <br/> | <span data-ttu-id="4ec75-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="4ec75-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4ec75-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="4ec75-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="4ec75-135">无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="4ec75-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="4ec75-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="4ec75-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="4ec75-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="4ec75-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="4ec75-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4ec75-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="4ec75-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="4ec75-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="4ec75-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ec75-142">子元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-142">Child elements</span></span>

|<span data-ttu-id="4ec75-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ec75-143">**Element**</span></span>|<span data-ttu-id="4ec75-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ec75-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec75-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="4ec75-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4ec75-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="4ec75-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4ec75-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4ec75-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="4ec75-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4ec75-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4ec75-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4ec75-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="4ec75-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="4ec75-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4ec75-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4ec75-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="4ec75-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-154">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4ec75-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="4ec75-155">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="4ec75-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4ec75-156">诊断</span><span class="sxs-lookup"><span data-stu-id="4ec75-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="4ec75-157">提供用于报告数据中心中的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="4ec75-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-158">错误</span><span class="sxs-lookup"><span data-stu-id="4ec75-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4ec75-159">包含用于存储通过 Web 服务返回的错误的属性包。</span><span class="sxs-lookup"><span data-stu-id="4ec75-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="4ec75-160">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="4ec75-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="4ec75-161">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="4ec75-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ec75-162">父元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-162">Parent elements</span></span>

<span data-ttu-id="4ec75-163">无。</span><span class="sxs-lookup"><span data-stu-id="4ec75-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4ec75-164">文本值</span><span class="sxs-lookup"><span data-stu-id="4ec75-164">Text value</span></span>

<span data-ttu-id="4ec75-165">无。</span><span class="sxs-lookup"><span data-stu-id="4ec75-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ec75-166">备注</span><span class="sxs-lookup"><span data-stu-id="4ec75-166">Remarks</span></span>

<span data-ttu-id="4ec75-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4ec75-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ec75-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="4ec75-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ec75-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="4ec75-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ec75-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="4ec75-170">Schema Name</span></span>  <br/> |<span data-ttu-id="4ec75-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="4ec75-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ec75-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="4ec75-172">Validation File</span></span>  <br/> |<span data-ttu-id="4ec75-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4ec75-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ec75-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="4ec75-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ec75-175">False</span><span class="sxs-lookup"><span data-stu-id="4ec75-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ec75-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4ec75-176">See also</span></span>

- [<span data-ttu-id="4ec75-177">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="4ec75-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="4ec75-178">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4ec75-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

