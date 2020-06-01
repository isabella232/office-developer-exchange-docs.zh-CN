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
description: DistinguishedFolderId 元素标识可通过名称引用的文件夹。 如果不使用此元素，则必须使用 FolderId 元素来标识文件夹。
ms.openlocfilehash: be883cbca00910b24e4c45ba047803e5a5024566
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462694"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

**DistinguishedFolderId**元素标识可通过名称引用的文件夹。 如果不使用此元素，则必须使用[FolderId](folderid.md)元素来标识文件夹。 
  
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
|**ChangeKey** <br/> |包含标识由**Id**属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性可确保使用的是正确的文件夹版本。  <br/> |
   
#### <a name="id-attribute-values"></a>Id 属性值

|**值**|**说明**|
|:-----|:-----|
|日历  <br/> |代表 "日历" 文件夹。  <br/> |
|contacts  <br/> |代表 "联系人" 文件夹。  <br/> |
|deleteditems  <br/> |代表 "已删除邮件" 文件夹。  <br/> |
|drafts  <br/> |代表 "草稿" 文件夹。  <br/> |
|inbox  <br/> |代表 "收件箱" 文件夹。  <br/> |
|日志  <br/> |代表 "日记" 文件夹。  <br/> |
|注释  <br/> |代表 "便笺" 文件夹。  <br/> |
|outbox  <br/> |代表 "发件箱" 文件夹。  <br/> |
|sentitems  <br/> |代表 "已发送邮件" 文件夹。  <br/> |
|tasks  <br/> |代表 "任务" 文件夹。  <br/> |
|msgfolderroot  <br/> |表示邮件文件夹根目录。  <br/> |
|root  <br/> |表示邮箱的根。  <br/> |
|junkemail  <br/> |代表 "垃圾邮件" 文件夹。  <br/> |
|searchfolders  <br/> |代表 "搜索文件夹" 文件夹。  <br/> |
|语音邮件  <br/> |代表 "语音邮件" 文件夹。  <br/> |
|recoverableitemsroot  <br/> |表示转储程序根文件夹。  <br/> |
|recoverableitemsdeletions  <br/> |代表 "转储程序删除" 文件夹。  <br/> |
|recoverableitemsversions  <br/> |代表 "转储程序版本" 文件夹。  <br/> |
|recoverableitemspurges  <br/> |表示 "转储程序清除" 文件夹。  <br/> |
|archiveroot  <br/> |表示根存档文件夹。  <br/> |
|archivemsgfolderroot  <br/> |代表 "根存档邮件" 文件夹。  <br/> |
|archivedeleteditems  <br/> |代表 "存档已删除邮件" 文件夹。  <br/> |
|archiveinbox  <br/> |代表 "存档收件箱" 文件夹。 从内部版本号开始的 Exchange 版本15.00.0913.09 包含此值。  <br/> |
|archiverecoverableitemsroot  <br/> |代表 "存档可恢复项目" 根文件夹。  <br/> |
|archiverecoverableitemsdeletions  <br/> |代表 "存档可恢复项目删除" 文件夹。  <br/> |
|archiverecoverableitemsversions  <br/> |代表 "存档可恢复项目版本" 文件夹。  <br/> |
|archiverecoverableitemspurges  <br/> |代表 "存档可恢复项目清除" 文件夹。  <br/> |
|syncissues  <br/> |代表 "同步问题" 文件夹。  <br/> |
|conflicts  <br/> |代表 "冲突" 文件夹。  <br/> |
|localfailures  <br/> |代表 "本地故障" 文件夹。  <br/> |
|serverfailures  <br/> |代表 "服务器故障" 文件夹。  <br/> |
|recipientcache  <br/> |代表 "收件人缓存" 文件夹。  <br/> |
|quickcontacts  <br/> |代表 "快速联系人" 文件夹。  <br/> |
|conversationhistory  <br/> |代表 "对话历史记录" 文件夹。  <br/> |
|adminauditlogs  <br/> |代表 "管理员审核日志" 文件夹。  <br/> |
|todosearch  <br/> |表示 todo 搜索文件夹。  <br/> |
|mycontacts  <br/> |代表 "我的联系人" 文件夹。  <br/> |
|文件夹  <br/> |表示目录文件夹。  <br/> |
|imcontactlist  <br/> |表示 IM 联系人列表文件夹。  <br/> |
|peopleconnect  <br/> |代表 "人员连接" 文件夹。  <br/> |
|精品  <br/> |代表 "收藏夹" 文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识主 SMTP 地址。 不允许使用代理地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的对话操作的文件夹。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示用于复制和移动对话操作的目标文件夹。  <br/> |
|[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md) <br/> | 标识在其中创建新文件夹或项目的文件夹。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识用于搜索[FindItem 操作](finditem-operation.md)和[FindFolder 操作](findfolder-operation.md)的文件夹。  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |代表将搜索的文件夹的集合，以确定搜索文件夹的内容。  <br/> |
|[FolderIds](folderids.md) <br/> |包含用于标识要复制、移动、获取、删除或监视事件通知的文件夹的文件夹标识符的数组。  <br/> |
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> <br/>下面是此元素的 XPath 表达式:  <br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | 代表复制或移动的项或文件夹的目标文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | 标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |表示包含要同步的项目的文件夹。  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |表示用户配置对象的名称。 "用户配置" 对象名称是 "用户配置" 对象的标识符。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |代表将电子邮件项目复制到的文件夹的 ID。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |表示电子邮件项目将移动到的文件夹的 ID。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

**DistinguishedFolderId**解析为**FolderId**。 
  
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

