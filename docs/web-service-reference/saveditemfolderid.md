---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: SavedItemFolderId 元素标识用于更新、发送和创建邮箱中的项目的操作的目标文件夹。
ms.openlocfilehash: 75245cf842336621aa098c115d62a7802711dd54
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546117"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

**SavedItemFolderId** 元素标识用于更新、发送和创建邮箱中的项目的操作的目标文件夹。 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含目标文件夹的标识符和更改键，用于更新、发送和创建邮件存储中的Exchange项。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |通过命名标识符标识目标文件夹，用于更新、发送和创建邮件存储中的Exchange项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |定义在项目存储中创建Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |定义更新项目存储中的Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |定义一个请求，以发送项目Exchange存储区。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

