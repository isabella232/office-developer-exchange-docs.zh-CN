---
title: ConvertId 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: 查找有关 ConvertId EWS 操作的信息。
ms.openlocfilehash: 04f20d8446ab3117adb3f00ea17f93c068eeffb9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536629"
---
# <a name="convertid-operation"></a>ConvertId 操作

查找有关 **ConvertId** EWS 操作的信息。 
  
**ConvertId** Exchange Web 服务 (EWS) 操作在 Exchange Online 接受的格式、Exchange Online 作为 Office 365 的一部分以及从 Exchange Server 2013 开始本地版本的 Exchange 之间转换项和文件夹标识符。 
  
## <a name="using-the-convertid-operation"></a>使用 ConvertId 操作
<a name="bk_usingConvertId"> </a>

可以使用 **ConvertId** 操作转换以下标识符： 
  
- 2007 年 10 月初版中 EWS 的Exchange格式。 这由  `EwsLegacyId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) 枚举中的枚举值表示。 
    
- 2007 SP1 或 Exchange 2010 中 EWS Exchange格式。 这由  `EwsId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。
    
- MAPI 标识符，如 **PR_ENTRYID** 属性。 这由  `EntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) 枚举中的枚举值表示。 
    
- 可用性日历事件标识符。 这是一个十六进制编码的 PR_ENTRYID **表示形式** 。 这由  `HexEntryId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。
    
- 存储Exchange标识符。 这由  `StoreId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示。 **ConvertId** 操作不会将公用文件夹标识符从 EWS 标识符转换为存储标识符。 
    
- Outlook Web App标识符。 这由 `OwaId` [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)中的枚举值表示
    
    不支持将从此标识符创建的 URL 传递到Outlook Web App URL。 此Outlook Web App标识符适用于 2007 Exchange 2010 Exchange 2010。 Outlook Web App 2013 Exchange Online 2013 Exchange EWS 标识符Exchange Server版本和版本。
    
**ConvertId** 操作在将公用文件夹标识符从 EWS 标识符转换为 Exchange Online 和 Exchange 2013 中的存储标识符时不起作用。 你可以手动更新作为解决方法返回的标识符。 若要手动更新标识符，请执行以下操作： 
  
1. 在应用程序代码中，确定目标项目/文件夹是否位于公用文件夹中。 
    
2. 解码 Base64 编码的标识符字符串。
    
3. 验证类型字节类型 (21 字节) 值为 7。 值 7 表示标识符的格式不正确。
    
4. 跳过前四个字节。 它们必须设置为零。
    
5. 使用以下 GUID 更新接下来的 16 个字节：1A447390AA6611CD9BC800AA002FC45A
    
6. 更新下一个 (字节类型) 值为 9。
    
7. 将标识符更改为 Base64 编码的字符串。
    
> [!NOTE]
> **ConvertId** 操作验证给定的 SMTP 地址是否具有有效的格式。 此操作无法确定 SMTP 地址是否表示有效的邮箱。 
  
**ConvertId** 操作可以使用下表中列出的 SOAP 标头。 
  
**表 1.ConvertId 操作 SOAP 标头**

|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序正在模拟的用户。 这适用于请求。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本 这适用于请求。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 这适用于响应。  <br/> |
   
## <a name="convertid-operation-request-example"></a>ConvertId 操作请求示例
<a name="bk_usingConvertId"> </a>

ConvertId 请求的以下示例演示如何从 EWS 标识符转换为Outlook Web App标识符。 
  
SOAP 标头中的 [RequestServerVersion](requestserverversion.md) 元素必须设置为 Exchange2007_SP1或更高版本，此操作正常运行。 
  
> [!NOTE]
> 已缩短项目标识符以保持可读性。 
  
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

以下示例显示了对 **ConvertId** 请求的成功响应。 此响应示例包含一个Outlook Web App标识符。 
  
> [!NOTE]
> 已Outlook Web App标识符以保留可读性。 
  
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

以下示例显示对包含错误标识符格式类型的请求的响应。
  
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

EWS 标识符格式在 Exchange 2007 的初始发行版和 Exchange 2007 Service Pack 1 (SP1 版本) 。 Exchange Online Office 365、Exchange Online 和本地版本的 Exchange（从 Exchange 2010 开始）的一部分，请使用 Exchange 2007 SP1 使用的相同标识符格式。
  
**ConvertId** 操作将公用文件夹标识符从 EWS 标识符转换为 Exchange 2007 和 Exchange 2010 中的存储标识符。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_ConvertIdVersionDiff"> </a>

- [转换标识符](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

