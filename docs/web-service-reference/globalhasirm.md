---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: GlobalHasIrm 元素指定对话中以及所有文件夹中是否至少有一封邮件是受 IRM 保护的邮件。
ms.openlocfilehash: bd3414136a115b016c291fa0482682efcc7d9e1a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516830"
---
# <a name="globalhasirm"></a>GlobalHasIrm

**GlobalHasIrm** 元素指定对话中以及所有文件夹中是否至少有一封邮件是受 IRM 保护的邮件。 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
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

如果对话中以及所有文件夹中至少有一封邮件是受 IRM 保护的邮件，**则 GlobalHasIrm** 元素的文本值为 **true。** 否则值为 **false**。
  
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

