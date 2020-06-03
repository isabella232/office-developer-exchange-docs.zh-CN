---
title: 请求（GetOrganizationRelationship）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: Request 元素表示 GetOrganizationRelationshipSettingsRequest （SOAP）请求。 Request 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 90ccd3579c91c916ea645e6a3b466c9de4706421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459558"
---
# <a name="request-getorganizationrelationship-soap"></a>请求（GetOrganizationRelationship）（SOAP）

**Request**元素表示[GetOrganizationRelationshipSettingsRequest （SOAP）](getorganizationrelationshipsettingsrequest-soap.md)请求。 **Request**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<Request>
   <Domains/>
</Request>
```

 **GetOrganizationRelationshipSettingsRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域（SOAP）](domains-soap.md) <br/> |表示要在其中运行自动发现并在查询中使用的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetOrganizationRelationshipSettingsRequestMessage （SOAP）](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |表示[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)操作请求。  <br/> |
   
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



[GetOrganizationRelationshipSettingsRequest （SOAP）](getorganizationrelationshipsettingsrequest-soap.md)


[使用自动发现](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

