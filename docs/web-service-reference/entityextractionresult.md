---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: EntityExtractionResult 元素指定项目的 EntityExtractionResult 属性。
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754139"
---
# <a name="entityextractionresult"></a>EntityExtractionResult

**EntityExtractionResult**元素指定项目的**EntityExtractionResult**属性。 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 **EntityExtractionResultType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[地址 (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |指定**AddressEntity**元素的数组。  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |指定**MeetingSuggestion**元素的数组。  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |指定**TaskSuggestion**元素的数组。  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |指定电子邮件地址实体的数组。  <br/> |
|[联系人 (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |指定联系人的数组。  <br/> |
|[Url (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |指定的 Url 的数组。  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |指定电话号码的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Item](item.md) <br/> |表示 Exchange 存储中的泛型项。  <br/> |
   
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

