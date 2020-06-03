---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: ManagedFolderInformation 元素包含有关托管自定义文件夹的信息。
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44450947"
---
# <a name="managedfolderinformation"></a>ManagedFolderInformation

**ManagedFolderInformation**元素包含有关托管自定义文件夹的信息。 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 **ManagedFolderInformationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |指示托管文件夹是否可由客户删除。  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |指示客户是否可以重命名或移动给定的托管文件夹。  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |指示是否必须显示托管文件夹注释。  <br/> |
|[HasQuota](hasquota.md) <br/> |指示托管文件夹是否具有配额。  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |指示托管文件夹是否为所有托管文件夹的根。  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |包含托管文件夹的文件夹 ID。  <br/> |
|[Comment](comment.md) <br/> |包含与托管文件夹相关联的注释。  <br/> |
|[StorageQuota](storagequota.md) <br/> |描述托管文件夹的存储配额。  <br/> |
|[FolderSize](foldersize.md) <br/> |描述托管文件夹中所有内容的总大小。  <br/> |
|[HomePage](homepage.md) <br/> |指定将作为托管文件夹的默认主页的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |表示 Exchange 存储中的文件夹。 托管自定义文件夹只能是名为 "**托管文件夹**" 的文件夹的子文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |不适用。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |不适用。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |不适用。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |不适用。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateManagedFolder 操作](createmanagedfolder-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

