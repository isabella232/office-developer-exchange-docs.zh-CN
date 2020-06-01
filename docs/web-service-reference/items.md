---
title: 项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: Items 元素包含项的数组。
ms.openlocfilehash: 489e34ad0e4bcc2520febb3c213db970fa496051
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458129"
---
# <a name="items"></a><span data-ttu-id="1436d-103">项目</span><span class="sxs-lookup"><span data-stu-id="1436d-103">Items</span></span>

<span data-ttu-id="1436d-104">**Items**元素包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="1436d-104">The **Items** element contains an array of items.</span></span> 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 <span data-ttu-id="1436d-105">**ArrayOfRealItemsType**</span><span class="sxs-lookup"><span data-stu-id="1436d-105">**ArrayOfRealItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1436d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1436d-106">Attributes and elements</span></span>

<span data-ttu-id="1436d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1436d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1436d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1436d-108">Attributes</span></span>

<span data-ttu-id="1436d-109">无。</span><span class="sxs-lookup"><span data-stu-id="1436d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1436d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1436d-110">Child elements</span></span>

|<span data-ttu-id="1436d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1436d-111">**Element**</span></span>|<span data-ttu-id="1436d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1436d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1436d-113">项目</span><span class="sxs-lookup"><span data-stu-id="1436d-113">Item</span></span>](item.md) <br/> |<span data-ttu-id="1436d-114">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="1436d-114">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-115">Message</span><span class="sxs-lookup"><span data-stu-id="1436d-115">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1436d-116">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="1436d-116">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1436d-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1436d-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1436d-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="1436d-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1436d-119">Contact</span><span class="sxs-lookup"><span data-stu-id="1436d-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="1436d-120">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="1436d-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="1436d-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="1436d-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="1436d-122">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="1436d-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="1436d-123">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-123">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="1436d-124">表示 Exchange 存储中的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="1436d-124">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-125">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1436d-125">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1436d-126">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="1436d-126">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-127">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="1436d-127">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="1436d-128">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="1436d-128">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-129">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="1436d-129">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="1436d-130">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="1436d-130">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-131">任务</span><span class="sxs-lookup"><span data-stu-id="1436d-131">Task</span></span>](task.md) <br/> |<span data-ttu-id="1436d-132">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="1436d-132">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1436d-133">PostItem</span><span class="sxs-lookup"><span data-stu-id="1436d-133">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="1436d-134">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="1436d-134">Represents a post item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1436d-135">父元素</span><span class="sxs-lookup"><span data-stu-id="1436d-135">Parent elements</span></span>

|<span data-ttu-id="1436d-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="1436d-136">**Element**</span></span>|<span data-ttu-id="1436d-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="1436d-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1436d-138">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-138">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md) <br/> |<span data-ttu-id="1436d-139">包含[CopyItem 操作](copyitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-139">Contains the status and result of a [CopyItem operation](copyitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1436d-140">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-140">CreateItemResponseMessage</span></span>](createitemresponsemessage.md) <br/> |<span data-ttu-id="1436d-141">包含单个[CreateItem 操作](createitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-141">Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1436d-142">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-142">GetItemResponseMessage</span></span>](getitemresponsemessage.md) <br/> |<span data-ttu-id="1436d-143">包含[GetItem 操作](getitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-143">Contains the status and result of a [GetItem operation](getitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1436d-144">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="1436d-144">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="1436d-145">表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。</span><span class="sxs-lookup"><span data-stu-id="1436d-145">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="1436d-146">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-146">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md) <br/> |<span data-ttu-id="1436d-147">包含[MoveItem 操作](moveitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-147">Contains the status and result of a [MoveItem operation](moveitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1436d-148">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="1436d-148">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="1436d-149">包含在[FindItem 操作](finditem-operation.md)过程中搜索单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-149">Contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1436d-150">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1436d-150">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="1436d-151">包含[UpdateItem 操作](updateitem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1436d-151">Contains the status and result of an [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1436d-152">备注</span><span class="sxs-lookup"><span data-stu-id="1436d-152">Remarks</span></span>

<span data-ttu-id="1436d-153">有关[CreateItem 操作](createitem-operation.md)请求中的项目集的信息，请参阅[items （NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md)。</span><span class="sxs-lookup"><span data-stu-id="1436d-153">For information about the set of items in a [CreateItem operation](createitem-operation.md) request, see [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span></span>
  
<span data-ttu-id="1436d-154">[Message](message-ex15websvcsotherref.md)元素表示电子邮件以及 Exchange Web 服务（EWS）架构未强类型化的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="1436d-154">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="1436d-155">项目，如 IPM。共享和 IPM. InfoPath 以**邮件**元素的形式返回。</span><span class="sxs-lookup"><span data-stu-id="1436d-155">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="1436d-156">从 Exchange Server 2010 开始的 Exchange 版本不会在响应中返回基本[项目](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="1436d-156">Versions of Exchange starting with Exchange Server 2010 do not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="1436d-157">描述此元素的架构位于运行 Exchange 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1436d-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1436d-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="1436d-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1436d-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="1436d-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1436d-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="1436d-160">Schema Name</span></span>  <br/> |<span data-ttu-id="1436d-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="1436d-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="1436d-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="1436d-162">Validation File</span></span>  <br/> |<span data-ttu-id="1436d-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1436d-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1436d-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="1436d-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="1436d-165">False</span><span class="sxs-lookup"><span data-stu-id="1436d-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1436d-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1436d-166">See also</span></span>



[<span data-ttu-id="1436d-167">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="1436d-167">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="1436d-168">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1436d-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

