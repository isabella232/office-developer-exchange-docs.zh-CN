---
title: ExecutedSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExecutedSearchScope
api_type:
- schema
ms.assetid: 2de5f0ad-43f2-4d38-b520-06540066564e
description: ExecutedSearchScope 元素包含为获取搜索结果而执行的搜索的范围。
ms.openlocfilehash: 828fe3800b8c13a0e18c0daba6cdeab140a1c394
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456967"
---
# <a name="executedsearchscope"></a>ExecutedSearchScope

**ExecutedSearchScope**元素包含为获取搜索结果而执行的搜索的范围。 
  
```xml
<ExecutedSearchScope/>
```

 **String**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是可选的。 客户端应用程序使用此信息来更有效地缓存结果。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

