---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: DistinguishedUser 元素标识委派访问的匿名和默认用户帐户。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: ce59b5775f6f0516c469c7ee8bc4546780ce86d0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544239"
---
# <a name="distinguisheduser"></a>DistinguishedUser

**DistinguishedUser 元素** 标识委派访问的匿名和默认用户帐户。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 **DistinguishedUserType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserId](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

Default **的文本值描述** 添加到主体邮箱的委派用户的默认设置。 Anonymous **的文本值描述** 匿名用户对主体邮箱具有的委派访问设置。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [AddDelegate 操作](adddelegate-operation.md)  
- [UpdateDelegate 操作](updatedelegate-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [添加代理人](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

