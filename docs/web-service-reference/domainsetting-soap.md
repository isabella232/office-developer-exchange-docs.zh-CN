---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: DomainSetting 元素包含由 GETDomainSettings 操作返回的域设置 (SOAP) 请求。
ms.openlocfilehash: 19c88e6f3f517d012a5c51f548da3d3776770444
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541446"
---
# <a name="domainsetting-soap"></a>DomainSetting (SOAP)

**DomainSetting** 元素包含由 [GETDomainSettings](getdomainsettings-operation-soap.md)操作返回的域设置 (SOAP) 请求。 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 **DomainSetting**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Name (SOAP)](name-soap.md) <br/> |表示设置的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |表示在自动发现请求中提交或由自动发现响应返回的域设置。  <br/> |
   
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

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

