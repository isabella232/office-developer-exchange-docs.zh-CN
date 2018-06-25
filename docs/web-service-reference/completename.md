---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: CompleteName 元素均表示一个联系人的完整名称。
ms.openlocfilehash: 1f6c9ba68fe941f848d0e250a39aea6894fca61e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753464"
---
# <a name="completename"></a>CompleteName

**CompleteName**元素均表示一个联系人的完整名称。 
  
```xml
<CompleteName>
   <Title/>
   <FirstName/>
   <MiddleName/>
   <LastName/>
   <Suffix/>
   <Initials/>
   <FullName/>
   <Nickname/>
   <YomiFirstName/>
   <YomiLastName/>
</CompleteName>
```

 **CompleteNameType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Title](title.md) <br/> |代表联系人的标题。  <br/> |
|[FirstName](firstname.md) <br/> |代表联系人的名字。  <br/> |
|[MiddleName](middlename.md) <br/> |代表中间名的联系人。  <br/> |
|[姓氏](lastname.md) <br/> |代表最后一个联系人的姓名。  <br/> |
|[Suffix](suffix.md) <br/> |表示指向联系人的姓名的后缀。  <br/> |
|[首字母缩写](initials.md) <br/> |代表联系人的姓名缩写。  <br/> |
|[FullName](fullname.md) <br/> |代表联系人的完整名称。  <br/> |
|[昵称](nickname.md) <br/> |代表联系人的别名。  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |表示用于日语的第一个名称的可搜索或拼音拼写日本中使用的名称。  <br/> |
|[YomiLastName](yomilastname.md) <br/> |表示用于日语的最后一个名称的可搜索或拼音拼写日本中使用的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
   
## <a name="remarks"></a>备注

[CompleteName](completename.md)属性为[默认](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx)形状的一部分。 在 Microsoft Exchange Server 2007 的初始发行版本，由[GetItem 操作](getitem-operation.md)，但不是[FindItem 操作](finditem-operation.md)返回[CompleteName](completename.md)属性。 从 Exchange Server 2007 Service Pack 1 (SP1) 开始， [FindItem 操作](finditem-operation.md)也会返回与[默认](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx)形状的[CompleteName](completename.md)属性。 此更改不会影响架构。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
  
[CompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.ContactItemType.CompleteName.aspx)
  
[contactsCompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.UnindexedFieldURIType.contactsCompleteName.aspx)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

