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
description: FolderIds 元素包含用于标识要复制、 移动、 获取、 删除或监视事件通知的文件夹的文件夹标识符的数组。
ms.openlocfilehash: 911a74ca778ee988c270c16c67620a40656d82d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754391"
---
# <a name="folderids"></a>FolderIds

**FolderIds**元素包含用于标识要复制、 移动、 获取、 删除或监视事件通知的文件夹的文件夹标识符的数组。 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[文件夹 Id](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可以通过名称引用的 Microsoft Exchange Server 文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |定义从 Exchange 存储中获取文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |定义从 Exchange 存储中删除文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |定义从 Exchange 存储中删除文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |定义将文件夹移 Exchange 存储中的请求。  <br/> 下面是此元素的 XPath 表达式:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |定义在 Exchange 存储中复制文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |代表对基于推送的事件通知订阅的订阅。  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |代表对基于请求的事件通知订阅的订阅。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages 和 http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |邮件架构;类型架构  <br/> |
|验证文件  <br/> |Messages.xsd;Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFolder Operation](getfolder-operation.md)
  
[DeleteFolder 操作](deletefolder-operation.md)
  
[MoveFolder 操作](movefolder-operation.md)
  
[CopyFolder 操作](copyfolder-operation.md)
  
[订阅操作](subscribe-operation.md)

