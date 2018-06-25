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
description: IndexedPageFolderView 元素描述如何分页的项目信息 FindFolder 响应中返回。
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825910"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

**IndexedPageFolderView**元素描述如何分页的项目信息[FindFolder](findfolder.md)响应中返回。 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |介绍在响应中返回的文件夹的最大数目。 此属性是可选的。  <br/> |
|**Offset** <br/> |介绍从**基点**的偏移量。 偏移量必须大于或等于零。 如果**基点**等于开头，则偏移量为正数。 如果**基点**等于结束，则好像它是负数处理偏移量。  <br/> 这标识了哪个文件夹将传递的响应中的第一个文件夹。 此属性是必需的。  <br/> |
|**基点** <br/> |描述是否的文件夹页上将启动从开始或结束处的一组与搜索条件找到的文件夹。 始终从末尾查找往回搜索。 此属性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>基点属性

|**值**|**说明**|
|:-----|:-----|
|开始  <br/> |找到的文件夹集的开头开始分页的视图。  <br/> |
|End  <br/> |找到的文件夹集的末尾开始分页的视图。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义查找邮箱中的文件夹的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>注解

从最终查找涉及将移至原点标识的偏移量。 此外，将指针向后移动请求的记录数。 例如，如果有 100 条记录，偏移量为 25 从末尾，从 75 开始搜索。 如果返回了 10 条记录，10 个附加到 65 记录，并返回记录到 75 65 指针是向后移动。 下一个索引为 64。 从页面结尾的下一步偏移量为 100 减 64 其等于 36。 从结束后，若要获取的已编制索引的下一页的下一步偏移量值为 36。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

