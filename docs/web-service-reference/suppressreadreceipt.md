---
title: SuppressReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuppressReadReceipt
api_type:
- schema
ms.assetid: fc09bcc2-c003-4322-8315-d929bd0a9e2e
description: SuppressReadReceipt 元素用于取消已读的回执。
ms.openlocfilehash: de2eef68abd25c8208530ba5e98ab3278c8702d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838164"
---
# <a name="suppressreadreceipt"></a><span data-ttu-id="aa60b-103">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="aa60b-103">SuppressReadReceipt</span></span>

<span data-ttu-id="aa60b-104">**SuppressReadReceipt**元素用于取消已读的回执。</span><span class="sxs-lookup"><span data-stu-id="aa60b-104">The **SuppressReadReceipt** element is used to suppress read receipts.</span></span> 
  
```xml
<SuppressReadReceipt>
   <ReferenceItemId/>
</SuppressReadReceipt>
```

 <span data-ttu-id="aa60b-105">**SuppressReadReceiptType**</span><span class="sxs-lookup"><span data-stu-id="aa60b-105">**SuppressReadReceiptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa60b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa60b-106">Attributes and elements</span></span>

<span data-ttu-id="aa60b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa60b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa60b-108">属性</span><span class="sxs-lookup"><span data-stu-id="aa60b-108">Attributes</span></span>

<span data-ttu-id="aa60b-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa60b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa60b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa60b-110">Child elements</span></span>

|<span data-ttu-id="aa60b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa60b-111">**Element**</span></span>|<span data-ttu-id="aa60b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa60b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa60b-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="aa60b-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="aa60b-114">标识响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="aa60b-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa60b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="aa60b-115">Parent elements</span></span>

|<span data-ttu-id="aa60b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa60b-116">**Element**</span></span>|<span data-ttu-id="aa60b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa60b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa60b-118">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="aa60b-118">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="aa60b-119">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="aa60b-119">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="aa60b-120">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="aa60b-120">The following are some of the XPath expressions to this element:</span></span><br/>  <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="aa60b-121">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="aa60b-121">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="aa60b-122">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="aa60b-122">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="aa60b-123">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="aa60b-123">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="aa60b-124">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="aa60b-124">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="aa60b-125">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="aa60b-125">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="aa60b-126">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="aa60b-126">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="aa60b-127">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="aa60b-127">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa60b-128">备注</span><span class="sxs-lookup"><span data-stu-id="aa60b-128">Remarks</span></span>

<span data-ttu-id="aa60b-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aa60b-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa60b-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa60b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa60b-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa60b-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa60b-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa60b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="aa60b-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="aa60b-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa60b-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa60b-134">Validation File</span></span>  <br/> |<span data-ttu-id="aa60b-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa60b-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa60b-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa60b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa60b-137">False</span><span class="sxs-lookup"><span data-stu-id="aa60b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa60b-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa60b-138">See also</span></span>

- [<span data-ttu-id="aa60b-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aa60b-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

