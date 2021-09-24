---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: VotingResponse 元素指定提交的投票。 此元素仅存在于对投票请求邮件的响应中，而不是对审批的响应中。
ms.openlocfilehash: 4d554cc3fc92911420b48b2da86d3ca3004018f7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510552"
---
# <a name="votingresponse"></a>VotingResponse

**VotingResponse** 元素指定提交的投票。 此元素仅存在于对投票请求邮件的响应中，而不是对审批的响应中。 
  
```XML
<VotingResponse />
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[VotingInformation](votinginformation.md)
  
## <a name="text-value"></a>文本值

**VotingResponse** 元素的文本值是提交的投票。 
  
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



[VotingInformation](votinginformation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

