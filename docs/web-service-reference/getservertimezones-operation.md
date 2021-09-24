---
title: GetServerTimeZones 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 680173e1-e916-466b-b573-5a3182316345
description: GetServerTimeZones 操作从可用于服务器中的时区定义Exchange信息。
ms.openlocfilehash: f46222251729d5e82042f267d4b6293afb16de00
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516949"
---
# <a name="getservertimezones-operation"></a>GetServerTimeZones 操作

**GetServerTimeZones** 操作从可用于服务器中的时区定义Exchange信息。 
  
## <a name="soap-headers"></a>SOAP 标头

**GetServerTimeZones** 操作可以使用下表中列出和描述的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的 RFC3066 区域性。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。  <br/> |
   
## <a name="getservertimezones-request-examples"></a>GetServerTimeZones 请求示例

### <a name="getting-the-name-and-identifier-of-each-time-zone"></a>获取每个时区的名称和标识符

以下代码示例演示如何检索东部标准时间和太平洋标准时区的名称和标识符。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="false">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
        <t:Id>Pacific Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

[TimeZone (元素) ](id-timezone.md) Id 包含所请求的时区定义的标识符。 若要请求所有时区的信息，请省略 [请求中的 Ids](ids.md) 元素。 
  
### <a name="getting-the-full-definition-of-each-time-zone"></a>获取每个时区的完整定义

以下代码示例演示如何检索东部标准时区的完整时区定义。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="true">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

[TimeZone (元素) ](id-timezone.md) Id 包含所请求的时区定义的标识符。 若要请求所有时区的信息，请省略 [请求中的 Ids](ids.md) 元素。 
  
## <a name="getservertimezones-response-examples"></a>GetServerTimeZones 响应示例

### <a name="receiving-the-time-zone-name-and-identifier-only"></a>仅接收时区名称和标识符

**GetServerTimeZones** 响应的以下示例显示对 **GetServerTimeZones** 请求的成功响应，其中 **ReturnFullTimeZoneData** 属性设置为 **false**。 该响应包含东部标准时间和太平洋标准时区的名称和标识符。
  
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
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)" />
            <t:TimeZoneDefinition Id="Pacific Standard Time" Name="(GMT-08:00) Pacific Time (US &amp;amp; Canada)" />
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="receiving-a-full-time-zone-definition"></a>接收完整时区定义

**GetServerTimeZones** 响应的以下示例显示对 **GetServerTimeZones** 请求的成功响应，其中 **ReturnFullTimeZoneData** 属性设置为 **true**。 该响应包含东部标准时区的完整时区定义。
  
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
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)">
              <t:Periods>
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Daylight" />
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Daylight" />
              </t:Periods>
              <t:TransitionsGroups>
                <t:TransitionsGroup Id="0">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>4</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>10</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>-1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
                <t:TransitionsGroup Id="1">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>3</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>2</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>11</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
              </t:TransitionsGroups>
              <t:Transitions>
                <t:Transition>
                  <t:To Kind="Group">0</t:To>
                </t:Transition>
                <t:AbsoluteDateTransition>
                  <t:To Kind="Group">1</t:To>
                  <t:DateTime>2007-01-01T00:00:00</t:DateTime>
                </t:AbsoluteDateTransition>
              </t:Transitions>
            </t:TimeZoneDefinition>
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[GetServerTimeZones](getservertimezones.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)
  
 **GetServerTimeZonesType**


[EWS 操作在Exchange](ews-operations-in-exchange.md)
  
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

