---
title: 请求（GetFederationInformation）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: Request 元素表示 GetFederationInformationRequest （SOAP）请求。
ms.openlocfilehash: dbd88537d03f6325cf0025d08c63ae486544d705
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459579"
---
# <a name="request-getfederationinformation-soap"></a>请求（GetFederationInformation）（SOAP）

**Request**元素表示[GetFederationInformationRequest （SOAP）](getfederationinformationrequest-soap.md)请求。 
  
```XML
<Request>
   <Domain/>
</Request>
```

 **GetFederationInformationRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Domain （GetFederationInformation）（SOAP）](domain-getfederationinformationsoap.md) <br/> |标识具有联合身份验证信任的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationRequestMessage （SOAP）](getfederationinformationrequestmessage-soap.md) <br/> |准备对服务器的调用，以请求安全令牌服务（STS）的配置数据。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[使用自动发现](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

