---
title: SetPlayOnPhoneDialString （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: SetPlayOnPhoneDialString 元素定义一个请求，用于设置 PlayOnPhone 操作（UM web 服务）和 PlayOnPhoneGreeting 操作（UM web 服务）请求的默认拨号字符串。
ms.openlocfilehash: 40021e9dedafb5fafda91bf3612d8a6485dae8e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458626"
---
# <a name="setplayonphonedialstring-um-web-service"></a>SetPlayOnPhoneDialString （UM web 服务）

**SetPlayOnPhoneDialString**元素定义一个请求，用于设置[PLAYONPHONE 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PlayOnPhoneGreeting 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)请求的默认拨号字符串。 
  
[SetPlayOnPhoneDialString （UM web 服务）](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 **complexType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[dialString （UM web 服务）](dialstring-um-web-service.md) <br/> |要设置为默认拨号字符串的电话号码。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SetPlayOnPhoneDialString 操作（UM web 服务）](setplayonphonedialstring-operation-um-web-service.md)

