---
title: Request (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: Request 元素表示 SOAP 请求 (GetOrganizationRelationshipSettingsRequest) 。 Request 元素供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: 06af9ca1067407f7fac9db3ff7c5b4e0fbe8a108
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512364"
---
# <a name="request-getorganizationrelationship-soap"></a>Request (GetOrganizationRelationship) (SOAP)

**Request** 元素表示 SOAP 请求 ([GetOrganizationRelationshipSettingsRequest) 。](getorganizationrelationshipsettingsrequest-soap.md) **Request** 元素供内部使用。 此元素不由客户端使用。 
  
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
|[Domains (SOAP)](domains-soap.md) <br/> |表示要运行自动发现以及要用于查询的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetOrganizationRelationshipSettingsRequestMessage (SOAP)](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |表示 [SOAP (请求) GetOrganizationRelationshipSettings ](getorganizationrelationshipsettings-operation-soap.md) 操作。  <br/> |
   
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



[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)


[使用自动发现](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

