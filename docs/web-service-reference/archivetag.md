---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: ArchiveTag 元素指定在项目或文件夹上设置的存档标记的保留标识符。
ms.openlocfilehash: c3545b505dc0596d7465154e0be7d6c758b24ec9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525237"
---
# <a name="archivetag"></a>ArchiveTag

**ArchiveTag** 元素指定在项目或文件夹上设置的存档标记的保留标识符。 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**IsExplicit** <br/> |指定是否对项目或文件夹显式设置保留策略，或者是否从父文件夹继承保留策略。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |表示一个主要包含日历项目的文件夹。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示对 Exchange 存储中的联系人项目。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示包含在邮箱中的联系人文件夹。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[Folder](folder.md) <br/> |定义要创建、获取、查找、同步或更新的文件夹。  <br/> |
|[项目](item.md) <br/> |表示活动存储中的Exchange项。  <br/> |
|[消息](message-ex15websvcsotherref.md) <br/> |代表 Microsoft Exchange电子邮件。  <br/> |
|[PostItem](postitem.md) <br/> |表示应用商店中的Exchange项。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示包含在邮箱中的搜索文件夹。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示包含在邮箱中的任务文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

**ArchiveTag** 元素的文本值是标识保留策略的 GUID。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

