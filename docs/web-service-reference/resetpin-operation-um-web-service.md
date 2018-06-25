---
title: ResetPIN 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: ResetPIN 操作更改为新的随机值的 PIN （TUI 密码）。
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827146"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN 操作 （UM web 服务）

ResetPIN 操作更改为新的随机值的 PIN （TUI 密码）。
  
## <a name="remarks"></a>注解

ResetPIN 操作创建一个新的 PIN，基于 PIN 策略。 如果操作成功，对邮箱的用户发送电子邮件包含新的 PIN。 如果操作失败，它将引发异常，其中包含有关失败情况的信息。
  
## <a name="resetpin-request-example"></a>ResetPIN 请求示例

### <a name="description"></a>说明

ResetPIN 请求的下面的示例演示如何以形成请求重置邮箱的 PIN。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>成功 ResetPIN 响应示例

### <a name="description"></a>说明

ResetPIN 响应的下面的示例演示 ResetPIN 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[ResetPIN （UM web 服务）](resetpin-um-web-service.md)
  
[ResetPINResponse （UM web 服务）](resetpinresponse-um-web-service.md)

