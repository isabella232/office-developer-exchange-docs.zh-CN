---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: SavedItemFolderId 元素标识用于更新、 发送和邮箱中创建项目的操作的目标文件夹。
ms.openlocfilehash: c57a7fb4abc2f7ee7b599f56f016811d6ff2c21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827277"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

**SavedItemFolderId**元素标识用于更新、 发送和邮箱中创建项目的操作的目标文件夹。 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[文件夹 Id](folderid.md) <br/> |包含标识符和更改密钥的目标文件夹的更新、 发送和在 Exchange 存储中创建项目操作。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |通过更新、 发送和在 Exchange 存储中创建项目的操作的命名标识符标识目标文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |定义在 Exchange 存储中创建项的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |定义更新 Exchange 存储中的项的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |定义发送 Exchange 存储中的项目的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

