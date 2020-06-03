---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: FolderIds 元素包含一个由文件夹标识符组成的数组，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530991"
---
# <a name="folderids"></a>FolderIds

**FolderIds**元素包含一个由文件夹标识符组成的数组，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可通过名称引用的 Microsoft Exchange Server 文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |定义从 Exchange 存储中获取文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |定义从 Exchange 存储中删除文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |定义从 Exchange 存储中删除文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |定义在 Exchange 存储中移动文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |定义在 Exchange 存储中复制文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知订阅的订阅。  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于请求的事件通知订阅的订阅。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |邮件架构;类型架构  <br/> |
|验证文件  <br/> |消息 .xsd;类型 .xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFolder 操作](getfolder-operation.md)
  
[DeleteFolder 操作](deletefolder-operation.md)
  
[MoveFolder 操作](movefolder-operation.md)
  
[CopyFolder 操作](copyfolder-operation.md)
  
[订阅操作](subscribe-operation.md)

