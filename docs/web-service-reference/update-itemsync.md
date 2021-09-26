---
title: Update (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: Update 元素标识要在本地客户端存储中更新的单个项。
ms.openlocfilehash: 936226c671916b974eed9dea9ad2ea39bde482a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541817"
---
# <a name="update-itemsync"></a>Update (ItemSync)

**Update** 元素标识要在本地客户端存储中更新的单个项。 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)  
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)  
- [Changes (Items)](changes-items.md)  
- [Update (ItemSync)](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Item](item.md) <br/> |表示要更新Exchange常规项目。  <br/> |
|[消息](message-ex15websvcsotherref.md) <br/> |表示Exchange电子邮件的收件人。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示要Exchange的日历项目。  <br/> |
|[联系人](contact.md) <br/> |表示要Exchange联系人项目的详细信息。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示要更新的通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示要更新的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示要更新的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示要更新的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示要更新的会议取消。  <br/> |
|[任务](task.md) <br/> |表示要更新的任务。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |包含一个变更类型的序列数组，这些更改类型表示客户端上的项目与客户端服务器上项目Exchange的类型。  <br/> |
   
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

