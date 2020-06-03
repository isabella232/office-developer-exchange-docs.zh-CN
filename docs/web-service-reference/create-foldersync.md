---
title: 创建 (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: Create 元素标识要在本地客户端存储中创建的单个文件夹。
ms.openlocfilehash: 43f6a6b3c084c8ecae767c512181bbdf50c7e786
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458374"
---
# <a name="create-foldersync"></a><span data-ttu-id="29ff4-103">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="29ff4-103">Create (FolderSync)</span></span>

<span data-ttu-id="29ff4-104">**Create**元素标识要在本地客户端存储中创建的单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="29ff4-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="29ff4-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="29ff4-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="29ff4-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="29ff4-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="29ff4-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="29ff4-108">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="29ff4-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="29ff4-109">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="29ff4-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="29ff4-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="29ff4-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29ff4-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="29ff4-111">Attributes and elements</span></span>

<span data-ttu-id="29ff4-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="29ff4-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29ff4-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="29ff4-113">Attributes</span></span>

<span data-ttu-id="29ff4-114">无。</span><span class="sxs-lookup"><span data-stu-id="29ff4-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29ff4-115">子元素</span><span class="sxs-lookup"><span data-stu-id="29ff4-115">Child elements</span></span>

|<span data-ttu-id="29ff4-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="29ff4-116">**Element**</span></span>|<span data-ttu-id="29ff4-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="29ff4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ff4-118">Folder</span><span class="sxs-lookup"><span data-stu-id="29ff4-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="29ff4-119">定义要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="29ff4-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="29ff4-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="29ff4-121">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="29ff4-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="29ff4-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="29ff4-123">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="29ff4-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="29ff4-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="29ff4-125">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="29ff4-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="29ff4-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="29ff4-127">表示邮箱中包含的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="29ff4-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="29ff4-128">父元素</span><span class="sxs-lookup"><span data-stu-id="29ff4-128">Parent elements</span></span>

|<span data-ttu-id="29ff4-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="29ff4-129">**Element**</span></span>|<span data-ttu-id="29ff4-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="29ff4-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ff4-131">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="29ff4-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="29ff4-132">包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="29ff4-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ff4-133">说明</span><span class="sxs-lookup"><span data-stu-id="29ff4-133">Remarks</span></span>

<span data-ttu-id="29ff4-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="29ff4-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29ff4-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="29ff4-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29ff4-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="29ff4-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29ff4-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="29ff4-137">Schema name</span></span>  <br/> |<span data-ttu-id="29ff4-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="29ff4-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="29ff4-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="29ff4-139">Validation file</span></span>  <br/> |<span data-ttu-id="29ff4-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="29ff4-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29ff4-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="29ff4-141">Can be empty</span></span>  <br/> |<span data-ttu-id="29ff4-142">False</span><span class="sxs-lookup"><span data-stu-id="29ff4-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29ff4-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="29ff4-143">See also</span></span>



[<span data-ttu-id="29ff4-144">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="29ff4-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="29ff4-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="29ff4-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

