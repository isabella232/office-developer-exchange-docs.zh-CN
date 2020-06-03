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
# <a name="setfolderfield"></a>SetFolderField

**SetFolderField**元素表示一个更新，该更新在 UpdateFolder 操作中设置文件夹中单个属性的值。 

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


**SetFolderFieldType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识扩展 MAPI 属性。  <br/> |
|[Folder](folder.md) <br/> |标识要更新的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |代表主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的 "联系人" 文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中包含的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中包含的 "任务" 文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Updates 文件夹](updates-folder.md) <br/> |包含一组元素，这些元素定义追加、设置和删除对文件夹属性所做的更改。  <br/> |
   
## <a name="remarks"></a>备注

如果该属性存在，则将属性值设置为指定的值。 如果该属性不存在，则使用指定的值创建属性。
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateFolder 操作](updatefolder-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

