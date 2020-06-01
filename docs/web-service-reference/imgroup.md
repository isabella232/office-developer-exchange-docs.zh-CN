---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: ImGroup 元素表示即时消息组。
ms.openlocfilehash: a0ff3fcb82e7f18837af5a6f5daa16e90043034d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460685"
---
# <a name="imgroup"></a>ImGroup

**ImGroup**元素表示即时消息组。 
  
```XML
<ImGroup>
   <DisplayName/>
   <GroupType/>
   <ExchangeStoreId/>
   <MemberCorrelationKey/>
   <ExtendedProperties/>
   <SmtpAddress/>
</ImGroup>
```

 **ImGroupType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[DisplayName （NonEmptyStringType）](displayname-nonemptystringtype.md)  | [GroupType](grouptype.md)  | [ExchangeStoreId](exchangestoreid.md)  | [MemberCorrelationKey](membercorrelationkey.md)  | [ExtendedProperties （NonEmptyArrayOfExtendedPropertyType）](extendedproperties-nonemptyarrayofextendedpropertytype.md)  | [SmtpAddress](smtpaddress.md)
  
### <a name="parent-elements"></a>父元素

[组（ArrayOfImGroupType）](groups-arrayofimgrouptype.md)  | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  | [AddImGroupResponse](addimgroupresponse.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

