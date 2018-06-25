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
description: ResolveNames 元素定义请求解析模糊名称。
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827172"
---
# <a name="resolvenames"></a>ResolveNames

**ResolveNames**元素定义请求解析模糊名称。 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |描述是否在响应中返回解析名称的公共联系人的完整联系人详细信息。 此属性是必需的公共联系人。 专用的联系人和私人通讯组列表，则始终返回[ItemId](itemid.md) ，就不会影响此值。  <br/> |
|**SearchScope** <br/> |标识的顺序和 ResolveNames 搜索范围。  <br/> |
|ContactDataShape  <br/> |标识设置联系人返回的属性。 此属性是在 Exchange Server 2010 Service Pack 2 (SP2) 中引入的。  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>ReturnFullContactData 属性值

|**值**|**说明**|
|:-----|:-----|
|True  <br/> |返回公共联系人的完整联系人详细信息。  <br/> |
|False  <br/> |不返回公共联系人的完整联系人详细信息。  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope 属性值

|**值**|**说明**|
|:-----|:-----|
|与 active Directory  <br/> |搜索仅 Active Directory 目录服务。  <br/> |
|ActiveDirectoryContacts  <br/> |首先，搜索 active Directory，然后搜索[ParentFolderIds](parentfolderids.md)属性中指定的联系人文件夹。  <br/> |
|联系人  <br/> |仅由[ParentFolderIds](parentfolderids.md)属性标识的联系人的文件夹中搜索。  <br/> |
|ContactsActiveDirectory  <br/> |先搜索联系人由[ParentFolderIds](parentfolderids.md)属性标识的文件夹，然后搜索 Active Directory。  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>ContactDataShape 属性值

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |联系人项目标识符属性返回。  <br/> |
|默认  <br/> |返回默认的联系人项属性集。 有关详细信息，请参阅[响应形状中的 ews](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
|AllProperties  <br/> |返回了 AllProperties 一组联系人项目属性。 有关详细信息，请参阅[响应形状中的 ews](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |包含**SearchScope**属性设置为 ActiveDirectoryContacts、 联系人或 ContactsActiveDirectory 将搜索的联系人文件夹标识符的数组。 ParentFolderIds 数组只能包含单个联系人文件夹标识符。 如果**ParentFolderIds**元素不存在，则搜索默认联系人文件夹。  <br/> 文件夹标识符可用于代理访问。  <br/> 使用访问控制列表 (Acl) 执行 active Directory 搜索。 某些用户可能没有看到某些 Active Directory 对象的权限。  <br/> 此元素是可选的。  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |包含要解析的联系人或通讯组列表的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ResolveNames 操作](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[使用名称解析](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

