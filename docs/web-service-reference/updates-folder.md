---
title: Updates 文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: Updates元素中包含的一组定义的元素追加、 设置，以及删除对文件夹属性的更改。
ms.openlocfilehash: 31f25b1e88fb8756f189a6d75259dd4fc198582f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838427"
---
# <a name="updates-folder"></a><span data-ttu-id="f970a-103">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="f970a-103">Updates (Folder)</span></span>

<span data-ttu-id="f970a-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Updates**元素中包含的一组定义的元素追加、 设置，以及删除对文件夹属性的更改。</span><span class="sxs-lookup"><span data-stu-id="f970a-104">The **Updates** element contains a set of elements that define append, set, and delete changes to folder properties.</span></span> 
  
- [<span data-ttu-id="f970a-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="f970a-105">UpdateFolder</span></span>](updatefolder.md)
  
- [<span data-ttu-id="f970a-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="f970a-106">FolderChanges</span></span>](folderchanges.md)
  
- [<span data-ttu-id="f970a-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="f970a-107">FolderChange</span></span>](folderchange.md)
  
- [<span data-ttu-id="f970a-108">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="f970a-108">Updates (Folder)</span></span>](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

<span data-ttu-id="f970a-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="f970a-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f970a-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f970a-110">Attributes and elements</span></span>

<span data-ttu-id="f970a-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f970a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f970a-112">属性</span><span class="sxs-lookup"><span data-stu-id="f970a-112">Attributes</span></span>

<span data-ttu-id="f970a-113">无。</span><span class="sxs-lookup"><span data-stu-id="f970a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f970a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f970a-114">Child elements</span></span>

|<span data-ttu-id="f970a-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="f970a-115">**Element**</span></span>|<span data-ttu-id="f970a-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="f970a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f970a-117">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="f970a-117">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="f970a-118">表示要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="f970a-118">Represents data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f970a-119">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="f970a-119">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="f970a-120">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="f970a-120">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f970a-121">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="f970a-121">DeleteFolderField</span></span>](deletefolderfield.md) <br/> |<span data-ttu-id="f970a-122">表示要在[UpdateFolder Operation](updatefolder-operation.md)期间从文件夹中删除给定的属性的操作。</span><span class="sxs-lookup"><span data-stu-id="f970a-122">Represents an operation to delete a given property from a folder during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f970a-123">父元素</span><span class="sxs-lookup"><span data-stu-id="f970a-123">Parent elements</span></span>

|<span data-ttu-id="f970a-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="f970a-124">**Element**</span></span>|<span data-ttu-id="f970a-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="f970a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f970a-126">FolderChange</span><span class="sxs-lookup"><span data-stu-id="f970a-126">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="f970a-127">表示要在单个文件夹上进行的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="f970a-127">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="f970a-128">下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange[i]`</span><span class="sxs-lookup"><span data-stu-id="f970a-128">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f970a-129">备注</span><span class="sxs-lookup"><span data-stu-id="f970a-129">Remarks</span></span>

<span data-ttu-id="f970a-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f970a-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f970a-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="f970a-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f970a-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="f970a-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f970a-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="f970a-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f970a-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="f970a-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f970a-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="f970a-135">Validation File</span></span>  <br/> |<span data-ttu-id="f970a-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f970a-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f970a-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="f970a-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f970a-138">False</span><span class="sxs-lookup"><span data-stu-id="f970a-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f970a-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f970a-139">See also</span></span>

- [<span data-ttu-id="f970a-140">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="f970a-140">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="f970a-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f970a-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
