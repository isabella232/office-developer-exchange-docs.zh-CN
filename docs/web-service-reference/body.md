---
title: Body
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: Body 元素指定项的正文。
ms.openlocfilehash: c565c5701ae5bc210cf0a9dc694108752860e24b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529488"
---
# <a name="body"></a><span data-ttu-id="13cb3-103">正文</span><span class="sxs-lookup"><span data-stu-id="13cb3-103">Body</span></span>

<span data-ttu-id="13cb3-104">**Body**元素指定项的正文。</span><span class="sxs-lookup"><span data-stu-id="13cb3-104">The **Body** element specifies the body of an item.</span></span> 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 <span data-ttu-id="13cb3-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="13cb3-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13cb3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="13cb3-106">Attributes and elements</span></span>

<span data-ttu-id="13cb3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="13cb3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13cb3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="13cb3-108">Attributes</span></span>

|<span data-ttu-id="13cb3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="13cb3-109">**Attribute**</span></span>|<span data-ttu-id="13cb3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="13cb3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb3-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="13cb3-111">BodyType</span></span>  <br/> |<span data-ttu-id="13cb3-112">指定正文的类型。</span><span class="sxs-lookup"><span data-stu-id="13cb3-112">Specifies the type of the body.</span></span>  <br/> |
|<span data-ttu-id="13cb3-113">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="13cb3-113">IsTruncated</span></span>  <br/> |<span data-ttu-id="13cb3-114">指示正文是否被截断的布尔值。</span><span class="sxs-lookup"><span data-stu-id="13cb3-114">Boolean value that indicates whether the body is truncated.</span></span>  <br/> |
   
#### <a name="bodytype"></a><span data-ttu-id="13cb3-115">BodyType</span><span class="sxs-lookup"><span data-stu-id="13cb3-115">BodyType</span></span>

|<span data-ttu-id="13cb3-116">**值**</span><span class="sxs-lookup"><span data-stu-id="13cb3-116">**Value**</span></span>|<span data-ttu-id="13cb3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="13cb3-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb3-118">HTML</span><span class="sxs-lookup"><span data-stu-id="13cb3-118">HTML</span></span>  <br/> |<span data-ttu-id="13cb3-119">指示正文位于 HTML 中。</span><span class="sxs-lookup"><span data-stu-id="13cb3-119">Indicates that the body is in HTML.</span></span>  <br/> |
|<span data-ttu-id="13cb3-120">文本</span><span class="sxs-lookup"><span data-stu-id="13cb3-120">Text</span></span>  <br/> |<span data-ttu-id="13cb3-121">指示正文在文本中。</span><span class="sxs-lookup"><span data-stu-id="13cb3-121">Indicates that the body is in text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13cb3-122">子元素</span><span class="sxs-lookup"><span data-stu-id="13cb3-122">Child elements</span></span>

<span data-ttu-id="13cb3-123">无。</span><span class="sxs-lookup"><span data-stu-id="13cb3-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13cb3-124">父元素</span><span class="sxs-lookup"><span data-stu-id="13cb3-124">Parent elements</span></span>

|<span data-ttu-id="13cb3-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="13cb3-125">**Element**</span></span>|<span data-ttu-id="13cb3-126">**描述**</span><span class="sxs-lookup"><span data-stu-id="13cb3-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13cb3-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="13cb3-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="13cb3-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="13cb3-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-129">联系人</span><span class="sxs-lookup"><span data-stu-id="13cb3-129">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="13cb3-130">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="13cb3-130">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-131">DistributionList</span><span class="sxs-lookup"><span data-stu-id="13cb3-131">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="13cb3-132">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="13cb3-132">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-133">项</span><span class="sxs-lookup"><span data-stu-id="13cb3-133">Item</span></span>](item.md) <br/> |<span data-ttu-id="13cb3-134">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="13cb3-134">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-135">消息</span><span class="sxs-lookup"><span data-stu-id="13cb3-135">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="13cb3-136">表示 Microsoft Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="13cb3-136">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-137">PostItem</span><span class="sxs-lookup"><span data-stu-id="13cb3-137">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="13cb3-138">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="13cb3-138">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="13cb3-139">任务</span><span class="sxs-lookup"><span data-stu-id="13cb3-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="13cb3-140">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="13cb3-140">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13cb3-141">文本值</span><span class="sxs-lookup"><span data-stu-id="13cb3-141">Text value</span></span>

<span data-ttu-id="13cb3-142">**Body**元素的文本值是项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="13cb3-142">The text value of the **Body** element is the body content of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13cb3-143">备注</span><span class="sxs-lookup"><span data-stu-id="13cb3-143">Remarks</span></span>

<span data-ttu-id="13cb3-144">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="13cb3-144">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="13cb3-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="13cb3-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13cb3-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="13cb3-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13cb3-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="13cb3-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13cb3-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="13cb3-148">Schema Name</span></span>  <br/> |<span data-ttu-id="13cb3-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="13cb3-149">Type schema</span></span>  <br/> |
|<span data-ttu-id="13cb3-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="13cb3-150">Validation File</span></span>  <br/> |<span data-ttu-id="13cb3-151">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="13cb3-151">types.xsd</span></span>  <br/> |
|<span data-ttu-id="13cb3-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="13cb3-152">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="13cb3-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="13cb3-153">See also</span></span>



- [<span data-ttu-id="13cb3-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="13cb3-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

