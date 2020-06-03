---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: SharingEffectiveRights 元素指示用户对要共享的日历数据所具有的权限。
ms.openlocfilehash: 5581e9cc001608a124ae94e69eba836f6fd98520
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458577"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="5e4cb-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="5e4cb-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="5e4cb-104">**SharingEffectiveRights**元素指示用户对要共享的日历数据所具有的权限。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="5e4cb-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="5e4cb-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e4cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5e4cb-106">Attributes and elements</span></span>

<span data-ttu-id="5e4cb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e4cb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5e4cb-108">Attributes</span></span>

<span data-ttu-id="5e4cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e4cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5e4cb-110">Child elements</span></span>

<span data-ttu-id="5e4cb-111">无。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5e4cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5e4cb-112">Parent elements</span></span>

|<span data-ttu-id="5e4cb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e4cb-113">**Element**</span></span>|<span data-ttu-id="5e4cb-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="5e4cb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e4cb-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="5e4cb-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="5e4cb-116">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5e4cb-117">文本值</span><span class="sxs-lookup"><span data-stu-id="5e4cb-117">Text value</span></span>

<span data-ttu-id="5e4cb-118">下表列出了**SharingEffectiveRights**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="5e4cb-119">**值**</span><span class="sxs-lookup"><span data-stu-id="5e4cb-119">**Value**</span></span>|<span data-ttu-id="5e4cb-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e4cb-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e4cb-121">无</span><span class="sxs-lookup"><span data-stu-id="5e4cb-121">None</span></span>  <br/> |<span data-ttu-id="5e4cb-122">指示用户不具有查看日历中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="5e4cb-123">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="5e4cb-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="5e4cb-124">指示用户具有仅查看日历中的忙/闲时间的权限。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="5e4cb-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="5e4cb-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="5e4cb-126">指示用户有权查看日历中的忙/闲时间以及约会的主题和位置。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="5e4cb-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="5e4cb-127">FullDetails</span></span>  <br/> |<span data-ttu-id="5e4cb-128">指示用户有权查看日历中的所有项目，包括忙/闲时间、主题、位置和约会的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e4cb-129">说明</span><span class="sxs-lookup"><span data-stu-id="5e4cb-129">Remarks</span></span>

<span data-ttu-id="5e4cb-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5e4cb-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e4cb-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="5e4cb-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e4cb-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="5e4cb-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e4cb-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="5e4cb-133">Schema Name</span></span>  <br/> |<span data-ttu-id="5e4cb-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="5e4cb-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e4cb-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="5e4cb-135">Validation File</span></span>  <br/> |<span data-ttu-id="5e4cb-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5e4cb-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e4cb-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="5e4cb-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e4cb-138">False</span><span class="sxs-lookup"><span data-stu-id="5e4cb-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e4cb-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e4cb-139">See also</span></span>



- [<span data-ttu-id="5e4cb-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5e4cb-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

