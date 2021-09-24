---
title: ServerVersionInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: ServerVersionInfo 元素表示Microsoft Exchange Server版本号。
ms.openlocfilehash: 6907559e1ac98981028a017b64a38a343c36da70
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517712"
---
# <a name="serverversioninfo"></a>ServerVersionInfo

**ServerVersionInfo** 元素表示Microsoft Exchange Server版本号。 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|MajorVersion  <br/> |描述主要版本号。  <br/> |
|MinorVersion  <br/> |描述次要版本号。  <br/> |
|MajorBuildNumber  <br/> |描述主内部版本编号。  <br/> |
|MinorBuildNumber  <br/> |描述次要内部版本号。  <br/> |
|版本  <br/> |介绍 Exchange EWS (EWS) 版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

此元素在 Web 服务响应消息的 SOAP Exchange返回。
  
描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

