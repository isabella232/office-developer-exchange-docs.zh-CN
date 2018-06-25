---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: TokenIssuers 元素表示 TokenIssuer (SOAP) 集合。
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838256"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

**TokenIssuers**元素表示[TokenIssuer (SOAP)](tokenissuer-soap.md)集合。 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |指定安全令牌服务的[Uri (SOAP)](uri-soap.md)和[终结点 (SOAP)](endpoint-soap.md) 。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应。  <br/> |
   
## <a name="remarks"></a>注解

**TokenIssuers**代表[TokenIssuer (SOAP)](tokenissuer-soap.md)元素，用于自动发现的集合。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

