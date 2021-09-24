---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: IsUndecidedApprovalRequest 元素指定是否对审批请求邮件进行了处理。
ms.openlocfilehash: 5204793490015bd2999322c0f029445c7df91e02
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511411"
---
# <a name="isundecidedapprovalrequest"></a>IsUndecidedApprovalRequest

**IsUndecidedApprovalRequest** 元素指定是否对审批请求邮件进行了处理。 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>文本值

如果尚未处理审批请求邮件 **，IsUndecidedApprovalRequest** 元素的文本值为 **true。** false **值表示** 批准请求已决定。 
  
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



[ApprovalRequestData](approvalrequestdata.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

