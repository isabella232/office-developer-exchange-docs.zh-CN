---
title: Body
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: Body 元素指定项目的正文。
ms.openlocfilehash: a4803c0e5ac3b027396983a5524241590eac35f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753351"
---
# <a name="body"></a><span data-ttu-id="c8bd3-103">正文</span><span class="sxs-lookup"><span data-stu-id="c8bd3-103">Body</span></span>

<span data-ttu-id="c8bd3-104">**Body**元素指定项目的正文。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-104">The **Body** element specifies the body of an item.</span></span> 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 <span data-ttu-id="c8bd3-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8bd3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c8bd3-106">Attributes and elements</span></span>

<span data-ttu-id="c8bd3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8bd3-108">属性</span><span class="sxs-lookup"><span data-stu-id="c8bd3-108">Attributes</span></span>

|<span data-ttu-id="c8bd3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-109">**Attribute**</span></span>|<span data-ttu-id="c8bd3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8bd3-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="c8bd3-111">BodyType</span></span>  <br/> |<span data-ttu-id="c8bd3-112">指定主体的类型。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-112">Specifies the type of the body.</span></span>  <br/> |
|<span data-ttu-id="c8bd3-113">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="c8bd3-113">IsTruncated</span></span>  <br/> |<span data-ttu-id="c8bd3-114">布尔值，该值指示是否正文会被截断。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-114">Boolean value that indicates whether the body is truncated.</span></span>  <br/> |
   
#### <a name="bodytype"></a><span data-ttu-id="c8bd3-115">BodyType</span><span class="sxs-lookup"><span data-stu-id="c8bd3-115">BodyType</span></span>

|<span data-ttu-id="c8bd3-116">**值**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-116">**Value**</span></span>|<span data-ttu-id="c8bd3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8bd3-118">HTML</span><span class="sxs-lookup"><span data-stu-id="c8bd3-118">HTML</span></span>  <br/> |<span data-ttu-id="c8bd3-119">指示正文采用 HTML。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-119">Indicates that the body is in HTML.</span></span>  <br/> |
|<span data-ttu-id="c8bd3-120">Text</span><span class="sxs-lookup"><span data-stu-id="c8bd3-120">Text</span></span>  <br/> |<span data-ttu-id="c8bd3-121">指示正文文本中。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-121">Indicates that the body is in text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8bd3-122">子元素</span><span class="sxs-lookup"><span data-stu-id="c8bd3-122">Child elements</span></span>

<span data-ttu-id="c8bd3-123">无。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8bd3-124">父元素</span><span class="sxs-lookup"><span data-stu-id="c8bd3-124">Parent elements</span></span>

|<span data-ttu-id="c8bd3-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-125">**Element**</span></span>|<span data-ttu-id="c8bd3-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8bd3-127">日历项目</span><span class="sxs-lookup"><span data-stu-id="c8bd3-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c8bd3-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-129">联系人</span><span class="sxs-lookup"><span data-stu-id="c8bd3-129">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c8bd3-130">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-130">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-131">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c8bd3-131">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c8bd3-132">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-132">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-133">Item</span><span class="sxs-lookup"><span data-stu-id="c8bd3-133">Item</span></span>](item.md) <br/> |<span data-ttu-id="c8bd3-134">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-134">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-135">Message</span><span class="sxs-lookup"><span data-stu-id="c8bd3-135">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c8bd3-136">代表 Microsoft Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-136">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-137">PostItem</span><span class="sxs-lookup"><span data-stu-id="c8bd3-137">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="c8bd3-138">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-138">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8bd3-139">任务</span><span class="sxs-lookup"><span data-stu-id="c8bd3-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="c8bd3-140">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-140">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8bd3-141">文本值</span><span class="sxs-lookup"><span data-stu-id="c8bd3-141">Text value</span></span>

<span data-ttu-id="c8bd3-142">**Body**元素的文本值是项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-142">The text value of the **Body** element is the body content of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8bd3-143">备注</span><span class="sxs-lookup"><span data-stu-id="c8bd3-143">Remarks</span></span>

<span data-ttu-id="c8bd3-144">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-144">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c8bd3-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8bd3-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="c8bd3-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8bd3-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="c8bd3-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8bd3-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="c8bd3-148">Schema Name</span></span>  <br/> |<span data-ttu-id="c8bd3-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="c8bd3-149">Type schema</span></span>  <br/> |
|<span data-ttu-id="c8bd3-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="c8bd3-150">Validation File</span></span>  <br/> |<span data-ttu-id="c8bd3-151">types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8bd3-151">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8bd3-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="c8bd3-152">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c8bd3-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8bd3-153">See also</span></span>



- [<span data-ttu-id="c8bd3-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c8bd3-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

