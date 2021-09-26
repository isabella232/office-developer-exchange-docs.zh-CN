---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: AlternateMailbox 元素表示备用邮箱。
ms.openlocfilehash: 3646efef9b63b2af8dbba41a07a86462e18ac1c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543721"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

**AlternateMailbox** 元素表示备用邮箱。 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 **AlternateMailbox**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Type (SOAP)](type-soap.md) <br/> |表示备用邮箱类型。  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |代表备用邮箱显示名称。  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |表示备用邮箱旧版可分辨名称。  <br/> |
|[Server (SOAP)](server-soap.md) <br/> |代表备用邮箱服务器。  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |代表备用邮箱 SMTP 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |表示备用邮箱的集合。  <br/> |
   
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

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

