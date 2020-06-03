---
title: 错误（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Error 元素包含自动发现错误响应。
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530647"
---
# <a name="error-pox"></a>错误（POX）

**Error**元素包含自动发现错误响应。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[错误（POX）](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Time  <br/> |表示返回错误响应的时间。  <br/> |
|Id  <br/> |表示运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的名称的哈希值。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode （POX）](errorcode-pox.md) <br/> |包含错误发现响应的错误代码。  <br/> |
|[Message （POX）](message-pox.md) <br/> |包含错误发现响应的错误消息。  <br/> |
|[DebugData （POX）](debugdata-pox.md) <br/> |包含错误发现响应的调试数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户（POX）](account-pox.md) <br/> |包含自动发现错误响应。  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

