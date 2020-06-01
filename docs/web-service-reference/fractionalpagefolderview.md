---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: FractionalPageFolderView 元素说明分页视图的起始位置以及在 FindFolder 请求中返回的最大文件夹数。
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463067"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

**FractionalPageFolderView**元素说明分页视图的起始位置以及在[FindFolder](findfolder.md)请求中返回的最大文件夹数。 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |标识要在[FindFolder](findfolder.md)响应中返回的最大结果数。 此特性是可选的。  <br/> |
|**分子** <br/> |表示从结果集的开头的小数偏移量的分子。 此特性是必需的。 分子必须等于或小于分母。 此属性必须代表等于或大于零的整数值。 有关详细信息，请参阅本主题后面的 "备注"。  <br/> |
|**母** <br/> |表示从结果集内的文件夹总数开始的小数偏移量的分母。 此特性是必需的。 此属性必须代表大于1的整数值。 有关详细信息，请参阅本主题后面的 "备注"。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义用于标识邮箱中的文件夹的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>备注

从找到的文件夹集开始的分页视图偏移量按分数进行描述。 由**分子**和**分母**属性定义的小数描述了信息页面的起始位置。 例如，如果**分子**等于四，**分母**等于5，则返回的信息的页面从 fifths 中的一个条目开始，该条目位于结果集内。 
  
如果分式的计算结果为零，则指示结果集的开头。 如果该分数的计算结果为1，则指示结果集的结尾。
  
> [!NOTE]
> 分数表示页面的起始点，而不是返回结果集中的结果数。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder 操作](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

