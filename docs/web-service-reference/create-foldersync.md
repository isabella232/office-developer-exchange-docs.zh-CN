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
description: 创建元素标识在本地客户端库中创建一个文件夹。
ms.openlocfilehash: 867eecb89c115b008d4828e162b21d078eba695c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753618"
---
# <a name="create-foldersync"></a><span data-ttu-id="b7921-103">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b7921-103">Create (FolderSync)</span></span>

<span data-ttu-id="b7921-104">**创建**元素标识在本地客户端库中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="b7921-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="b7921-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="b7921-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7921-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="b7921-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7921-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="b7921-108">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="b7921-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="b7921-109">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b7921-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="b7921-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="b7921-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7921-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7921-111">Attributes and elements</span></span>

<span data-ttu-id="b7921-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7921-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7921-113">属性</span><span class="sxs-lookup"><span data-stu-id="b7921-113">Attributes</span></span>

<span data-ttu-id="b7921-114">无。</span><span class="sxs-lookup"><span data-stu-id="b7921-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7921-115">子元素</span><span class="sxs-lookup"><span data-stu-id="b7921-115">Child elements</span></span>

|<span data-ttu-id="b7921-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7921-116">**Element**</span></span>|<span data-ttu-id="b7921-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7921-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7921-118">Folder</span><span class="sxs-lookup"><span data-stu-id="b7921-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="b7921-119">定义要创建、 获取、 查找、 同步，或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="b7921-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="b7921-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="b7921-121">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="b7921-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="b7921-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="b7921-123">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b7921-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="b7921-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="b7921-125">表示邮箱中所包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b7921-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="b7921-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="b7921-127">表示邮箱中所包含的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="b7921-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7921-128">父元素</span><span class="sxs-lookup"><span data-stu-id="b7921-128">Parent elements</span></span>

|<span data-ttu-id="b7921-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7921-129">**Element**</span></span>|<span data-ttu-id="b7921-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7921-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7921-131">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="b7921-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="b7921-132">包含表示的客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="b7921-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7921-133">备注</span><span class="sxs-lookup"><span data-stu-id="b7921-133">Remarks</span></span>

<span data-ttu-id="b7921-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7921-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7921-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7921-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7921-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7921-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7921-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7921-137">Schema name</span></span>  <br/> |<span data-ttu-id="b7921-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="b7921-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="b7921-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7921-139">Validation file</span></span>  <br/> |<span data-ttu-id="b7921-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b7921-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7921-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7921-141">Can be empty</span></span>  <br/> |<span data-ttu-id="b7921-142">False</span><span class="sxs-lookup"><span data-stu-id="b7921-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7921-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7921-143">See also</span></span>



[<span data-ttu-id="b7921-144">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="b7921-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="b7921-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7921-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

