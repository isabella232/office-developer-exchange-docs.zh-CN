---
title: ReminderMessageData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: ReminderMessageData 元素指定提醒邮件中的数据。
ms.openlocfilehash: f2632062cd02581c426f7dbfa2a33d53e5594d72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458549"
---
# <a name="remindermessagedata"></a>ReminderMessageData

**ReminderMessageData**元素指定提醒邮件中的数据。 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 **ReminderMessageDataType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ReminderText](remindertext.md)  | [位置](location.md)  | [StartTime （ReminderMessageDataType）](starttime-remindermessagedatatype.md)  | [EndTime （ReminderMessageDataType）](endtime-remindermessagedatatype.md)  | [AssociatedCalendarItemId](associatedcalendaritemid.md)
  
### <a name="parent-elements"></a>父元素

[邮件](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
从内部版本号15.00.0913.09 开始的 Exchange 版本可以将**AssociatedCalendarItemId**元素作为**ReminderMessageData**元素的子元素包括在内。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[邮件](message-ex15websvcsotherref.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

