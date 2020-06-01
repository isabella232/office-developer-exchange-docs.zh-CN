---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: IncludePersonalArchive 元素指定是否在搜索中包含个人存档。
ms.openlocfilehash: a25dd45bc0717af8f949d14b88793af3821ca69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458248"
---
# <a name="includepersonalarchive"></a>IncludePersonalArchive

**IncludePersonalArchive**元素指定是否在搜索中包含个人存档。 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md) <br/> |指定按关键字搜索邮箱统计信息的请求。  <br/> |
   
## <a name="text-value"></a>文本值

如果**IncludePersonalArchive**元素的文本值为**true** ，则表示该个人存档包含在搜索中。 **如果值为 false** ，则表示个人存档不包含在搜索中。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

