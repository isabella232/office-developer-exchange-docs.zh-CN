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
description: RemoveItem 元素表示一个 response 对象，该对象用于在收到 MeetingCancellation 邮件时删除会议项目。
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467688"
---
# <a name="removeitem"></a><span data-ttu-id="c0aca-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="c0aca-103">RemoveItem</span></span>

<span data-ttu-id="c0aca-104">**RemoveItem**元素表示一个 response 对象，该对象用于在收到 MeetingCancellation 邮件时删除会议项目。</span><span class="sxs-lookup"><span data-stu-id="c0aca-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="c0aca-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="c0aca-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0aca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0aca-106">Attributes and elements</span></span>

<span data-ttu-id="c0aca-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0aca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0aca-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c0aca-108">Attributes</span></span>

|<span data-ttu-id="c0aca-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c0aca-109">**Attribute**</span></span>|<span data-ttu-id="c0aca-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0aca-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0aca-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="c0aca-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="c0aca-112">将 RemoveItem reply 对象类的名称表示为英文字符串。</span><span class="sxs-lookup"><span data-stu-id="c0aca-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0aca-113">子元素</span><span class="sxs-lookup"><span data-stu-id="c0aca-113">Child elements</span></span>

|<span data-ttu-id="c0aca-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0aca-114">**Element**</span></span>|<span data-ttu-id="c0aca-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0aca-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0aca-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="c0aca-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="c0aca-117">标识 RemoveItem 响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="c0aca-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0aca-118">父元素</span><span class="sxs-lookup"><span data-stu-id="c0aca-118">Parent elements</span></span>

|<span data-ttu-id="c0aca-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0aca-119">**Element**</span></span>|<span data-ttu-id="c0aca-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0aca-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0aca-121">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="c0aca-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="c0aca-122">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="c0aca-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="c0aca-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="c0aca-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="c0aca-124">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="c0aca-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0aca-125">备注</span><span class="sxs-lookup"><span data-stu-id="c0aca-125">Remarks</span></span>

 <span data-ttu-id="c0aca-126">**RemoveItem**仅对[MeetingCancellation](meetingcancellation.md)有效。</span><span class="sxs-lookup"><span data-stu-id="c0aca-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="c0aca-127">否则，将引发错误。</span><span class="sxs-lookup"><span data-stu-id="c0aca-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0aca-128">会议取消的[ItemClass](itemclass.md)为 IPM。日程安排. 会议. 已取消。</span><span class="sxs-lookup"><span data-stu-id="c0aca-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="c0aca-129">若要删除[MeetingRequest](meetingrequest.md)和关联的[CalendarItem](calendaritem.md)，请使用[DeclineItem](declineitem.md) Response 对象，而不是**RemoveItem**。</span><span class="sxs-lookup"><span data-stu-id="c0aca-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="c0aca-130">代理访问不支持**RemoveItem** 。</span><span class="sxs-lookup"><span data-stu-id="c0aca-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="c0aca-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0aca-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0aca-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0aca-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0aca-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0aca-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0aca-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0aca-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c0aca-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="c0aca-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0aca-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0aca-136">Validation File</span></span>  <br/> |<span data-ttu-id="c0aca-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0aca-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0aca-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0aca-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0aca-139">False</span><span class="sxs-lookup"><span data-stu-id="c0aca-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0aca-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0aca-140">See also</span></span>



- [<span data-ttu-id="c0aca-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0aca-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

