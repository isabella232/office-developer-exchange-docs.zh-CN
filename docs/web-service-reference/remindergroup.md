---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: ReminderGroup 元素指定提醒是用于日历项目还是任务。
ms.openlocfilehash: be6f4a7d7e9d495ed7b42ed40c60f016468e8c2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529866"
---
# <a name="remindergroup"></a>ReminderGroup

**ReminderGroup**元素指定提醒是用于日历项目还是任务。 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 **ReminderGroupType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[提醒](reminder.md)
  
## <a name="text-value"></a>文本值

**ReminderGroup**元素的文本值是提醒的组类型。 **Calendar**的文本值指定 "日历" 项目的提醒。 **任务**的文本值指定该提醒针对的是任务项。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[提醒](reminder.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

