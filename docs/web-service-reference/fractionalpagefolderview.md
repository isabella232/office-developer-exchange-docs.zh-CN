---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: FractionalPageFolderView 元素描述分页视图的起始位置以及 FindFolder 请求中返回的最大文件夹数。
ms.openlocfilehash: b3d4bd63f94c2db7761dabfad1e32558ceb30be5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530251"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

**FractionalPageFolderView** 元素描述分页视图的起始位置以及 [FindFolder](findfolder.md)请求中返回的最大文件夹数。 
  
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
|**MaxEntriesReturned** <br/> |标识在 [FindFolder](findfolder.md) 响应中返回的最大结果数。 此特性是可选的。  <br/> |
|**Numerator** <br/> |表示从起始位置开始的小数偏移的结果集。 此特性是必需的。 分子必须等于或小于分母。 此属性必须表示等于或大于零的整数值。 有关详细信息，请参阅本主题稍后的"说明"。  <br/> |
|**Denominator** <br/> |表示从文件夹中文件夹总数开始的小数偏移的分母结果集。 此特性是必需的。 此属性必须表示大于 1 的整数值。 有关详细信息，请参阅本主题稍后的"说明"。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义标识邮箱中的文件夹的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>注解

找到的文件夹集的起始位置的分页视图偏移量由小数部分描述。 分数（由 **Numerator** 和 **Denominator** 属性定义）描述信息页的起始位置。 例如，如果 **Numerator** 等于 4， **并且 Denominator** 等于 5，则返回信息的页面从位于进入该数字的 4/5 结果集。 
  
如果分数计算结果为零，则指示结果集的开始。 如果分数计算结果为 1，则表明结果集。
  
> [!NOTE]
> 分数表示页面的起始点，而不是返回结果集的结果数。 
  
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

