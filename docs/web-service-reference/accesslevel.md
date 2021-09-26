---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: AccessLevel 元素指定联机会议的访问级别。
ms.openlocfilehash: f1c85579affe7d1142b22a890808bceeb8f82d38
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544414"
---
# <a name="accesslevel"></a>AccessLevel

**AccessLevel** 元素指定联机会议的访问级别。 
  
```XML
<AccessLevel/>
```

 **OnlineMeetingSettingsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |指定联机会议的设置。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **AccessLevel** 元素的文本值。 
  
**AccessLevel 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|所有人  <br/> |访问级别对全部开放。  <br/> |
|内部  <br/> |访问级别仅为内部级别。  <br/> |
|受邀  <br/> |访问级别仅为受邀参与者。  <br/> |
|已锁定  <br/> |访问级别已锁定。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2013 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

