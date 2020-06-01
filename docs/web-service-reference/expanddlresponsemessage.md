---
title: ExpandDLResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: ExpandDLResponseMessage 元素包含单个 ExpandDL 操作请求的状态和结果。
ms.openlocfilehash: e186c4e14cbb9c922a4d262c85c130b9c33ff939
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460636"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="b00c1-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b00c1-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="b00c1-104">**ExpandDLResponseMessage**元素包含单个[ExpandDL 操作](expanddl-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="b00c1-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="b00c1-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="b00c1-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="b00c1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b00c1-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="b00c1-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b00c1-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="b00c1-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b00c1-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b00c1-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-109">Attributes and elements</span></span>

<span data-ttu-id="b00c1-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b00c1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b00c1-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="b00c1-111">Attributes</span></span>

|<span data-ttu-id="b00c1-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="b00c1-112">**Attribute**</span></span>|<span data-ttu-id="b00c1-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="b00c1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b00c1-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b00c1-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b00c1-115">描述[ExpandDL 操作](expanddl-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="b00c1-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="b00c1-116">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="b00c1-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="b00c1-117">-成功</span><span class="sxs-lookup"><span data-stu-id="b00c1-117">-  Success</span></span>  <br/><span data-ttu-id="b00c1-118">-警告</span><span class="sxs-lookup"><span data-stu-id="b00c1-118">-  Warning</span></span>  <br/><span data-ttu-id="b00c1-119">-错误</span><span class="sxs-lookup"><span data-stu-id="b00c1-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="b00c1-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="b00c1-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="b00c1-121">表示在使用索引分页视图时应用于下一个请求的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="b00c1-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="b00c1-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="b00c1-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="b00c1-123">表示在使用分数页面视图时用于下一个请求的新分子值。</span><span class="sxs-lookup"><span data-stu-id="b00c1-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="b00c1-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="b00c1-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="b00c1-125">表示执行分数分页时用于下一个请求的下一个分母。</span><span class="sxs-lookup"><span data-stu-id="b00c1-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="b00c1-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="b00c1-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="b00c1-127">指示不需要其他分页。</span><span class="sxs-lookup"><span data-stu-id="b00c1-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="b00c1-128">如果当前结果包含查询中的最后一项，则此属性为 true。</span><span class="sxs-lookup"><span data-stu-id="b00c1-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="b00c1-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="b00c1-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="b00c1-130">表示传递限制的项目总数。</span><span class="sxs-lookup"><span data-stu-id="b00c1-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b00c1-131">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="b00c1-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="b00c1-132">**值**</span><span class="sxs-lookup"><span data-stu-id="b00c1-132">**Value**</span></span>|<span data-ttu-id="b00c1-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="b00c1-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b00c1-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="b00c1-134">**Success**</span></span> <br/> |<span data-ttu-id="b00c1-135">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="b00c1-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b00c1-136">**警告**</span><span class="sxs-lookup"><span data-stu-id="b00c1-136">**Warning**</span></span> <br/> | <span data-ttu-id="b00c1-137">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="b00c1-137">Describes a request that was not processed.</span></span> <span data-ttu-id="b00c1-138">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="b00c1-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="b00c1-139">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="b00c1-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="b00c1-140">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="b00c1-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b00c1-141">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="b00c1-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="b00c1-142">-移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="b00c1-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="b00c1-143">-邮箱数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="b00c1-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b00c1-144">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="b00c1-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="b00c1-145">-超出了配额。</span><span class="sxs-lookup"><span data-stu-id="b00c1-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="b00c1-146">**Error**</span><span class="sxs-lookup"><span data-stu-id="b00c1-146">**Error**</span></span> <br/> | <span data-ttu-id="b00c1-147">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="b00c1-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="b00c1-148">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="b00c1-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b00c1-149">-属性或元素无效</span><span class="sxs-lookup"><span data-stu-id="b00c1-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b00c1-150">-超出范围的属性或元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="b00c1-151">-未知标记</span><span class="sxs-lookup"><span data-stu-id="b00c1-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="b00c1-152">-上下文中无效的属性或元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="b00c1-153">-任何客户端进行未经授权的访问尝试</span><span class="sxs-lookup"><span data-stu-id="b00c1-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b00c1-154">-响应有效客户端调用的服务器端故障</span><span class="sxs-lookup"><span data-stu-id="b00c1-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="b00c1-155">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="b00c1-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b00c1-156">子元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-156">Child elements</span></span>

|<span data-ttu-id="b00c1-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="b00c1-157">**Element**</span></span>|<span data-ttu-id="b00c1-158">**描述**</span><span class="sxs-lookup"><span data-stu-id="b00c1-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b00c1-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="b00c1-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b00c1-160">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="b00c1-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b00c1-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b00c1-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b00c1-162">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="b00c1-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b00c1-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b00c1-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b00c1-164">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="b00c1-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="b00c1-165">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="b00c1-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b00c1-166">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b00c1-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b00c1-167">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="b00c1-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b00c1-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="b00c1-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="b00c1-169">包含通讯组列表包含的邮箱数组。</span><span class="sxs-lookup"><span data-stu-id="b00c1-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b00c1-170">父元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-170">Parent elements</span></span>

|<span data-ttu-id="b00c1-171">**元素**</span><span class="sxs-lookup"><span data-stu-id="b00c1-171">**Element**</span></span>|<span data-ttu-id="b00c1-172">**描述**</span><span class="sxs-lookup"><span data-stu-id="b00c1-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b00c1-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b00c1-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b00c1-174">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="b00c1-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b00c1-175">备注</span><span class="sxs-lookup"><span data-stu-id="b00c1-175">Remarks</span></span>

<span data-ttu-id="b00c1-176">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b00c1-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b00c1-177">元素信息</span><span class="sxs-lookup"><span data-stu-id="b00c1-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b00c1-178">命名空间</span><span class="sxs-lookup"><span data-stu-id="b00c1-178">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b00c1-179">架构名称</span><span class="sxs-lookup"><span data-stu-id="b00c1-179">Schema Name</span></span>  <br/> |<span data-ttu-id="b00c1-180">类型架构</span><span class="sxs-lookup"><span data-stu-id="b00c1-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="b00c1-181">验证文件</span><span class="sxs-lookup"><span data-stu-id="b00c1-181">Validation File</span></span>  <br/> |<span data-ttu-id="b00c1-182">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b00c1-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b00c1-183">可以为空</span><span class="sxs-lookup"><span data-stu-id="b00c1-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="b00c1-184">False</span><span class="sxs-lookup"><span data-stu-id="b00c1-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b00c1-185">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b00c1-185">See also</span></span>

- [<span data-ttu-id="b00c1-186">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="b00c1-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="b00c1-187">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="b00c1-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="b00c1-188">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b00c1-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

