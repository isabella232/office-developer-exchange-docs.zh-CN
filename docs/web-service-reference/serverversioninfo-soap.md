---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: ServerVersionInfo 元素包含处理请求的服务器的版本。
ms.openlocfilehash: ac52b3eda429e65cb1ec046167a63fe4029d423a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521451"
---
# <a name="serverversioninfo-soap"></a>ServerVersionInfo (SOAP)

**ServerVersionInfo** 元素包含处理请求的服务器的版本。 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 **ServerVersionInfo**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MajorVersion (SOAP)](majorversion-soap.md) <br/> |服务器的主要版本号。  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |服务器的次要版本号。  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |服务器的主要内部版本号。  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |服务器的次要内部版本号。  <br/> |
|[Version (SOAP)](version-soap.md) <br/> |服务器产品版本的说明。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

此元素在 SOAP 标头中返回。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

