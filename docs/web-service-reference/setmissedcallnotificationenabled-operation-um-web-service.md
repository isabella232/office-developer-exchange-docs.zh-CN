---
title: SetMissedCallNotificationEnabled 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。
ms.openlocfilehash: ca4942942a81bc187e8e18a5e6f003f8587f79d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467394"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>SetMissedCallNotificationEnabled 操作（UM web 服务）

SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。
  
## <a name="setmissedcallnotificationenabled-request-example"></a>SetMissedCallNotificationEnabled 请求示例

### <a name="description"></a>Description

以下示例的 SetMissedCallNotificationEnabled 请求显示如何构成启用未接来电通知的请求。
  
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

下面的 PlayOnPhoneGreeting 响应示例显示对 SetMissedCallNotificationEnabled 请求的响应。
  
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



[SetMissedCallNotificationEnabled （UM web 服务）](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse （UM web 服务）](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status （UM web 服务-SetMissedCallNotificationEnabled）](status-um-web-servicesetmissedcallnotificationenabled.md)

