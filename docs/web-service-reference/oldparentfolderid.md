---
title: OldParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OldParentFolderId
api_type:
- schema
ms.assetid: da1b8c88-c650-455d-b749-0cd160b012d8
description: OldParentFolderId 元素包含已复制或移动的项目或文件夹的父文件夹的标识符。
ms.openlocfilehash: 9cf7eb834c0c7b70f234df26b466977e8e11957a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537455"
---
# <a name="oldparentfolderid"></a>OldParentFolderId

**OldParentFolderId** 元素包含已复制或移动的项目或文件夹的父文件夹的标识符。 
  
```xml
<OldParentFolderId Id="" ChangeKey=""/>
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |包含一个字符串，用于标识Exchange文件夹。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |包含一个标识由 Id 属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性确保使用正确版本的文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |表示复制项目或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示一个事件，其中项目或文件夹从一个父文件夹移动到另一个父文件夹。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

