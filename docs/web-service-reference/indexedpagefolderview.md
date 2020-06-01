---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: IndexedPageFolderView 元素介绍如何在 FindFolder 响应中返回分页项目信息。
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457198"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

**IndexedPageFolderView**元素介绍如何在[FindFolder](findfolder.md)响应中返回分页项目信息。 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |描述要在响应中返回的最大文件夹数。 此特性是可选的。  <br/> |
|**Offset** <br/> |描述**BasePoint**中的偏移量。 偏移量必须大于或等于零。 如果**BasePoint**等于开头，则偏移量为正值。 如果**BasePoint**等于 End，则处理的是负的偏移量。  <br/> 这将标识哪个文件夹将是在响应中传递的第一个文件夹。 此特性是必需的。  <br/> |
|**BasePoint** <br/> |描述文件夹页面是否将从使用搜索条件找到的文件夹集的开头或结尾开始。 从末尾进行的查找始终向后搜索。 此特性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint 属性

|**值**|**说明**|
|:-----|:-----|
|始  <br/> |分页视图从找到的文件夹集的开头开始。  <br/> |
|End  <br/> |分页视图从找到的文件夹集的末尾开始。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义在邮箱中查找文件夹的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>备注

从 end 中查找包括移到由偏移量标识的源。 此外，还会按请求的记录数向后移动指针。 例如，如果有100条记录，偏移量是从末尾到25，则搜索从75开始。 如果返回10个记录，指针将向后移动10条记录到65，并返回记录65至75。 下一个索引为64。 距页面末尾的下一个偏移量是100减去64，等于36。 用于获取下一个索引页的终点的下一个偏移值为36。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

