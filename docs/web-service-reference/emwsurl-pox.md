---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: EmwsUrl 元素指定最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS) 启用邮件的用户。
ms.openlocfilehash: d8905d098c9978c3413f67e9a1b2443a52fb0d1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754096"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

**EmwsUrl**元素指定最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS) 启用邮件的用户。 
  
- [自动发现 (POX)](autodiscover-pox.md) 
- [响应 (POX)](response-pox.md) 
- [帐户 (POX)](account-pox.md) 
- [协议 (POX)](protocol-pox.md) 
- [EmwsUrl (POX)](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的 EWS 终结点的 URL。 它等效于[EwsUrl (POX)](ewsurl-pox.md)元素。 
  
## <a name="remarks"></a>备注

**EmwsUrl**元素是**协议**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

