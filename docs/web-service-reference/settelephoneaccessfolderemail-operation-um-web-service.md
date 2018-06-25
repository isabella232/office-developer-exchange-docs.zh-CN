---
title: SetTelephoneAccessFolderEmail 操作 （UM web 服务）
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
description: SetTelephoneAccessFolderEmail 操作设置从其中统一消息将读取后邮件向用户通过电话的文件夹。
ms.openlocfilehash: 9497e58f66b8efcf7e358aa529223942298a3bed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827459"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a><span data-ttu-id="05cbd-103">SetTelephoneAccessFolderEmail 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="05cbd-103">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>

<span data-ttu-id="05cbd-104">SetTelephoneAccessFolderEmail 操作设置从其中统一消息将读取后邮件向用户通过电话的文件夹。</span><span class="sxs-lookup"><span data-stu-id="05cbd-104">The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.</span></span>
  
## <a name="settelephoneaccessfolderemail-request-example"></a><span data-ttu-id="05cbd-105">SetTelephoneAccessFolderEmail 请求示例</span><span class="sxs-lookup"><span data-stu-id="05cbd-105">SetTelephoneAccessFolderEmail request example</span></span>

### <a name="description"></a><span data-ttu-id="05cbd-106">说明</span><span class="sxs-lookup"><span data-stu-id="05cbd-106">Description</span></span>

<span data-ttu-id="05cbd-107">SetTelephoneAccessFolderEmail 请求的下面的示例演示如何以形成一个请求来设置从其中统一消息将读取回用户通过电话的文件夹。</span><span class="sxs-lookup"><span data-stu-id="05cbd-107">The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="05cbd-108">代码</span><span class="sxs-lookup"><span data-stu-id="05cbd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a><span data-ttu-id="05cbd-109">成功 SetTelephoneAccessFolderEmail 响应示例</span><span class="sxs-lookup"><span data-stu-id="05cbd-109">Successful SetTelephoneAccessFolderEmail response example</span></span>

### <a name="description"></a><span data-ttu-id="05cbd-110">说明</span><span class="sxs-lookup"><span data-stu-id="05cbd-110">Description</span></span>

<span data-ttu-id="05cbd-111">SetTelephoneAccessFolderEmail 响应的下面的示例演示 SetTelephoneAccessFolderEmail 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="05cbd-111">The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.</span></span>
  
### <a name="code"></a><span data-ttu-id="05cbd-112">代码</span><span class="sxs-lookup"><span data-stu-id="05cbd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="05cbd-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05cbd-113">See also</span></span>



[<span data-ttu-id="05cbd-114">SetTelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="05cbd-114">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="05cbd-115">SetTelephoneAccessFolderEmailResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="05cbd-115">SetTelephoneAccessFolderEmailResponse (UM web service)</span></span>](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[<span data-ttu-id="05cbd-116">base64FolderId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="05cbd-116">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)

