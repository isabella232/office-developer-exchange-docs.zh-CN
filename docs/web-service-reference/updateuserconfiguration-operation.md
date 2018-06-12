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
description: UpdateUserConfiguration 操作可更新的文件夹的用户配置对象。
ms.openlocfilehash: 9da7c7ba15b3cf6b35f0489db539660aefa2e40a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838425"
---
# <a name="updateuserconfiguration-operation"></a><span data-ttu-id="c0440-103">UpdateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="c0440-103">UpdateUserConfiguration operation</span></span>

<span data-ttu-id="c0440-104">**UpdateUserConfiguration**操作可更新的文件夹的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="c0440-104">The **UpdateUserConfiguration** operation updates a user configuration object on a folder.</span></span> 
  
## <a name="updateuserconfiguration-request-example"></a><span data-ttu-id="c0440-105">UpdateUserConfiguration 请求示例</span><span class="sxs-lookup"><span data-stu-id="c0440-105">UpdateUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="c0440-106">说明</span><span class="sxs-lookup"><span data-stu-id="c0440-106">Description</span></span>

<span data-ttu-id="c0440-107">**UpdateUserConfiguration**请求的下面的示例演示如何以形成一个请求来更新用户配置对象上草稿文件夹。</span><span class="sxs-lookup"><span data-stu-id="c0440-107">The following example of an **UpdateUserConfiguration** request shows how to form a request to update a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c0440-108">代码</span><span class="sxs-lookup"><span data-stu-id="c0440-108">Code</span></span>

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

## <a name="updateuserconfiguration-response-example"></a><span data-ttu-id="c0440-109">UpdateUserConfiguration 响应示例</span><span class="sxs-lookup"><span data-stu-id="c0440-109">UpdateUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="c0440-110">说明</span><span class="sxs-lookup"><span data-stu-id="c0440-110">Description</span></span>

<span data-ttu-id="c0440-111">下面的示例演示对**UpdateUserConfiguration**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="c0440-111">The following example shows a successful response to the **UpdateUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c0440-112">代码</span><span class="sxs-lookup"><span data-stu-id="c0440-112">Code</span></span>

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
    <m:UpdateUserConfigurationResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UpdateUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:UpdateUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="c0440-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0440-113">See also</span></span>



[<span data-ttu-id="c0440-114">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="c0440-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="c0440-115">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0440-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

