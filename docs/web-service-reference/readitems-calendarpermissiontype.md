---
title: ReadItems (CalendarPermissionType)
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
description: ReadItems 元素指示用户是否有权读取日历文件夹中的项目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 532b90c47cca7117a89d59e7012436268be9ebb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826964"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="b767f-104">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="b767f-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="b767f-105">**ReadItems**元素指示用户是否有权读取日历文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="b767f-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="b767f-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b767f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="b767f-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="b767f-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b767f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b767f-108">Attributes and elements</span></span>

<span data-ttu-id="b767f-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b767f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b767f-110">属性</span><span class="sxs-lookup"><span data-stu-id="b767f-110">Attributes</span></span>

<span data-ttu-id="b767f-111">无。</span><span class="sxs-lookup"><span data-stu-id="b767f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b767f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b767f-112">Child elements</span></span>

<span data-ttu-id="b767f-113">无。</span><span class="sxs-lookup"><span data-stu-id="b767f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b767f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="b767f-114">Parent elements</span></span>

|<span data-ttu-id="b767f-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="b767f-115">**Element**</span></span>|<span data-ttu-id="b767f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b767f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b767f-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="b767f-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="b767f-p103">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b767f-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b767f-120">文本值</span><span class="sxs-lookup"><span data-stu-id="b767f-120">Text value</span></span>

<span data-ttu-id="b767f-121">下表列出了**ReadItems**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="b767f-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="b767f-122">**ReadItems 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="b767f-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="b767f-123">**值**</span><span class="sxs-lookup"><span data-stu-id="b767f-123">**Value**</span></span>|<span data-ttu-id="b767f-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="b767f-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b767f-125">无</span><span class="sxs-lookup"><span data-stu-id="b767f-125">None</span></span>  <br/> |<span data-ttu-id="b767f-126">指示用户没有权限在日历中查看的项目。</span><span class="sxs-lookup"><span data-stu-id="b767f-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="b767f-127">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="b767f-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="b767f-128">指示用户有权在日历中查看仅忙/闲时间。</span><span class="sxs-lookup"><span data-stu-id="b767f-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="b767f-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="b767f-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="b767f-130">指示用户有权查看忙/闲时间中日历的主题和约会的位置。</span><span class="sxs-lookup"><span data-stu-id="b767f-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="b767f-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b767f-131">FullDetails</span></span>  <br/> |<span data-ttu-id="b767f-132">指示用户有权查看日历，包括忙/闲时间和主题、 位置和约会的详细信息中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="b767f-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b767f-133">备注</span><span class="sxs-lookup"><span data-stu-id="b767f-133">Remarks</span></span>

<span data-ttu-id="b767f-134">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b767f-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b767f-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="b767f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b767f-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="b767f-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b767f-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="b767f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="b767f-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="b767f-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="b767f-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="b767f-139">Validation File</span></span>  <br/> |<span data-ttu-id="b767f-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b767f-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b767f-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="b767f-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="b767f-142">False</span><span class="sxs-lookup"><span data-stu-id="b767f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b767f-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b767f-143">See also</span></span>



- [<span data-ttu-id="b767f-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b767f-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b767f-145">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="b767f-145">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

