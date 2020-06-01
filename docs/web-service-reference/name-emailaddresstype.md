---
title: 名称 (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: Name 元素表示邮箱用户的名称。
ms.openlocfilehash: db6eb547b5c848dc31bbaa377692989b16771673
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466925"
---
# <a name="name-emailaddresstype"></a>名称 (EmailAddressType)

**Name**元素表示邮箱用户的名称。 
  
```xml
<Name/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示字符串的文本值。
  
## <a name="remarks"></a>说明

此元素为可选。 **Name**元素存在于**AttachmentType**、 **EmailAddressType**和**EmailAddress**类型中。 "[名称" （EmailAddress）](name-emailaddress.md)元素主题中介绍了**EmailAddress**类型中的**name**元素。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

