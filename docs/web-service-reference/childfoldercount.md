---
title: ChildFolderCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ChildFolderCount
api_type:
- schema
ms.assetid: e0e4eabd-802f-4dd0-9911-89e08c66a15e
description: ChildFolderCount 元素表示文件夹中包含的直接子文件夹的数量。 此属性是只读的。
ms.openlocfilehash: c05d93e3f9df2d2acbb1b65f1116dab1aea24a3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536999"
---
# <a name="childfoldercount"></a>ChildFolderCount

**ChildFolderCount** 元素表示文件夹中包含的直接子文件夹的数量。 此属性是只读的。 
  
```xml
<ChildFolderCount/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示邮箱中的日历文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |代表邮箱中的"联系人"文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |代表邮箱中的"任务"文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示一个整数。 此属性是只读的。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

