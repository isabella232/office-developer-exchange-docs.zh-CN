---
title: LastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- LastDeliveryTime
api_type:
- schema
ms.assetid: 23d02ceb-f28e-40f2-8f63-673723a50e2a
description: LastDeliveryTime 元素包含当前文件夹中此对话中最后一次接收的邮件的传递时间。
ms.openlocfilehash: bb0ad41272d26efecf36113d9c82a647c237ac47
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546173"
---
# <a name="lastdeliverytime"></a>LastDeliveryTime

**LastDeliveryTime** 元素包含当前文件夹中此对话中最后一次接收的邮件的传递时间。 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[对话 (ConversationType)](conversation-conversationtype.md)
  
[LastDeliveryTime](lastdeliverytime.md)
  
```XML
<LastDeliveryTime/>
```

 **xs：dateTime**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
   
## <a name="text-value"></a>文本值

**LastDeliveryTime** 元素的文本值是当前文件夹中此对话中最后一次收到邮件的日期和时间。 
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction 操作](applyconversationaction-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

