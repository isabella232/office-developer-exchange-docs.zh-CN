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
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838348"
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |定义请求解析模糊名称。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示公共联系人或通讯组列表的名称。 字符串的最小长度是一个字符。
  
## <a name="remarks"></a>备注

此元素的文本值用于解析名称针对以下字段：
  
- 名
    
- 姓
    
- 显示名称
    
- 全名
    
- Office
    
- Alias
    
- SMTP 地址
    
多值数组中保存前缀的路由类型，如 smtp 或 sip，与电子邮件地址。 无法解析的名称，例如"sip:User1@Contoso.com"的开头添加路由类型时， [ResolveNames 操作](resolvenames-operation.md)执行针对该数组的每个值的部分匹配。 如果不指定传送类型， **ResolveNames**操作将默认为 smtp 的路由类型、 匹配到主 SMTP 地址属性，和搜索多值数组。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ResolveNames 操作](resolvenames-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

