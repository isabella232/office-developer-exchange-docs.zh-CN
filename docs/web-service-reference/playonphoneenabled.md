---
title: PlayOnPhoneEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PlayOnPhoneEnabled
api_type:
- schema
ms.assetid: 6f800912-be4c-46f9-aa1e-dff0bbf877c5
description: PlayOnPhoneEnabled 元素指示是否启用"电话播放"功能。
ms.openlocfilehash: ebbcea0d055b8cdc869f468295eb20396caa99fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516515"
---
# <a name="playonphoneenabled"></a>PlayOnPhoneEnabled

**PlayOnPhoneEnabled** 元素指示是否启用"电话播放"功能。 
  
```XML
<PlayOnPhoneEnabled>true | false</PlayOnPhoneEnabled>
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
|[UnifiedMessagingConfiguration](unifiedmessagingconfiguration.md) <br/> |包含统一消息服务的配置信息。  <br/> |
   
## <a name="text-value"></a>文本值

如果为帐户启用了"在电话上播放"，则 **PlayOnPhoneEnabled** 元素的值为 **true;** 否则，值为 **false**。
  
## <a name="remarks"></a>注解

此元素是必需的。
  
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

