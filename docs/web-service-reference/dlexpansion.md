---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: DLExpansion 元素包含一个数组包含通讯组列表中的邮箱。
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753967"
---
# <a name="dlexpansion"></a><span data-ttu-id="a2f45-103">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="a2f45-103">DLExpansion</span></span>

<span data-ttu-id="a2f45-104">**DLExpansion**元素包含一个数组包含通讯组列表中的邮箱。</span><span class="sxs-lookup"><span data-stu-id="a2f45-104">The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list.</span></span> 
  
- [<span data-ttu-id="a2f45-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="a2f45-105">ExpandDLResponse</span></span>](expanddlresponse.md) 
- [<span data-ttu-id="a2f45-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2f45-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="a2f45-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2f45-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
- [<span data-ttu-id="a2f45-108">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="a2f45-108">DLExpansion</span></span>](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 <span data-ttu-id="a2f45-109">**ArrayOfDLExpansionType**</span><span class="sxs-lookup"><span data-stu-id="a2f45-109">**ArrayOfDLExpansionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2f45-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a2f45-110">Attributes and elements</span></span>

<span data-ttu-id="a2f45-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a2f45-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2f45-112">属性</span><span class="sxs-lookup"><span data-stu-id="a2f45-112">Attributes</span></span>

|<span data-ttu-id="a2f45-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="a2f45-113">**Attribute**</span></span>|<span data-ttu-id="a2f45-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2f45-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2f45-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="a2f45-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="a2f45-116">表示使用索引的页面视图时，则在下一个请求时应使用的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="a2f45-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="a2f45-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="a2f45-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="a2f45-118">代表要使用分数页面视图时使用的下一个请求的新分子值。</span><span class="sxs-lookup"><span data-stu-id="a2f45-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="a2f45-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="a2f45-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="a2f45-120">代表下一个分母使用分数页面视图时用于下一个请求。</span><span class="sxs-lookup"><span data-stu-id="a2f45-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="a2f45-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="a2f45-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="a2f45-122">指示当前结果是否包含在查询中的最后一项，以便不需要其他分页。</span><span class="sxs-lookup"><span data-stu-id="a2f45-122">Indicates whether the current results contain the last item in the query so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="a2f45-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="a2f45-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="a2f45-124">代表视图中的项目的总数。</span><span class="sxs-lookup"><span data-stu-id="a2f45-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a2f45-125">子元素</span><span class="sxs-lookup"><span data-stu-id="a2f45-125">Child elements</span></span>

|<span data-ttu-id="a2f45-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2f45-126">**Element**</span></span>|<span data-ttu-id="a2f45-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2f45-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2f45-128">Mailbox</span><span class="sxs-lookup"><span data-stu-id="a2f45-128">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="a2f45-129">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="a2f45-129">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2f45-130">父元素</span><span class="sxs-lookup"><span data-stu-id="a2f45-130">Parent elements</span></span>

|<span data-ttu-id="a2f45-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2f45-131">**Element**</span></span>|<span data-ttu-id="a2f45-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2f45-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2f45-133">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2f45-133">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md) <br/> |<span data-ttu-id="a2f45-134">包含状态和单个 ExpandDL 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a2f45-134">Contains the status and result of a single ExpandDL request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2f45-135">备注</span><span class="sxs-lookup"><span data-stu-id="a2f45-135">Remarks</span></span>

<span data-ttu-id="a2f45-136">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a2f45-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2f45-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="a2f45-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2f45-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="a2f45-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a2f45-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="a2f45-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a2f45-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="a2f45-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="a2f45-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="a2f45-141">Validation File</span></span>  <br/> |<span data-ttu-id="a2f45-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a2f45-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a2f45-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="a2f45-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a2f45-144">False</span><span class="sxs-lookup"><span data-stu-id="a2f45-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2f45-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a2f45-145">See also</span></span>

- [<span data-ttu-id="a2f45-146">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="a2f45-146">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="a2f45-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a2f45-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md) 
- [<span data-ttu-id="a2f45-148">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="a2f45-148">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

