---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: CompleteName 元素表示联系人的完整名称。
ms.openlocfilehash: 873d372657089d21e86025cdf7812659ac505491
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543553"
---
# <a name="completename"></a>CompleteName

**CompleteName** 元素表示联系人的完整名称。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Title](title.md) <br/> |表示联系人的标题。  <br/> |
|[FirstName](firstname.md) <br/> |表示联系人的名字。  <br/> |
|[MiddleName](middlename.md) <br/> |表示联系人的中间名。  <br/> |
|[LastName](lastname.md) <br/> |表示联系人的姓氏。  <br/> |
|[后缀](suffix.md) <br/> |表示联系人姓名的后缀。  <br/> |
|[缩写](initials.md) <br/> |表示联系人的缩写。  <br/> |
|[FullName](fullname.md) <br/> |表示联系人的全名。  <br/> |
|[Nickname](nickname.md) <br/> |表示联系人的昵称。  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |表示用于日语名字的可搜索或拼音拼写的日本名称。  <br/> |
|[YomiLastName](yomilastname.md) <br/> |表示用于日语姓氏的可搜索或拼音拼写的日本名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
   
## <a name="remarks"></a>说明

CompleteName 属性是默认形状 [的一](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) 部分。 在 2007 Microsoft Exchange Server版本中[，CompleteName](getitem-operation.md)属性由 GetItem 操作返回，而不是[由 FindItem 操作返回](finditem-operation.md)。 从 Exchange Server 2007 Service Pack 1 (SP1) 开始[，FindItem 操作](finditem-operation.md)还返回具有["](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy)默认"形状的 CompleteName 属性。 此更改不会影响架构。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

