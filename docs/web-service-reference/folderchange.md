---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: FolderChange 元素表示要在单个文件夹执行的更改的集合。
ms.openlocfilehash: 3f8b42ff4ac88eaef53d1d4ec1d61212bc14b8c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754389"
---
# <a name="folderchange"></a><span data-ttu-id="c076d-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="c076d-103">FolderChange</span></span>

<span data-ttu-id="c076d-104">**FolderChange**元素表示要在单个文件夹执行的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="c076d-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
[<span data-ttu-id="c076d-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="c076d-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="c076d-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="c076d-106">FolderChanges</span></span>](folderchanges.md)
  
[<span data-ttu-id="c076d-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="c076d-107">FolderChange</span></span>](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

 <span data-ttu-id="c076d-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="c076d-108">**FolderChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c076d-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c076d-109">Attributes and elements</span></span>

<span data-ttu-id="c076d-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c076d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c076d-111">属性</span><span class="sxs-lookup"><span data-stu-id="c076d-111">Attributes</span></span>

<span data-ttu-id="c076d-112">无。</span><span class="sxs-lookup"><span data-stu-id="c076d-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c076d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="c076d-113">Child elements</span></span>

|<span data-ttu-id="c076d-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="c076d-114">**Element**</span></span>|<span data-ttu-id="c076d-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="c076d-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c076d-116">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="c076d-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c076d-117">包含要更新的文件夹的标识符和更改密钥。</span><span class="sxs-lookup"><span data-stu-id="c076d-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="c076d-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c076d-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c076d-119">标识可以通过名称引用的 MicrosoftExchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="c076d-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="c076d-120">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="c076d-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="c076d-121">定义文件夹，由[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素执行更新的类型。</span><span class="sxs-lookup"><span data-stu-id="c076d-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c076d-122">父元素</span><span class="sxs-lookup"><span data-stu-id="c076d-122">Parent elements</span></span>

|<span data-ttu-id="c076d-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="c076d-123">**Element**</span></span>|<span data-ttu-id="c076d-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="c076d-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c076d-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="c076d-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="c076d-126">表示的文件夹的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="c076d-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="c076d-127">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="c076d-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c076d-128">备注</span><span class="sxs-lookup"><span data-stu-id="c076d-128">Remarks</span></span>

<span data-ttu-id="c076d-129">描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c076d-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c076d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="c076d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c076d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="c076d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c076d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="c076d-132">Schema name</span></span>  <br/> |<span data-ttu-id="c076d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="c076d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c076d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="c076d-134">Validation file</span></span>  <br/> |<span data-ttu-id="c076d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c076d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c076d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="c076d-136">Can be empty</span></span>  <br/> |<span data-ttu-id="c076d-137">False</span><span class="sxs-lookup"><span data-stu-id="c076d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c076d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c076d-138">See also</span></span>



[<span data-ttu-id="c076d-139">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c076d-139">UpdateFolder operation</span></span>](updatefolder-operation.md)

