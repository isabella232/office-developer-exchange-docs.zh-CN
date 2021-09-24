---
title: User (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: User 元素表示单个用户的标识。
ms.openlocfilehash: 545869e21726d60ecdd503106c743d66fc752414
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517376"
---
# <a name="user-soap"></a>User (SOAP)

**User** 元素表示单个用户的标识。 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 **用户**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |表示备用邮箱旧版可分辨名称。  <br/> |
|[Mailbox (SOAP)](mailbox-soap.md) <br/> |包含要发现的用户的电子邮件地址。  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |包含请求的配置设置的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |表示 User **元素** 的集合。  <br/> |
   
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



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

