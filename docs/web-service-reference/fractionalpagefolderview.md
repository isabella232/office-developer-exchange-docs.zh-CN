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
description: FractionalPageFolderView 元素描述其中分页的视图启动并返回 FindFolder 请求中的文件夹的最大数目。
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754415"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

**FractionalPageFolderView**元素描述其中分页的视图启动并返回[FindFolder](findfolder.md)请求中的文件夹的最大数目。 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |标识要[FindFolder](findfolder.md)响应中返回结果的最大数量。 此属性是可选的。  <br/> |
|**分子** <br/> |从结果集中的开始表示分数偏移量的分子。 此属性是必需的。 分子必须等于或小于分母。 此属性必须表示等于或大于零的整数值。 有关详细信息，请参阅本主题后面的备注。  <br/> |
|**分母** <br/> |代表分数偏移量的分母，为从的开始处的结果集内的文件夹的总数。 此属性是必需的。 此属性必须表示大于 1 的整数值。 有关详细信息，请参阅本主题后面的备注。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义一个请求，以确定邮箱中的文件夹。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>备注

通过一小部分介绍了从开始的一组找到文件夹的分页的视图偏移量。 分数，由**分子**和**分母**属性定义，介绍的信息页的起始位置。 例如，如果**分子**等于四**分母**等于 5，返回的信息开始的项的页面位于五分之四中到结果集中的方式。 
  
如果 fraction 计算结果为零，用于指示结果集的开头。 如果 fraction 计算结果为一个，表明结果集的末尾。
  
> [!NOTE]
> 分数表示的页面的起始点，则将返回结果集内的结果不数量。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder Operation](findfolder-operation.md)


[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

