---
title: UserID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: UserId 元素标识委派用户或具有文件夹访问权限的用户。
ms.openlocfilehash: f03914745f8f7f47c64685b3e7c52eefece5ff6d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510755"
---
# <a name="userid"></a>UserID

**UserId** 元素标识委派用户或具有文件夹访问权限的用户。 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 **UserIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SID](sid.md) <br/> |表示安全描述符定义语言 (SID) 安全标识符 (SDDL) 。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |代表要用于委派 () 帐户的主简单邮件传输协议或 SMTP 地址。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义显示名称、联系人、通讯组列表或代理用户的列表。  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |标识委派访问的匿名和默认用户帐户。  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |标识具有文件夹访问权限的外部委派用户或外部用户。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |标识要添加或更新邮箱中的单个代理。  <br/> |
|[权限](permission.md) <br/> |到文件夹定义用户拥有的访问权限。  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |定义日历文件夹的用户具有的访问权限。  <br/> |
|[UserIds](userids.md) <br/> |包含要从主体邮箱获取或删除的委派用户数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[AddDelegate 操作](adddelegate-operation.md)
  
[UpdateDelegate 操作](updatedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[添加代理人](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

