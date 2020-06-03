---
title: 创建（ItemSync）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: Create 元素标识要在本地客户端存储中创建的单个项目。
ms.openlocfilehash: b9c0f28333594a6c17ee9581a227fc4773874fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460797"
---
# <a name="create-itemsync"></a>创建（ItemSync）

**Create**元素标识要在本地客户端存储中创建的单个项目。 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) 
- [更改（项目）](changes-items.md) 
- [创建（ItemSync）](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Item](item.md) <br/> |表示要创建的通用 Exchange 项。  <br/> |
|[消息](message-ex15websvcsotherref.md) <br/> |表示要创建的 Exchange 电子邮件。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |代表要创建的 Exchange 日历项目。  <br/> |
|[联系人](contact.md) <br/> |表示要创建的 Exchange 联系人项。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示要创建的通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示要创建的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示要创建的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示要创建的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示要创建的会议取消。  <br/> |
|[任务](task.md) <br/> |表示要创建的任务。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[更改（项目）](changes-items.md) <br/> |包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。  <br/> |
   
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

- [SyncFolderItems 操作](syncfolderitems-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

