---
title: IsModerated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: IsModerated 元素指示是否正在对收件人的邮箱进行主持。
ms.openlocfilehash: e06e7e01e08cb8418adafaae09cae94ceb5c3b2c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522899"
---
# <a name="ismoderated"></a>IsModerated

**IsModerated** 元素指示是否正在对收件人的邮箱进行主持。 
  
```XML
<IsModerated>true | false</IsModerated>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[邮件提示](mailtips.md) <br/> |表示各种类型的邮件提示的值。  <br/> |
   
## <a name="text-value"></a>文本值

如果收件人的邮箱正在接受 **主持** ，则此元素的文本值为 true。 如果收件人的邮箱未进行主持，则值为 **false。** 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

