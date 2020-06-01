---
title: UserSettingErrors （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: UserSettingErrors 元素表示无法返回的设置的相关信息的集合。
ms.openlocfilehash: a6cc0fe114bd511dc4136532986b552c28b0d5c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467121"
---
# <a name="usersettingerrors-soap"></a>UserSettingErrors （SOAP）

**UserSettingErrors**元素表示无法返回的设置的相关信息的集合。 
  
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
|[UserSettingError （SOAP）](usersettingerror-soap.md) <br/> |表示检索用户设置时返回的错误。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserResponse （SOAP）](userresponse-soap.md) <br/> |表示对单个用户的 GetUserSettings 请求的响应。  <br/> |
   
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

