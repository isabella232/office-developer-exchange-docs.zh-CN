---
title: SetFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetFolderField
api_type:
- schema
ms.assetid: 8c69db7b-54b5-4ae2-abca-4d6e0937a790
description: SetFolderField 元素表示一个更新，该更新在 UpdateFolder 操作中设置文件夹中单个属性的值。
ms.openlocfilehash: ab75a3862801b9a7b3369d9a4116c653b461781c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530315"
---
# <a name="setfolderfield"></a><span data-ttu-id="655a0-103">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="655a0-103">SetFolderField</span></span>

<span data-ttu-id="655a0-104">**SetFolderField**元素表示一个更新，该更新在 UpdateFolder 操作中设置文件夹中单个属性的值。</span><span class="sxs-lookup"><span data-stu-id="655a0-104">The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation.</span></span> 

```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```
  
```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <SearchFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <Folder/> 
</SetFolderField>
```

```xml
<SetFolderField>
    <IndexedFieldURI/> 
    <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <TasksFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <Folder/>
</SetFolderField>
```

```xml
<SetFolderField>
    <FieldURI/> 
    <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <ContactsFolder/> 
</SetFolderField>
```


<span data-ttu-id="655a0-105">**SetFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="655a0-105">**SetFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="655a0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="655a0-106">Attributes and elements</span></span>

<span data-ttu-id="655a0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="655a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="655a0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="655a0-108">Attributes</span></span>

<span data-ttu-id="655a0-109">无。</span><span class="sxs-lookup"><span data-stu-id="655a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="655a0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="655a0-110">Child elements</span></span>

|<span data-ttu-id="655a0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="655a0-111">**Element**</span></span>|<span data-ttu-id="655a0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="655a0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="655a0-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="655a0-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="655a0-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="655a0-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="655a0-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="655a0-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="655a0-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="655a0-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="655a0-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="655a0-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="655a0-118">标识扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="655a0-118">Identifies extended MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="655a0-119">Folder</span><span class="sxs-lookup"><span data-stu-id="655a0-119">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="655a0-120">标识要更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="655a0-120">Identifies a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="655a0-121">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="655a0-121">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="655a0-122">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="655a0-122">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="655a0-123">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="655a0-123">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="655a0-124">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="655a0-124">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="655a0-125">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="655a0-125">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="655a0-126">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="655a0-126">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="655a0-127">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="655a0-127">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="655a0-128">表示邮箱中包含的 "任务" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="655a0-128">Represents a Tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="655a0-129">父元素</span><span class="sxs-lookup"><span data-stu-id="655a0-129">Parent elements</span></span>

|<span data-ttu-id="655a0-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="655a0-130">**Element**</span></span>|<span data-ttu-id="655a0-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="655a0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="655a0-132">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="655a0-132">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="655a0-133">包含一组元素，这些元素定义追加、设置和删除对文件夹属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="655a0-133">Contains a set of elements that defines append, set, and delete changes to folder properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="655a0-134">备注</span><span class="sxs-lookup"><span data-stu-id="655a0-134">Remarks</span></span>

<span data-ttu-id="655a0-135">如果该属性存在，则将属性值设置为指定的值。</span><span class="sxs-lookup"><span data-stu-id="655a0-135">If the property exists, the property value is set to the specified value.</span></span> <span data-ttu-id="655a0-136">如果该属性不存在，则使用指定的值创建属性。</span><span class="sxs-lookup"><span data-stu-id="655a0-136">If the property does not exist, the property is created with the specified value.</span></span>
  
<span data-ttu-id="655a0-137">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="655a0-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="655a0-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="655a0-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="655a0-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="655a0-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="655a0-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="655a0-140">Schema Name</span></span>  <br/> |<span data-ttu-id="655a0-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="655a0-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="655a0-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="655a0-142">Validation File</span></span>  <br/> |<span data-ttu-id="655a0-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="655a0-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="655a0-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="655a0-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="655a0-145">False</span><span class="sxs-lookup"><span data-stu-id="655a0-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="655a0-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="655a0-146">See also</span></span>

- [<span data-ttu-id="655a0-147">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="655a0-147">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="655a0-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="655a0-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

