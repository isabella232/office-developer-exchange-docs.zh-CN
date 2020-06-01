---
title: AppendToItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppendToItemField
api_type:
- schema
ms.assetid: 66dbcb4a-ae6d-4648-8610-67187bdb105c
description: AppendToItemField 元素标识在 UpdateItem 操作过程中追加到项的单个属性的数据。
ms.openlocfilehash: 902239155bff45d6f81989de954c9459cf012288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466043"
---
# <a name="appendtoitemfield"></a>AppendToItemField

**AppendToItemField**元素标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [更新（项目）](updates-item.md)
  
- [AppendToItemField](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 **AppendToItemFieldType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识要追加的扩展 MAPI 属性。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[更新（项目）](updates-item.md) <br/> |包含定义追加、设置和删除对项属性所做的更改的数组。  <br/> 下面是此元素的 XPath 表达式:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a>备注

只有某些属性支持 append 操作。 如果尝试追加到不支持追加的属性，则会导致错误。
  
对于更新操作，只能在单个请求中修改一个属性。 必须在[Path](path.md)元素中引用该单个属性。 然后，派生类中的**Item**元素可以仅保留与单个**Path**元素一致的单个属性。 
  
> [!NOTE]
> [Path](path.md)元素是抽象的。 它必须由[FieldURI](fielduri.md)、 [IndexedFieldURI](indexedfielduri.md)或[ExtendedFieldURI](extendedfielduri.md)元素替代。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateItem 操作](updateitem-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

