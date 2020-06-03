---
title: GetSharingMetadata 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: eaf29427-ecf8-4a5e-9a54-db2e6414b35e
description: GetSharingMetadata 操作获取一个不透明的身份验证令牌，用于标识共享邀请。
ms.openlocfilehash: 0390b9caa7b2e9847b1e8dcdc1b911a35e3c5864
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530181"
---
# <a name="getsharingmetadata-operation"></a><span data-ttu-id="96c23-103">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="96c23-103">GetSharingMetadata operation</span></span>

<span data-ttu-id="96c23-104">**GetSharingMetadata**操作获取一个不透明的身份验证令牌，用于标识共享邀请。</span><span class="sxs-lookup"><span data-stu-id="96c23-104">The **GetSharingMetadata** operation gets an opaque authentication token that identifies a sharing invitation.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="96c23-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="96c23-105">SOAP Headers</span></span>

<span data-ttu-id="96c23-106">**GetSharingMetadata**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="96c23-106">The **GetSharingMetadata** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="96c23-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="96c23-107">**Header**</span></span>|<span data-ttu-id="96c23-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="96c23-108">**Element**</span></span>|<span data-ttu-id="96c23-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="96c23-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96c23-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="96c23-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="96c23-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="96c23-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="96c23-112">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="96c23-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="96c23-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="96c23-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="96c23-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="96c23-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="96c23-115">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="96c23-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingmetadata-request-example"></a><span data-ttu-id="96c23-116">GetSharingMetadata 请求示例</span><span class="sxs-lookup"><span data-stu-id="96c23-116">GetSharingMetadata request example</span></span>

### <a name="description"></a><span data-ttu-id="96c23-117">Description</span><span class="sxs-lookup"><span data-stu-id="96c23-117">Description</span></span>

<span data-ttu-id="96c23-118">下面的示例演示如何形成请求以获取标识共享邀请的不透明身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="96c23-118">The following example shows how to form a request to get an opaque authentication token that identifies a sharing invitation.</span></span> <span data-ttu-id="96c23-119">在此示例中，user1@contoso.com 想要共享由[IdOfFolderToShare](idoffoldertoshare.md)元素使用 user1@fabikam.com 和 user2@test.com 指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="96c23-119">In this example, user1@contoso.com wants to share the folder that is specified by the [IdOfFolderToShare](idoffoldertoshare.md) element with user1@fabikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="96c23-120">代码</span><span class="sxs-lookup"><span data-stu-id="96c23-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingMetadata>
      <m:IdOfFolderToShare Id="AAMkAD=" ChangeKey="AwAAA=" />
      <m:SenderSmtpAddress>user1@contoso.com</m:SenderSmtpAddress>
      <m:Recipients>
        <t:SmtpAddress>user1@fabrikam.com</t:SmtpAddress>
        <t:SmtpAddress>user2@test.com</t:SmtpAddress>
      </m:Recipients>
    </m:GetSharingMetadata>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="96c23-121">备注</span><span class="sxs-lookup"><span data-stu-id="96c23-121">Comments</span></span>

<span data-ttu-id="96c23-122">[收件人（ArrayOfSmtpAddressType）](recipients-arrayofsmtpaddresstype.md)元素包含共享邀请的每个预期收件人的一个[SmtpAddress](smtpaddress.md)元素。</span><span class="sxs-lookup"><span data-stu-id="96c23-122">The [Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) element contains one [SmtpAddress](smtpaddress.md) element for each intended recipient of the sharing invitation.</span></span> 
  
## <a name="successful-getsharingmetadata-response"></a><span data-ttu-id="96c23-123">成功的 GetSharingMetadata 响应</span><span class="sxs-lookup"><span data-stu-id="96c23-123">Successful GetSharingMetadata Response</span></span>

### <a name="description"></a><span data-ttu-id="96c23-124">Description</span><span class="sxs-lookup"><span data-stu-id="96c23-124">Description</span></span>

