---
title: 更新 (ItemSync)
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
ms.openlocfilehash: ef1bd46906152affbe54372472766afc2a6ae8c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838363"
---
# <a name="update-itemsync"></a>更新 (ItemSync)

**更新**元素标识更新本地客户端存储中的单个项。 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[更改 （项）](changes-items.md)
  
[更新 (ItemSync)](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

 **SyncFolderItemsCreateOrUpdateType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Item](item.md) <br/> |代表要更新的泛型 Exchange 项目。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |代表要更新 Exchange 电子邮件。  <br/> |
|[日历项目](calendaritem.md) <br/> |代表要更新 Exchange 日历项。  <br/> |
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
|[更改 （项）](changes-items.md) <br/> |包含表示的客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

