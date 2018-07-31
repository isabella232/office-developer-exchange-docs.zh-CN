---
title: Update (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: 更新元素标识更新本地客户端存储中的单个项。
ms.openlocfilehash: bf560f18184151a3f17d7016d05cdb725db934ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353628"
---
# <a name="update-itemsync"></a>Update (ItemSync)

**更新**元素标识更新本地客户端存储中的单个项。 
  
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
|[Item](item.md) <br/> |代表要更新的泛型 Exchange 项目。  <br/> |
|[邮件](message-ex15websvcsotherref.md) <br/> |代表要更新 Exchange 电子邮件。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |代表要更新 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |代表要更新 Exchange 联系人项。  <br/> |
|[DistributionList](distributionlist.md) <br/> |代表要更新的通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |代表要更新的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示要更新的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |代表要更新的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |代表要更新会议取消。  <br/> |
|[任务](task.md) <br/> |代表要更新的任务。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |包含表示的客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SyncFolderItems 操作](syncfolderitems-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

