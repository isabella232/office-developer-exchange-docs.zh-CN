---
title: MaxChangesReturned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MaxChangesReturned
api_type:
- schema
ms.assetid: f471db84-a666-4dfa-9993-8ca9113a0384
description: MaxChangesReturned 元素描述同步响应中可返回的最大更改数。
ms.openlocfilehash: 8169e1a87ed22b68e5115cd7eaaa1084e44e8f33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523929"
---
# <a name="maxchangesreturned"></a>MaxChangesReturned

**MaxChangesReturned** 元素描述同步响应中可返回的最大更改数。 
  
[SyncFolderItems](syncfolderitems.md)
  
[MaxChangesReturned](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步邮件存储文件夹中Exchange的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示一个整数，该整数描述单个同步调用中返回的最大项目数。 该值必须介于 1 和 512 之间（包含两者）。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

