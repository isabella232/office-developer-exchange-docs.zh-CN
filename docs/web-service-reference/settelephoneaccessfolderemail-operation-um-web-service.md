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
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a><span data-ttu-id="8805c-103">SetTelephoneAccessFolderEmail 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="8805c-103">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>

<span data-ttu-id="8805c-104">SetTelephoneAccessFolderEmail 操作设置一个文件夹，统一消息将从该文件夹中通过电话将邮件读回用户。</span><span class="sxs-lookup"><span data-stu-id="8805c-104">The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.</span></span>
  
## <a name="settelephoneaccessfolderemail-request-example"></a><span data-ttu-id="8805c-105">SetTelephoneAccessFolderEmail 请求示例</span><span class="sxs-lookup"><span data-stu-id="8805c-105">SetTelephoneAccessFolderEmail request example</span></span>

### <a name="description"></a><span data-ttu-id="8805c-106">说明</span><span class="sxs-lookup"><span data-stu-id="8805c-106">Description</span></span>

<span data-ttu-id="8805c-107">以下示例的 SetTelephoneAccessFolderEmail 请求显示如何形成一个请求，以设置通过电话将统一消息从其读取到用户的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8805c-107">The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="8805c-108">代码</span><span class="sxs-lookup"><span data-stu-id="8805c-108">Code</span></span>

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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a><span data-ttu-id="8805c-109">成功的 SetTelephoneAccessFolderEmail 响应示例</span><span class="sxs-lookup"><span data-stu-id="8805c-109">Successful SetTelephoneAccessFolderEmail response example</span></span>

### <a name="description"></a><span data-ttu-id="8805c-110">说明</span><span class="sxs-lookup"><span data-stu-id="8805c-110">Description</span></span>

<span data-ttu-id="8805c-111">下面的 SetTelephoneAccessFolderEmail 响应示例显示对 SetTelephoneAccessFolderEmail 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="8805c-111">The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.</span></span>
  
### <a name="code"></a><span data-ttu-id="8805c-112">代码</span><span class="sxs-lookup"><span data-stu-id="8805c-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="8805c-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8805c-113">See also</span></span>



[<span data-ttu-id="8805c-114">SetTelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="8805c-114">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="8805c-115">SetTelephoneAccessFolderEmailResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="8805c-115">SetTelephoneAccessFolderEmailResponse (UM web service)</span></span>](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[<span data-ttu-id="8805c-116">base64FolderId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="8805c-116">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)

