---
title: SetMissedCallNotificationEnabled 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。
ms.openlocfilehash: 31f59887041aac02e5876b596931902373870203
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521415"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>SetMissedCallNotificationEnabled 操作（UM Web 服务）

SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。
  
## <a name="setmissedcallnotificationenabled-request-example"></a>SetMissedCallNotificationEnabled 请求示例

### <a name="description"></a>Description

SetMissedCallNotificationEnabled 请求的以下示例显示如何形成请求以启用未接来电通知。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>成功的 SetMissedCallNotificationEnabled 响应示例

### <a name="description"></a>Description

PlayOnPhoneGreeting 响应的以下示例显示对 SetMissedCallNotificationEnabled 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[SetMissedCallNotificationEnabled（UM Web 服务）](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse（UM Web 服务）](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status（UM Web 服务 - SetMissedCallNotificationEnabled）](status-um-web-servicesetmissedcallnotificationenabled.md)

