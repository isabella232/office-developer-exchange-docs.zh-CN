---
title: GetServerTimeZones 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 680173e1-e916-466b-b573-5a3182316345
description: GetServerTimeZones 操作返回从 Exchange 服务器可用的时区定义的信息。
ms.openlocfilehash: 9b202d510a599c9082d075228be4c479a2086753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754686"
---
# <a name="getservertimezones-operation"></a><span data-ttu-id="03ed3-103">GetServerTimeZones 操作</span><span class="sxs-lookup"><span data-stu-id="03ed3-103">GetServerTimeZones operation</span></span>

<span data-ttu-id="03ed3-104">**GetServerTimeZones**操作返回从 Exchange 服务器可用的时区定义的信息。</span><span class="sxs-lookup"><span data-stu-id="03ed3-104">The **GetServerTimeZones** operation returns information from time zone definitions that are available on an Exchange server.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="03ed3-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="03ed3-105">SOAP Headers</span></span>

<span data-ttu-id="03ed3-106">**GetServerTimeZones**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="03ed3-106">The **GetServerTimeZones** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="03ed3-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="03ed3-107">**Header**</span></span>|<span data-ttu-id="03ed3-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="03ed3-108">**Element**</span></span>|<span data-ttu-id="03ed3-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="03ed3-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03ed3-110">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="03ed3-110">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="03ed3-111">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="03ed3-111">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="03ed3-112">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="03ed3-112">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="03ed3-113">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="03ed3-113">RequestVersion</span></span>  <br/> |[<span data-ttu-id="03ed3-114">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="03ed3-114">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="03ed3-115">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="03ed3-115">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="03ed3-116">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="03ed3-116">ServerVersion</span></span>  <br/> |[<span data-ttu-id="03ed3-117">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="03ed3-117">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="03ed3-118">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="03ed3-118">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getservertimezones-request-examples"></a><span data-ttu-id="03ed3-119">GetServerTimeZones 请求示例</span><span class="sxs-lookup"><span data-stu-id="03ed3-119">GetServerTimeZones request examples</span></span>

### <a name="getting-the-name-and-identifier-of-each-time-zone"></a><span data-ttu-id="03ed3-120">获取的名称和每个时区的标识符</span><span class="sxs-lookup"><span data-stu-id="03ed3-120">Getting the Name and Identifier of Each Time Zone</span></span>

<span data-ttu-id="03ed3-121">下面的代码示例演示如何检索的名称和标识符在东部标准时间和太平洋标准时间时区。</span><span class="sxs-lookup"><span data-stu-id="03ed3-121">The following code example shows how to retrieve the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="03ed3-122">代码</span><span class="sxs-lookup"><span data-stu-id="03ed3-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="03ed3-123">注释</span><span class="sxs-lookup"><span data-stu-id="03ed3-123">Comments</span></span>

<span data-ttu-id="03ed3-124">[Id (TimeZone)](id-timezone.md)中的每个元素包含所在的时区定义所请求的标识符。</span><span class="sxs-lookup"><span data-stu-id="03ed3-124">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="03ed3-125">要请求的所有时区的信息，请省略请求中的[Id](ids.md)元素。</span><span class="sxs-lookup"><span data-stu-id="03ed3-125">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
### <a name="getting-the-full-definition-of-each-time-zone"></a><span data-ttu-id="03ed3-126">获取每个时区的完整定义</span><span class="sxs-lookup"><span data-stu-id="03ed3-126">Getting the Full Definition of Each Time Zone</span></span>

<span data-ttu-id="03ed3-127">下面的代码示例演示如何检索东部标准时间所在的时区的全职区域定义。</span><span class="sxs-lookup"><span data-stu-id="03ed3-127">The following code example shows how to retrieve the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="03ed3-128">代码</span><span class="sxs-lookup"><span data-stu-id="03ed3-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="03ed3-129">注释</span><span class="sxs-lookup"><span data-stu-id="03ed3-129">Comments</span></span>

<span data-ttu-id="03ed3-130">[Id (TimeZone)](id-timezone.md)中的每个元素包含所在的时区定义所请求的标识符。</span><span class="sxs-lookup"><span data-stu-id="03ed3-130">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="03ed3-131">要请求的所有时区的信息，请省略请求中的[Id](ids.md)元素。</span><span class="sxs-lookup"><span data-stu-id="03ed3-131">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
## <a name="getservertimezones-response-examples"></a><span data-ttu-id="03ed3-132">GetServerTimeZones 响应示例</span><span class="sxs-lookup"><span data-stu-id="03ed3-132">GetServerTimeZones response examples</span></span>

### <a name="receiving-the-time-zone-name-and-identifier-only"></a><span data-ttu-id="03ed3-133">仅接收所在的时区名称和标识符</span><span class="sxs-lookup"><span data-stu-id="03ed3-133">Receiving the Time Zone Name and Identifier Only</span></span>

<span data-ttu-id="03ed3-134">**GetServerTimeZones**响应的下面的示例演示**ReturnFullTimeZoneData**属性设置为**false**的**GetServerTimeZones**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="03ed3-134">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **false**.</span></span> <span data-ttu-id="03ed3-135">则响应中包含的名称和标识符在东部标准时间和太平洋标准时间时区。</span><span class="sxs-lookup"><span data-stu-id="03ed3-135">The response contains the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="03ed3-136">代码</span><span class="sxs-lookup"><span data-stu-id="03ed3-136">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="receiving-a-full-time-zone-definition"></a><span data-ttu-id="03ed3-137">接收全职区域定义</span><span class="sxs-lookup"><span data-stu-id="03ed3-137">Receiving a Full Time Zone Definition</span></span>

<span data-ttu-id="03ed3-138">**GetServerTimeZones**响应的下面的示例演示**ReturnFullTimeZoneData**属性设置为**true**的**GetServerTimeZones**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="03ed3-138">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **true**.</span></span> <span data-ttu-id="03ed3-139">则响应中包含东部标准时间所在的时区的全职区域定义。</span><span class="sxs-lookup"><span data-stu-id="03ed3-139">The response contains the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="03ed3-140">代码</span><span class="sxs-lookup"><span data-stu-id="03ed3-140">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a><span data-ttu-id="03ed3-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="03ed3-141">See also</span></span>



[<span data-ttu-id="03ed3-142">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="03ed3-142">GetServerTimeZones</span></span>](getservertimezones.md)
  
[<span data-ttu-id="03ed3-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="03ed3-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)
  
 <span data-ttu-id="03ed3-144">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="03ed3-144">**GetServerTimeZonesType**</span></span>


[<span data-ttu-id="03ed3-145">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="03ed3-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="03ed3-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="03ed3-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

