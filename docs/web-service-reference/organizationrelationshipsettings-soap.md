---
title: OrganizationRelationshipSettings （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: OrganizationRelationshipSettings 元素表示单个组织的组织关系列表。 OrganizationRelationshipSettings 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 383b3635e1435c6597ccf793a7990c411c02d36d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462456"
---
# <a name="organizationrelationshipsettings-soap"></a>OrganizationRelationshipSettings （SOAP）

**OrganizationRelationshipSettings**元素表示单个组织的组织关系列表。 **OrganizationRelationshipSettings**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<OrganizationRelationshipSettings>
    <DeliveryReportEnabled/>
    <DomainNames/>
    <FreeBusyAccessEnabled/>
    <FreeBusyAccessLevel/>
    <MailTipsAccessEnabled/>
    <MailTipsAccessLevel/>
    <MailboxMoveEnabled/>
    <Name/>
    <TargetApplicationUri/>
    <TargetAudodiscoverEpr/>
    <TargetSharingEpr/>
</OrganizationRelationshipSettings>
```

 **OrganizationRelationshipSettings**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DeliveryReportEnabled （SOAP）](deliveryreportenabled-soap.md) <br/> |代表 " [DeliveryReportEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx)标志。  <br/> |
|[DomainNames （SOAP）](domainnames-soap.md) <br/> |表示域名集合。  <br/> |
|[FreeBusyAccessEnabled （SOAP）](freebusyaccessenabled-soap.md) <br/> |代表 " [FreeBusyAccessEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx)标志。  <br/> |
|[FreeBusyAccessLevel （SOAP）](freebusyaccesslevel-soap.md) <br/> |表示[FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx)属性。  <br/> |
|[MailTipsAccessEnabled （SOAP）](mailtipsaccessenabled-soap.md) <br/> |代表 " [MailTipsAccessEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx)标志。  <br/> |
|[MailTipsAccessLevel （SOAP）](mailtipsaccesslevel-soap.md) <br/> |表示[MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx)属性。  <br/> |
|[MailboxMoveEnabled （SOAP）](mailboxmoveenabled-soap.md) <br/> |代表 " [MailboxMoveEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx)标志。  <br/> |
|[名称（SOAP）](name-soap.md) <br/> |表示组织关系的名称。  <br/> |
|[TargetApplicationUri （SOAP）](targetapplicationuri-soap.md) <br/> |定义目标应用程序 URI。  <br/> |
|[TargetAutodiscoverEpr （SOAP）](targetautodiscoverepr-soap.md) <br/> |表示[TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx)属性。  <br/> |
|[TargetSharingEpr （SOAP）](targetsharingepr-soap.md) <br/> |表示[TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx)属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettingsCollection （SOAP）](organizationrelationshipsettingscollection-soap.md) <br/> |表示与查询匹配的组织关系的列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

