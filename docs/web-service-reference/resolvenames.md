---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: ResolveNames 元素定义一个请求以解析不明确的名称。
ms.openlocfilehash: 9c36a5f84451f91e90a8e7148cf384b5cacd7f29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467947"
---
# <a name="resolvenames"></a>ResolveNames

**ResolveNames**元素定义一个请求以解析不明确的名称。 
  
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
|**ReturnFullContactData** <br/> |描述是否在响应中返回有关已解析名称的公用联系人的完整联系人详细信息。 此属性是公共联系人所必需的。 此值不影响私有联系人和私人通讯组列表，其[ItemId](itemid.md)始终返回。  <br/> |
|**SearchScope** <br/> |标识 ResolveNames 搜索的顺序和范围。  <br/> |
|ContactDataShape  <br/> |标识为联系人返回的属性集。 此属性是在 Exchange Server 2010 Service Pack 2 （SP2）中引入的。  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>ReturnFullContactData 属性值

|**值**|**说明**|
|:-----|:-----|
|True  <br/> |返回公用联系人的完整联系人详细信息。  <br/> |
|False  <br/> |不返回公用联系人的完整联系人详细信息。  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope 属性值

|**值**|**说明**|
|:-----|:-----|
|ActiveDirectory  <br/> |仅搜索 Active Directory 目录服务。  <br/> |
|ActiveDirectoryContacts  <br/> |首先搜索 Active Directory，然后在[ParentFolderIds](parentfolderids.md)属性中指定的联系人文件夹中进行搜索。  <br/> |
|联系人  <br/> |仅搜索由[ParentFolderIds](parentfolderids.md)属性标识的联系人文件夹。  <br/> |
|ContactsActiveDirectory  <br/> |首先搜索由[ParentFolderIds](parentfolderids.md)属性标识的联系人文件夹，然后搜索 Active Directory。  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>ContactDataShape 属性值

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |将返回 "联系人项目标识符" 属性。  <br/> |
|默认  <br/> |将返回默认的联系人项目属性集。 有关详细信息，请参阅[EWS 中的响应形状](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
|AllProperties  <br/> |将返回 AllProperties 的联系人项目属性集。 有关详细信息，请参阅[EWS 中的响应形状](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |包含联系人文件夹标识符的数组，如果将**SearchScope**属性设置为 ActiveDirectoryContacts、Contact 或 ContactsActiveDirectory，则会搜索这些标识符。 ParentFolderIds 数组仅可包含单个联系人文件夹标识符。 如果**ParentFolderIds**元素不存在，则会搜索默认的 "联系人" 文件夹。  <br/> 文件夹标识符可用于代理访问。  <br/> Active Directory 搜索通过使用访问控制列表（Acl）来执行。 某些用户可能没有查看某些 Active Directory 对象的权限。  <br/> 此元素为可选。  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |包含要解析的联系人或通讯组列表的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

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

