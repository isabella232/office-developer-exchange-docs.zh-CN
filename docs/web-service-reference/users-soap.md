---
title: 用户 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Users 元素表示的设置应为其检索用户的电子邮件地址的集合。
ms.openlocfilehash: d7655f0020a315dcb32adbbc58610ca0e630c1fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838488"
---
# <a name="users-soap"></a>用户 (SOAP)

**Users**元素表示的设置应为其检索用户的电子邮件地址的集合。 
  
```XML
<Users>
   <User/>
</Users>
```

 **用户**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[用户 (SOAP)](user-soap.md) <br/> |代表用户的电子邮件地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |表示检索指定的设置为一个或多个用户的请求。  <br/> |
|[请求 (SOAP)](request-soap.md) <br/> |包含请求的配置设置和目标用户。  <br/> |
   
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



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)

