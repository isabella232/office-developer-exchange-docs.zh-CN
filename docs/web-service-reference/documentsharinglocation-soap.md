---
title: DocumentSharingLocation （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: DocumentSharingLocation 元素包含文档共享位置的位置和元数据信息。
ms.openlocfilehash: 6fed933da979ab3e3fca51ba606127b7f0a4e3f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457058"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation （SOAP）

**DocumentSharingLocation**元素包含文档共享位置的位置和元数据信息。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ServiceUrl （SOAP）](serviceurl-soap.md) <br/> |表示文档共享 web 服务的 URL。  <br/> |
|[LocationUrl （SOAP）](locationurl-soap.md) <br/> |表示文档共享位置的 URL。  <br/> |
|[DisplayName （SOAP）](displayname-soap.md) <br/> |表示要在 UI 中使用的文档共享位置的名称。  <br/> |
|[SupportedFileExtensions （SOAP）](supportedfileextensions-soap.md) <br/> |表示可存储在文档共享位置的文件扩展名。  <br/> |
|[ExternalAccessAllowed （SOAP）](externalaccessallowed-soap.md) <br/> |指示文档共享位置是否可用于外部连接。  <br/> |
|[AnonymousAccessAllowed （SOAP）](anonymousaccessallowed-soap.md) <br/> |指示对共享位置的访问是否需要经过身份验证的用户。  <br/> |
|[CanModifyPermissions （SOAP）](canmodifypermissions-soap.md) <br/> |指示用户是否可以修改文档共享位置的访问权限。  <br/> |
|[IsDefault （SOAP）](isdefault-soap.md) <br/> |指示文档共享位置是否为用户的默认共享位置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DocumentSharingLocations （SOAP）](documentsharinglocations-soap.md) <br/> |包含文档共享位置和元数据的列表。  <br/> |
   
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

- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

