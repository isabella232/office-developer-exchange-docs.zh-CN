---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: FolderIds 元素包含一组文件夹标识符，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。
ms.openlocfilehash: 7c0cf46d5fdaf35ec72cf3b5750b51edc5a8bfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518363"
---
# <a name="folderids"></a>FolderIds

**FolderIds** 元素包含一组文件夹标识符，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。 
  
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
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识Microsoft Exchange Server名称引用的文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |定义从应用商店获取文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |定义从邮件存储中删除文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |定义从邮件存储中删除文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |定义移动邮件存储中的文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |定义一个请求，请求将文件夹复制到Exchange存储中。  <br/> 下面是此元素的 XPath 表达式:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知订阅的订阅。  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于拉取的事件通知订阅的订阅。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |邮件架构;类型架构  <br/> |
|验证文件  <br/> |Messages.xsd;Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFolder 操作](getfolder-operation.md)
  
[DeleteFolder 操作](deletefolder-operation.md)
  
[MoveFolder 操作](movefolder-operation.md)
  
[CopyFolder 操作](copyfolder-operation.md)
  
[订阅操作](subscribe-operation.md)

