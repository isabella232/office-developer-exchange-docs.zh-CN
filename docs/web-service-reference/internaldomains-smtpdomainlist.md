---
title: InternalDomains (SmtpDomainList)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: InternalDomains 元素标识组织的内部 SMTP 域的列表。
ms.openlocfilehash: 3aa879ae7f441f63520ab037f86a8da1056af4c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515570"
---
# <a name="internaldomains-smtpdomainlist"></a>InternalDomains (SmtpDomainList)

**InternalDomains** 元素标识组织的内部 SMTP 域的列表。 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 **SmtpDomainList**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域](domain.md) <br/> |标识单个 SMTP 域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |包含邮件提示服务的服务配置信息。  <br/> |
|[ProtectionRulesConfiguration](protectionrulesconfiguration.md) <br/> |包含保护规则服务的服务配置信息。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

此元素是必需的。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

