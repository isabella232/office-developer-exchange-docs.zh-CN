---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: ArchiveTag 元素指定存档标记设置项目或文件夹的保留标识符。
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753261"
---
# <a name="archivetag"></a><span data-ttu-id="874f0-103">ArchiveTag</span><span class="sxs-lookup"><span data-stu-id="874f0-103">ArchiveTag</span></span>

<span data-ttu-id="874f0-104">**ArchiveTag**元素指定存档标记设置项目或文件夹的保留标识符。</span><span class="sxs-lookup"><span data-stu-id="874f0-104">The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder.</span></span> 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 <span data-ttu-id="874f0-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="874f0-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="874f0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="874f0-106">Attributes and elements</span></span>

<span data-ttu-id="874f0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="874f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="874f0-108">属性</span><span class="sxs-lookup"><span data-stu-id="874f0-108">Attributes</span></span>

|<span data-ttu-id="874f0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="874f0-109">**Attribute**</span></span>|<span data-ttu-id="874f0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="874f0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="874f0-111">**IsExplicit**</span><span class="sxs-lookup"><span data-stu-id="874f0-111">**IsExplicit**</span></span> <br/> |<span data-ttu-id="874f0-112">指定是否将保留策略的项或文件夹上明确地设置了或是否从父文件夹继承。</span><span class="sxs-lookup"><span data-stu-id="874f0-112">Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="874f0-113">子元素</span><span class="sxs-lookup"><span data-stu-id="874f0-113">Child elements</span></span>

<span data-ttu-id="874f0-114">无。</span><span class="sxs-lookup"><span data-stu-id="874f0-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="874f0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="874f0-115">Parent elements</span></span>

|<span data-ttu-id="874f0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="874f0-116">**Element**</span></span>|<span data-ttu-id="874f0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="874f0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="874f0-118">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="874f0-118">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="874f0-119">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="874f0-119">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="874f0-120">日历项目</span><span class="sxs-lookup"><span data-stu-id="874f0-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="874f0-121">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="874f0-121">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="874f0-122">联系人</span><span class="sxs-lookup"><span data-stu-id="874f0-122">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="874f0-123">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="874f0-123">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="874f0-124">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="874f0-124">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="874f0-125">表示包含在邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="874f0-125">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="874f0-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="874f0-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="874f0-127">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="874f0-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="874f0-128">Folder</span><span class="sxs-lookup"><span data-stu-id="874f0-128">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="874f0-129">定义一个文件夹，用于创建、 获取、 查找、 同步，或更新。</span><span class="sxs-lookup"><span data-stu-id="874f0-129">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="874f0-130">Item</span><span class="sxs-lookup"><span data-stu-id="874f0-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="874f0-131">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="874f0-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="874f0-132">Message</span><span class="sxs-lookup"><span data-stu-id="874f0-132">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="874f0-133">代表 Microsoft Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="874f0-133">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="874f0-134">PostItem</span><span class="sxs-lookup"><span data-stu-id="874f0-134">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="874f0-135">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="874f0-135">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="874f0-136">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="874f0-136">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="874f0-137">表示包含在邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="874f0-137">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="874f0-138">任务</span><span class="sxs-lookup"><span data-stu-id="874f0-138">Task</span></span>](task.md) <br/> |<span data-ttu-id="874f0-139">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="874f0-139">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="874f0-140">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="874f0-140">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="874f0-141">表示包含在邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="874f0-141">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="874f0-142">文本值</span><span class="sxs-lookup"><span data-stu-id="874f0-142">Text value</span></span>

<span data-ttu-id="874f0-143">**ArchiveTag**元素的文本值是一个标识的保留策略的 GUID。</span><span class="sxs-lookup"><span data-stu-id="874f0-143">The text value of the **ArchiveTag** element is a GUID that identifies the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="874f0-144">备注</span><span class="sxs-lookup"><span data-stu-id="874f0-144">Remarks</span></span>

<span data-ttu-id="874f0-145">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="874f0-145">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="874f0-146">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="874f0-146">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="874f0-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="874f0-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="874f0-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="874f0-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="874f0-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="874f0-149">Schema Name</span></span>  <br/> |<span data-ttu-id="874f0-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="874f0-150">Type schema</span></span>  <br/> |
|<span data-ttu-id="874f0-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="874f0-151">Validation File</span></span>  <br/> |<span data-ttu-id="874f0-152">types.xsd</span><span class="sxs-lookup"><span data-stu-id="874f0-152">types.xsd</span></span>  <br/> |
|<span data-ttu-id="874f0-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="874f0-153">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="874f0-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="874f0-154">See also</span></span>

- [<span data-ttu-id="874f0-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="874f0-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

