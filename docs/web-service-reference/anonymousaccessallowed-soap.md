---
title: AnonymousAccessAllowed （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: AnonymousAccessAllowed 元素指示文档共享位置是否需要经过身份验证的用户。
ms.openlocfilehash: b3ff22fbba603bbd74dc08a0dbb1d8687714fe7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466078"
---
# <a name="anonymousaccessallowed-soap"></a>AnonymousAccessAllowed （SOAP）

**AnonymousAccessAllowed**元素指示文档共享位置是否需要经过身份验证的用户。 
  
```XML
<AnonymousAccessAllowed /> 
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DocumentSharingLocation （SOAP）](documentsharinglocation-soap.md) <br/> |表示文档共享位置的位置和元数据信息。  <br/> |
   
## <a name="text-value"></a>文本值

**AnonymousAccessAllowed**元素的布尔值指示共享位置是否需要经过身份验证的用户。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

