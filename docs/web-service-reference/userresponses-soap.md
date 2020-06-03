---
title: UserResponses （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: UserResponses 元素包含每个请求的用户的配置设置。
ms.openlocfilehash: db2bab16334b90395d29dc03353dce05b0e45357
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526744"
---
# <a name="userresponses-soap"></a>UserResponses （SOAP）

**UserResponses**元素包含每个请求的用户的配置设置。 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 **ArrayOfUserResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserResponse （SOAP）](userresponse-soap.md) <br/> |表示对单个用户的[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[响应（SOAP）](response-soap.md) <br/> |包含对[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)

