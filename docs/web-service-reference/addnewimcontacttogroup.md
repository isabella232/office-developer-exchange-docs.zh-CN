---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: AddNewImContactToGroup 元素定义向即时消息组添加新即时消息联系人的请求。
ms.openlocfilehash: 48d4fe37964a2851a32398425ed4fbd5d5d4f77d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541565"
---
# <a name="addnewimcontacttogroup"></a>AddNewImContactToGroup

**AddNewImContactToGroup** 元素定义向即时消息组添加新即时消息联系人的请求。 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 **AddNewImContactToGroupType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ImAddress (NonEmptyStringType) ](imaddress-nonemptystringtype.md)  | [DisplayName (NonEmptyStringType) ](displayname-nonemptystringtype.md)  | [GroupId](groupid.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

