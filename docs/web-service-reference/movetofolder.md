---
title: MoveToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveToFolder
api_type:
- schema
ms.assetid: 991673b9-b627-4848-bfba-59a187b8575f
description: MoveToFolder元素指定电子邮件项可以移动到的文件夹的标识符。
ms.openlocfilehash: e323b2ac5390855b3db0b5495af667cdf2da5596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530004"
---
# <a name="movetofolder"></a>MoveToFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MoveToFolder**元素指定电子邮件项可以移动到的文件夹的标识符。 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含用于复制或移动的项或文件夹的目标文件夹的标识符。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识命名的目标文件夹复制或移动的项或文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[操作](actions.md) <br/> |表示可在满足条件时要采取对邮件的操作的集合.  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[CopyToFolder](copytofolder.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

