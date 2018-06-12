---
title: UnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnreadCount
api_type:
- schema
ms.assetid: 53b22647-1453-4707-9ea0-6a8369748d56
description: UnreadCount 元素包含文件夹中的未读项目的计数。
ms.openlocfilehash: fbe887f8f6d83fbcf48ed9593b3d19322a7f48be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838350"
---
# <a name="unreadcount"></a>UnreadCount

**UnreadCount**元素包含文件夹中的未读项目的计数。 
  
```XML
<UnreadCount/>
```

 **xs:int**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示修改项目或文件夹的事件。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示的整数值。 此属性是只读的。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

