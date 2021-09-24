---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Position 元素指定从邮件中提取的实体的位置。
ms.openlocfilehash: 6b4e7c12bbcf12b8804619caa508f5c2c0bc4eda
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515290"
---
# <a name="position"></a>Position

**Position** 元素指定从邮件中提取的实体的位置。 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 **EmailPositionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[UrlEntity](urlentity.md)  | [AddressEntity](addressentity.md)  | [EmailAddressEntity](emailaddressentity.md)  | [MeetingSuggestion](meetingsuggestion.md)  | [Contact (ContactType) ](contact-contacttype.md)  | [电话 (PhoneEntityType) ](phone-phoneentitytype.md)  | [TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>文本值

**Position** 元素的文本值是提取的实体源自源邮件的位置。 **Position** 元素的文本值为： 
  
- **LatestReply** - 提取的实体源自对邮件的最新回复。 
    
- **Other** - 提取的实体源自邮件的未定义部分。 
    
- **Subject** - 提取的实体源自邮件主题。 
    
- **Signature** - 提取的实体源自邮件签名。 
    
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

