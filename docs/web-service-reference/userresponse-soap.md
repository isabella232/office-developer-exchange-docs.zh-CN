---
title: UserResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: UserResponse 元素表示对单个用户的 GetUserSettings 请求的响应。
ms.openlocfilehash: 73848cb19d9c859e07216f354965ac4051d0d20c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468899"
---
# <a name="userresponse-soap"></a>UserResponse （SOAP）

**UserResponse**元素表示对单个用户的 GetUserSettings 请求的响应。 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 **UserResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[RedirectTarget （SOAP）](redirecttarget-soap.md) <br/> |包含重定向 URL 或电子邮件地址的目标。  <br/> |
|[UserSettingErrors （SOAP）](usersettingerrors-soap.md) <br/> |表示有关无法返回的设置的信息的集合。  <br/> |
|[UserSettings （SOAP）](usersettings-soap.md) <br/> |用户的请求设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ArrayOfUserResponse （SOAP）](arrayofuserresponse-soap.md) <br/> |包含用户响应的数组。  <br/> |
|[UserResponses （SOAP）](userresponses-soap.md) <br/> |包含每个请求的用户的配置设置。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

