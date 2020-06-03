---
title: UserID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: UserId 元素标识的代理用户或具有文件夹访问权限的用户。
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455539"
---
# <a name="userid"></a>UserID

**UserId**元素标识的代理用户或具有文件夹访问权限的用户。 
  
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
|[SID](sid.md) <br/> |表示安全标识符（SID）的安全描述符定义语言（SDDL）形式。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示要用于代理访问的帐户的主要简单邮件传输协议（SMTP）地址。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义文件夹、联系人、通讯组列表或代理用户的显示名称。  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |标识代理访问的匿名和默认用户帐户。  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |标识具有文件夹访问权限的外部代理用户或外部用户。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |标识要在邮箱中添加或更新的单个代理。  <br/> |
|[权限](permission.md) <br/> |到文件夹定义用户拥有的访问权限。  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |定义日历文件夹的用户具有的访问权限。  <br/> |
|[UserIds](userids.md) <br/> |包含要从主体邮箱中获取或删除的委派用户的数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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


[添加委派](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

