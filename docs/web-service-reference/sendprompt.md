---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: SendPrompt 元素指定的投票选项允许的操作的类型。
ms.openlocfilehash: f3220d957482ea04c46b014cdf1c67025d5ec21a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827346"
---
# <a name="sendprompt"></a>SendPrompt

**SendPrompt**元素指定的投票选项允许的操作的类型。 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[VotingOptionData](votingoptiondata.md)
  
## <a name="text-value"></a>文本值

**SendPrompt**元素的文本值的投票选项操作。 下表列出了此元素的可能值。 
  
****

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |执行任何操作。  <br/> |
|已发送  <br/> |立即发送响应。  <br/> |
|VotingOption  <br/> |审批者可以批准或拒绝时输入注释。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[VotingOptionData](votingoptiondata.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

