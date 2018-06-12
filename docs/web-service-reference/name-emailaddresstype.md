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
description: Name 元素表示的邮箱用户的名称。
ms.openlocfilehash: b140fd46608a04f9aaba17f917cc4171c056dcf2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826504"
---
# <a name="name-emailaddresstype"></a>名称 (EmailAddressType)

**Name**元素表示的邮箱用户的名称。 
  
```xml
<Name/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室的列表。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要用于表示字符串的文本值。
  
## <a name="remarks"></a>备注

此元素为可选。 **Name**元素存在于**AttachmentType**、 **EmailAddressType**和**电子邮件地址**类型。 **Name**元素中的**电子邮件地址**类型[名称 (EmailAddress)](name-emailaddress.md)元素主题所述。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

