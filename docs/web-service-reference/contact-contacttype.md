---
title: Contact （ContactType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: Contact 元素指定统一联系人存储库中的联系人。
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461518"
---
# <a name="contact-contacttype"></a>Contact （ContactType）

**Contact**元素指定统一联系人存储库中的联系人。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Contact.personname](personname.md) <br/> |指定个人的名称。  <br/> |
|[BusinessName](businessname.md) <br/> |指定企业的名称。  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |表示联系人的电话号码的集合。  <br/> |
|[Urls](urls.md) <br/> |指定角色的 Url 数组。  <br/> |
|[EmailAddresses （ArrayOfExtractedEmailAddresses）](emailaddresses-arrayofextractedemailaddresses.md) <br/> |指定已提取的电子邮件地址数组。  <br/> |
|[地址（ArrayOfAddressesType）](addresses-arrayofaddressestype.md) <br/> |指定**Address**元素的数组。  <br/> |
|[ContactString](contactstring.md) <br/> |指定联系人的显示名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[联系人（ArrayOfContactsType）](contacts-arrayofcontactstype.md) <br/> |指定联系人数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

