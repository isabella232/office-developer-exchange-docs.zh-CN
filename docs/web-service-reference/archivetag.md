---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: ArchiveTag 元素指定在项目或文件夹上设置的存档标记的保留标识符。
ms.openlocfilehash: 23167f3c96a6756fe4c6d915a4de91e815e620d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464761"
---
# <a name="archivetag"></a><span data-ttu-id="5ad3d-103">ArchiveTag</span><span class="sxs-lookup"><span data-stu-id="5ad3d-103">ArchiveTag</span></span>

<span data-ttu-id="5ad3d-104">**ArchiveTag**元素指定在项目或文件夹上设置的存档标记的保留标识符。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-104">The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder.</span></span> 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 <span data-ttu-id="5ad3d-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ad3d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5ad3d-106">Attributes and elements</span></span>

<span data-ttu-id="5ad3d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ad3d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5ad3d-108">Attributes</span></span>

|<span data-ttu-id="5ad3d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-109">**Attribute**</span></span>|<span data-ttu-id="5ad3d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ad3d-111">**IsExplicit**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-111">**IsExplicit**</span></span> <br/> |<span data-ttu-id="5ad3d-112">指定是在项目或文件夹中显式设置保留策略，还是从父文件夹中继承保留策略。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-112">Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ad3d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="5ad3d-113">Child elements</span></span>

<span data-ttu-id="5ad3d-114">无。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ad3d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5ad3d-115">Parent elements</span></span>

|<span data-ttu-id="5ad3d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-116">**Element**</span></span>|<span data-ttu-id="5ad3d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5ad3d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ad3d-118">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="5ad3d-118">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="5ad3d-119">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-119">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5ad3d-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5ad3d-121">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-121">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-122">联系人</span><span class="sxs-lookup"><span data-stu-id="5ad3d-122">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5ad3d-123">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-123">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-124">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="5ad3d-124">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="5ad3d-125">表示邮箱中包含的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-125">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5ad3d-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5ad3d-127">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-128">Folder</span><span class="sxs-lookup"><span data-stu-id="5ad3d-128">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="5ad3d-129">定义要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-129">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-130">项</span><span class="sxs-lookup"><span data-stu-id="5ad3d-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="5ad3d-131">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-132">邮件</span><span class="sxs-lookup"><span data-stu-id="5ad3d-132">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5ad3d-133">表示 Microsoft Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-133">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-134">PostItem</span><span class="sxs-lookup"><span data-stu-id="5ad3d-134">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="5ad3d-135">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-135">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-136">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5ad3d-136">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="5ad3d-137">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-137">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-138">任务</span><span class="sxs-lookup"><span data-stu-id="5ad3d-138">Task</span></span>](task.md) <br/> |<span data-ttu-id="5ad3d-139">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-139">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5ad3d-140">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="5ad3d-140">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="5ad3d-141">表示邮箱中包含的 "任务" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-141">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5ad3d-142">文本值</span><span class="sxs-lookup"><span data-stu-id="5ad3d-142">Text value</span></span>

<span data-ttu-id="5ad3d-143">**ArchiveTag**元素的文本值是标识保留策略的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-143">The text value of the **ArchiveTag** element is a GUID that identifies the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5ad3d-144">备注</span><span class="sxs-lookup"><span data-stu-id="5ad3d-144">Remarks</span></span>

<span data-ttu-id="5ad3d-145">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-145">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5ad3d-146">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5ad3d-146">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ad3d-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="5ad3d-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ad3d-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="5ad3d-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5ad3d-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="5ad3d-149">Schema Name</span></span>  <br/> |<span data-ttu-id="5ad3d-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="5ad3d-150">Type schema</span></span>  <br/> |
|<span data-ttu-id="5ad3d-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="5ad3d-151">Validation File</span></span>  <br/> |<span data-ttu-id="5ad3d-152">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="5ad3d-152">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5ad3d-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="5ad3d-153">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5ad3d-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5ad3d-154">See also</span></span>

- [<span data-ttu-id="5ad3d-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5ad3d-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

