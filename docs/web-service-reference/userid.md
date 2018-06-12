---
title: UserId
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
description: UserId 元素标识委派用户或具有文件夹访问权限的用户。
ms.openlocfilehash: 8e9867f5a8cdd62dd2dae55fbf527595ac14f46d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838469"
---
# <a name="userid"></a>UserId

**UserId**元素标识委派用户或具有文件夹访问权限的用户。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SID](sid.md) <br/> |代表安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示用于代理访问的帐户的主要简单邮件传输协议 (SMTP) 地址。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义文件夹、 联系人、 通讯组列表或代理用户的显示名称。  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |标识匿名和默认代理访问的用户帐户。  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |标识外部委托用户或外部用户拥有文件夹访问权限。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |标识要添加或更新的邮箱中的单个委托。  <br/> |
|[权限](permission.md) <br/> |到文件夹定义用户拥有的访问权限。  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |定义日历文件夹的用户具有的访问权限。  <br/> |
|[UserIds](userids.md) <br/> |包含用于获取或删除主体的邮箱的委派用户的数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[AddDelegate 操作](adddelegate-operation.md)
  
[UpdateDelegate 操作](updatedelegate-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[添加代理人](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

