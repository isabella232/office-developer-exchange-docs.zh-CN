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
description: ExpandDLResponseMessage 元素包含状态和单个 ExpandDL 操作请求的结果。
ms.openlocfilehash: 62a81574f9c513b905a92876b3d757c635b4f07b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754206"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="cf450-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf450-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="cf450-104">**ExpandDLResponseMessage**元素包含状态和的单个结果[ExpandDL 操作](expanddl-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="cf450-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="cf450-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="cf450-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="cf450-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf450-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="cf450-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf450-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="cf450-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf450-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cf450-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf450-109">Attributes and elements</span></span>

<span data-ttu-id="cf450-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf450-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf450-111">属性</span><span class="sxs-lookup"><span data-stu-id="cf450-111">Attributes</span></span>

|<span data-ttu-id="cf450-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="cf450-112">**Attribute**</span></span>|<span data-ttu-id="cf450-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf450-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf450-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf450-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf450-115">介绍[ExpandDL 操作](expanddl-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="cf450-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="cf450-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="cf450-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="cf450-117">-成功</span><span class="sxs-lookup"><span data-stu-id="cf450-117">-  Success</span></span>  <br/><span data-ttu-id="cf450-118">-警告</span><span class="sxs-lookup"><span data-stu-id="cf450-118">-  Warning</span></span>  <br/><span data-ttu-id="cf450-119">-错误</span><span class="sxs-lookup"><span data-stu-id="cf450-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="cf450-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="cf450-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="cf450-121">表示使用索引的分页视图时，则在下一个请求时应使用的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="cf450-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="cf450-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="cf450-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="cf450-123">代表要用于下一个请求时使用分数页面视图的新分子值。</span><span class="sxs-lookup"><span data-stu-id="cf450-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="cf450-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="cf450-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="cf450-125">代表下一步分母执行分数分页时用于下一个请求。</span><span class="sxs-lookup"><span data-stu-id="cf450-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="cf450-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="cf450-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="cf450-127">指示而无需其他分页。</span><span class="sxs-lookup"><span data-stu-id="cf450-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="cf450-128">此属性将当前结果包含在查询中的最后一项如果为 true。</span><span class="sxs-lookup"><span data-stu-id="cf450-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="cf450-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="cf450-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="cf450-130">表示超出限制的项目总数。</span><span class="sxs-lookup"><span data-stu-id="cf450-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cf450-131">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="cf450-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="cf450-132">**值**</span><span class="sxs-lookup"><span data-stu-id="cf450-132">**Value**</span></span>|<span data-ttu-id="cf450-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf450-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf450-134">**成功**</span><span class="sxs-lookup"><span data-stu-id="cf450-134">**Success**</span></span> <br/> |<span data-ttu-id="cf450-135">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="cf450-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf450-136">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cf450-136">**Warning**</span></span> <br/> | <span data-ttu-id="cf450-137">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="cf450-137">Describes a request that was not processed.</span></span> <span data-ttu-id="cf450-138">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="cf450-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="cf450-139">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="cf450-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="cf450-140">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="cf450-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cf450-141">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="cf450-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cf450-142">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="cf450-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="cf450-143">-邮箱数据库 (MDB) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="cf450-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cf450-144">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="cf450-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf450-145">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="cf450-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf450-146">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf450-146">**Error**</span></span> <br/> | <span data-ttu-id="cf450-147">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="cf450-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="cf450-148">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="cf450-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cf450-149">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="cf450-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf450-150">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="cf450-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="cf450-151">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="cf450-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="cf450-152">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="cf450-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="cf450-153">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="cf450-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf450-154">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="cf450-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="cf450-155">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="cf450-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf450-156">子元素</span><span class="sxs-lookup"><span data-stu-id="cf450-156">Child elements</span></span>

|<span data-ttu-id="cf450-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf450-157">**Element**</span></span>|<span data-ttu-id="cf450-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf450-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf450-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf450-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf450-160">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="cf450-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf450-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf450-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf450-162">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="cf450-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf450-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf450-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf450-164">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="cf450-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="cf450-165">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="cf450-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf450-166">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cf450-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf450-167">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="cf450-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cf450-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="cf450-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="cf450-169">包含通讯组列表包含的邮箱数组。</span><span class="sxs-lookup"><span data-stu-id="cf450-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf450-170">父元素</span><span class="sxs-lookup"><span data-stu-id="cf450-170">Parent elements</span></span>

|<span data-ttu-id="cf450-171">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf450-171">**Element**</span></span>|<span data-ttu-id="cf450-172">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf450-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf450-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf450-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cf450-174">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="cf450-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf450-175">备注</span><span class="sxs-lookup"><span data-stu-id="cf450-175">Remarks</span></span>

<span data-ttu-id="cf450-176">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cf450-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf450-177">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf450-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf450-178">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf450-178">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cf450-179">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf450-179">Schema Name</span></span>  <br/> |<span data-ttu-id="cf450-180">类型架构</span><span class="sxs-lookup"><span data-stu-id="cf450-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="cf450-181">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf450-181">Validation File</span></span>  <br/> |<span data-ttu-id="cf450-182">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cf450-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cf450-183">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf450-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf450-184">False</span><span class="sxs-lookup"><span data-stu-id="cf450-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf450-185">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf450-185">See also</span></span>

- [<span data-ttu-id="cf450-186">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="cf450-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="cf450-187">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="cf450-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="cf450-188">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cf450-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

