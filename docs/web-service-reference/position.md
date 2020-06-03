---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Position 元素指定从邮件提取的实体的位置。
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465420"
---
# <a name="position"></a>Position

**Position**元素指定从邮件提取的实体的位置。 
  
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

[UrlEntity](urlentity.md)  | [AddressEntity](addressentity.md)  | [EmailAddressEntity](emailaddressentity.md)  | [MeetingSuggestion](meetingsuggestion.md)  | [Contact （ContactType）](contact-contacttype.md)  | [电话（PhoneEntityType）](phone-phoneentitytype.md)  | [TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>文本值

**Position**元素的文本值是提取的实体在源消息中产生的位置。 **Position**元素的文本值为： 
  
- **LatestReply** -提取的实体源自最新的邮件答复。 
    
- **其他**-提取的实体来自未定义的邮件部分。 
    
- **Subject** -提取的实体来自邮件主题。 
    
- **签名**-提取的实体源于邮件签名。 
    
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

