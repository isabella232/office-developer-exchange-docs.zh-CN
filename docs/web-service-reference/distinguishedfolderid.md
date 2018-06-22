---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: DistinguishedFolderId 元素标识可以通过名称引用的文件夹。 如果您不使用此元素，您必须使用文件夹 Id 元素来识别文件夹。
ms.openlocfilehash: 834166be3d882fa8c0533cfcc2999600430b82ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753960"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

**DistinguishedFolderId**元素标识可以通过名称引用的文件夹。 如果您不使用此元素，您必须使用[文件夹 Id](folderid.md)元素来识别文件夹。 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |包含一个字符串，标识默认文件夹。 此属性是必需的。  <br/> |
|**更改密钥** <br/> |包含一个字符串，标识的文件夹的**Id**属性标识的版本。 此属性是可选的。 使用此属性以确保正确版本的文件夹使用。  <br/> |
   
#### <a name="id-attribute-values"></a>Id 属性值

|**值**|**说明**|
|:-----|:-----|
|日历  <br/> |代表日历文件夹。  <br/> |
|contacts  <br/> |代表联系人文件夹。  <br/> |
|DeletedItems  <br/> |代表已删除邮件文件夹。  <br/> |
|草稿  <br/> |代表草稿文件夹。  <br/> |
|收件箱  <br/> |代表收件箱文件夹。  <br/> |
|日记  <br/> |代表日记文件夹。  <br/> |
|notes  <br/> |代表便笺文件夹。  <br/> |
|发件箱  <br/> |代表发件箱文件夹。  <br/> |
|sentitems  <br/> |代表已发送邮件文件夹。  <br/> |
|tasks  <br/> |代表任务文件夹。  <br/> |
|msgfolderroot  <br/> |代表邮件文件夹根目录。  <br/> |
|root  <br/> |表示邮箱的根。  <br/> |
|junkemail  <br/> |代表垃圾邮件文件夹。  <br/> |
|searchfolders  <br/> |代表搜索文件夹文件夹。  <br/> |
|语音邮件  <br/> |代表语音邮件文件夹。  <br/> |
|recoverableitemsroot  <br/> |代表转储程序根文件夹。  <br/> |
|recoverableitemsdeletions  <br/> |代表转储程序删除文件夹。  <br/> |
|recoverableitemsversions  <br/> |代表转储程序版本文件夹。  <br/> |
|recoverableitemspurges  <br/> |代表转储程序清除文件夹。  <br/> |
|archiveroot  <br/> |代表根存档文件夹。  <br/> |
|archivemsgfolderroot  <br/> |代表根存档邮件文件夹。  <br/> |
|archivedeleteditems  <br/> |代表存档已删除邮件文件夹。  <br/> |
|archiveinbox  <br/> |代表存档收件箱文件夹。 内部版本号 15.00.0913.09 开头的 Exchange 版本包括此值。  <br/> |
|archiverecoverableitemsroot  <br/> |代表存档可恢复的项目根文件夹。  <br/> |
|archiverecoverableitemsdeletions  <br/> |代表存档可恢复的项目删除文件夹。  <br/> |
|archiverecoverableitemsversions  <br/> |代表存档可恢复的项目版本文件夹。  <br/> |
|archiverecoverableitemspurges  <br/> |代表存档可恢复的项目清除文件夹。  <br/> |
|syncissues  <br/> |代表同步问题文件夹。  <br/> |
|冲突  <br/> |代表冲突文件夹。  <br/> |
|localfailures  <br/> |代表本地故障文件夹。  <br/> |
|serverfailures  <br/> |代表服务器故障文件夹。  <br/> |
|recipientcache  <br/> |代表收件人缓存文件夹。  <br/> |
|quickcontacts  <br/> |代表快速联系人文件夹。  <br/> |
|conversationhistory  <br/> |代表对话历史记录文件夹。  <br/> |
|adminauditlogs  <br/> |代表管理员审核日志文件夹。  <br/> |
|todosearch  <br/> |代表 todo 搜索文件夹。  <br/> |
|mycontacts  <br/> |代表我的联系人文件夹。  <br/> |
|目录  <br/> |表示目录文件夹。  <br/> |
|imcontactlist  <br/> |代表 IM 联系人列表文件夹。  <br/> |
|peopleconnect  <br/> |代表人员连接文件夹。  <br/> |
|收藏夹  <br/> |代表收藏夹文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识的主 SMTP 地址。 不允许使用代理地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示对话操作使用文件夹的目标文件夹。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示副本的目标文件夹，并移动对话操作。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | 标识在其中创建新的文件夹或项目的文件夹。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识要[FindItem 操作](finditem-operation.md)和[FindFolder 操作](findfolder-operation.md)搜索文件夹。  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |代表将搜索以确定搜索文件夹的内容的文件夹的集合。  <br/> |
|[FolderIds](folderids.md) <br/> |包含用于标识要复制、 移动、 获取、 删除或监视事件通知的文件夹的文件夹标识符的数组。  <br/> |
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> <br/>以下是此元素的 XPath 表达式：<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | 表示复制或移动项目或文件夹的目标文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | 标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |代表包含要同步的项的文件夹。  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |代表用户配置对象的名称。 用户配置对象名称为用户配置对象的标识符。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |表示的文件夹的 ID 项将被复制到该电子邮件。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |表示的文件夹的 ID 将项目移至的电子邮件。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

**DistinguishedFolderId**解析为**文件夹 Id**。 
  
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
- [Creating Folders (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

