---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: VotingInformation 元素指定投票邮件和审批请求邮件的投票信息，其中ApproveandReject是投票选项。
ms.openlocfilehash: 7e5aedddbfe97bba935aa56b3583e2fb8b081320
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543854"
---
# <a name="votinginformation"></a>VotingInformation

**VotingInformation** 元素指定对投票邮件和审批请求邮件的投票信息，其中"批准"和"拒绝"是投票选项。 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 **VotingInformationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[UserOptions](useroptions.md)  | [VotingResponse](votingresponse.md)
  
### <a name="parent-elements"></a>父元素

[消息](message-ex15websvcsotherref.md)
  
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



[消息](message-ex15websvcsotherref.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

