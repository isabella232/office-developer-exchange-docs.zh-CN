---
title: ContactSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContactSource
api_type:
- schema
ms.assetid: 500b0423-864e-4cde-a39b-6b5b06d1aa6a
description: ContactSource 元素描述联系人是位于 AD DS Exchange还是 Active Directory 域服务 (AD DS) 。
ms.openlocfilehash: 538739a47d257de90b961a2c4d391e95eae0d620
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536734"
---
# <a name="contactsource"></a>ContactSource

**ContactSource** 元素描述联系人是位于 AD DS Exchange还是 Active Directory 域服务 (AD DS) 。 
  
```xml
<ContactSource/>
```

 **ContactSourceType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[联系人](contact.md) <br/> |表示对 Exchange 存储中的联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
   
## <a name="text-value"></a>文本值

以下是此元素的可能值：
  
- ActiveDirectory
    
- 应用商店
    
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

