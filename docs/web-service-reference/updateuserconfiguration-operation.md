---
title: UpdateUserConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateUserConfiguration
api_type:
- schema
ms.assetid: eda73b62-6a3a-43ae-8fd9-f30892811f27
description: UpdateUserConfiguration 操作将更新文件夹上的用户配置对象。
ms.openlocfilehash: 95fe6518fa30104463ec7f0aec8f786183eb513b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468542"
---
# <a name="updateuserconfiguration-operation"></a><span data-ttu-id="dced1-103">UpdateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="dced1-103">UpdateUserConfiguration operation</span></span>

<span data-ttu-id="dced1-104">**UpdateUserConfiguration**操作将更新文件夹上的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="dced1-104">The **UpdateUserConfiguration** operation updates a user configuration object on a folder.</span></span> 
  
## <a name="updateuserconfiguration-request-example"></a><span data-ttu-id="dced1-105">UpdateUserConfiguration 请求示例</span><span class="sxs-lookup"><span data-stu-id="dced1-105">UpdateUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="dced1-106">Description</span><span class="sxs-lookup"><span data-stu-id="dced1-106">Description</span></span>

<span data-ttu-id="dced1-107">以下示例的**UpdateUserConfiguration**请求显示如何在 "草稿" 文件夹中形成更新用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="dced1-107">The following example of an **UpdateUserConfiguration** request shows how to form a request to update a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="dced1-108">代码</span><span class="sxs-lookup"><span data-stu-id="dced1-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:UpdateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="TestConfig">
          <t:DistinguishedFolderId Id="drafts"/>
        </t:UserConfigurationName>
        <t:Dictionary>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>PhoneNumber</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>String</t:Type>
              <t:Value>111-111-5555</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
        </t:Dictionary>
      </m:UserConfiguration>
    </m:UpdateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="updateuserconfiguration-response-example"></a><span data-ttu-id="dced1-109">UpdateUserConfiguration 响应示例</span><span class="sxs-lookup"><span data-stu-id="dced1-109">UpdateUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="dced1-110">Description</span><span class="sxs-lookup"><span data-stu-id="dced1-110">Description</span></span>

<span data-ttu-id="dced1-111">下面的示例演示对**UpdateUserConfiguration**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="dced1-111">The following example shows a successful response to the **UpdateUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="dced1-112">代码</span><span class="sxs-lookup"><span data-stu-id="dced1-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0"
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UpdateUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UpdateUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:UpdateUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="dced1-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dced1-113">See also</span></span>



[<span data-ttu-id="dced1-114">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="dced1-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="dced1-115">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dced1-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

