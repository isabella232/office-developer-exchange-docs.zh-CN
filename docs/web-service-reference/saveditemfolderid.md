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
description: SavedItemFolderId 元素标识在邮箱中更新、发送和创建项目的操作的目标文件夹。
ms.openlocfilehash: 8e18b8863a54aa4e9d6e65f7a54e20904f5a9599
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465273"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

**SavedItemFolderId**元素标识在邮箱中更新、发送和创建项目的操作的目标文件夹。 
  
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
|[FolderId](folderid.md) <br/> |包含更新、发送和创建 Exchange 存储中的项的操作的目标文件夹的标识符和更改键。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |通过在 Exchange 存储中更新、发送和创建项目的操作的命名标识符标识目标文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |定义在 Exchange 存储中创建项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |定义对 Exchange 存储中的项目的更新请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |定义在 Exchange 存储中发送项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

