---
title: ReadItems （CalendarPermissionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: ReadItems 元素指示用户是否有权读取日历文件夹中的项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e040b643016781f9f890050f189191356f8d4f0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468297"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="0b0b1-104">ReadItems （CalendarPermissionType）</span><span class="sxs-lookup"><span data-stu-id="0b0b1-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="0b0b1-105">**ReadItems**元素指示用户是否有权读取日历文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="0b0b1-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="0b0b1-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b0b1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b0b1-108">Attributes and elements</span></span>

<span data-ttu-id="0b0b1-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b0b1-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="0b0b1-110">Attributes</span></span>

<span data-ttu-id="0b0b1-111">无。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b0b1-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0b0b1-112">Child elements</span></span>

<span data-ttu-id="0b0b1-113">无。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b0b1-114">父元素</span><span class="sxs-lookup"><span data-stu-id="0b0b1-114">Parent elements</span></span>

|<span data-ttu-id="0b0b1-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-115">**Element**</span></span>|<span data-ttu-id="0b0b1-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b0b1-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="0b0b1-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="0b0b1-p103">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0b0b1-120">文本值</span><span class="sxs-lookup"><span data-stu-id="0b0b1-120">Text value</span></span>

<span data-ttu-id="0b0b1-121">下表列出了**ReadItems**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="0b0b1-122">**ReadItems 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="0b0b1-123">**值**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-123">**Value**</span></span>|<span data-ttu-id="0b0b1-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b0b1-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b0b1-125">无</span><span class="sxs-lookup"><span data-stu-id="0b0b1-125">None</span></span>  <br/> |<span data-ttu-id="0b0b1-126">指示用户不具有查看日历中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="0b0b1-127">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="0b0b1-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="0b0b1-128">指示用户具有仅查看日历中的忙/闲时间的权限。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="0b0b1-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="0b0b1-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="0b0b1-130">指示用户有权查看日历中的忙/闲时间以及约会的主题和位置。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="0b0b1-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="0b0b1-131">FullDetails</span></span>  <br/> |<span data-ttu-id="0b0b1-132">指示用户有权查看日历中的所有项目，包括忙/闲时间、主题、位置和约会的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b0b1-133">说明</span><span class="sxs-lookup"><span data-stu-id="0b0b1-133">Remarks</span></span>

<span data-ttu-id="0b0b1-134">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0b0b1-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b0b1-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b0b1-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b0b1-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b0b1-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b0b1-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b0b1-137">Schema Name</span></span>  <br/> |<span data-ttu-id="0b0b1-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="0b0b1-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b0b1-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b0b1-139">Validation File</span></span>  <br/> |<span data-ttu-id="0b0b1-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b0b1-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b0b1-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b0b1-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="0b0b1-142">False</span><span class="sxs-lookup"><span data-stu-id="0b0b1-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b0b1-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b0b1-143">See also</span></span>



- [<span data-ttu-id="0b0b1-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0b0b1-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0b0b1-145">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0b0b1-145">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

