---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: IndexedPageFolderView 元素介绍如何在 FindFolder 响应中返回分页项目信息。
ms.openlocfilehash: 0a5d0f7e63549b7a851862d957ff32dff4333ce3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542237"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

**IndexedPageFolderView** 元素描述如何在 [FindFolder](findfolder.md)响应中返回分页项目信息。 
  
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
|**MaxEntriesReturned** <br/> |描述响应中要返回的最大文件夹数。 此特性是可选的。  <br/> |
|**Offset** <br/> |描述与 **BasePoint 的偏移** 量。 Offset 必须大于或等于零。 如果 **BasePoint** 等于 Beginning，则偏移量为正。 如果 **BasePoint** 等于 End，则处理偏移量就像负值一样。  <br/> 这将标识哪个文件夹将是响应中传递的第一个文件夹。 此特性是必需的。  <br/> |
|**BasePoint** <br/> |描述文件夹页面是从使用搜索条件找到的文件夹集的开始还是结尾开始。 从末尾查找始终向后搜索。 此特性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint 属性

|**值**|**说明**|
|:-----|:-----|
|开始  <br/> |分页视图从找到的文件夹集的开头开始。  <br/> |
|End  <br/> |分页视图从找到的文件夹集的末尾开始。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义查找邮箱中的文件夹的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>注解

从一端寻找涉及移动到由偏移标识的原点。 此外，指针将移回所请求的记录数。 例如，如果有 100 条记录，并且从结尾偏移 25，则搜索从 75 开始。 如果返回 10 条记录，则指针向后移动 10 条记录到 65，并返回记录 65 到 75。 下一个索引为 64。 页面末尾的下一个偏移量是 100 减 64，等于 36。 从结尾到获取下一个索引页的下一个偏移的值为 36。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

