---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: ConnectionFailureCause 元素指定断开与电话呼叫连接的原因。
ms.openlocfilehash: de2f06ae89577b0141b8555f98dba1671a228d45
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543532"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

**ConnectionFailureCause** 元素指定断开与电话呼叫连接的原因。 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |指定电话呼叫的状态信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **ConnectionFailureCause** 元素的可能值。 
  
**ConnectionFailureCause 元素值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |呼叫状态未断开或断开连接原因未知。  <br/> |
|UserBusy  <br/> |被叫方线路繁忙。  <br/> |
|NoAnswer  <br/> |被叫方未应答。  <br/> |
|不可用  <br/> |被叫方号码不可用。  <br/> |
|其他  <br/> |由于其他断开连接原因，捕获全部。  <br/> |
   
## <a name="remarks"></a>说明

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

