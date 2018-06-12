---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: RemoveItem 元素表示用于时收到 MeetingCancellation 邮件中删除的会议项目的响应对象。
ms.openlocfilehash: 6897363eba602e6a135ad255822197f9296dd44a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827108"
---
# <a name="removeitem"></a><span data-ttu-id="68299-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="68299-103">RemoveItem</span></span>

<span data-ttu-id="68299-104">**RemoveItem**元素表示用于时收到 MeetingCancellation 邮件中删除的会议项目的响应对象。</span><span class="sxs-lookup"><span data-stu-id="68299-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="68299-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="68299-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68299-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="68299-106">Attributes and elements</span></span>

<span data-ttu-id="68299-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="68299-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68299-108">属性</span><span class="sxs-lookup"><span data-stu-id="68299-108">Attributes</span></span>

|<span data-ttu-id="68299-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="68299-109">**Attribute**</span></span>|<span data-ttu-id="68299-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="68299-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68299-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="68299-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="68299-112">以英语字符串表示 RemoveItem 答复对象类的名称。</span><span class="sxs-lookup"><span data-stu-id="68299-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68299-113">子元素</span><span class="sxs-lookup"><span data-stu-id="68299-113">Child elements</span></span>

|<span data-ttu-id="68299-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="68299-114">**Element**</span></span>|<span data-ttu-id="68299-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="68299-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68299-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="68299-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="68299-117">标识 RemoveItem response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="68299-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="68299-118">父元素</span><span class="sxs-lookup"><span data-stu-id="68299-118">Parent elements</span></span>

|<span data-ttu-id="68299-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="68299-119">**Element**</span></span>|<span data-ttu-id="68299-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="68299-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68299-121">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="68299-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="68299-122">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="68299-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="68299-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="68299-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="68299-124">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="68299-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68299-125">备注</span><span class="sxs-lookup"><span data-stu-id="68299-125">Remarks</span></span>

 <span data-ttu-id="68299-126">仅对[MeetingCancellation](meetingcancellation.md)有效**RemoveItem** 。</span><span class="sxs-lookup"><span data-stu-id="68299-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="68299-127">否则，将引发错误。</span><span class="sxs-lookup"><span data-stu-id="68299-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="68299-128">[ItemClass](itemclass.md)会议取消是 IPM。Schedule.Meeting.Canceled。</span><span class="sxs-lookup"><span data-stu-id="68299-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="68299-129">若要删除[MeetingRequest](meetingrequest.md)和关联的[日历项目](calendaritem.md)，而不是**RemoveItem**使用[DeclineItem](declineitem.md) response 对象。</span><span class="sxs-lookup"><span data-stu-id="68299-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="68299-130">**RemoveItem**不支持代理访问。</span><span class="sxs-lookup"><span data-stu-id="68299-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="68299-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="68299-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68299-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="68299-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68299-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="68299-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68299-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="68299-134">Schema Name</span></span>  <br/> |<span data-ttu-id="68299-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="68299-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="68299-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="68299-136">Validation File</span></span>  <br/> |<span data-ttu-id="68299-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68299-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68299-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="68299-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="68299-139">False</span><span class="sxs-lookup"><span data-stu-id="68299-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68299-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="68299-140">See also</span></span>



- [<span data-ttu-id="68299-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="68299-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

