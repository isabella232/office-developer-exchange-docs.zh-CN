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
description: 更新元素标识一个文件夹中的本地客户端存储更新。
ms.openlocfilehash: 6d4a6233df41ea95e1fd9b394502bfb2728bddb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838361"
---
# <a name="update-foldersync"></a><span data-ttu-id="38475-103">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="38475-103">Update (FolderSync)</span></span>

<span data-ttu-id="38475-104">**更新**元素标识一个文件夹中的本地客户端存储更新。</span><span class="sxs-lookup"><span data-stu-id="38475-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
[<span data-ttu-id="38475-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="38475-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="38475-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="38475-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="38475-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="38475-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="38475-108">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="38475-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="38475-109">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="38475-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

 <span data-ttu-id="38475-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="38475-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38475-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="38475-111">Attributes and elements</span></span>

<span data-ttu-id="38475-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="38475-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38475-113">属性</span><span class="sxs-lookup"><span data-stu-id="38475-113">Attributes</span></span>

<span data-ttu-id="38475-114">无。</span><span class="sxs-lookup"><span data-stu-id="38475-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38475-115">子元素</span><span class="sxs-lookup"><span data-stu-id="38475-115">Child elements</span></span>

|<span data-ttu-id="38475-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="38475-116">**Element**</span></span>|<span data-ttu-id="38475-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="38475-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38475-118">Folder</span><span class="sxs-lookup"><span data-stu-id="38475-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="38475-119">定义要创建、 获取、 查找、 同步，或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="38475-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="38475-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="38475-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="38475-121">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="38475-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="38475-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="38475-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="38475-123">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="38475-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="38475-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="38475-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="38475-125">表示包含在邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="38475-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="38475-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="38475-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="38475-127">代表的任务文件夹 t 是 thcontained 邮箱中的。</span><span class="sxs-lookup"><span data-stu-id="38475-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38475-128">父元素</span><span class="sxs-lookup"><span data-stu-id="38475-128">Parent elements</span></span>

|<span data-ttu-id="38475-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="38475-129">**Element**</span></span>|<span data-ttu-id="38475-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="38475-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38475-131">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="38475-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="38475-132">包含表示的客户端上的文件夹和 Exchange 服务器上的文件夹之间的差异的类型的更改类型排序的数组。</span><span class="sxs-lookup"><span data-stu-id="38475-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38475-133">备注</span><span class="sxs-lookup"><span data-stu-id="38475-133">Remarks</span></span>

<span data-ttu-id="38475-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="38475-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38475-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="38475-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38475-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="38475-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38475-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="38475-137">Schema name</span></span>  <br/> |<span data-ttu-id="38475-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="38475-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="38475-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="38475-139">Validation file</span></span>  <br/> |<span data-ttu-id="38475-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38475-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38475-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="38475-141">Can be empty</span></span>  <br/> |<span data-ttu-id="38475-142">False</span><span class="sxs-lookup"><span data-stu-id="38475-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38475-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38475-143">See also</span></span>



[<span data-ttu-id="38475-144">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="38475-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="38475-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="38475-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

