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
description: SuppressReadReceipt 元素用于禁止已读回执。
ms.openlocfilehash: b6b4fe5db26195882a7def5cac8266a942def996
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455952"
---
# <a name="suppressreadreceipt"></a><span data-ttu-id="58860-103">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="58860-103">SuppressReadReceipt</span></span>

<span data-ttu-id="58860-104">**SuppressReadReceipt**元素用于禁止已读回执。</span><span class="sxs-lookup"><span data-stu-id="58860-104">The **SuppressReadReceipt** element is used to suppress read receipts.</span></span> 
  
```xml
<SuppressReadReceipt>
   <ReferenceItemId/>
</SuppressReadReceipt>
```

 <span data-ttu-id="58860-105">**SuppressReadReceiptType**</span><span class="sxs-lookup"><span data-stu-id="58860-105">**SuppressReadReceiptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58860-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58860-106">Attributes and elements</span></span>

<span data-ttu-id="58860-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58860-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58860-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="58860-108">Attributes</span></span>

<span data-ttu-id="58860-109">无。</span><span class="sxs-lookup"><span data-stu-id="58860-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58860-110">子元素</span><span class="sxs-lookup"><span data-stu-id="58860-110">Child elements</span></span>

|<span data-ttu-id="58860-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="58860-111">**Element**</span></span>|<span data-ttu-id="58860-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="58860-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58860-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="58860-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="58860-114">标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="58860-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58860-115">父元素</span><span class="sxs-lookup"><span data-stu-id="58860-115">Parent elements</span></span>

|<span data-ttu-id="58860-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="58860-116">**Element**</span></span>|<span data-ttu-id="58860-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="58860-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58860-118">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="58860-118">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="58860-119">描述与会议时间相邻的所有项目。</span><span class="sxs-lookup"><span data-stu-id="58860-119">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="58860-120">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="58860-120">The following are some of the XPath expressions to this element:</span></span><br/>  <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="58860-121">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="58860-121">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="58860-122">描述与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="58860-122">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="58860-123">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="58860-123">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="58860-124">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="58860-124">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="58860-125">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="58860-125">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="58860-126">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="58860-126">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="58860-127">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="58860-127">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58860-128">说明</span><span class="sxs-lookup"><span data-stu-id="58860-128">Remarks</span></span>

<span data-ttu-id="58860-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58860-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58860-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="58860-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58860-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="58860-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58860-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="58860-132">Schema Name</span></span>  <br/> |<span data-ttu-id="58860-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="58860-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="58860-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="58860-134">Validation File</span></span>  <br/> |<span data-ttu-id="58860-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58860-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58860-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="58860-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="58860-137">False</span><span class="sxs-lookup"><span data-stu-id="58860-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58860-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58860-138">See also</span></span>

- [<span data-ttu-id="58860-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58860-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

