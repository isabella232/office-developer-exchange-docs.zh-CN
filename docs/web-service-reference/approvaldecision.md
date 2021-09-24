---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: ApprovalDecision 元素指定对审批请求邮件做出的决定。
ms.openlocfilehash: 903b75f04255a19ebb7a9b4d0e47b685f22d4339
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517229"
---
# <a name="approvaldecision"></a>ApprovalDecision

**ApprovalDecision** 元素指定对审批请求邮件做出的决定。 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>文本值

**ApprovalDecision** 元素的文本值为 1（如果已批准）和 2（如果被拒绝）。 
  
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

- [ApprovalRequestData](approvalrequestdata.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

