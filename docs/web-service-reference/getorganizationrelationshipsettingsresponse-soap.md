---
title: GetOrganizationRelationshipSettingsResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: GetOrganizationRelationshipSettingsResponse 元素包含 GetOrganizationRelationshipSettings 操作（SOAP）响应。 GetOrganizationRelationshipSettingsResponse 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 0f34fbc6577b379dd0ac379564c5e6bbd940d379
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457919"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a>GetOrganizationRelationshipSettingsResponse （SOAP）

**GetOrganizationRelationshipSettingsResponse**元素包含[GETORGANIZATIONRELATIONSHIPSETTINGS 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)响应。 **GetOrganizationRelationshipSettingsResponse**元素仅供内部使用。 客户端不使用此元素。 
  
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
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[OrganizationRelationshipSettingsCollection （SOAP）](organizationrelationshipsettingscollection-soap.md) <br/> |表示与查询匹配的组织关系的集合。  <br/> |
   
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



[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

