---
title: 联系人 (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: 联系人元素指定在统一联系人存储库中的联系人。
ms.openlocfilehash: f1593da78a46851c7db43abc567eb66c0c74e0f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753494"
---
# <a name="contact-contacttype"></a>联系人 (ContactType)

**联系人**元素指定统一联系人存储库中的联系人。 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 **ContactType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |指定某人的姓名。  <br/> |
|[BusinessName](businessname.md) <br/> |指定业务的名称。  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |表示联系人的电话号码的集合。  <br/> |
|[Urls](urls.md) <br/> |指定的 Url 为角色外的数组。  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |指定数组提取电子邮件地址。  <br/> |
|[地址 (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |指定**地址**元素的数组。  <br/> |
|[ContactString](contactstring.md) <br/> |指定联系人的显示名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[联系人 (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |指定联系人的数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

