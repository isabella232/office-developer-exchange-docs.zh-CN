---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: ConnectionFailureCause 元素指定从电话呼叫断开连接的原因。
ms.openlocfilehash: 54b4f5b89efdb42ef82dbef8f1af14a39c0ccc6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753484"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

**ConnectionFailureCause**元素指定从电话呼叫断开连接的原因。 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |指定电话呼叫的状态的信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**ConnectionFailureCause**元素的可能值。 
  
**ConnectionFailureCause 元素的值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |不断开连接的呼叫状态或不知道断开原因。  <br/> |
|UserBusy  <br/> |呼叫的方线路繁忙。  <br/> |
|NoAnswer  <br/> |呼叫的方没有应答。  <br/> |
|不可用  <br/> |呼叫的方号码不可用。  <br/> |
|其他  <br/> |全包式其他断开连接的原因。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

