---
title: AutodiscoverResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: AutodiscoverResponse （SOAP）元素表示自动发现服务返回的所有响应的基本元素。
ms.openlocfilehash: 81fd557578bde9552d07e24386c93903e44a9afa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463963"
---
# <a name="autodiscoverresponse-soap"></a>AutodiscoverResponse （SOAP）

**AutodiscoverResponse （SOAP）** 元素表示自动发现服务返回的所有响应的基本元素。 
  
- [AutodiscoverResponse （SOAP）](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 **AutodiscoverResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserResponses （SOAP）](userresponses-soap.md) <br/> |表示[UserResponse （SOAP）](userresponse-soap.md)元素的集合。  <br/> |
|[UserSettingErrors （SOAP）](usersettingerrors-soap.md) <br/> |表示[UserSettingError （SOAP）](usersettingerror-soap.md)元素的集合。  <br/> |
|[UserSettings （SOAP）](usersettings-soap.md) <br/> |表示[UserSetting （SOAP）](usersetting-soap.md)元素的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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

- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)
- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

