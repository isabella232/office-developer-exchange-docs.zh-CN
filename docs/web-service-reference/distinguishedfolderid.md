---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: DistinguishedFolderId 元素标识可通过名称引用的文件夹。 如果不使用此元素，则必须使用 FolderId 元素标识文件夹。
ms.openlocfilehash: 309db925bb783c435320aeb283915ece39da2271
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521992"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

**DistinguishedFolderId** 元素标识可通过名称引用的文件夹。 如果不使用此元素，则必须使用 [FolderId](folderid.md) 元素标识文件夹。 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |包含标识默认文件夹的字符串。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |包含一个标识由 **Id** 属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性确保使用正确版本的文件夹。  <br/> |
   
#### <a name="id-attribute-values"></a>Id 属性值

|**值**|**说明**|
|:-----|:-----|
|日历  <br/> |代表"日历"文件夹。  <br/> |
|contacts  <br/> |代表"联系人"文件夹。  <br/> |
|deleteditems  <br/> |代表"已删除邮件"文件夹。  <br/> |
|drafts  <br/> |代表"草稿"文件夹。  <br/> |
|inbox  <br/> |代表"收件箱"文件夹。  <br/> |
|journal  <br/> |代表"日记"文件夹。  <br/> |
|notes  <br/> |代表"便笺"文件夹。  <br/> |
|outbox  <br/> |代表发件箱文件夹。  <br/> |
|sentitems  <br/> |代表"已发送的项目"文件夹。  <br/> |
|tasks  <br/> |代表"任务"文件夹。  <br/> |
|msgfolderroot  <br/> |表示邮件文件夹根目录。  <br/> |
|root  <br/> |表示邮箱的根。  <br/> |
|junkemail  <br/> |代表"垃圾邮件"文件夹。  <br/> |
|searchfolders  <br/> |代表"搜索文件夹"文件夹。  <br/> |
|语音邮件  <br/> |代表"语音邮件"文件夹。  <br/> |
|recoverableitemsroot  <br/> |表示垃圾站根文件夹。  <br/> |
|recoverableitemsdeletions  <br/> |代表垃圾站删除文件夹。  <br/> |
|recoverableitemsversions  <br/> |代表垃圾站版本文件夹。  <br/> |
|recoverableitemspurges  <br/> |代表垃圾站清除文件夹。  <br/> |
|archiveroot  <br/> |代表根存档文件夹。  <br/> |
|archivemsgfolderroot  <br/> |代表根存档邮件文件夹。  <br/> |
|archivedeleteditems  <br/> |代表存档已删除邮件文件夹。  <br/> |
|archiveinbox  <br/> |代表存档的"收件箱"文件夹。 从内部Exchange号 15.00.0913.09 开始的版本包含此值。  <br/> |
|archiverecoverableitemsroot  <br/> |表示存档的可恢复项目根文件夹。  <br/> |
|archiverecoverableitemsdeletions  <br/> |代表"存档可恢复的项目删除"文件夹。  <br/> |
|archiverecoverableitemsversions  <br/> |代表"存档可恢复的项目版本"文件夹。  <br/> |
|archiverecoverableitemspurges  <br/> |代表"存档可恢复的项目清除"文件夹。  <br/> |
|syncissues  <br/> |代表"同步问题"文件夹。  <br/> |
|conflicts  <br/> |代表"冲突"文件夹。  <br/> |
|localfailures  <br/> |代表本地故障文件夹。  <br/> |
|serverfailures  <br/> |代表"服务器故障"文件夹。  <br/> |
|recipientcache  <br/> |代表收件人缓存文件夹。  <br/> |
|quickcontacts  <br/> |代表快速联系人文件夹。  <br/> |
|conversationhistory  <br/> |代表对话历史记录文件夹。  <br/> |
|adminauditlogs  <br/> |代表管理员审核日志文件夹。  <br/> |
|todosearch  <br/> |表示 todo 搜索文件夹。  <br/> |
|mycontacts  <br/> |代表"我的联系人"文件夹。  <br/> |
|directory  <br/> |表示目录文件夹。  <br/> |
|imcontactlist  <br/> |代表 IM 联系人列表文件夹。  <br/> |
|peopleconnect  <br/> |代表人员连接文件夹。  <br/> |
|收藏夹  <br/> |代表"收藏夹"文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识主 SMTP 地址。 不允许使用代理地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的对话操作的文件夹。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示复制和移动对话操作的目标文件夹。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | 标识创建一个新文件夹或项目的文件夹。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识要搜索 [FindItem 操作和](finditem-operation.md) [FindFolder](findfolder-operation.md)操作的文件夹。  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |表示将搜索以确定搜索文件夹内容的文件夹的集合。  <br/> |
|[FolderIds](folderids.md) <br/> |包含一组文件夹标识符，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。  <br/> |
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> <br/>下面是此元素的 XPath 表达式:  <br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | 表示复制或移动的项目或文件夹的目标文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | 标识用于更新、发送和创建邮件存储中项目的操作Exchange文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |表示包含要同步的项目的文件夹。  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |表示用户配置对象的名称。 用户配置对象名称是用户配置对象的标识符。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |表示电子邮件项目将复制到的文件夹的 ID。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |表示电子邮件项目将移动到的文件夹的 ID。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

**DistinguishedFolderId** 解析为 **FolderId**。 
  
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
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

