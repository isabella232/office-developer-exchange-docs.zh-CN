---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: HasIrm 元素指定会话和当前文件夹中是否至少有一封邮件是受 IRM 保护的邮件。
ms.openlocfilehash: ef194c045bfd2b416e382c12381afd68ba56dcf3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516690"
---
# <a name="hasirm"></a>HasIrm

**HasIrm** 元素指定会话和当前文件夹中是否至少有一封邮件是受 IRM 保护的邮件。 
  
```XML
<HasIrm> true | false </HasIrm>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[对话 (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>文本值

如果对话中至少有一封邮件并且当前文件夹具有IRM，**则 HasIrm** 元素的文本值为 true。 否则，值为 **false**。
  
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[对话 (ConversationType)](conversation-conversationtype.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

