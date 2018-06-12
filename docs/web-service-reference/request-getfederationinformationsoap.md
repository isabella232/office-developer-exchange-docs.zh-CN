---
title: 请求 (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: 请求元素均表示一个 GetFederationInformationRequest (SOAP) 请求。
ms.openlocfilehash: 0fb9301c2f318aa2c27155675dd3c43b41aabecd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827119"
---
# <a name="request-getfederationinformation-soap"></a>请求 (GetFederationInformation) (SOAP)

**请求**元素均表示一个[GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md)请求。 
  
```XML
<Request>
   <Domain/>
</Request>
```

 **GetFederationInformationRequest**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域 (GetFederationInformation) (SOAP)](domain-getfederationinformationsoap.md) <br/> |标识了联合身份验证信任的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationRequestMessage (SOAP)](getfederationinformationrequestmessage-soap.md) <br/> |为安全令牌服务 (STS) 准备调用请求配置数据的服务器。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[使用自动发现](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

