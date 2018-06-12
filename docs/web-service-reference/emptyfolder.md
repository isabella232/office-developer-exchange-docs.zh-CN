---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: EmptyFolder元素定义为空对 Exchange 存储中的邮箱中的文件夹的请求。(可选) 还可以文件夹被清空时删除子文件夹。
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754095"
---
# <a name="emptyfolder"></a>EmptyFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **EmptyFolder**元素定义为空对 Exchange 存储中的邮箱中的文件夹的请求。(可选) 还可以文件夹被清空时删除子文件夹。 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 **EmptyFolderType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**DeleteType** <br/> |指定如何清空文件夹。此属性是必需的。  <br/> |
|**DeleteSubFolders** <br/> |指定是否要删除子文件夹。此属性是必需的。  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType 属性

|**值**|**说明**|
|:-----|:-----|
|HardDelete  <br/> |一个存储区中永久删除邮件和文件夹。  <br/> |
|SoftDelete  <br/> |一个邮件和文件夹移动到垃圾站如果转储程序已启用。  <br/> |
|MoveToDeletedItems  <br/> |一个邮件和文件夹移到已删除邮件文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含用于标识要删除的文件夹的文件夹标识符的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[EmptyFolder 操作](emptyfolder-operation.md)

