---
title: 常量
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: 常量元素标识限制中的常量值。
ms.openlocfilehash: 6cb2eaa4227a8fd0985e8ff5a15d647c3bb1cd6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461553"
---
# <a name="constant"></a>常量

**常量**元素标识限制中的常量值。 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**值** <br/> |指定要在限制中比较的值。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Contains](contains.md) <br/> |表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |表示与其他属性进行比较时要使用的属性或常数值。  <br/> |
   
## <a name="remarks"></a>备注

**Value**属性中的字符串值必须强制转换为您尝试进行比较的类型。 例如，如果要将日期/时间属性与常量值进行比较，则字符串值必须代表日期/时间。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

