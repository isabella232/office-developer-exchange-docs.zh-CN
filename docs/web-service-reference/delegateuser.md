---
title: DelegateUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: DelegateUser 元素标识在邮箱中添加或更新的单个代理，或在委派管理响应中返回的代理。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 1963bef64e32ff536f0544a03f019e7785bae4d0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510252"
---
# <a name="delegateuser"></a>DelegateUser

**DelegateUser 元素** 标识在邮箱中添加或更新的单个代理，或在委派管理响应中返回的代理。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

**DelegateUserType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserId](userid.md) <br/> |标识代理。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |包含委派权限级别设置。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |指示代理是否接收发送给主体的会议相关邮件的副本。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |指示代理是否有权查看主体邮箱中的私人日历项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |包含要添加或更新到邮箱中的代理的标识。  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |包含用于委派管理操作的响应消息。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
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

