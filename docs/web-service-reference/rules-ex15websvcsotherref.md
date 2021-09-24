---
title: 规则
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rules
api_type:
- schema
ms.assetid: 53f59054-8f68-4eaa-be9c-ccfc9383bcf2
description: Rules 元素包含一组保护规则。
ms.openlocfilehash: 492111e53c01a0848bd87c460670f35c524baf31
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517859"
---
# <a name="rules"></a>规则

**Rules** 元素包含一组保护规则。 
  
```xml
<Rules>   <Rule/></Rules>
```

 **ArrayOfProtectionRulesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Rule](rule.md) <br/> |包含单个保护规则。 此元素可以出现零次或多次。 当组织未定义保护规则时，此元素将发生零次。 如果组织定义了至少一个规则，则会发生一次或多次。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ProtectionRulesConfiguration](protectionrulesconfiguration.md) <br/> |包含保护规则服务的服务配置。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

