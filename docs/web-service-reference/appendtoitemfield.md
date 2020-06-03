---
title: AppendToItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppendToItemField
api_type:
- schema
ms.assetid: 66dbcb4a-ae6d-4648-8610-67187bdb105c
description: AppendToItemField 元素标识在 UpdateItem 操作过程中追加到项的单个属性的数据。
ms.openlocfilehash: 902239155bff45d6f81989de954c9459cf012288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466043"
---
# <a name="appendtoitemfield"></a><span data-ttu-id="27f9a-103">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="27f9a-103">AppendToItemField</span></span>

<span data-ttu-id="27f9a-104">**AppendToItemField**元素标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="27f9a-104">The **AppendToItemField** element identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>
  
- [<span data-ttu-id="27f9a-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="27f9a-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="27f9a-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="27f9a-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="27f9a-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="27f9a-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="27f9a-108">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="27f9a-108">Updates (Item)</span></span>](updates-item.md)
  
- [<span data-ttu-id="27f9a-109">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="27f9a-109">AppendToItemField</span></span>](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 <span data-ttu-id="27f9a-110">**AppendToItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="27f9a-110">**AppendToItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27f9a-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27f9a-111">Attributes and elements</span></span>

<span data-ttu-id="27f9a-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27f9a-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27f9a-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="27f9a-113">Attributes</span></span>

<span data-ttu-id="27f9a-114">无。</span><span class="sxs-lookup"><span data-stu-id="27f9a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27f9a-115">子元素</span><span class="sxs-lookup"><span data-stu-id="27f9a-115">Child elements</span></span>

|<span data-ttu-id="27f9a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="27f9a-116">**Element**</span></span>|<span data-ttu-id="27f9a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="27f9a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27f9a-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="27f9a-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="27f9a-119">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="27f9a-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="27f9a-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="27f9a-121">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="27f9a-121">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="27f9a-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="27f9a-123">标识要追加的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="27f9a-123">Identifies extended MAPI properties to append.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-124">项目</span><span class="sxs-lookup"><span data-stu-id="27f9a-124">Item</span></span>](item.md) <br/> |<span data-ttu-id="27f9a-125">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="27f9a-125">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-126">Message</span><span class="sxs-lookup"><span data-stu-id="27f9a-126">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="27f9a-127">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="27f9a-127">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-128">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="27f9a-128">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="27f9a-129">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="27f9a-129">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-130">Contact</span><span class="sxs-lookup"><span data-stu-id="27f9a-130">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="27f9a-131">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="27f9a-131">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="27f9a-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="27f9a-133">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="27f9a-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="27f9a-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="27f9a-135">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="27f9a-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="27f9a-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="27f9a-137">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="27f9a-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="27f9a-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="27f9a-139">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="27f9a-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="27f9a-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="27f9a-141">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="27f9a-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27f9a-142">任务</span><span class="sxs-lookup"><span data-stu-id="27f9a-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="27f9a-143">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="27f9a-143">Represents a task in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27f9a-144">父元素</span><span class="sxs-lookup"><span data-stu-id="27f9a-144">Parent elements</span></span>

|<span data-ttu-id="27f9a-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="27f9a-145">**Element**</span></span>|<span data-ttu-id="27f9a-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="27f9a-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27f9a-147">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="27f9a-147">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="27f9a-148">包含定义追加、设置和删除对项属性所做的更改的数组。</span><span class="sxs-lookup"><span data-stu-id="27f9a-148">Contains an array that defines append, set, and delete changes to item properties.</span></span>  <br/> <span data-ttu-id="27f9a-149">下面是此元素的 XPath 表达式:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="27f9a-149">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27f9a-150">备注</span><span class="sxs-lookup"><span data-stu-id="27f9a-150">Remarks</span></span>

<span data-ttu-id="27f9a-151">只有某些属性支持 append 操作。</span><span class="sxs-lookup"><span data-stu-id="27f9a-151">Only certain properties support append operations.</span></span> <span data-ttu-id="27f9a-152">如果尝试追加到不支持追加的属性，则会导致错误。</span><span class="sxs-lookup"><span data-stu-id="27f9a-152">An attempt to append to a property that does not support appending will result in an error.</span></span>
  
<span data-ttu-id="27f9a-153">对于更新操作，只能在单个请求中修改一个属性。</span><span class="sxs-lookup"><span data-stu-id="27f9a-153">For update operations, only one property can be modified within a single request.</span></span> <span data-ttu-id="27f9a-154">必须在[Path](path.md)元素中引用该单个属性。</span><span class="sxs-lookup"><span data-stu-id="27f9a-154">That single property must be referenced in the [Path](path.md) element.</span></span> <span data-ttu-id="27f9a-155">然后，派生类中的**Item**元素可以仅保留与单个**Path**元素一致的单个属性。</span><span class="sxs-lookup"><span data-stu-id="27f9a-155">The **Item** element in the derived classes can then only hold a single property that is in agreement with the single **Path** element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="27f9a-156">[Path](path.md)元素是抽象的。</span><span class="sxs-lookup"><span data-stu-id="27f9a-156">The [Path](path.md) element is abstract.</span></span> <span data-ttu-id="27f9a-157">它必须由[FieldURI](fielduri.md)、 [IndexedFieldURI](indexedfielduri.md)或[ExtendedFieldURI](extendedfielduri.md)元素替代。</span><span class="sxs-lookup"><span data-stu-id="27f9a-157">It must be substituted by the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="27f9a-158">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27f9a-158">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27f9a-159">元素信息</span><span class="sxs-lookup"><span data-stu-id="27f9a-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27f9a-160">命名空间</span><span class="sxs-lookup"><span data-stu-id="27f9a-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27f9a-161">架构名称</span><span class="sxs-lookup"><span data-stu-id="27f9a-161">Schema Name</span></span>  <br/> |<span data-ttu-id="27f9a-162">类型架构</span><span class="sxs-lookup"><span data-stu-id="27f9a-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="27f9a-163">验证文件</span><span class="sxs-lookup"><span data-stu-id="27f9a-163">Validation File</span></span>  <br/> |<span data-ttu-id="27f9a-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27f9a-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27f9a-165">可以为空</span><span class="sxs-lookup"><span data-stu-id="27f9a-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="27f9a-166">False</span><span class="sxs-lookup"><span data-stu-id="27f9a-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27f9a-167">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27f9a-167">See also</span></span>

- [<span data-ttu-id="27f9a-168">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="27f9a-168">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="27f9a-169">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27f9a-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

