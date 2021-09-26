---
title: UserSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: UserSettingErrors 元素表示有关无法返回的设置的信息集合。
ms.openlocfilehash: dfcd2a0475857d95d1a7dadb3cb65b544e0f2c5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541684"
---
# <a name="usersettingerrors-soap"></a>UserSettingErrors (SOAP)

**UserSettingErrors** 元素表示有关无法返回的设置的信息的集合。 
  
```XML
<UserSettingErrors>
    <UserSettingError/>
</UserSettingErrors>
```

 **UserSettingErrors**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |表示检索用户设置时返回的错误。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |表示对单个用户的 GetUserSettings 请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

