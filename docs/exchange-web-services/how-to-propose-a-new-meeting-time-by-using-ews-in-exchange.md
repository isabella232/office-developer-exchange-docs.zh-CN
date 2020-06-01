---
title: 使用 Exchange 中的 EWS 建议新的会议时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: 了解如何使用 Exchange 中的 EWS 在 Exchange 客户端应用程序中建议新的会议时间。
ms.openlocfilehash: 4f001bb82d2325624b567412620283619b51f25b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456807"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 建议新的会议时间

了解如何使用 Exchange 中的 EWS 在 Exchange 客户端应用程序中建议新的会议时间。
  
"建议新时间" 功能使与会者能够将新会议时间作为 Exchange 日历工作流的一部分建议给会议组织者。 当与会者提出新会议时，组织者可以使用建议的新会议时间更新会议并将更新发送给所有与会者。 您需要先确定组织者是否允许新的时间建议，然后才能使与会者能够建议新的会议时间。 本文介绍如何确定是否可以建议新时间以及如何使用 EWS 建议新时间。
  
> [!NOTE]
> EWS 托管 API 无法实现此功能。 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>确定是否可以使用 EWS 为会议建议新时间
<a name="bk_Determine"> </a>

在为会议建议新时间之前，需要查找对该会议的引用，并确定会议组织者是否已将会议配置为支持新的时间建议。 您可以通过执行以下任一操作来获取对会议的引用： 
  
- 在收件箱中查找会议请求
    
- 在日历中查找约会
    
若要查找会议引用，请执行以下步骤：
  
1. 使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作（或[FINDITEMS](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) ews 托管 API 方法）查找目标会议请求或日历项目。 或者，也可以使用[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS 操作获取目标会议请求或日历项目的标识符。 
    
2. 分析**FindItem**操作（或**FindItems**方法）的结果，以获取会议项目的项目标识符。 
    
3. 使用[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作获取会议的响应对象。 
    
下面的 XML 显示了发送给请求项目的响应对象的内容。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ResponseObjects"/>
          <t:FieldURI FieldURI="item:Subject"/>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

如果请求项目标识符、会议开始和结束时间、响应对象集合以及组织者允许对会议时间进行建议的更改，则**GetItem**操作响应将如以下 XML 所示。 Response 对象集合（由[ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx)元素表示）包含对日历项目有效的响应集。 **ProposeNewTime**元素是一个 response 对象，该对象指示用户可以为会议建议新时间。 [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx)、 [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)和[DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx)元素代表可用于向会议组织者建议新会议时间的响应对象。 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
              <t:Subject>Competitive analysis: kick off meeting</t:Subject>
              <t:ResponseObjects>
                <t:AcceptItem/>
                <t:TentativelyAcceptItem/>
                <t:DeclineItem/>
                <t:ProposeNewTime/>
                <t:ReplyToItem/>
                <t:ReplyAllToItem/>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2013-11-09T17:00:00Z</t:Start>
              <t:End>2013-11-09T17:30:00Z</t:End>
            </t:MeetingRequest>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="propose-a-new-meeting-time-by-using-ews"></a>使用 EWS 建议新的会议时间
<a name="bk_Propose"> </a>

如果您在使用**GetItem**操作获取日历项目或会议请求时收到**ProposeNewTime**响应对象，则可以使用建议的新会议时间进行响应。 如果您没有收到**ProposeNewTime**响应对象，则不能在日历工作流中建议新的会议时间。 但是，您可以答复组织者以请求新的会议时间。 如果您收到**ProposeNewTime** response 对象，则可以通过引用会议的标识符来响应会议，并向组织者建议新的会议时间。 在这种情况下， **ProposeNewTime** response 对象与典型的响应对象模式不同，因为您不会使用**ProposeNewTime** response 对象进行响应。 您可以使用其他会议响应对象（如**AcceptItem**、 **TentativelyAcceptItem**或**DeclineItem**）建议新会议。 此示例使用**AcceptItem** response 对象。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:CreateItem>
      <m:Items>
        <t:AcceptItem>
          <t:Body BodyType="Text">This time works better for the HiPPO.</t:Body>
          <t:ReferenceItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
          <t:ProposedStart>2013-11-28T04:00:00Z</t:ProposedStart>
          <t:ProposedEnd>2013-11-28T04:30:00Z</t:ProposedEnd>
        </t:AcceptItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

对此请求的响应包含添加到与会者日历中的日历项目的标识符和被放入与会者的 "已删除邮件" 文件夹中的会议请求的副本。 带有新时间建议的响应邮件也保存在与会者的 "已发送邮件" 文件夹中（需要找到会议响应消息才能获取该会议的句柄）。
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAGRmOWE2OWAAA=" ChangeKey="DwAAJsmU"/>
            </t:CalendarItem>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkAGRmOWE2AAABB=" ChangeKey="AAAGJu1A"/>
            </t:MeetingRequest>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

当与会者使用建议的新会议时间进行响应时，组织者将收到一条[MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)消息。 **MeetingResponse**邮件包含建议的新会议开始时间和结束时间，以及组织者日历中关联日历项的标识符。 组织者可以使用该信息更新会议的现有日历项目。 以下是组织者对提出新会议时间的**MeetingResponse**消息做出响应的工作流： 
  
1. 确定是否已在**MeetingResponse**中设置了**ProposedStart**或**ProposedEnd**元素。 如果是这样，请转到步骤2。 如果不是，则**MeetingResponse**消息仅指示与会者是接受、暂时接受还是谢绝了会议。 
    
2. 使用**AssociatedCalendarItemId**元素中返回的 EWS 标识符获取会议组织者的现有日历项。 
    
3. 将最初的开始时间和结束时间与建议的新会议时间进行比较。 如果建议的新会议时间对组织者是可接受的，请转到步骤4。 否则，会议组织者既可以忽略建议的会议时间，也可以向建议新会议时间的与会者发送电子邮件响应。
    
4. Optional执行[GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS 操作调用，了解建议的时间是否适用于所有与会者，包括会议室和资源邮箱。 （也可以使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS 托管 API 方法执行此操作。） 
    
5. 然后，组织者可以使用新的建议会议时间更新其会议，并使用[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS 操作（或[约会. 更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)EWS 托管 API 方法）将更新发送给所有与会者。 
    
下图显示了会议组织者、与会者和处理 EWS 呼叫的 Exchange 服务器之间发生的过程。
  
**图1。建议新会议时间的过程**

![此图显示计划了新的会议时间后，组织者、Exchange 和参与者之间的工作流。如果组织者允许新的会议计划，则参与者可以使用响应对象提出新的会议时间。](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>版本差异
<a name="bk_Behavior"> </a>

"建议新时间" 功能是在 Exchange build 版本15.00.0800.007 中引入的。 在早期版本的 Exchange 中，EWS 应用程序用户必须向会议组织者发送单独的电子邮件，以请求不同的会议时间。 
  
## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

