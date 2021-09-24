---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: FailedMailbox元素指定搜索邮箱失败的错误消息。
ms.openlocfilehash: 5e2bfbce5da35ecacd1757a9c612ed226af963ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535256"
---
# <a name="failedmailbox"></a>FailedMailbox

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FailedMailbox** 元素指定搜索邮箱失败的错误消息。 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 **FailedSearchMailboxType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[邮箱 (字符串)](mailbox-string.md) <br/> |包含邮箱的标识符。  <br/> |
|[错误代码 (int)](errorcode-int.md) <br/> |指定的邮箱，搜索失败的错误代码。  <br/> |
|[ErrorMessage](errormessage.md) <br/> |表示为验证错误的原因。  <br/> |
|[IsArchive](isarchive.md) <br/> |指定一个布尔值，该值指示该邮箱是否存档。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FailedMailboxes](failedmailboxes.md) <br/> |指定数组的邮箱失败。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

