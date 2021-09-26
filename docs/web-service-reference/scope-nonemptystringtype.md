---
title: Scope (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Scope 元素指定邮件跟踪报告的范围。
ms.openlocfilehash: 036ff1007c9e7ec9cc385f8df81c045b7b9335b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546124"
---
# <a name="scope-nonemptystringtype"></a>Scope (NonEmptyStringType)

**Scope** 元素指定邮件跟踪报告的范围。 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[FindMessageTrackingReport](findmessagetrackingreport.md)  | [GetMessageTrackingReport](getmessagetrackingreport.md)
  
## <a name="text-value"></a>文本值

下表列出了 Scope **元素的可能值** 。 
  
|**值**|**说明**|
|:-----|:-----|
|组织  <br/> |邮件跟踪作用域跨越整个组织。  <br/> |
|林  <br/> |邮件跟踪作用域跨越林。  <br/> |
|网站  <br/> |邮件跟踪范围跨网站。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

