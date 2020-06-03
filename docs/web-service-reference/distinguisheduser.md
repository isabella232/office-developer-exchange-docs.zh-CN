---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: DistinguishedUser 元素标识代理访问的匿名帐户和默认用户帐户。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 922c36251290d7090cdafbed9e570144593ca97e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530731"
---
# <a name="distinguisheduser"></a>DistinguishedUser

**DistinguishedUser**元素标识代理访问的匿名帐户和默认用户帐户。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
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
|[UserId](userid.md) <br/> |标识代理用户或具有文件夹访问权限的用户。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

**默认**的文本值描述了为添加到主体邮箱的用户委派用户的默认设置。 "**匿名**" 文本值描述匿名用户对主体邮箱的代理访问设置。 
  
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
- [添加委派](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

