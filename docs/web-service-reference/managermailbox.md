---
title: ManagerMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 70c324d5-2196-406d-a674-73323f8d8b92
description: ManagerMailbox元素包含标识联系人的经理的邮箱的 SMTP 信息。
ms.openlocfilehash: 605ecfe40d3d2c2d43378cddda4cf5789098e3f0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524789"
---
# <a name="managermailbox"></a>ManagerMailbox

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ManagerMailbox** 元素包含标识联系人的经理的邮箱的 SMTP 信息。 
  
```XML
<ManagerMailbox>
   <Mailbox/>
</ManagerMailbox>
```

 **SingleRecipientType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识标识发件人的启用邮件的 Active Directory 对象。  <br/> |
  
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[联系人](contact.md) <br/> |表示对 Exchange 存储中的联系人项目。  <br/> |

## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

