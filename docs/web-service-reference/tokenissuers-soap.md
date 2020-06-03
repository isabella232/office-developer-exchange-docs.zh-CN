---
title: TokenIssuers （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: TokenIssuers 元素表示 TokenIssuer （SOAP）集合。
ms.openlocfilehash: 352487ad3fd9c1ee7de756a109fb98a49d0cdcd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457072"
---
# <a name="tokenissuers-soap"></a>TokenIssuers （SOAP）

**TokenIssuers**元素表示[TokenIssuer （SOAP）](tokenissuer-soap.md)集合。 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[TokenIssuer （SOAP）](tokenissuer-soap.md) <br/> |指定安全令牌服务的[Uri （soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md) 。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationResponse （SOAP）](getfederationinformationresponse-soap.md) <br/> |包含[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)响应。  <br/> |
   
## <a name="remarks"></a>备注

**TokenIssuers**表示要在自动发现中使用的[TokenIssuer （SOAP）](tokenissuer-soap.md)元素的集合。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

