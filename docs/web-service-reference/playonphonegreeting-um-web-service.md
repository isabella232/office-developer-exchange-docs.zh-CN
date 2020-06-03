---
title: PlayOnPhoneGreeting （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: PlayOnPhoneGreeting 元素定义一个请求，以在电话上播放统一消息问候语。
ms.openlocfilehash: 197e4ba671e1711b73b1e7c239339db589357581
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529922"
---
# <a name="playonphonegreeting-um-web-service"></a>PlayOnPhoneGreeting （UM web 服务）

**PlayOnPhoneGreeting**元素定义一个请求，以在电话上播放统一消息问候语。 
  
[PlayOnPhoneGreeting （UM web 服务）](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 **complexType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[GreetingType （UM web 服务）](greetingtype-um-web-service.md) <br/> |定义要在[PlayOnPhoneGreeting 操作（UM web 服务）](playonphonegreeting-operation-um-web-service.md)请求中使用的问候语的类型。  <br/> |
|[dialString （UM web 服务）](dialstring-um-web-service.md) <br/> |包含要拨打的电话号码的值。  <br/> |
   
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



[PlayOnPhoneGreeting 操作（UM web 服务）](playonphonegreeting-operation-um-web-service.md)

