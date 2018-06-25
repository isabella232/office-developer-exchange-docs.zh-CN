---
title: ExportItems 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: e2846abb-0b16-4732-bbd8-038a674672f6
description: ExportItems 操作将邮箱出的项目导出。
ms.openlocfilehash: 6f0760705c05de2a615544fe52ac50b398be6040
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754209"
---
# <a name="exportitems-operation"></a><span data-ttu-id="69168-103">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="69168-103">ExportItems operation</span></span>

<span data-ttu-id="69168-104">**ExportItems**操作将邮箱出的项目导出。</span><span class="sxs-lookup"><span data-stu-id="69168-104">The **ExportItems** operation exports items out of a mailbox.</span></span> 
  
## <a name="exportitems-request-example"></a><span data-ttu-id="69168-105">ExportItems 请求示例</span><span class="sxs-lookup"><span data-stu-id="69168-105">ExportItems request example</span></span>

### <a name="description"></a><span data-ttu-id="69168-106">说明</span><span class="sxs-lookup"><span data-stu-id="69168-106">Description</span></span>

<span data-ttu-id="69168-107">**ExportItems**请求的下面的示例演示如何获取三项从邮箱导出请求的表单。</span><span class="sxs-lookup"><span data-stu-id="69168-107">The following example of an **ExportItems** request shows how to form a request to get three items exported from a mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="69168-108">代码</span><span class="sxs-lookup"><span data-stu-id="69168-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA="/>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="69168-109">Comment</span><span class="sxs-lookup"><span data-stu-id="69168-109">Comment</span></span>

<span data-ttu-id="69168-110">在示例中的项标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="69168-110">The item identifiers in the example have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="69168-111">请求元素</span><span class="sxs-lookup"><span data-stu-id="69168-111">Request elements</span></span>

<span data-ttu-id="69168-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="69168-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="69168-113">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="69168-113">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="69168-114">ExportItems</span><span class="sxs-lookup"><span data-stu-id="69168-114">ExportItems</span></span>](exportitems.md)
    
