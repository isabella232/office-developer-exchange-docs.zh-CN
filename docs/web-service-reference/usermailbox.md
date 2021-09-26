---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: UserMailbox元素标识用户邮箱。
ms.openlocfilehash: c2a66b23de5e4b312f60019f0b4ecfb4088b3da2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542615"
---
# <a name="usermailbox"></a>UserMailbox

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UserMailbox** 元素标识用户邮箱。 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 **UserMailboxType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |**Id** 属性的文本值是邮箱的标识符。  <br/> |
|IsArchive  <br/> |**IsArchive** 属性的文本值指示该邮箱是否存档邮箱。 **true** **IsArchive** 属性的文本值表示邮箱存档邮箱。 **false** **IsArchive** 属性的值表示邮箱是一个主邮箱。 <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[邮箱 (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

