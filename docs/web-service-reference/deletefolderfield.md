---
title: DeleteFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderField
api_type:
- schema
ms.assetid: f9c2187b-4c60-4358-b4b4-ede50eadae48
description: DeleteFolderField 元素均表示 UpdateFolder 呼叫期间，从文件夹中删除给定的属性的操作。
ms.openlocfilehash: d0a5fb18c5f3445982a6417007ad6af9b1b365af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753802"
---
# <a name="deletefolderfield"></a><span data-ttu-id="05b12-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="05b12-103">DeleteFolderField</span></span>

<span data-ttu-id="05b12-104">**DeleteFolderField**元素均表示 UpdateFolder 呼叫期间，从文件夹中删除给定的属性的操作。</span><span class="sxs-lookup"><span data-stu-id="05b12-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="05b12-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="05b12-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="05b12-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="05b12-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="05b12-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="05b12-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="05b12-108">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="05b12-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="05b12-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="05b12-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

 <span data-ttu-id="05b12-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="05b12-110">**DeleteFolderFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05b12-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="05b12-111">Attributes and elements</span></span>

<span data-ttu-id="05b12-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05b12-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05b12-113">属性</span><span class="sxs-lookup"><span data-stu-id="05b12-113">Attributes</span></span>

<span data-ttu-id="05b12-114">无。</span><span class="sxs-lookup"><span data-stu-id="05b12-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05b12-115">子元素</span><span class="sxs-lookup"><span data-stu-id="05b12-115">Child elements</span></span>

|<span data-ttu-id="05b12-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="05b12-116">**Element**</span></span>|<span data-ttu-id="05b12-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="05b12-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05b12-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="05b12-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="05b12-119">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="05b12-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="05b12-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="05b12-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="05b12-121">标识字典属性中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="05b12-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="05b12-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="05b12-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="05b12-123">标识扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="05b12-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05b12-124">父元素</span><span class="sxs-lookup"><span data-stu-id="05b12-124">Parent elements</span></span>

|<span data-ttu-id="05b12-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="05b12-125">**Element**</span></span>|<span data-ttu-id="05b12-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="05b12-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05b12-127">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="05b12-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="05b12-128">包含一组定义的元素的 append、 设置和删除对文件夹属性的更改。</span><span class="sxs-lookup"><span data-stu-id="05b12-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="05b12-129">下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="05b12-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05b12-130">备注</span><span class="sxs-lookup"><span data-stu-id="05b12-130">Remarks</span></span>

<span data-ttu-id="05b12-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="05b12-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05b12-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="05b12-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05b12-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="05b12-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05b12-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="05b12-134">Schema Name</span></span>  <br/> |<span data-ttu-id="05b12-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="05b12-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="05b12-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="05b12-136">Validation File</span></span>  <br/> |<span data-ttu-id="05b12-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05b12-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05b12-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="05b12-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="05b12-139">False</span><span class="sxs-lookup"><span data-stu-id="05b12-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05b12-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05b12-140">See also</span></span>

- [<span data-ttu-id="05b12-141">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="05b12-141">UpdateFolder operation</span></span>](updatefolder-operation.md)

