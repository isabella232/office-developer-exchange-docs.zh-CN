---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: DocumentSharingLocation 元素包含位置和文档共享位置的元数据信息。
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753966"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

**DocumentSharingLocation**元素包含位置和文档共享位置的元数据信息。 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 **DocumentSharingLocation**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |代表共享 web 服务的文档的 URL。  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |代表共享位置的文档的 URL。  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |代表共享位置，用于在 UI 中的文档的名称。  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |表示可以共享位置在文档中存储的文件扩展名。  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |指示是否可用于外部连接共享位置的文档。  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |指示访问共享位置是否需要身份验证的用户。  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |指示用户是否可以修改到文档共享位置的访问权限。  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |指示文档共享位置是否为用户的默认共享位置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |包含共享位置和元数据文档的列表。  <br/> |
   
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

- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
- [SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

