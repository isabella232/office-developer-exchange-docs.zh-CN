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
description: DeleteFolderField 元素表示在 UpdateFolder 调用过程中从文件夹中删除给定属性的操作。
ms.openlocfilehash: a0b48b667c8c8afbd5729d5deb84359a6a6ccc25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462155"
---
# <a name="deletefolderfield"></a><span data-ttu-id="6abb5-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="6abb5-103">DeleteFolderField</span></span>

<span data-ttu-id="6abb5-104">**DeleteFolderField**元素表示在 UpdateFolder 调用过程中从文件夹中删除给定属性的操作。</span><span class="sxs-lookup"><span data-stu-id="6abb5-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="6abb5-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="6abb5-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="6abb5-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="6abb5-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="6abb5-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="6abb5-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="6abb5-108">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="6abb5-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="6abb5-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="6abb5-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <ExtendedFieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <IndexedFieldURI/>
</DeleteFolderField>
```

<span data-ttu-id="6abb5-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="6abb5-110">**DeleteFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6abb5-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6abb5-111">Attributes and elements</span></span>

<span data-ttu-id="6abb5-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6abb5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6abb5-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="6abb5-113">Attributes</span></span>

<span data-ttu-id="6abb5-114">无。</span><span class="sxs-lookup"><span data-stu-id="6abb5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6abb5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="6abb5-115">Child elements</span></span>

|<span data-ttu-id="6abb5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6abb5-116">**Element**</span></span>|<span data-ttu-id="6abb5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6abb5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6abb5-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="6abb5-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="6abb5-119">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="6abb5-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="6abb5-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="6abb5-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="6abb5-121">标识 dictionary 属性的各个成员。</span><span class="sxs-lookup"><span data-stu-id="6abb5-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="6abb5-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="6abb5-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="6abb5-123">标识扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="6abb5-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6abb5-124">父元素</span><span class="sxs-lookup"><span data-stu-id="6abb5-124">Parent elements</span></span>

|<span data-ttu-id="6abb5-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="6abb5-125">**Element**</span></span>|<span data-ttu-id="6abb5-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="6abb5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6abb5-127">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="6abb5-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="6abb5-128">包含一组元素，这些元素定义追加、设置和删除对文件夹属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="6abb5-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="6abb5-129">下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="6abb5-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6abb5-130">说明</span><span class="sxs-lookup"><span data-stu-id="6abb5-130">Remarks</span></span>

<span data-ttu-id="6abb5-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6abb5-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6abb5-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="6abb5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6abb5-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="6abb5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6abb5-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="6abb5-134">Schema Name</span></span>  <br/> |<span data-ttu-id="6abb5-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="6abb5-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="6abb5-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="6abb5-136">Validation File</span></span>  <br/> |<span data-ttu-id="6abb5-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6abb5-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6abb5-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="6abb5-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="6abb5-139">False</span><span class="sxs-lookup"><span data-stu-id="6abb5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6abb5-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6abb5-140">See also</span></span>

- [<span data-ttu-id="6abb5-141">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="6abb5-141">UpdateFolder operation</span></span>](updatefolder-operation.md)

