---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: EffectiveRights 元素包含基于的项目或文件夹的权限设置的客户端的权限。 此元素是只读的。
ms.openlocfilehash: 610d9e214a8de648ece667799bb5e67dfcc358f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754030"
---
# <a name="effectiverights"></a>EffectiveRights

**EffectiveRights**元素包含基于的项目或文件夹的权限设置的客户端的权限。 此元素是只读的。 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 **EffectiveRightsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |指示客户端是否可以创建关联的内容表。 此属性仅可用于文件夹对象。  <br/> |
|[CreateContents](createcontents.md) <br/> |指示客户端是否可以创建内容表。 此属性仅可用于文件夹对象。  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |指示客户端是否可以创建层次结构表。 此属性仅可用于文件夹对象。  <br/> |
|[删除](delete.md) <br/> |指示客户端是否可以删除文件夹或项目。  <br/> |
|[修改](modify.md) <br/> |指示客户端是否可以修改文件夹或项目。  <br/> |
|[Read](read.md) <br/> |指示客户端是否可以读取文件夹或项目。  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |指示是否可以查看的私有项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示邮箱中的日历文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[Item](item.md) <br/> |表示的泛型 Exchange 项目。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[PostItem](postitem.md) <br/> |代表一个 Exchange 存储中的公告项目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

GetFolder、 GetItem、 FindFolder、 FindItem、 SyncFolderHierarchy 和 SyncFolderItems 响应中支持**EffectiveRights** 。 文件夹和项目的**AllProperties**形状中的公开**EffectiveRights**属性。 
  
此**EffectiveRights**属性提供对相同**PR_ACCESS MAPI**属性中提供的信息的访问。 
  
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
- [Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