<span data-ttu-id="96c23-125">下面的示例演示对**GetSharingMetadata**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="96c23-125">The following example shows a successful response to a **GetSharingMetadata** request.</span></span> <span data-ttu-id="96c23-126">在此示例中，在对应的**GetSharingMetadata**请求中指定了两个收件人： user1@fabrikam.com 和 user2@test.com。</span><span class="sxs-lookup"><span data-stu-id="96c23-126">In this example, two recipients were specified in the corresponding **GetSharingMetadata** request: user1@fabrikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="96c23-127">代码</span><span class="sxs-lookup"><span data-stu-id="96c23-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Success" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</ResponseCode>
      <m:EncryptedSharedFolderDataCollection>
        <t:EncryptedSharedFolderData>
          <t:Token>
            <EncryptedData Id="Assertion0" Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#tripledes-cbc"></EncryptionMethod>
              <ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey>
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#rsa-oaep-mgf1p"></EncryptionMethod>
                  <ds:KeyInfo Id="keyinfo">
                    <wsse:SecurityTokenReference xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
                      <wsse:KeyIdentifier 
                                  EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary" 
                                  ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509SubjectKeyIdentifier">
                        B4VEEAf=
                      </wsse:KeyIdentifier>
                    </wsse:SecurityTokenReference>
                  </ds:KeyInfo>
                  <CipherData>
                    <CipherValue>GI/Dxqvw2na==</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </ds:KeyInfo>
              <CipherData>
                <CipherValue>L77I7Hr06z</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Token>
          <t:Data>
            <EncryptedData Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#aes256-cbc" />
              <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey xmlns="http://www.w3.org/2001/04/xmlenc#">
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#kw-tripledes" />
                  <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                    <KeyName>key</KeyName>
                  </KeyInfo>
                  <CipherData>
                    <CipherValue>9UgtjrHiU</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </KeyInfo>
              <CipherData>
                <CipherValue>NCNsJoGtQ==</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Data>
        </t:EncryptedSharedFolderData>
      </m:EncryptedSharedFolderDataCollection>
      <m:InvalidRecipients>
        <t:InvalidRecipient>
          <t:SmtpAddress>user2@test.com</t:SmtpAddress>
          <t:ResponseCode>RecipientOrganizationNotFederated</t:ResponseCode>
          <m:MessageText>The organization of these recipients is not federated for external sharing.</m:MessageText>
        </t:InvalidRecipient>
      </m:InvalidRecipients>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="96c23-128">备注</span><span class="sxs-lookup"><span data-stu-id="96c23-128">Comments</span></span>

<span data-ttu-id="96c23-129">响应包含由**GetSharingMetadata**请求中指定的有效收件人表示的每个组织的一个[EncryptedSharedFolderData](encryptedsharedfolderdata.md)元素。</span><span class="sxs-lookup"><span data-stu-id="96c23-129">The response contains one [EncryptedSharedFolderData](encryptedsharedfolderdata.md) element for each organization that is represented by valid recipients that are specified in the **GetSharingMetadata** request.</span></span> 
  
<span data-ttu-id="96c23-130">即使在请求中指定了无效的收件人， **GetSharingMetadata**请求也将成功。</span><span class="sxs-lookup"><span data-stu-id="96c23-130">The **GetSharingMetadata** request will succeed even if invalid recipients are specified in the request.</span></span> <span data-ttu-id="96c23-131">[InvalidRecipients](invalidrecipients.md)元素包含有关无效收件人的信息。</span><span class="sxs-lookup"><span data-stu-id="96c23-131">The [InvalidRecipients](invalidrecipients.md) element contains information about invalid recipients.</span></span> <span data-ttu-id="96c23-132">有关收件人可能无效的原因的信息，请参阅[ResponseCode （InvalidRecipientResponseCodeType）](responsecode-invalidrecipientresponsecodetype.md)。</span><span class="sxs-lookup"><span data-stu-id="96c23-132">For information about the reasons why a recipient might be invalid, see [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span></span>
  
<span data-ttu-id="96c23-133">如果所有预期收件人都无效，则[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md)元素将为空。</span><span class="sxs-lookup"><span data-stu-id="96c23-133">If all intended recipients are invalid, the [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) element will be empty.</span></span> 
  
## <a name="getsharingmetadata-error-response"></a><span data-ttu-id="96c23-134">GetSharingMetadata 错误响应</span><span class="sxs-lookup"><span data-stu-id="96c23-134">GetSharingMetadata error response</span></span>

### <a name="description"></a><span data-ttu-id="96c23-135">Description</span><span class="sxs-lookup"><span data-stu-id="96c23-135">Description</span></span>

<span data-ttu-id="96c23-136">下面的示例演示对**GetSharingMetadata**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="96c23-136">The following example shows an error response to a **GetSharingMetadata** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="96c23-137">代码</span><span class="sxs-lookup"><span data-stu-id="96c23-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>The SMTP address format is invalid.</MessageText>
      <m:ResponseCode>ErrorInvalidSmtpAddress</ResponseCode>
      <m:DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="96c23-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96c23-138">See also</span></span>



[<span data-ttu-id="96c23-139">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="96c23-139">GetSharingMetadata</span></span>](getsharingmetadata.md)
  
[<span data-ttu-id="96c23-140">GetSharingMetadataType</span><span class="sxs-lookup"><span data-stu-id="96c23-140">GetSharingMetadataType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataType.aspx)
  
[<span data-ttu-id="96c23-141">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="96c23-141">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md)
  
[<span data-ttu-id="96c23-142">GetSharingMetadataResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="96c23-142">GetSharingMetadataResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataResponseMessageType.aspx)


[<span data-ttu-id="96c23-143">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="96c23-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="96c23-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="96c23-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

