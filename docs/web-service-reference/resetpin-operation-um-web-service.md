---
title: ResetPIN 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: ResetPIN 操作将 TUI 密码 (PIN) 一个新的随机值。
ms.openlocfilehash: 12f1e5719184df84f6c29ab3d02cc362f87abc76
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539106"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN 操作（UM Web 服务）

ResetPIN 操作将 TUI 密码 (PIN) 一个新的随机值。
  
## <a name="remarks"></a>注解

ResetPIN 操作基于 PIN 策略创建新的 PIN。 如果操作成功，则包含新 PIN 的电子邮件将发送到用户的邮箱。 如果操作失败，它将引发包含有关失败信息的异常。
  
## <a name="resetpin-request-example"></a>ResetPIN 请求示例

### <a name="description"></a>说明

ResetPIN 请求的以下示例显示如何形成重置邮箱 PIN 的请求。
  
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

以下 ResetPIN 响应示例显示对 ResetPIN 请求的响应。
  
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



[ResetPIN（UM Web 服务）](resetpin-um-web-service.md)
  
[ResetPINResponse（UM Web 服务）](resetpinresponse-um-web-service.md)

