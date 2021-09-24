---
title: GetOrganizationRelationshipSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: GetOrganizationRelationshipSettingsResponse 元素包含 SOAP 响应 (GetOrganizationRelationshipSettings) 操作。 GetOrganizationRelationshipSettingsResponse 元素仅供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: e62496b70c89477fa87a50de256aa8a6b37f3111
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524243"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a>GetOrganizationRelationshipSettingsResponse (SOAP)

**GetOrganizationRelationshipSettingsResponse** 元素包含 SOAP 响应 ([GetOrganizationRelationshipSettings)](getorganizationrelationshipsettings-operation-soap.md)操作。 **GetOrganizationRelationshipSettingsResponse** 元素仅供内部使用。 此元素不由客户端使用。 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 **GetOrganizationRelationshipSettingsResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[OrganizationRelationshipSettingsCollection (SOAP)](organizationrelationshipsettingscollection-soap.md) <br/> |表示与查询匹配的组织关系的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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



[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

