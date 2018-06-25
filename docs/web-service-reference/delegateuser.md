---
title: DelegateUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: DelegateUser 元素标识要添加或更新的邮箱中的单个委托或委托管理响应中返回的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 72ddc313a5a76cd0345918cad63b7775ff85026b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753780"
---
# <a name="delegateuser"></a>DelegateUser

**DelegateUser**元素标识要添加或更新的邮箱中的单个委托或委托管理响应中返回的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[用户 Id](userid.md) <br/> |标识该委托。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |包含委派权限级别设置。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |指示是否代理接收发往主体的会议相关邮件的副本。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |指示代理人是否有权查看的主体的邮箱中的个人日历项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |包含代理人来添加或更新的邮箱中的标识。  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |包含委派管理操作的响应消息。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [AddDelegate 操作](adddelegate-operation.md) 
- [UpdateDelegate 操作](updatedelegate-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [添加代理人](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

