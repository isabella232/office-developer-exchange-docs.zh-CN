---
title: SetTelephoneAccessFolderEmail 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: SetTelephoneAccessFolderEmail 操作设置一个文件夹，统一消息将从该文件夹中通过电话将邮件读回用户。
ms.openlocfilehash: a2bb630f812ca811b4cbe68db1308dc18e5d3ba0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467331"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>SetTelephoneAccessFolderEmail 操作（UM web 服务）

SetTelephoneAccessFolderEmail 操作设置一个文件夹，统一消息将从该文件夹中通过电话将邮件读回用户。
  
## <a name="settelephoneaccessfolderemail-request-example"></a>SetTelephoneAccessFolderEmail 请求示例

### <a name="description"></a>说明

以下示例的 SetTelephoneAccessFolderEmail 请求显示如何形成一个请求，以设置通过电话将统一消息从其读取到用户的文件夹。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>成功的 SetTelephoneAccessFolderEmail 响应示例

### <a name="description"></a>说明

下面的 SetTelephoneAccessFolderEmail 响应示例显示对 SetTelephoneAccessFolderEmail 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[SetTelephoneAccessFolderEmail （UM web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse （UM web 服务）](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId （UM web 服务）](base64folderid-um-web-service.md)

