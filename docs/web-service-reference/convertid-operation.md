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
# <a name="convertid-operation"></a>ConvertId 操作

查找有关**ConvertId** EWS 操作的信息。 
  
**ConvertId** Exchange Web Services (EWS) 操作将转换所接受的 Exchange Online 中，Exchange Online 作为 Office 365 的一部分的格式之间的项目和文件夹标识符和本地 Exchange 启动与 Exchange Server 版本2013。 
  
## <a name="using-the-convertid-operation"></a>使用 ConvertId 操作
<a name="bk_usingConvertId"> </a>

您可以将以下标识符转换使用**ConvertId**操作： 
  
- EWS 的初始发行版 Exchange 2007 中的标识符格式。 这由`EwsLegacyId` [id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值。 
    
- 在 Exchange 2007 SP1 或 Exchange 2010 的 EWS 标识符格式。 这由`EwsId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。
    
- MAPI 的标识符，如**PR_ENTRYID**属性中所示。 这由`EntryId` [id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)枚举中的枚举值。 
    
- 可用性日历事件标识符。 这是**PR_ENTRYID**属性的十六进制编码表示形式。 这由`HexEntryId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。
    
- Exchange 存储区标识符。 这由`StoreId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值。 **ConvertId**操作不能转换公用文件夹标识符从 EWS 标识符与存储标识符。 
    
- Outlook Web App 标识符。 这由`OwaId`中[id 格式](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)的枚举值
    
    不支持传递到 Outlook Web App 创建的此标识符的 Url。 适用于 Exchange 2007 和 Exchange 2010 Outlook Web App 标识符。 Exchange Online 和 Exchange Server 2013 开头的 Exchange 版本的 outlook Web App 使用 EWS 标识符。
    
**ConvertId**操作不未按预期从 EWS 标识符的公用文件夹标识符转换到 Exchange Online 和 Exchange 2013 中的存储标识符时。 您可以手动更新作为一种解决方法返回的标识符。 手动更新标识符： 
  
1. 在应用程序代码中，确定目标项目/文件夹是否在公用文件夹中。 
    
2. 对 Base64 编码标识符字符串进行解码。
    
3. 验证类型字节 （21 字节） 的值为 7。 值为 7 指示标识符格式不正确。
    
4. 跳过前四个字节。 它们必须设置为零。
    
5. 使用下列 GUID 更新下一个 16 字节： 1A447390AA6611CD9BC800AA002FC45A
    
6. 值为 9 更新的下一个字节 （类型字节）。
    
7. 更改为使用 Base64 编码的字符串标识符。
    
> [!NOTE]
> **ConvertId**操作验证给定的 SMTP 地址具有有效的格式。 此操作将不确定的 SMTP 地址是否表示有效的邮箱。 
  
**ConvertId**操作可以使用下表中列出的 SOAP 标头。 
  
**表 1。ConvertId 操作 SOAP 标头**

|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。 这是适用于请求。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求这是适用于请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 这是适用于响应。  <br/> |
   
## <a name="convertid-operation-request-example"></a>ConvertId 操作请求示例
<a name="bk_usingConvertId"> </a>

**ConvertId**请求的下面的示例演示如何从 EWS 标识符将转换为 Outlook Web App 标识符。 
  
此操作能够执行到 Exchange2007_SP1 或更高版本，必须设置中的 SOAP 标头的[RequestServerVersion](requestserverversion.md)元素。 
  
> [!NOTE]
> 已缩短的项标识符，若要保留可读性。 
  
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

## <a name="convertid-operation-response-example"></a>ConvertId 操作响应示例
<a name="bk_usingConvertId"> </a>

下面的示例演示对**ConvertId**请求成功响应。 以下响应示例包含的 Outlook Web App 标识符。 
  
> [!NOTE]
> Outlook Web App 标识符已缩短要保留可读性。 
  
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

## <a name="convertid-operation-error-response-example"></a>ConvertId 操作错误响应示例
<a name="bk_usingConvertId"> </a>

下面的示例演示包含错误的标识符格式类型请求的响应。
  
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

## <a name="version-differences"></a>版本差异
<a name="bk_ConvertIdVersionDiff"> </a>

EWS 标识符格式之间的初始发行版本的 Exchange 2007 和 Exchange 2007 Service Pack 1 (SP1) 发生更改。 Exchange Online 作为 Office 365 的一部分，Exchange Online 和本地版本的 Exchange 与 Exchange 2010 开始使用 Exchange 2007 SP1 使用的相同标识符格式。
  
**ConvertId**操作将公用文件夹标识符从 EWS 标识符转换为 Exchange 2007 和 Exchange 2010 中的存储标识符。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_ConvertIdVersionDiff"> </a>

- [转换标识符](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

