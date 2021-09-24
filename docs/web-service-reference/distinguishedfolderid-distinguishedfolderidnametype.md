---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: DistinguishedFolderId 元素标识可通过名称引用的文件夹。
ms.openlocfilehash: 23d1dead5a97fe8b2ceb29235f4b784f667d2ee1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526438"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

**DistinguishedFolderId** 元素标识可通过名称引用的文件夹。 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |指定泛型文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |指定日历文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |指定联系人文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

**DistinguishedFolderId 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|日历  <br/> |指示日历文件夹的 URL。  <br/> |
|contacts  <br/> |指示联系人文件夹的 URL。  <br/> |
|deleteditems  <br/> |指示已删除项目文件夹的 URL。  <br/> |
|drafts  <br/> |指示草稿文件夹的 URL。  <br/> |
|inbox  <br/> |指示收件箱文件夹的 URL。  <br/> |
|journal  <br/> |指示日记文件夹的 URL。  <br/> |
|notes  <br/> |指示便笺文件夹的 URL。  <br/> |
|outbox  <br/> |指示发件箱文件夹的 URL。  <br/> |
|sentitems  <br/> |指示已发送项目文件夹的 URL。  <br/> |
|tasks  <br/> |指示任务文件夹的 URL。  <br/> |
|msgfolderroot  <br/> |指示邮件根文件夹的 URL。  <br/> |
|publicfoldersroot  <br/> |指示公用文件夹根文件夹的 URL。  <br/> |
|root  <br/> |指示根文件夹的 URL。  <br/> |
|junkemail  <br/> |指示垃圾邮件文件夹的 URL。  <br/> |
|searchfolders  <br/> |指示搜索文件夹的 URL。  <br/> |
|语音邮件  <br/> |指示语音邮件文件夹的 URL。  <br/> |
|recoverableitemsroot  <br/> |指示可恢复项目根文件夹的 URL。  <br/> |
|recoverableitemsdeletions  <br/> |指示已删除的可恢复邮件文件夹的 URL。  <br/> |
|recoverableitemsversions  <br/> |指示可恢复项目版本文件夹的 URL。  <br/> |
|recoverableitemspurges  <br/> |指示已清除的可恢复邮件文件夹的 URL。  <br/> |
|archiveroot  <br/> |指示存档根文件夹的 URL。  <br/> |
|archivemsgfolderroot  <br/> |指示存档的邮件文件夹根文件夹的 URL。  <br/> |
|archivedeleteditems  <br/> |指示存档的已删除邮件文件夹的 URL。  <br/> |
|archiverecoverableitemsroot  <br/> |指示存档的可恢复项目根文件夹的 URL。  <br/> |
|archiverecoverableitemsdeletions  <br/> |指示存档的可恢复已删除邮件文件夹的 URL。  <br/> |
|archiverecoverableitemsversions  <br/> |指示存档的可恢复项目版本文件夹的 URL。  <br/> |
|archiverecoverableitemspurges  <br/> |指示存档的已清除可恢复邮件文件夹的 URL。  <br/> |
|syncissues  <br/> |指示同步问题文件夹的 URL。  <br/> |
|conflicts  <br/> |指示冲突文件夹的 URL。  <br/> |
|localfailures  <br/> |指示本地故障文件夹的 URL。  <br/> |
|serverfailures  <br/> |指示服务器故障文件夹的 URL。  <br/> |
|recipientcache  <br/> |指示收件人缓存文件夹的 URL。  <br/> |
|quickcontacts  <br/> |指示快速联系人文件夹的 URL。  <br/> |
|conversationhistory  <br/> |指示对话历史记录文件夹的 URL。  <br/> |
|adminauditlogs  <br/> |指示管理文件夹审核日志 URL。  <br/> |
|todosearch  <br/> |指示搜索目标文件夹的 URL。  <br/> |
|mycontacts  <br/> |指示我的联系人文件夹的 URL。  <br/> |
|directory  <br/> |指示目录文件夹的 URL。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

