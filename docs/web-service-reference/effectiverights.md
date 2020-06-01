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
description: EffectiveRights 元素包含客户端根据项目或文件夹的权限设置的权限。 此元素是只读的。
ms.openlocfilehash: 3055eb73056750508b48ead29136b56e7ce97ee9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459242"
---
# <a name="effectiverights"></a>EffectiveRights

**EffectiveRights**元素包含客户端根据项目或文件夹的权限设置的权限。 此元素是只读的。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |指示客户端是否可以创建关联的内容表。 此属性仅用于 folder 对象。  <br/> |
|[CreateContents](createcontents.md) <br/> |指示客户端是否可以创建内容表。 此属性仅用于 folder 对象。  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |指示客户端是否可以创建层次结构表。 此属性仅用于 folder 对象。  <br/> |
|[删除](delete.md) <br/> |指示客户端是否可以删除文件夹或项目。  <br/> |
|[Modify](modify.md) <br/> |指示客户端是否可以修改文件夹或项目。  <br/> |
|[Read](read.md) <br/> |指示客户端是否可以读取文件夹或项目。  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |指示是否可以查看私有项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的 "联系人" 文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |代表邮箱中的 "日历" 文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[项](item.md) <br/> |表示通用 Exchange 项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[PostItem](postitem.md) <br/> |表示 Exchange 存储中的公告项。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

**EffectiveRights**在 GetFolder、GetItem、FindFolder、FindItem、SyncFolderHierarchy 和 SyncFolderItems 响应中受支持。 **EffectiveRights**属性在文件夹和项目的**AllProperties**形状中公开。 
  
此**EffectiveRights**属性提供对**PR_ACCESS MAPI**属性中提供的相同信息的访问权限。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

