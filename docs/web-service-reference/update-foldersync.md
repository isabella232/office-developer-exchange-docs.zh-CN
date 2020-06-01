---
title: 更新 (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: Update 元素标识要在本地客户端存储中更新的单个文件夹。
ms.openlocfilehash: 5c1b5b1fd87e4651125293eac431c56f732c6c02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467135"
---
# <a name="update-foldersync"></a><span data-ttu-id="3f5f0-103">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="3f5f0-103">Update (FolderSync)</span></span>

<span data-ttu-id="3f5f0-104">**Update**元素标识要在本地客户端存储中更新的单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
- [<span data-ttu-id="3f5f0-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="3f5f0-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="3f5f0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3f5f0-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="3f5f0-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3f5f0-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="3f5f0-108">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="3f5f0-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md) 
- [<span data-ttu-id="3f5f0-109">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="3f5f0-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

```xml
<Update>
   <CalendarFolder/>
</Update>
```

```xml
<Update>
   <ContactsFolder/>
</Update>
```

```xml
<Update>
   <TasksFolder/>
</Update>
```

```xml
<Update>
   <SearchFolder/>
</Update>
```

<span data-ttu-id="3f5f0-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="3f5f0-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3f5f0-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3f5f0-111">Attributes and elements</span></span>

<span data-ttu-id="3f5f0-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f5f0-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="3f5f0-113">Attributes</span></span>

<span data-ttu-id="3f5f0-114">无。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f5f0-115">子元素</span><span class="sxs-lookup"><span data-stu-id="3f5f0-115">Child elements</span></span>

|<span data-ttu-id="3f5f0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3f5f0-116">**Element**</span></span>|<span data-ttu-id="3f5f0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f5f0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f5f0-118">Folder</span><span class="sxs-lookup"><span data-stu-id="3f5f0-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="3f5f0-119">定义要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="3f5f0-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="3f5f0-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="3f5f0-121">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="3f5f0-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="3f5f0-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="3f5f0-123">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3f5f0-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="3f5f0-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="3f5f0-125">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3f5f0-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="3f5f0-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="3f5f0-127">表示邮箱中 thcontained 的任务文件夹 t。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f5f0-128">父元素</span><span class="sxs-lookup"><span data-stu-id="3f5f0-128">Parent elements</span></span>

|<span data-ttu-id="3f5f0-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="3f5f0-129">**Element**</span></span>|<span data-ttu-id="3f5f0-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f5f0-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f5f0-131">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="3f5f0-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="3f5f0-132">包含更改类型的序列化数组，这些类型代表客户端上的文件夹和 Exchange 服务器上的文件夹之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f5f0-133">说明</span><span class="sxs-lookup"><span data-stu-id="3f5f0-133">Remarks</span></span>

<span data-ttu-id="3f5f0-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3f5f0-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f5f0-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="3f5f0-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f5f0-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="3f5f0-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f5f0-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="3f5f0-137">Schema name</span></span>  <br/> |<span data-ttu-id="3f5f0-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="3f5f0-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="3f5f0-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="3f5f0-139">Validation file</span></span>  <br/> |<span data-ttu-id="3f5f0-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f5f0-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f5f0-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="3f5f0-141">Can be empty</span></span>  <br/> |<span data-ttu-id="3f5f0-142">False</span><span class="sxs-lookup"><span data-stu-id="3f5f0-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f5f0-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f5f0-143">See also</span></span>

- [<span data-ttu-id="3f5f0-144">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="3f5f0-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="3f5f0-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3f5f0-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

