---
title: DomainSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a4ce19de-f560-4984-8047-ecbbc86c9b91
description: DomainSettingsErrors 元素包含无法返回的设置的错误信息。
ms.openlocfilehash: d34fa8be4b4bc24e99fb6b1cd36d02e4c4915dd7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544211"
---
# <a name="domainsettingerrors-soap"></a>DomainSettingErrors (SOAP)

**DomainSettingsErrors** 元素包含无法返回的设置的错误信息。 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 **DomainSettingsErrors**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSettingError (SOAP)](domainsettingerror-soap.md) <br/> |表示检索域设置时发生的错误。 这表示 SOAP 请求的 [GetDomainSettings (错误) ](getdomainsettings-operation-soap.md) 错误。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |包含指定域的请求设置。  <br/> |
   
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