- [<span data-ttu-id="69168-115">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="69168-115">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
    
- [<span data-ttu-id="69168-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="69168-116">ItemId</span></span>](itemid.md)
    
## <a name="successful-exportitems-response-example"></a><span data-ttu-id="69168-117">成功 ExportItems 响应示例</span><span class="sxs-lookup"><span data-stu-id="69168-117">Successful ExportItems response example</span></span>

### <a name="description"></a><span data-ttu-id="69168-118">说明</span><span class="sxs-lookup"><span data-stu-id="69168-118">Description</span></span>

<span data-ttu-id="69168-119">下面的示例演示对**ExportItems**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="69168-119">The following example shows a successful response to an **ExportItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="69168-120">代码</span><span class="sxs-lookup"><span data-stu-id="69168-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <t:ServerVersionInfo MajorVersion="14"
    MinorVersion="1"
    MajorBuildNumber="139"
    MinorBuildNumber="0"
    Version="Exchange2010_SP1"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
    xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89FAAA=" ChangeKey="FwAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            QAAyAAAh9SpR08oBAwAEQAMAFkANABMOAwAAQAMAIQ4AAAAAsIQSN0oAAAAyAGEAYgAxADYA
            MQA2ADYALQBhAGUANQBkAC0ANAAyAGUAZgAtAGEANQA1ADkALQBjADgAOQAwADgANwBkADIA
            MwBkADgANAAAAAMACzf/////AwAgDmQEAAADAPcPAAAAAEAABzBPMXstUdPKAUAACDBPMXst
            UdPKAQMABTcFAAAAsIQONx4AAABtAGUAcwBzAGEAZwBlAC8AcgBmAGMAOAAyADIAAACwhAEw
            IgAAAE0AbwBzAHQAIABmAGEAcwBjAGkAbgBhAHQAaQBuAGcAAAACAfkPBAAAAAAAAAADAAFA
            FABKZ3QrAAAAZF2mAwAXAAEAAACwhBoAEgAAAEkAUABNAC4ATgBvAHQAZQAAAAMANgAAAAAA
            sIQ3ACIAAABNAG8AcwB0ACAAZgBhAHMAYwBpAG4AYQB0AGkAbgBnAAAAQAA5AACq+za80coB
            AgE7AGUAAABFWDovTz1GSVJTVCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RS
            QVRJVkUgR1JPVVAgKEZZRElCT0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05F
            ALCEPQACAAAAAAACAUEAfgAAAAAAAADcp0DIwEIQGrS5CAArL+GCAQAAAAAAAAAvTz1GSVJT
            VCBPUkdBTklaQVRJT04vT1U9RVhDSEFOR0UgQURNSU5JU1RSQVRJVkUgR1JPVVAgKEZZRElC
            T0hGMjNTUERMVCkvQ049UkVDSVBJRU5UUy9DTj1VU0VST05FALCEQgAQAAAAVQB
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY87NAAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAAAAAEYAJACA
            BAAAAAYAAAABDouAAAACAAAAEiAAAOSECEBbAAAAL089RklSU1QgT1JHQU5JWkFUSU9OL09V
            PUVYQ0hBTkdFIEFETUlOSVNUUkFUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJF
            Q0lQSUVOVFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAAALACMAAAAL
            ACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUAcwB0AGkAbgBnACAALQAgAGYAcgBv
            AG0AIABFAFcAUwBNAEEAAABAADkAAHZeFxfRygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FO
            SVpBVElPTi9PVT1FWENIQU5HRSBBRE1JTklTVFJBVElWRSBHUk9VUCAoRllESUJPSEYyM1NQ
            RExUKS9DTj1SRUNJUElFTlRTL0NOPVVTRVJPTkUAsIQ9AAIAAAAAAAIBPwB+AAAAAAAAANyn
            QMjAQhAatLkIACsv4YIBAAAAAAAAAC9PPUZJUlNUIE9SR0FOSVpBVElPTi9PVT1FWENIQU5H
          </m:Data>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comment"></a><span data-ttu-id="69168-121">Comment</span><span class="sxs-lookup"><span data-stu-id="69168-121">Comment</span></span>

<span data-ttu-id="69168-122">已缩短的项标识符和更改键在示例中，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="69168-122">The item identifiers and change keys in the example have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="69168-123">响应元素</span><span class="sxs-lookup"><span data-stu-id="69168-123">Response elements</span></span>

<span data-ttu-id="69168-124">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="69168-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="69168-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69168-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="69168-126">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="69168-126">ExportItemsResponse</span></span>](exportitemsresponse.md)
    
- [<span data-ttu-id="69168-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69168-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="69168-128">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69168-128">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
    
- [<span data-ttu-id="69168-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="69168-129">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="69168-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="69168-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="69168-131">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="69168-131">Data (base64Binary)</span></span>](data-base64binary.md)
    
## <a name="exportitems-error-response-example"></a><span data-ttu-id="69168-132">ExportItems 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="69168-132">ExportItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="69168-133">说明</span><span class="sxs-lookup"><span data-stu-id="69168-133">Description</span></span>

<span data-ttu-id="69168-134">下面的示例演示包含两个错误和成功导出的一项**ExportItems**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="69168-134">The following example shows a response to the **ExportItems** request that contains two errors and one successfully exported item.</span></span> <span data-ttu-id="69168-135">在示例中的第一项成功导出。</span><span class="sxs-lookup"><span data-stu-id="69168-135">The first item in the example is successfully exported.</span></span> <span data-ttu-id="69168-136">第二个项目包含不正确的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="69168-136">The second item contains an incorrect change key.</span></span> <span data-ttu-id="69168-137">第三项表示尝试导出错误的邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="69168-137">The third item represents an attempt to export an item from the wrong mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="69168-138">代码</span><span class="sxs-lookup"><span data-stu-id="69168-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ExportItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGU0oMf0GPIQeAAAAUC8iAABseAAAAUFZ7AAA=" ChangeKey="CQAAAA=="/>
          <m:Data>
            AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
            YwBvAG0AAABTAE0AVABQAAAAVQBzAGUAcgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUA
            eAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMAbwBmAHQALgBjAG8AbQAAALCE/jlMAAAAVQBzAGUA
            cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
            bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
          </m:Data>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExportItemsResponseMessage>
        <m:ExportItemsResponseMessage ResponseClass="Error">
          <m:MessageText>No mailbox with such guid.</m:MessageText>
          <m:ResponseCode>ErrorNonExistentMailbox</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:Value Name="MailboxGuid">f3f6f699-2254-40ce-9994-388d9d98419e</t:Value>
          </m:MessageXml>
        </m:ExportItemsResponseMessage>
      </m:ResponseMessages>
    </m:ExportItemsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="comments"></a><span data-ttu-id="69168-139">注释</span><span class="sxs-lookup"><span data-stu-id="69168-139">Comments</span></span>

<span data-ttu-id="69168-140">项标识符，更改键，并在示例中的数据具有缩短，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="69168-140">The item identifiers, change keys, and data in the example have been shortened to preserve readability.</span></span>
  
### <a name="error-response-elements"></a><span data-ttu-id="69168-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="69168-141">Error response elements</span></span>

<span data-ttu-id="69168-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="69168-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="69168-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69168-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="69168-144">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="69168-144">ExportItemsResponse</span></span>](exportitemsresponse.md)
    
- [<span data-ttu-id="69168-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69168-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="69168-146">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69168-146">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
    
- [<span data-ttu-id="69168-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="69168-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="69168-148">ItemId</span><span class="sxs-lookup"><span data-stu-id="69168-148">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="69168-149">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="69168-149">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="69168-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="69168-150">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="69168-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="69168-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="69168-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="69168-152">MessageXml</span></span>](messagexml.md)
    
- <span data-ttu-id="69168-153">**值**</span><span class="sxs-lookup"><span data-stu-id="69168-153">**Value**</span></span>
    
> [!NOTE]
> <span data-ttu-id="69168-154">**Value**元素不存在架构中。</span><span class="sxs-lookup"><span data-stu-id="69168-154">The **Value** element does not exist in the schema.</span></span> <span data-ttu-id="69168-155">此元素是有效的因为[MessageXml](messagexml.md)元素中，在其中**值**实例元素发生，可以包含任何有效的 XML。</span><span class="sxs-lookup"><span data-stu-id="69168-155">This element is valid because the [MessageXml](messagexml.md) element, in which the **Value** instance element occurs, can contain any well-formed XML.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69168-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69168-156">See also</span></span>



[<span data-ttu-id="69168-157">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="69168-157">UploadItems operation</span></span>](uploaditems-operation.md)


[<span data-ttu-id="69168-158">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="69168-158">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="69168-159">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="69168-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

