---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: ArchiveTag 元素指定存档标记设置项目或文件夹的保留标识符。
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753261"
---
# <a name="archivetag"></a>ArchiveTag

**ArchiveTag**元素指定存档标记设置项目或文件夹的保留标识符。 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**IsExplicit** <br/> |指定是否将保留策略的项或文件夹上明确地设置了或是否从父文件夹继承。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |表示主要包含日历项目的文件夹。  <br/> |
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示对 Exchange 存储中的联系人项目。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示包含在邮箱中的联系人文件夹。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[Folder](folder.md) <br/> |定义一个文件夹，用于创建、 获取、 查找、 同步，或更新。  <br/> |
|[Item](item.md) <br/> |表示 Exchange 存储中的泛型项。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |代表 Microsoft Exchange 电子邮件。  <br/> |
|[PostItem](postitem.md) <br/> |代表一个 Exchange 存储中的公告项目。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示包含在邮箱中的搜索文件夹。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示包含在邮箱中的任务文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

**ArchiveTag**元素的文本值是一个标识的保留策略的 GUID。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

