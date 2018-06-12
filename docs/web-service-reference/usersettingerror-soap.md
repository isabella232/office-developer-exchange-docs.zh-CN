---
title: UserSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: UserSettingError 元素表示由于尝试获取用户设置返回的错误。
ms.openlocfilehash: 886e0be0aa900ce3a00902c21cc115e866d0cd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838490"
---
# <a name="usersettingerror-soap"></a>UserSettingError (SOAP)

**UserSettingError**元素表示由于尝试获取用户设置返回的错误。 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 **UserSettingError**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |代表由自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |表示与错误代码返回的自动发现服务关联的消息。  <br/> |
|[SettingName (SOAP)](settingname-soap.md) <br/> |代表用户设置的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |表示不会返回的设置的信息的集合。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

