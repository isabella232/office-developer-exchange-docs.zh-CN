---
title: WebClientUrl （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: WebClientUrl 元素表示 Exchange web 客户端的 URL。
ms.openlocfilehash: bcf9c8d4fe80de8af4c9500e5e850558a8451d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464971"
---
# <a name="webclienturl-soap"></a>WebClientUrl （SOAP）

**WebClientUrl**元素表示 Exchange web 客户端的 URL。 
  
[UserSetting （SOAP）](usersetting-soap.md)
  
[WebClientUrls （SOAP）](webclienturls-soap.md)
  
[WebClientUrl （SOAP）](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 **WebClientUrl**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AuthenticationMethods （SOAP）](authenticationmethods-soap.md) <br/> |表示在访问指定的 URL 时要使用的身份验证方法。  <br/> |
|[Url （SOAP）](url-soap.md) <br/> |表示 URL 的 web 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[WebClientUrls （SOAP）](webclienturls-soap.md) <br/> |表示一个用户设置，其中包含**WebClientUrl**元素的集合。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Url （SOAP）](url-soap.md)
  
[WebClientUrls （SOAP）](webclienturls-soap.md)

