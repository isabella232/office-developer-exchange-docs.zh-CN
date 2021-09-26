---
title: SetTelephoneAccessFolderEmail 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: SetTelephoneAccessFolderEmail 操作设置统一消息通过电话将邮件读回给用户的文件夹。
ms.openlocfilehash: cf8e80e021d6467ba3a724cc0d04e165e00e8397
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544715"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>SetTelephoneAccessFolderEmail 操作（UM Web 服务）

SetTelephoneAccessFolderEmail 操作设置统一消息通过电话将邮件读回给用户的文件夹。
  
## <a name="settelephoneaccessfolderemail-request-example"></a>SetTelephoneAccessFolderEmail 请求示例

### <a name="description"></a>说明

SetTelephoneAccessFolderEmail 请求的以下示例显示如何形成请求，以设置统一消息通过电话向用户重新读取的文件夹。
  
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

SetTelephoneAccessFolderEmail 响应的以下示例显示对 SetTelephoneAccessFolderEmail 请求的响应。
  
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



[SetTelephoneAccessFolderEmail（UM Web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse（UM Web 服务）](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId（UM Web 服务）](base64folderid-um-web-service.md)

