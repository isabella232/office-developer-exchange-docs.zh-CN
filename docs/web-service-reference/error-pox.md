---
title: 错误 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Error 元素包含自动发现错误响应。
ms.openlocfilehash: 3135a352365fe3000ce2d202ad78452d5c8ccc7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754144"
---
# <a name="error-pox"></a>错误 (POX)

**Error**元素包含自动发现错误响应。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[错误 (POX)](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|时间  <br/> |表示时返回的错误响应时间。  <br/> |
|Id  <br/> |代表为运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的名称的哈希值。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |包含自动发现响应的错误的错误代码。  <br/> |
|[消息 (POX)](message-pox.md) <br/> |包含错误自动发现响应的错误消息。  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |包含错误自动发现响应的调试数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户 (POX)](account-pox.md) <br/> |包含自动发现错误响应。  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

