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
description: 查找有关 ConvertId EWS 操作的信息。
ms.openlocfilehash: 36bd47d3fc7c7ca7cea7b38222abb25fba6074ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452550"
---
# <a name="convertid-operation"></a><span data-ttu-id="8b62c-103">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="8b62c-103">ConvertId operation</span></span>

<span data-ttu-id="8b62c-104">查找有关**ConvertId** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8b62c-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="8b62c-105">**ConvertId** Exchange Web 服务（EWS）操作将项目和文件夹标识符转换为 exchange online、exchange Online 作为 Office 365 的一部分以及从 exchange Server 2013 开始的 exchange 内部部署版本之间的格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="8b62c-106">使用 ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="8b62c-106">Using the ConvertId operation</span></span>
<span data-ttu-id="8b62c-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-107"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="8b62c-108">您可以使用**ConvertId**操作来转换以下标识符：</span><span class="sxs-lookup"><span data-stu-id="8b62c-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="8b62c-109">Exchange 2007 的初始发布版本中的 EWS 标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="8b62c-110">这由 `EwsLegacyId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值表示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="8b62c-111">Exchange 2007 SP1 或 Exchange 2010 中的 EWS 的标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="8b62c-112">这由 `EwsId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-112">This is represented by the  `EwsId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="8b62c-113">MAPI 标识符，如**PR_ENTRYID**属性中所示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="8b62c-114">这由 `EntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值表示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="8b62c-115">可用性日历事件标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-115">The availability calendar event identifier.</span></span> <span data-ttu-id="8b62c-116">这是**PR_ENTRYID**属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="8b62c-117">这由 `HexEntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="8b62c-118">Exchange 存储标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-118">The Exchange store identifier.</span></span> <span data-ttu-id="8b62c-119">这由 `StoreId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。</span><span class="sxs-lookup"><span data-stu-id="8b62c-119">This is represented by the  `StoreId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="8b62c-120">**ConvertId**操作不会将公用文件夹标识符从 EWS 标识符转换为存储标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="8b62c-121">Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="8b62c-122">这由 `OwaId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示</span><span class="sxs-lookup"><span data-stu-id="8b62c-122">This is represented by the  `OwaId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="8b62c-123">不支持将从此标识符创建的 Url 传递到 Outlook Web App。</span><span class="sxs-lookup"><span data-stu-id="8b62c-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="8b62c-124">Outlook Web App 标识符适用于 Exchange 2007 和 Exchange 2010。</span><span class="sxs-lookup"><span data-stu-id="8b62c-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="8b62c-125">适用于 Exchange Online 的 Outlook Web App 和从 Exchange Server 2013 开始的 Exchange 版本使用 EWS 标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="8b62c-126">在将公用文件夹标识符从 EWS 标识符转换为 Exchange Online 和 Exchange 2013 中的存储标识符时， **ConvertId**操作不会按预期工作。</span><span class="sxs-lookup"><span data-stu-id="8b62c-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="8b62c-127">您可以手动更新作为解决方法返回的标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="8b62c-128">若要手动更新标识符：</span><span class="sxs-lookup"><span data-stu-id="8b62c-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="8b62c-129">在应用程序代码中，确定目标项目/文件夹是否位于公用文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8b62c-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="8b62c-130">对 Base64 编码的标识符字符串进行解码。</span><span class="sxs-lookup"><span data-stu-id="8b62c-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="8b62c-131">验证类型 "字节（21字节）" 的值是否为7。</span><span class="sxs-lookup"><span data-stu-id="8b62c-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="8b62c-132">值为7表示标识符的格式不正确。</span><span class="sxs-lookup"><span data-stu-id="8b62c-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="8b62c-133">跳过前四个字节。</span><span class="sxs-lookup"><span data-stu-id="8b62c-133">Skip the first four bytes.</span></span> <span data-ttu-id="8b62c-134">必须将其设置为零。</span><span class="sxs-lookup"><span data-stu-id="8b62c-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="8b62c-135">使用以下 GUID 更新接下来的16个字节：1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="8b62c-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="8b62c-136">更新值为9的下一个字节（类型为 byte）。</span><span class="sxs-lookup"><span data-stu-id="8b62c-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="8b62c-137">将标识符更改为 Base64 编码的字符串。</span><span class="sxs-lookup"><span data-stu-id="8b62c-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8b62c-138">**ConvertId**操作验证给定的 SMTP 地址是否具有有效的格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="8b62c-139">该操作不确定 SMTP 地址是否表示有效邮箱。</span><span class="sxs-lookup"><span data-stu-id="8b62c-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="8b62c-140">**ConvertId**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="8b62c-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="8b62c-141">**表1。ConvertId 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="8b62c-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="8b62c-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="8b62c-142">**Header**</span></span>|<span data-ttu-id="8b62c-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="8b62c-143">**Element**</span></span>|<span data-ttu-id="8b62c-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="8b62c-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b62c-145">模拟</span><span class="sxs-lookup"><span data-stu-id="8b62c-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="8b62c-146">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="8b62c-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="8b62c-147">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="8b62c-147">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="8b62c-148">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="8b62c-148">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8b62c-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="8b62c-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="8b62c-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8b62c-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8b62c-151">标识适用于请求的操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="8b62c-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8b62c-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="8b62c-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="8b62c-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8b62c-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8b62c-154">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="8b62c-154">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8b62c-155">这适用于响应。</span><span class="sxs-lookup"><span data-stu-id="8b62c-155">This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="8b62c-156">ConvertId 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="8b62c-156">ConvertId operation request example</span></span>
<span data-ttu-id="8b62c-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-157"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="8b62c-158">以下示例的**ConvertId**请求显示如何从 EWS 标识符转换为 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="8b62c-159">必须将 SOAP 标头中的[RequestServerVersion](requestserverversion.md)元素设置为 Exchange2007_SP1 或更高版本，才能使此操作生效。</span><span class="sxs-lookup"><span data-stu-id="8b62c-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b62c-160">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8b62c-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="8b62c-161">ConvertId 操作响应示例</span><span class="sxs-lookup"><span data-stu-id="8b62c-161">ConvertId operation response example</span></span>
<span data-ttu-id="8b62c-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-162"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="8b62c-163">下面的示例演示对**ConvertId**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8b62c-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="8b62c-164">此响应示例包含 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b62c-165">Outlook Web App 标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8b62c-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="8b62c-166">ConvertId 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="8b62c-166">ConvertId operation error response example</span></span>
<span data-ttu-id="8b62c-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-167"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="8b62c-168">下面的示例演示对包含错误类型的标识符格式的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="8b62c-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="version-differences"></a><span data-ttu-id="8b62c-169">版本差异</span><span class="sxs-lookup"><span data-stu-id="8b62c-169">Version differences</span></span>
<span data-ttu-id="8b62c-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-170"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

<span data-ttu-id="8b62c-171">在 Exchange 2007 和 Exchange 2007 Service Pack 1 （SP1）的初始发行版之间更改了 EWS 标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="8b62c-172">Exchange Online 作为 Office 365、Exchange Online 和 Exchange 内部部署版本的一部分从 exchange 2010 开始使用 Exchange 2007 SP1 使用的相同标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8b62c-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="8b62c-173">**ConvertId**操作将公用文件夹标识符从 EWS 标识符转换为 exchange 2007 和 exchange 2010 中的存储标识符。</span><span class="sxs-lookup"><span data-stu-id="8b62c-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b62c-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8b62c-174">See also</span></span>
<span data-ttu-id="8b62c-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="8b62c-175"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

- [<span data-ttu-id="8b62c-176">转换标识符</span><span class="sxs-lookup"><span data-stu-id="8b62c-176">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="8b62c-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="8b62c-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="8b62c-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="8b62c-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

