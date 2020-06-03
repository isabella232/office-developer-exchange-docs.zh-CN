---
title: Status （UM web 服务-SetOofStatus）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: Status 元素定义要在 SetOofStatus 操作（UM web 服务）请求中使用的值。
ms.openlocfilehash: 865152baf28c22578664e16db2dcd5f82a04af98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459978"
---
# <a name="status-um-web-service---setoofstatus"></a>Status （UM web 服务-SetOofStatus）

**Status**元素定义要在[SETOOFSTATUS 操作（UM web 服务）](setoofstatus-operation-um-web-service.md)请求中使用的值。 
  
[SetOofStatus （UM web 服务）](setoofstatus-um-web-service.md)
  
[Status （UM web 服务-SetOofStatus）](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SetOofStatus （UM web 服务）](setoofstatus-um-web-service.md) <br/> |定义一个请求，用于为发出请求的用户设置统一消息 "外出" （OOF）状态。  <br/> |
   
## <a name="text-value"></a>文本值

布尔值是必需的。 以下是可能的值：
  
- True
    
- False
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SetOofStatus 操作（UM web 服务）](setoofstatus-operation-um-web-service.md)

