---
title: GetSharingMetadata 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: eaf29427-ecf8-4a5e-9a54-db2e6414b35e
description: GetSharingMetadata 操作获取标识共享邀请的不透明身份验证令牌。
ms.openlocfilehash: c7b2d021f618abe5e49022949e85aa212184800c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516900"
---
# <a name="getsharingmetadata-operation"></a>GetSharingMetadata 操作

**GetSharingMetadata** 操作获取标识共享邀请的不透明身份验证令牌。 
  
## <a name="soap-headers"></a>SOAP 标头

**GetSharingMetadata** 操作可以使用下表中列出和描述的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。  <br/> |
   
## <a name="getsharingmetadata-request-example"></a>GetSharingMetadata 请求示例

### <a name="description"></a>Description

以下示例演示如何形成请求，以获取标识共享邀请的不透明身份验证令牌。 本示例中，user1@contoso.com 希望将 [IdOfFolderToShare](idoffoldertoshare.md) 元素指定的文件夹与 user1@fabikam.com 和 user2@test.com。 
  
### <a name="code"></a>代码

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

### <a name="comments"></a>备注

[Recipients (ArrayOfSmtpAddressType) ](recipients-arrayofsmtpaddresstype.md)元素包含共享邀请的每个预期收件人的一个[SmtpAddress](smtpaddress.md)元素。 
  
## <a name="successful-getsharingmetadata-response"></a>成功的 GetSharingMetadata 响应

### <a name="description"></a>Description

以下示例显示了对 **GetSharingMetadata** 请求的成功响应。 本示例在对应的 **GetSharingMetadata** 请求中指定了两个收件人：user1@fabrikam.com 和 user2@test.com。 
  
### <a name="code"></a>代码

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

### <a name="comments"></a>备注

该响应包含每个组织的一个 [EncryptedSharedFolderData](encryptedsharedfolderdata.md) 元素，该元素由 **GetSharingMetadata** 请求中指定的有效收件人表示。 
  
**GetSharingMetadata** 请求将成功，即使请求中指定了无效收件人。 [InvalidRecipients](invalidrecipients.md)元素包含有关无效收件人的信息。 有关收件人可能无效的原因的信息，请参阅 [ResponseCode (InvalidRecipientResponseCodeType) ](responsecode-invalidrecipientresponsecodetype.md)。
  
如果所有目标收件人都无效， [则 EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) 元素将为空。 
  
## <a name="getsharingmetadata-error-response"></a>GetSharingMetadata 错误响应

### <a name="description"></a>Description

以下示例显示对 **GetSharingMetadata** 请求的错误响应。 
  
### <a name="code"></a>代码

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

## <a name="see-also"></a>另请参阅



[GetSharingMetadata](getsharingmetadata.md)
  
[GetSharingMetadataType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataType.aspx)
  
[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md)
  
[GetSharingMetadataResponseMessageType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataResponseMessageType.aspx)


[EWS 操作在Exchange](ews-operations-in-exchange.md)
  
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

