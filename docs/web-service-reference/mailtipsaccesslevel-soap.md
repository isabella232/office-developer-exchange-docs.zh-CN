---
title: MailTipsAccessLevel (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 730e349e-8250-4236-af53-cd9039c74d8f
description: MailTipsAccessLevel 元素表示 MailTipsAccessLevel 属性。 MailTipsAccessLevel 元素仅供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: 275bdab1be5a754aa0cfa57eea232175e3d39ff3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524040"
---
# <a name="mailtipsaccesslevel-soap"></a>MailTipsAccessLevel (SOAP)

**MailTipsAccessLevel** 元素表示 **MailTipsAccessLevel** 属性。 **MailTipsAccessLevel** 元素仅供内部使用。 此元素不由客户端使用。 
  
```XML
<MailTipsAccessLevel/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="remarks"></a>注解

此元素指定响应中将返回的邮件提示详细信息的最大数量。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

