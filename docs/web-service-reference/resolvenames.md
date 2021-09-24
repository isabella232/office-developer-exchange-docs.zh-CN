---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: ResolveNames 元素定义解析不明确名称的请求。
ms.openlocfilehash: 8fbf933593b43de656bf8731aa86cc8c8eb76bb4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514142"
---
# <a name="resolvenames"></a>ResolveNames

**ResolveNames** 元素定义解析不明确名称的请求。 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |描述是否在响应中返回已解析名称的公共联系人的完整联系人详细信息。 公共联系人需要此属性。 此值不影响始终返回 [ItemId](itemid.md) 的私人联系人和专用通讯组列表。  <br/> |
|**SearchScope** <br/> |标识 ResolveNames 搜索的顺序和范围。  <br/> |
|ContactDataShape  <br/> |标识为联系人返回的属性集。 此属性是在 SP2 Exchange Server 2010 Service Pack 2 (中引入) 。  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>ReturnFullContactData 属性值

|**值**|**说明**|
|:-----|:-----|
|True  <br/> |返回公共联系人的完整联系人详细信息。  <br/> |
|错误  <br/> |不返回公共联系人的完整联系人详细信息。  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope 属性值

|**值**|**说明**|
|:-----|:-----|
|ActiveDirectory  <br/> |仅搜索 Active Directory 目录服务。  <br/> |
|ActiveDirectoryContacts  <br/> |首先搜索 Active Directory，然后搜索 [ParentFolderIds](parentfolderids.md) 属性中指定的联系人文件夹。  <br/> |
|联系人  <br/> |仅搜索由 [ParentFolderIds](parentfolderids.md) 属性标识的联系人文件夹。  <br/> |
|ContactsActiveDirectory  <br/> |首先搜索 [由 ParentFolderIds](parentfolderids.md) 属性标识的联系人文件夹，然后搜索 Active Directory。  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>ContactDataShape 属性值

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |返回联系人项目标识符属性。  <br/> |
|默认值  <br/> |返回默认的联系人项目属性集。 有关详细信息，请参阅 [EWS 中的响应形状](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
|AllProperties  <br/> |将返回联系人项目属性的 AllProperties 集合。 有关详细信息，请参阅 [EWS 中的响应形状](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |包含将 **SearchScope** 属性设置为 ActiveDirectoryContacts、Contacts 或 ContactsActiveDirectory 时将搜索的联系人文件夹标识符数组。 ParentFolderIds 数组只能包含一个联系人文件夹标识符。 如果 **ParentFolderIds** 元素不存在，则搜索默认的"联系人"文件夹。  <br/> 文件夹标识符可用于委派访问。  <br/> Active Directory 搜索通过使用访问控制列表和 ACL (执行) 。 某些用户可能没有查看某些 Active Directory 对象的权利。  <br/> 此元素为可选。  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |包含要解析的联系人或通讯组列表的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ResolveNames 操作](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[使用名称解析](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

