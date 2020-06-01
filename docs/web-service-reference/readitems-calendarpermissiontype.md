---
title: ReadItems （CalendarPermissionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: ReadItems 元素指示用户是否有权读取日历文件夹中的项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e040b643016781f9f890050f189191356f8d4f0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468297"
---
# <a name="readitems-calendarpermissiontype"></a>ReadItems （CalendarPermissionType）

**ReadItems**元素指示用户是否有权读取日历文件夹中的项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 **CalendarPermissionReadAccessType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**ReadItems**元素的可能值。 
  
**ReadItems 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示用户不具有查看日历中的项目的权限。  <br/> |
|TimeOnly  <br/> |指示用户具有仅查看日历中的忙/闲时间的权限。  <br/> |
|TimeAndSubjectAndLocation  <br/> |指示用户有权查看日历中的忙/闲时间以及约会的主题和位置。  <br/> |
|FullDetails  <br/> |指示用户有权查看日历中的所有项目，包括忙/闲时间、主题、位置和约会的详细信息。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

