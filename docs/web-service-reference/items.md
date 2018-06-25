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
description: 项目元素包含数组的项目。
ms.openlocfilehash: 241a56ee23e87d6a4320b93cc65b1f5aa1f60120
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826163"
---
# <a name="items"></a><span data-ttu-id="916ed-103">项目</span><span class="sxs-lookup"><span data-stu-id="916ed-103">Items</span></span>

<span data-ttu-id="916ed-104">**项目**元素包含数组的项目。</span><span class="sxs-lookup"><span data-stu-id="916ed-104">The **Items** element contains an array of items.</span></span> 
  
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

 <span data-ttu-id="916ed-105">**ArrayOfRealItemsType**</span><span class="sxs-lookup"><span data-stu-id="916ed-105">**ArrayOfRealItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="916ed-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="916ed-106">Attributes and elements</span></span>

<span data-ttu-id="916ed-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="916ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="916ed-108">属性</span><span class="sxs-lookup"><span data-stu-id="916ed-108">Attributes</span></span>

<span data-ttu-id="916ed-109">无。</span><span class="sxs-lookup"><span data-stu-id="916ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="916ed-110">子元素</span><span class="sxs-lookup"><span data-stu-id="916ed-110">Child elements</span></span>

|<span data-ttu-id="916ed-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="916ed-111">**Element**</span></span>|<span data-ttu-id="916ed-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="916ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="916ed-113">Item</span><span class="sxs-lookup"><span data-stu-id="916ed-113">Item</span></span>](item.md) <br/> |<span data-ttu-id="916ed-114">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="916ed-114">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-115">Message</span><span class="sxs-lookup"><span data-stu-id="916ed-115">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="916ed-116">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="916ed-116">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="916ed-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="916ed-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="916ed-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="916ed-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="916ed-119">联系人</span><span class="sxs-lookup"><span data-stu-id="916ed-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="916ed-120">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="916ed-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="916ed-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="916ed-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="916ed-122">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="916ed-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="916ed-123">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-123">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="916ed-124">代表 Exchange 存储中的会议消息。</span><span class="sxs-lookup"><span data-stu-id="916ed-124">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-125">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="916ed-125">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="916ed-126">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="916ed-126">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-127">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="916ed-127">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="916ed-128">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="916ed-128">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-129">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="916ed-129">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="916ed-130">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="916ed-130">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-131">任务</span><span class="sxs-lookup"><span data-stu-id="916ed-131">Task</span></span>](task.md) <br/> |<span data-ttu-id="916ed-132">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="916ed-132">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="916ed-133">PostItem</span><span class="sxs-lookup"><span data-stu-id="916ed-133">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="916ed-134">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="916ed-134">Represents a post item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="916ed-135">父元素</span><span class="sxs-lookup"><span data-stu-id="916ed-135">Parent elements</span></span>

|<span data-ttu-id="916ed-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="916ed-136">**Element**</span></span>|<span data-ttu-id="916ed-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="916ed-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="916ed-138">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-138">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md) <br/> |<span data-ttu-id="916ed-139">包含状态和[CopyItem 操作](copyitem-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="916ed-139">Contains the status and result of a [CopyItem operation](copyitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="916ed-140">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-140">CreateItemResponseMessage</span></span>](createitemresponsemessage.md) <br/> |<span data-ttu-id="916ed-141">包含状态和的单个结果[CreateItem operation，](createitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="916ed-141">Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="916ed-142">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-142">GetItemResponseMessage</span></span>](getitemresponsemessage.md) <br/> |<span data-ttu-id="916ed-143">包含状态和[GetItem operation，](getitem-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="916ed-143">Contains the status and result of a [GetItem operation](getitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="916ed-144">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="916ed-144">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="916ed-145">调用表示项的组合[FindItem 操作](finditem-operation.md)的结果的集合。</span><span class="sxs-lookup"><span data-stu-id="916ed-145">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="916ed-146">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-146">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md) <br/> |<span data-ttu-id="916ed-147">包含状态和[MoveItem 操作](moveitem-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="916ed-147">Contains the status and result of a [MoveItem operation](moveitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="916ed-148">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="916ed-148">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="916ed-149">[FindItem 操作](finditem-operation.md)过程中包含单个根文件夹的搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="916ed-149">Contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="916ed-150">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="916ed-150">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="916ed-151">包含状态和[UpdateItem 操作](updateitem-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="916ed-151">Contains the status and result of an [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="916ed-152">注解</span><span class="sxs-lookup"><span data-stu-id="916ed-152">Remarks</span></span>

<span data-ttu-id="916ed-153">有关组[CreateItem operation，](createitem-operation.md)请求中的项的信息，请参阅[项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)。</span><span class="sxs-lookup"><span data-stu-id="916ed-153">For information about the set of items in a [CreateItem operation](createitem-operation.md) request, see [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span></span>
  
<span data-ttu-id="916ed-154">[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="916ed-154">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="916ed-155">如 IPM 的项目。共享和**消息**元素以返回 IPM.InfoPath。</span><span class="sxs-lookup"><span data-stu-id="916ed-155">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="916ed-156">启动 Exchange Server 2010 与 Exchange 版本不在响应中返回基本的[Item](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="916ed-156">Versions of Exchange starting with Exchange Server 2010 do not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="916ed-157">描述此元素的架构位于运行 Exchange 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="916ed-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="916ed-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="916ed-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="916ed-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="916ed-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="916ed-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="916ed-160">Schema Name</span></span>  <br/> |<span data-ttu-id="916ed-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="916ed-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="916ed-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="916ed-162">Validation File</span></span>  <br/> |<span data-ttu-id="916ed-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="916ed-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="916ed-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="916ed-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="916ed-165">False</span><span class="sxs-lookup"><span data-stu-id="916ed-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="916ed-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="916ed-166">See also</span></span>



[<span data-ttu-id="916ed-167">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="916ed-167">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="916ed-168">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="916ed-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

