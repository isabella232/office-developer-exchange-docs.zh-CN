---
title: GetServiceConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: 070cbfe5-325a-4955-8e4a-8230ea0459a7
description: GetServiceConfiguration 操作获取的服务的指定类型的配置信息。 此操作可返回的统一消息、 保护规则和邮件提示服务配置设置。
ms.openlocfilehash: 7fdc4d8defac3d6d352c121483bf8a4c735d9629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825667"
---
# <a name="getserviceconfiguration-operation"></a><span data-ttu-id="3d9e5-104">GetServiceConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="3d9e5-104">GetServiceConfiguration operation</span></span>

<span data-ttu-id="3d9e5-105">**GetServiceConfiguration**操作获取的服务的指定类型的配置信息。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-105">The **GetServiceConfiguration** operation gets configuration information for the specified type of service.</span></span> <span data-ttu-id="3d9e5-106">此操作可返回的统一消息、 保护规则和邮件提示服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-106">This operation can return configuration settings for the Unified Messaging, Protection Rules, and Mail Tips services.</span></span> 
  
## <a name="getserviceconfiguration-request-example"></a><span data-ttu-id="3d9e5-107">GetServiceConfiguration 请求示例</span><span class="sxs-lookup"><span data-stu-id="3d9e5-107">GetServiceConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="3d9e5-108">说明</span><span class="sxs-lookup"><span data-stu-id="3d9e5-108">Description</span></span>

<span data-ttu-id="3d9e5-109">**GetServiceConfiguration**请求的下面的示例演示如何以形成一个请求以获取统一消息服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-109">The following example of a **GetServiceConfiguration** request shows how to form a request to get configuration information for the Unified Messaging service.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3d9e5-110">代码</span><span class="sxs-lookup"><span data-stu-id="3d9e5-110">Code</span></span>

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
    <m:GetServiceConfiguration>
      <m:RequestedConfiguration>
        <m:ConfigurationName>UnifiedMessagingConfiguration</m:ConfigurationName>
      </m:RequestedConfiguration>
    </m:GetServiceConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="getserviceconfiguration-response-example"></a><span data-ttu-id="3d9e5-111">GetServiceConfiguration 响应示例</span><span class="sxs-lookup"><span data-stu-id="3d9e5-111">GetServiceConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="3d9e5-112">说明</span><span class="sxs-lookup"><span data-stu-id="3d9e5-112">Description</span></span>

<span data-ttu-id="3d9e5-113">下面的示例演示对**GetServiceConfiguration**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-113">The following example shows a successful response to the **GetServiceConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3d9e5-114">代码</span><span class="sxs-lookup"><span data-stu-id="3d9e5-114">Code</span></span>

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
    <GetServiceConfigurationResponse ResponseClass="Success" 
                                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <ResponseMessages>
        <ServiceConfigurationResponseMessageType ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <m:UnifiedMessagingConfiguration xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
            <t:UmEnabled xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">true</t:UmEnabled>
            <t:PlayOnPhoneDialString xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">user@contoso.com</t:PlayOnPhoneDialString>
            <t:PlayOnPhoneEnabled xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">true</t:PlayOnPhoneEnabled>
          </m:UnifiedMessagingConfiguration>
        </ServiceConfigurationResponseMessageType>
      </ResponseMessages>
    </GetServiceConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="getserviceconfiguration-error-response-example"></a><span data-ttu-id="3d9e5-115">GetServiceConfiguration 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="3d9e5-115">GetServiceConfiguration Error response example</span></span>

### <a name="description"></a><span data-ttu-id="3d9e5-116">说明</span><span class="sxs-lookup"><span data-stu-id="3d9e5-116">Description</span></span>

<span data-ttu-id="3d9e5-117">下面的示例演示对**GetServiceConfiguration**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-117">The following example shows an error response to the **GetServiceConfiguration** request.</span></span> <span data-ttu-id="3d9e5-118">不正确配置名称导致出现此错误。</span><span class="sxs-lookup"><span data-stu-id="3d9e5-118">This error was caused by an incorrect configuration name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3d9e5-119">代码</span><span class="sxs-lookup"><span data-stu-id="3d9e5-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body>
    <s:Fault>
      <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
      <faultstring xml:lang="en-US">The request failed schema validation: 
      The 'http://schemas.microsoft.com/exchange/services/2006/messages:ConfigurationName' element 
      is invalid - The value 'UUnifiedMessagingConfiguration' is invalid according to its 
      datatype 'http://schemas.microsoft.com/exchange/services/2006/types:ServiceConfigurationType' 
      - The Enumeration constraint failed.</faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
        <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:LineNumber>13</t:LineNumber>
          <t:LinePosition>62</t:LinePosition>
          <t:Violation>The 'http://schemas.microsoft.com/exchange/services/2006/messages:ConfigurationName' element 
          is invalid - The value 'UUnifiedMessagingConfiguration' is invalid according to its 
          datatype 'http://schemas.microsoft.com/exchange/services/2006/types:ServiceConfigurationType'
          - The Enumeration constraint failed.</t:Violation>
        </t:MessageXml>
      </detail>
    </s:Fault>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="3d9e5-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d9e5-120">See also</span></span>



[<span data-ttu-id="3d9e5-121">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="3d9e5-121">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="3d9e5-122">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3d9e5-122">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

