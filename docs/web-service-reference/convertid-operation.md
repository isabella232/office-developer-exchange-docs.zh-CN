---
title: ConvertId 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: 查找信息 ConvertId EWS 操作。
ms.openlocfilehash: 5f1bcd8a9f0adc25b7c598ef10cc6bb139dfe02d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753594"
---
# <a name="convertid-operation"></a><span data-ttu-id="ebade-103">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="ebade-103">ConvertId operation</span></span>

<span data-ttu-id="ebade-104">查找有关**ConvertId** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="ebade-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="ebade-105">**ConvertId** Exchange Web Services (EWS) 操作将转换所接受的 Exchange Online 中，Exchange Online 作为 Office 365 的一部分的格式之间的项目和文件夹标识符和本地 Exchange 启动与 Exchange Server 版本2013。</span><span class="sxs-lookup"><span data-stu-id="ebade-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="ebade-106">使用 ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="ebade-106">Using the ConvertId operation</span></span>
<span data-ttu-id="ebade-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-107"></span></span>

<span data-ttu-id="ebade-108">您可以将以下标识符转换使用**ConvertId**操作：</span><span class="sxs-lookup"><span data-stu-id="ebade-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="ebade-109">EWS 的初始发行版 Exchange 2007 中的标识符格式。</span><span class="sxs-lookup"><span data-stu-id="ebade-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="ebade-110">这由`EwsLegacyId` [id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值。</span><span class="sxs-lookup"><span data-stu-id="ebade-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="ebade-111">在 Exchange 2007 SP1 或 Exchange 2010 的 EWS 标识符格式。</span><span class="sxs-lookup"><span data-stu-id="ebade-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="ebade-112">这由`EwsId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。</span><span class="sxs-lookup"><span data-stu-id="ebade-112">This is represented by the  `EwsId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="ebade-113">MAPI 的标识符，如**PR_ENTRYID**属性中所示。</span><span class="sxs-lookup"><span data-stu-id="ebade-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="ebade-114">这由`EntryId` [id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值。</span><span class="sxs-lookup"><span data-stu-id="ebade-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="ebade-115">可用性日历事件标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-115">The availability calendar event identifier.</span></span> <span data-ttu-id="ebade-116">这是**PR_ENTRYID**属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="ebade-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="ebade-117">这由`HexEntryId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。</span><span class="sxs-lookup"><span data-stu-id="ebade-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="ebade-118">Exchange 存储区标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-118">The Exchange store identifier.</span></span> <span data-ttu-id="ebade-119">这由`StoreId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。</span><span class="sxs-lookup"><span data-stu-id="ebade-119">This is represented by the  `StoreId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="ebade-120">**ConvertId**操作不能转换公用文件夹标识符从 EWS 标识符与存储标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="ebade-121">Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="ebade-122">这由`OwaId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值</span><span class="sxs-lookup"><span data-stu-id="ebade-122">This is represented by the  `OwaId` enumeration value in [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="ebade-123">不支持传递到 Outlook Web App 创建的此标识符的 Url。</span><span class="sxs-lookup"><span data-stu-id="ebade-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="ebade-124">适用于 Exchange 2007 和 Exchange 2010 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="ebade-125">Exchange Online 和 Exchange Server 2013 开头的 Exchange 版本的 outlook Web App 使用 EWS 标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="ebade-126">**ConvertId**操作不未按预期从 EWS 标识符的公用文件夹标识符转换到 Exchange Online 和 Exchange 2013 中的存储标识符时。</span><span class="sxs-lookup"><span data-stu-id="ebade-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="ebade-127">您可以手动更新作为一种解决方法返回的标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="ebade-128">手动更新标识符：</span><span class="sxs-lookup"><span data-stu-id="ebade-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="ebade-129">在应用程序代码中，确定目标项目/文件夹是否在公用文件夹中。</span><span class="sxs-lookup"><span data-stu-id="ebade-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="ebade-130">对 Base64 编码标识符字符串进行解码。</span><span class="sxs-lookup"><span data-stu-id="ebade-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="ebade-131">验证类型字节 （21 字节） 的值为 7。</span><span class="sxs-lookup"><span data-stu-id="ebade-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="ebade-132">值为 7 指示标识符格式不正确。</span><span class="sxs-lookup"><span data-stu-id="ebade-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="ebade-133">跳过前四个字节。</span><span class="sxs-lookup"><span data-stu-id="ebade-133">Skip the first four bytes.</span></span> <span data-ttu-id="ebade-134">它们必须设置为零。</span><span class="sxs-lookup"><span data-stu-id="ebade-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="ebade-135">使用下列 GUID 更新下一个 16 字节： 1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="ebade-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="ebade-136">值为 9 更新的下一个字节 （类型字节）。</span><span class="sxs-lookup"><span data-stu-id="ebade-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="ebade-137">更改为使用 Base64 编码的字符串标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ebade-138">**ConvertId**操作验证给定的 SMTP 地址具有有效的格式。</span><span class="sxs-lookup"><span data-stu-id="ebade-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="ebade-139">此操作将不确定的 SMTP 地址是否表示有效的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ebade-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="ebade-140">**ConvertId**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="ebade-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="ebade-141">**表 1。ConvertId 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="ebade-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="ebade-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="ebade-142">**Header**</span></span>|<span data-ttu-id="ebade-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="ebade-143">**Element**</span></span>|<span data-ttu-id="ebade-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="ebade-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebade-145">模拟</span><span class="sxs-lookup"><span data-stu-id="ebade-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="ebade-146">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ebade-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ebade-147">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="ebade-147">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="ebade-148">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="ebade-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebade-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="ebade-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="ebade-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ebade-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ebade-151">标识操作请求这是适用于请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="ebade-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebade-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ebade-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="ebade-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ebade-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ebade-154">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="ebade-154">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ebade-155">这是适用于响应。</span><span class="sxs-lookup"><span data-stu-id="ebade-155">This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="ebade-156">ConvertId 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="ebade-156">ConvertId operation request example</span></span>
<span data-ttu-id="ebade-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-157"></span></span>

<span data-ttu-id="ebade-158">**ConvertId**请求的下面的示例演示如何从 EWS 标识符将转换为 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="ebade-159">此操作能够执行到 Exchange2007_SP1 或更高版本，必须设置中的 SOAP 标头的[RequestServerVersion](requestserverversion.md)元素。</span><span class="sxs-lookup"><span data-stu-id="ebade-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ebade-160">已缩短的项标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="ebade-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="ebade-161">ConvertId 操作响应示例</span><span class="sxs-lookup"><span data-stu-id="ebade-161">ConvertId operation response example</span></span>
<span data-ttu-id="ebade-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-162"></span></span>

<span data-ttu-id="ebade-163">下面的示例演示对**ConvertId**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="ebade-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="ebade-164">以下响应示例包含的 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ebade-165">Outlook Web App 标识符已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="ebade-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="ebade-166">ConvertId 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="ebade-166">ConvertId operation error response example</span></span>
<span data-ttu-id="ebade-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-167"></span></span>

<span data-ttu-id="ebade-168">下面的示例演示包含错误的标识符格式类型请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ebade-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="ebade-169">版本差异</span><span class="sxs-lookup"><span data-stu-id="ebade-169">Version differences</span></span>
<span data-ttu-id="ebade-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-170"></span></span>

<span data-ttu-id="ebade-171">EWS 标识符格式之间的初始发行版本的 Exchange 2007 和 Exchange 2007 Service Pack 1 (SP1) 发生更改。</span><span class="sxs-lookup"><span data-stu-id="ebade-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="ebade-172">Exchange Online 作为 Office 365 的一部分，Exchange Online 和本地版本的 Exchange 与 Exchange 2010 开始使用 Exchange 2007 SP1 使用的相同标识符格式。</span><span class="sxs-lookup"><span data-stu-id="ebade-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="ebade-173">**ConvertId**操作将公用文件夹标识符从 EWS 标识符转换为 Exchange 2007 和 Exchange 2010 中的存储标识符。</span><span class="sxs-lookup"><span data-stu-id="ebade-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ebade-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ebade-174">See also</span></span>
<span data-ttu-id="ebade-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="ebade-175"></span></span>

- [<span data-ttu-id="ebade-176">转换标识符</span><span class="sxs-lookup"><span data-stu-id="ebade-176">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="ebade-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="ebade-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="ebade-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="ebade-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

