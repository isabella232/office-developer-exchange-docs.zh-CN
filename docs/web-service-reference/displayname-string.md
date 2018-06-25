---
title: DisplayName （字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisplayName
api_type:
- schema
ms.assetid: e7efbbe1-6629-4d11-bed1-ed899e3f9d77
description: DisplayName 元素定义文件夹、 联系人、 通讯组列表、 代理用户、 位置或规则的显示名称。
ms.openlocfilehash: 53f4e083d9e6617206e383d4408e08ed7ea0fe08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753932"
---
# <a name="displayname-string"></a>DisplayName （字符串）

**DisplayName**元素定义文件夹、 联系人、 通讯组列表、 代理用户、 位置或规则的显示名称。 
  
```XML
<DisplayName/>
```

 **字符串**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |表示邮箱中的日历文件夹。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[规则 (RuleType)](rule-ruletype.md) <br/> |代表用户的邮箱中的规则。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[用户 Id](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示的显示名称的文本值。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示如何创建一个新文件夹并设置为"TestFolder"文件夹的 DisplayName。
  
```cs
FolderType folder = new FolderType();
folder.DisplayName = "TestFolder";
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

