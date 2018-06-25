---
title: 建议在 Exchange 使用 EWS 的新的会议时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: 了解如何在 Exchange 使用 EWS 建议 Exchange 客户端应用程序中的新会议时间。
ms.openlocfilehash: f9edd8511332474a728635a6aa369a772da24786
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752865"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>建议在 Exchange 使用 EWS 的新的会议时间

了解如何在 Exchange 使用 EWS 建议 Exchange 客户端应用程序中的新会议时间。
  
建议新时间功能，参与者可以作为 Exchange 日历工作流的一部分建议会议组织者的新会议时间。 当与会者提出新的会议时，组织者可以使用建议的新会议时间更新会议并将更新发送给所有与会者。 您可以让与会者建议新的会议时间之前，您需要确定组织者是否允许建议新的时间。 本文介绍如何确定是否您才能提出新时间以及如何使用 EWS 建议新时间。
  
> [!NOTE]
> EWS 托管 API 无法实现此功能。 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>确定您是否可以使用 EWS 建议会议的新时间
<a name="bk_Determine"> </a>

您才能提出新的会议时间之前，您需要查找对该会议的引用，并确定会议组织者是否配置会议支持建议新的时间。 您可以通过执行以下任一操作来获取对会议的引用： 
  
- 在收件箱中查找会议请求
    
- 在日历中查找约会
    
使用以下步骤可查找会议引用：
  
1. 使用[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作 （或[Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS 托管 API 方法） 查找目标会议请求或日历项目。 或者，可以使用[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS 操作来获取会议请求或日历项目的目标的标识符。 
    
2. 分析**FindItem**操作 （或**Folder.FindItems**方法） 若要获取的会议项目的项标识符的结果。 
    
3. 使用[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作来获取会议响应对象。 
    
以下 XML 显示发送请求的响应对象的项目的内容。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

如果您请求的项标识符，会议开始和结束时间，响应对象集合，并且如果组织者允许建议更改的会议时间的**GetItem**操作响应外观类似于下面的 XML。 该响应对象集合，这表示[ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx)元素，包含有效的日历项目的响应组。 **ProposeNewTime**元素是指示用户可以建议会议的新时间响应对象。 [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx)、 [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)和[DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx)元素表示您可以使用建议新的会议时间，会议组织者的响应对象。 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="propose-a-new-meeting-time-by-using-ews"></a>建议使用 EWS 的新的会议时间
<a name="bk_Propose"> </a>

如果您使用**GetItem**操作获取日历项目或会议请求时，您会收到**ProposeNewTime** response 对象，则您可以使用建议的新会议时间响应。 如果您未收到**ProposeNewTime** response 对象，您将无法建议新的会议时间的日历工作流的一部分。 但是，可以回复组织者要请求新的会议时间。 如果您收到**ProposeNewTime** response 对象，可以通过引用其标识符，响应会议和建议组织者向新的会议时间。 这是其中**ProposeNewTime** response 对象是不同的典型响应对象模式，不响应与**ProposeNewTime**响应对象。 您使用的另一个会议响应对象，如**AcceptItem**、 **TentativelyAcceptItem**或**DeclineItem**，提出新的会议。 此示例使用**AcceptItem**响应对象。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

对此请求的响应包含已添加到在与会者的日历的日历项目的标识符和的会议请求被放在与会者的已删除邮件文件夹的副本。 建议新的时间响应邮件还保存在与会者的已发送邮件文件夹中 (需要查找会议响应消息获取句柄)。
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

与会者使用建议的新会议时间响应时，组织者将收到[MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)消息。 **MeetingResponse**邮件包含建议的新会议组织者的日历中开始时间和结束时间，以及相关联的日历项目的标识符。 组织者可以使用这些信息更新会议其现有日历项。 以下是组织者要为新的会议时间借此过程的**MeetingResponse**消息响应工作流： 
  
1. 确定是否已在**MeetingResponse**设置**ProposedStart**或**ProposedEnd**元素。 如果是这样，转到步骤 2。 如果没有， **MeetingResponse**邮件仅指示参与者已接受、 暂时接受或拒绝会议。 
    
2. 通过使用**AssociatedCalendarItemId**元素中返回的 EWS 标识符获取会议组织者的现有日历项。 
    
3. 原始开始和结束时间与建议的新会议时间进行了比较。 如果向组织者可接受建议的新会议时间，请转到步骤 4。 否则为会议组织者可以忽略的建议的会议时间，或者发送电子邮件响应建议新的会议时间的与会者。
    
4. （可选）执行[GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS 操作呼叫以找出建议的时间将用于所有与会者，包括会议室和资源邮箱。 （您还可用[ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS 托管 API 方法来执行此操作。） 
    
5. 然后，组织者可以使用新的建议的会议时间内更新其会议，并通过[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS 操作 （或[Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS 托管 API 方法） 将更新发送给所有与会者。 
    
下图显示了会议组织者、 与会者和处理 EWS 调用的 Exchange 服务器之间发生的过程。
  
**图 1。建议新的会议时间的过程**

![此图显示计划了新的会议时间后，组织者、Exchange 和参与者之间的工作流。如果组织者允许新的会议计划，则参与者可以使用响应对象提出新的会议时间。](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>版本差异
<a name="bk_Behavior"> </a>

建议新时间功能是在 Exchange 内部版本 15.00.0800.007 中引入的。 在早期版本的 Exchange，EWS 应用程序用户必须将单独的电子邮件发送到会议组织者请求不同的会议时间。 
  
## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 中创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [在 Exchange 使用 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [删除约会，并在 Exchange 使用 EWS 取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

