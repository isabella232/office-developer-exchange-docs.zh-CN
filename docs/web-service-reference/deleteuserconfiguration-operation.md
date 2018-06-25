---
title: DeleteUserConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfiguration
api_type:
- schema
ms.assetid: 93e44690-be2d-4fdb-96a8-4ded3c193aed
description: DeleteUserConfiguration 操作中删除用户配置对象的文件夹。
ms.openlocfilehash: 033134a7e16aa8e7a3d6b928141012b646863a68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753817"
---
# <a name="deleteuserconfiguration-operation"></a><span data-ttu-id="6cb63-103">DeleteUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="6cb63-103">DeleteUserConfiguration operation</span></span>

<span data-ttu-id="6cb63-104">**DeleteUserConfiguration**操作中删除用户配置对象的文件夹。</span><span class="sxs-lookup"><span data-stu-id="6cb63-104">The **DeleteUserConfiguration** operation deletes a user configuration object on a folder.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6cb63-105">**DeleteUserConfiguration**操作将触发事件通知系统移动的事件。</span><span class="sxs-lookup"><span data-stu-id="6cb63-105">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="6cb63-106">用户配置对象将移至转储程序。</span><span class="sxs-lookup"><span data-stu-id="6cb63-106">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="deleteuserconfiguration-request-example"></a><span data-ttu-id="6cb63-107">DeleteUserConfiguration 请求示例</span><span class="sxs-lookup"><span data-stu-id="6cb63-107">DeleteUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="6cb63-108">说明</span><span class="sxs-lookup"><span data-stu-id="6cb63-108">Description</span></span>

<span data-ttu-id="6cb63-109">**DeleteUserConfiguration**请求的下面的示例演示如何窗体上草稿文件夹的用户配置对象删除的请求。</span><span class="sxs-lookup"><span data-stu-id="6cb63-109">The following example of a **DeleteUserConfiguration** request shows how to form a request to delete a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6cb63-110">代码</span><span class="sxs-lookup"><span data-stu-id="6cb63-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:DeleteUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts"/>
      </m:UserConfigurationName>
    </m:DeleteUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="deleteuserconfiguration-response-example"></a><span data-ttu-id="6cb63-111">DeleteUserConfiguration 响应示例</span><span class="sxs-lookup"><span data-stu-id="6cb63-111">DeleteUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="6cb63-112">说明</span><span class="sxs-lookup"><span data-stu-id="6cb63-112">Description</span></span>

<span data-ttu-id="6cb63-113">下面的示例演示对**DeleteUserConfiguration**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="6cb63-113">The following example shows a successful response to the **DeleteUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6cb63-114">代码</span><span class="sxs-lookup"><span data-stu-id="6cb63-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteUserConfigurationResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:DeleteUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6cb63-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6cb63-115">See also</span></span>

- [<span data-ttu-id="6cb63-116">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="6cb63-116">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="6cb63-117">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6cb63-117">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

