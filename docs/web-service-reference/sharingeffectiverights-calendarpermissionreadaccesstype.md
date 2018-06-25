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
description: SharingEffectiveRights 元素指示正在共享的日历数据的用户具有的权限。
ms.openlocfilehash: e7d2aa061650c33d27de042ae8a6348f9a7d3430
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827480"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="60b9e-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="60b9e-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="60b9e-104">**SharingEffectiveRights**元素指示正在共享的日历数据的用户具有的权限。</span><span class="sxs-lookup"><span data-stu-id="60b9e-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="60b9e-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="60b9e-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60b9e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="60b9e-106">Attributes and elements</span></span>

<span data-ttu-id="60b9e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="60b9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60b9e-108">属性</span><span class="sxs-lookup"><span data-stu-id="60b9e-108">Attributes</span></span>

<span data-ttu-id="60b9e-109">无。</span><span class="sxs-lookup"><span data-stu-id="60b9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60b9e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="60b9e-110">Child elements</span></span>

<span data-ttu-id="60b9e-111">无。</span><span class="sxs-lookup"><span data-stu-id="60b9e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60b9e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="60b9e-112">Parent elements</span></span>

|<span data-ttu-id="60b9e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="60b9e-113">**Element**</span></span>|<span data-ttu-id="60b9e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="60b9e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60b9e-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="60b9e-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="60b9e-116">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="60b9e-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60b9e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="60b9e-117">Text value</span></span>

<span data-ttu-id="60b9e-118">下表列出了**SharingEffectiveRights**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="60b9e-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="60b9e-119">**值**</span><span class="sxs-lookup"><span data-stu-id="60b9e-119">**Value**</span></span>|<span data-ttu-id="60b9e-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="60b9e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60b9e-121">无</span><span class="sxs-lookup"><span data-stu-id="60b9e-121">None</span></span>  <br/> |<span data-ttu-id="60b9e-122">指示用户没有权限在日历中查看的项目。</span><span class="sxs-lookup"><span data-stu-id="60b9e-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="60b9e-123">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="60b9e-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="60b9e-124">指示用户有权在日历中查看仅忙/闲时间。</span><span class="sxs-lookup"><span data-stu-id="60b9e-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="60b9e-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="60b9e-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="60b9e-126">指示用户有权查看忙/闲时间中日历的主题和约会的位置。</span><span class="sxs-lookup"><span data-stu-id="60b9e-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="60b9e-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="60b9e-127">FullDetails</span></span>  <br/> |<span data-ttu-id="60b9e-128">指示用户有权查看日历，包括忙/闲时间和主题、 位置和约会的详细信息中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="60b9e-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60b9e-129">备注</span><span class="sxs-lookup"><span data-stu-id="60b9e-129">Remarks</span></span>

<span data-ttu-id="60b9e-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="60b9e-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60b9e-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="60b9e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60b9e-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="60b9e-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60b9e-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="60b9e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="60b9e-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="60b9e-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="60b9e-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="60b9e-135">Validation File</span></span>  <br/> |<span data-ttu-id="60b9e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60b9e-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60b9e-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="60b9e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="60b9e-138">False</span><span class="sxs-lookup"><span data-stu-id="60b9e-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60b9e-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="60b9e-139">See also</span></span>



- [<span data-ttu-id="60b9e-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="60b9e-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

