---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: ToFolderId 元素表示复制或移动的项目或文件夹的目标文件夹。
ms.openlocfilehash: b58192aa4d1ffe609da78dfdf1b5c86522fc45c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515164"
---
# <a name="tofolderid"></a>ToFolderId

**ToFolderId** 元素表示复制或移动的项目或文件夹的目标文件夹。 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含用于复制或移动的项或文件夹的目标文件夹的标识符。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识命名的目标文件夹复制或移动的项或文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |定义移动邮件存储中的文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |定义一个请求，请求将文件夹复制到Exchange存储区中。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |定义在项目存储中移动Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |定义在应用商店中复制Exchange的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [MoveFolder 操作](movefolder-operation.md)  
- [CopyFolder 操作](copyfolder-operation.md) 
- [MoveItem 操作](moveitem-operation.md) 
- [CopyItem 操作](copyitem-operation.md)

