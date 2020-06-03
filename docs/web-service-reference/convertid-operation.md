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
# <a name="convertid-operation"></a>ConvertId 操作

查找有关**ConvertId** EWS 操作的信息。 
  
**ConvertId** Exchange Web 服务（EWS）操作将项目和文件夹标识符转换为 exchange online、exchange Online 作为 Office 365 的一部分以及从 exchange Server 2013 开始的 exchange 内部部署版本之间的格式。 
  
## <a name="using-the-convertid-operation"></a>使用 ConvertId 操作
<a name="bk_usingConvertId"> </a>

您可以使用**ConvertId**操作来转换以下标识符： 
  
- Exchange 2007 的初始发布版本中的 EWS 标识符格式。 这由 `EwsLegacyId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值表示。 
    
- Exchange 2007 SP1 或 Exchange 2010 中的 EWS 的标识符格式。 这由 `EwsId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。
    
- MAPI 标识符，如**PR_ENTRYID**属性中所示。 这由 `EntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值表示。 
    
- 可用性日历事件标识符。 这是**PR_ENTRYID**属性的十六进制编码表示形式。 这由 `HexEntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。
    
- Exchange 存储标识符。 这由 `StoreId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。 **ConvertId**操作不会将公用文件夹标识符从 EWS 标识符转换为存储标识符。 
    
- Outlook Web App 标识符。 这由 `OwaId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示
    
    不支持将从此标识符创建的 Url 传递到 Outlook Web App。 Outlook Web App 标识符适用于 Exchange 2007 和 Exchange 2010。 适用于 Exchange Online 的 Outlook Web App 和从 Exchange Server 2013 开始的 Exchange 版本使用 EWS 标识符。
    
在将公用文件夹标识符从 EWS 标识符转换为 Exchange Online 和 Exchange 2013 中的存储标识符时， **ConvertId**操作不会按预期工作。 您可以手动更新作为解决方法返回的标识符。 若要手动更新标识符： 
  
1. 在应用程序代码中，确定目标项目/文件夹是否位于公用文件夹中。 
    
2. 对 Base64 编码的标识符字符串进行解码。
    
3. 验证类型 "字节（21字节）" 的值是否为7。 值为7表示标识符的格式不正确。
    
4. 跳过前四个字节。 必须将其设置为零。
    
5. 使用以下 GUID 更新接下来的16个字节：1A447390AA6611CD9BC800AA002FC45A
    
6. 更新值为9的下一个字节（类型为 byte）。
    
7. 将标识符更改为 Base64 编码的字符串。
    
> [!NOTE]
> **ConvertId**操作验证给定的 SMTP 地址是否具有有效的格式。 该操作不确定 SMTP 地址是否表示有效邮箱。 
  
**ConvertId**操作可以使用下表中列出的 SOAP 标头。 
  
**表1。ConvertId 操作 SOAP 标头**

|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 这适用于请求。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识适用于请求的操作请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 这适用于响应。  <br/> |
   
## <a name="convertid-operation-request-example"></a>ConvertId 操作请求示例
<a name="bk_usingConvertId"> </a>

以下示例的**ConvertId**请求显示如何从 EWS 标识符转换为 Outlook Web App 标识符。 
  
必须将 SOAP 标头中的[RequestServerVersion](requestserverversion.md)元素设置为 Exchange2007_SP1 或更高版本，才能使此操作生效。 
  
> [!NOTE]
> 项目标识符已缩短，以保持可读性。 
  
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

## <a name="convertid-operation-response-example"></a>ConvertId 操作响应示例
<a name="bk_usingConvertId"> </a>

下面的示例演示对**ConvertId**请求的成功响应。 此响应示例包含 Outlook Web App 标识符。 
  
> [!NOTE]
> Outlook Web App 标识符已缩短，以保持可读性。 
  
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

## <a name="convertid-operation-error-response-example"></a>ConvertId 操作错误响应示例
<a name="bk_usingConvertId"> </a>

下面的示例演示对包含错误类型的标识符格式的请求的响应。
  
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

## <a name="version-differences"></a>版本差异
<a name="bk_ConvertIdVersionDiff"> </a>

在 Exchange 2007 和 Exchange 2007 Service Pack 1 （SP1）的初始发行版之间更改了 EWS 标识符格式。 Exchange Online 作为 Office 365、Exchange Online 和 Exchange 内部部署版本的一部分从 exchange 2010 开始使用 Exchange 2007 SP1 使用的相同标识符格式。
  
**ConvertId**操作将公用文件夹标识符从 EWS 标识符转换为 exchange 2007 和 exchange 2010 中的存储标识符。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_ConvertIdVersionDiff"> </a>

- [转换标识符](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

