---
title: EmwsUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: EmwsUrl 元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。
ms.openlocfilehash: 19e1078ae8d08513e85d75d87e960a910986f727
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530668"
---
# <a name="emwsurl-pox"></a>EmwsUrl （POX）

**EmwsUrl**元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。 
  
- [自动发现（POX）](autodiscover-pox.md) 
- [响应（POX）](response-pox.md) 
- [帐户（POX）](account-pox.md) 
- [协议（POX）](protocol-pox.md) 
- [EmwsUrl （POX）](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的 EWS 终结点的 URL。 它等效于[mailbox.ewsurl （POX）](ewsurl-pox.md)元素。 
  
## <a name="remarks"></a>备注

**EmwsUrl**元素是**Protocol**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

