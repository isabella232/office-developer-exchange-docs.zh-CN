---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: UnresolvedEntry 元素包含要解析的联系人或通讯组列表的名称。
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459838"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

**UnresolvedEntry**元素包含要解析的联系人或通讯组列表的名称。 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |定义用于解析不明确名称的请求。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值代表公共联系人或通讯组列表的名称。 字符串的最小长度为一个字符。
  
## <a name="remarks"></a>备注

此元素的文本值用于针对以下字段解析名称：
  
- 名
    
- 姓
    
- 可分辨名称 (DN)
    
- 全名
    
- Office
    
- 别名
    
- SMTP 地址
    
带有前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。 当您在未解析名称的开头添加路由类型（如 "sip:User1@Contoso.com"）时， [ResolveNames 操作](resolvenames-operation.md)将对该数组的每个值执行部分匹配。 如果不指定路由类型， **ResolveNames**操作将默认为 smtp 的路由类型，将其与主 smtp 地址属性相匹配，而不会搜索多值数组。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ResolveNames 操作](resolvenames-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

