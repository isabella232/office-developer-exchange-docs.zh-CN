---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: DistinguishedFolderId 元素标识可以通过名称引用的文件夹。
ms.openlocfilehash: 1f5b97fc7ee7b93989762c26e4b979a8dfb884be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753958"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

**DistinguishedFolderId**元素标识可以通过名称引用的文件夹。 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |指定一般文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |指定日历文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |指定联系人文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

**DistinguishedFolderId 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|日历  <br/> |指示日历文件夹的 URL。  <br/> |
|contacts  <br/> |指示联系人文件夹的 URL。  <br/> |
|DeletedItems  <br/> |指示已删除的邮件文件夹的 URL。  <br/> |
|草稿  <br/> |指示草稿文件夹的 URL。  <br/> |
|收件箱  <br/> |指示收件箱文件夹的 URL。  <br/> |
|日记  <br/> |指示日记文件夹的 URL。  <br/> |
|notes  <br/> |指示便笺文件夹的 URL。  <br/> |
|发件箱  <br/> |指示发件箱文件夹的 URL。  <br/> |
|sentitems  <br/> |指示已发送的邮件文件夹的 URL。  <br/> |
|tasks  <br/> |指示任务文件夹的 URL。  <br/> |
|msgfolderroot  <br/> |指示邮件根文件夹的 URL。  <br/> |
|publicfoldersroot  <br/> |指示公用文件夹根文件夹的 URL。  <br/> |
|root  <br/> |指示的根文件夹的 URL。  <br/> |
|junkemail  <br/> |指示垃圾邮件文件夹的 URL。  <br/> |
|searchfolders  <br/> |指示搜索文件夹的 URL。  <br/> |
|语音邮件  <br/> |指示语音邮件文件夹的 URL。  <br/> |
|recoverableitemsroot  <br/> |指示可恢复邮件根文件夹的 URL。  <br/> |
|recoverableitemsdeletions  <br/> |指示已删除的可恢复邮件文件夹的 URL。  <br/> |
|recoverableitemsversions  <br/> |指示可恢复项目版本文件夹的 URL。  <br/> |
|recoverableitemspurges  <br/> |指示清除可恢复邮件文件夹的 URL。  <br/> |
|archiveroot  <br/> |指示存档根文件夹的 URL。  <br/> |
|archivemsgfolderroot  <br/> |指示已存档的邮件文件夹根文件夹的 URL。  <br/> |
|archivedeleteditems  <br/> |指示已存档的已删除的邮件文件夹的 URL。  <br/> |
|archiverecoverableitemsroot  <br/> |指示已存档的可恢复项目根文件夹的 URL。  <br/> |
|archiverecoverableitemsdeletions  <br/> |指示存档可恢复已删除的邮件文件夹的 URL。  <br/> |
|archiverecoverableitemsversions  <br/> |指示已存档的可恢复项目版本文件夹的 URL。  <br/> |
|archiverecoverableitemspurges  <br/> |指示存档清除可恢复邮件文件夹的 URL。  <br/> |
|syncissues  <br/> |指示同步问题文件夹的 URL。  <br/> |
|冲突  <br/> |指示冲突文件夹的 URL。  <br/> |
|localfailures  <br/> |指示本地故障文件夹的 URL。  <br/> |
|serverfailures  <br/> |指示服务器故障文件夹的 URL。  <br/> |
|recipientcache  <br/> |指示收件人缓存文件夹的 URL。  <br/> |
|quickcontacts  <br/> |指示快速联系人文件夹的 URL。  <br/> |
|conversationhistory  <br/> |指示对话历史记录文件夹的 URL。  <br/> |
|adminauditlogs  <br/> |指示管理审核日志的文件夹的 URL。  <br/> |
|todosearch  <br/> |指示搜索待办事项文件夹的 URL。  <br/> |
|mycontacts  <br/> |指示的 URL 联系人文件夹。  <br/> |
|目录  <br/> |指示目录文件夹的 URL。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

