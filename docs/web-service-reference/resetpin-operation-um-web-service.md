---
title: ResetPIN 操作（UM web 服务）
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
description: ResetPIN 操作将 PIN （TUI 密码）更改为新的随机值。
ms.openlocfilehash: 8de64ce7a47e9c426f8eb9298e1ca00508fb616c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465490"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN 操作（UM web 服务）

ResetPIN 操作将 PIN （TUI 密码）更改为新的随机值。
  
## <a name="remarks"></a>备注

ResetPIN 操作根据 PIN 策略创建新 PIN。 如果操作成功，则会将包含新 PIN 的电子邮件发送到用户的邮箱。 如果操作失败，它将引发一个异常，其中包含有关失败的信息。
  
## <a name="resetpin-request-example"></a>ResetPIN 请求示例

### <a name="description"></a>说明

以下示例的 ResetPIN 请求显示如何形成一个重置邮箱的 PIN 的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>成功的 ResetPIN 响应示例

### <a name="description"></a>说明

下面的 ResetPIN 响应示例显示对 ResetPIN 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[ResetPIN （UM web 服务）](resetpin-um-web-service.md)
  
[ResetPINResponse （UM web 服务）](resetpinresponse-um-web-service.md)

