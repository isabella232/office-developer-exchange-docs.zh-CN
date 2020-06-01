---
title: CreateUserConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfiguration
api_type:
- schema
ms.assetid: eb5b8ab6-9743-481c-aac9-f9aa889bd353
description: CreateUserConfiguration 操作将在文件夹上创建一个用户配置对象。
ms.openlocfilehash: 0c9233146d21c7014be15896426b968106485200
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463781"
---
# <a name="createuserconfiguration-operation"></a><span data-ttu-id="96680-103">CreateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="96680-103">CreateUserConfiguration operation</span></span>

<span data-ttu-id="96680-104">**CreateUserConfiguration**操作将在文件夹上创建一个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="96680-104">The **CreateUserConfiguration** operation creates a user configuration object on a folder.</span></span> 
  
## <a name="createuserconfiguration-request-example"></a><span data-ttu-id="96680-105">CreateUserConfiguration 请求示例</span><span class="sxs-lookup"><span data-stu-id="96680-105">CreateUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="96680-106">说明</span><span class="sxs-lookup"><span data-stu-id="96680-106">Description</span></span>

<span data-ttu-id="96680-107">以下示例的**CreateUserConfiguration**请求显示如何在 "草稿" 文件夹中形成创建用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="96680-107">The following example of a **CreateUserConfiguration** request shows how to form a request to create a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="96680-108">代码</span><span class="sxs-lookup"><span data-stu-id="96680-108">Code</span></span>

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
    <m:CreateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="TestConfig">
          <t:DistinguishedFolderId Id="drafts">
          </t:DistinguishedFolderId>
        </t:UserConfigurationName>
        <t:Dictionary>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>PhoneNumber</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>String</t:Type>
              <t:Value>555-555-1111</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
        </t:Dictionary>
      </m:UserConfiguration>  
    </m:CreateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="createuserconfiguration-response-example"></a><span data-ttu-id="96680-109">CreateUserConfiguration 响应示例</span><span class="sxs-lookup"><span data-stu-id="96680-109">CreateUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="96680-110">说明</span><span class="sxs-lookup"><span data-stu-id="96680-110">Description</span></span>

<span data-ttu-id="96680-111">下面的示例演示对**CreateUserConfiguration**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="96680-111">The following example shows a successful response to the **CreateUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="96680-112">代码</span><span class="sxs-lookup"><span data-stu-id="96680-112">Code</span></span>

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
    <m:CreateUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:CreateUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:CreateUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="96680-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96680-113">See also</span></span>



[<span data-ttu-id="96680-114">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="96680-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="96680-115">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="96680-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

