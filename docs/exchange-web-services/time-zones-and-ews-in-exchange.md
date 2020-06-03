---
title: 时区和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: 了解时区如何与 Exchange 中的 EWS 托管 API 和 EWS 配合使用。
localization_priority: Priority
ms.openlocfilehash: 8435087d7709b77e7562e2b9d50ece58377dd8db
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463746"
---
# <a name="time-zones-and-ews-in-exchange"></a>时区和 Exchange 中的 EWS

了解时区如何与 Exchange 中的 EWS 托管 API 和 EWS 配合使用。
  
时区不是大多数人都能对其进行大量思考的操作。 但是，在使用 EWS 托管 API 或 EWS 指定日期和时间时，它们是一个重要概念。 在 EWS 托管 API 或 EWS 应用程序中，Mishandling 时区可能会产生意外的结果。 正确处理时区非常简单，只要您知道如何操作。
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>处理 EWS 托管 API 中的时区

如果使用 EWS 托管 API，则大多数情况下会自动处理时区。 如果没有任何显式操作，则 API 将使用客户端计算机的本地时区并处理幕后的所有必要转换。 如果这是所需的效果，但您具有其他选项，则这很有用。
  
一个选项是设置[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性。 此属性控制由 EWS 托管 API 执行的所有请求的时区。 此属性是只读的;设置它的唯一方法是通过类构造函数。 如果使用[ExchangeService （TimeZoneInfo）](https://msdn.microsoft.com/library/dd635875%28v=exchg.80%29.aspx)或[ExchangeService （ExchangeVersion、TimeZoneInfo）](https://msdn.microsoft.com/library/dd636248%28v=exchg.80%29.aspx)构造函数，则可以将特定的时区指定为[TimeZoneInfo](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx)对象。 如果使用不采用**TimeZoneInfo**对象作为参数的其他构造函数之一，则**ExchangeService**类会将**时区**属性设置为客户端计算机的当前时区。 
  
无论您是设置特定时区还是将其保留为客户端计算机的时区，所有日期和时间都用**时区**属性所代表的时区表示。 EWS 托管[API 以 system.string 结构的形式](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx)公开所有日期/时间属性。 因此，如果设置任何日期/时间属性，请注意指定的时间将根据**datetime**对象上的[datetime](https://msdn.microsoft.com/library/system.datetime.kind%28v=vs.110%29.aspx)属性值进行解释。 如果**Kind**属性的值设置为 "**未指定**"，则**DateTime**的值将被解释为位于 "**时区**" 属性所指定的时区中。 如果您正在读取日期/时间属性，则所有**DateTime**属性都在该时区中表示。 
  
如果要[创建新的约会或会议](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)或[更新现有约会或会议](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)，则可以替代在新的[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的**时区**中指定的时区。 但是，您可以重写的确切内容取决于您所针对的[EWS 架构版本](ews-schema-versions-in-exchange.md)。 对于[RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性的所有值，可以将 ExchangeService 设置[为对该](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx)约会或会议使用特定的时区。 如果您使用大于**Exchange2007_SP1**的**RequestedServerVersion**属性的值，则还可以设置 ExchangeService 属性，使您可以为[约会的 End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx)属性指定时区。 [Appointment.EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) 但请记住，这些属性仅影响对创建请求的日期/时间的解释。 如果您检索约会，则开始和结束时间仍将用**时区**属性指定的时区表示。 
  
如果要更新现有约会或会议，可以通过设置**StartTimeZone**属性和/或**EndTimeZone**属性来更改**约会**对象的时区。 执行此操作将导致相应的时间发生变化。 如果已将**ExchangeService**设置为**Exchange2007_SP1**，则不能设置**EndTimeZone**属性;将在其位置使用**StartTimeZone**属性的值。 
  
**表1。EWS 托管 API 中的时区属性**

|**时区属性**|**最低服务器请求版本**|**说明**|
|:-----|:-----|:-----|
|[时区](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |如果未通过**ExchangeService**类的构造函数进行设置，则此属性将设置为客户端计算机的时区。 创建项目时和检索现有项目时的所有**DateTime**属性都以该时区表示。 通过设置**StartTimeZone**和/或**EndTimeZone**属性，可以在约会和会议的创建请求中覆盖此时区。 如果未被**StartTimeZone**属性重写，则此时区被视为约会和会议的创建时区。  <br/> |
|[StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |如果在新的 "**约会**" 对象上设置，则此时区用于解释 ReminderDueBy 和 "[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx)"[属性。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) 此时，该时区也被视为**约会**对象的创建时区。  <br/> 检索现有项目时，此属性仅提供信息。 现有约会上**DateTime**属性的值始终以**ExchangeService**属性指定的时区表示。  <br/> |
|[EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |如果在新的 "**约会**" 对象上设置，则此时区用于解释 "[约会. End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) " 属性。  <br/> 检索现有项目时，此属性仅提供信息。 现有约会上**DateTime**属性的值始终以**ExchangeService**属性指定的时区表示。  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>处理 EWS 的时区

如果您使用的是 EWS，则不会自动处理时区，并且会稍微复杂一些。 时区对 EWS 请求和响应的影响方式取决于许多因素：
  
- 在[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素中指定的 Exchange 版本 
    
- 在[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素中指定的时区（如果存在） 
    
- 在[MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)、 [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)或[EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素中指定的时区（如果约会或会议上存在） 
    
- 在 XML **dateTime**元素中指定的时区（如果有） 
    
**DateTime**元素的值中指定的时区可以采用三种形式。 您可以阅读[XML 架构第2部分：数据类型第二版](http://www.w3.org/TR/xmlschema-2/#dateTime)中的所有详细信息，但 paraphrase：
  
- **通用协调时间（UTC）：** 由 "Z" 指定。 例如，  `2014-06-06T19:00:00.000Z`
    
- **特定时区：** 由 "+" 或 "-" 指定，后跟小时和分钟。 例如，  `2014-06-06T19:00:00.000-08:00`
    
- **无时区：** 由缺少任何时区指定。 例如，  `2014-06-06T19:00:00.000`
    
如果**dateTime**值中存在时区（UTC 或特定时区），该值将始终被解释为该时区。 如果不存在任何时区，则值的解释取决于其他与时区相关的元素的特定组合。 
  
**表2。EWS 中的时区元素及其效果**

|**RequestServerVersion**|**有 TimeZoneContext？**|**MeetingTimeZone、StartTimeZone 或 EndTimeZone 是否存在（仅限 CalendarItem 和 MeetingRequest）？**|**UTC 格式的日期时间**|**特定时区中的日期时间**|**不带时区的日期/时间**|**约会和会议创建时区**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |是  <br/> |是（ **MeetingTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |包含**MeetingTimeZone**元素的[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)元素中的元素被解释为**MeetingTimeZone**元素中的时区，其他所有人都解释为 UTC  <br/> |**MeetingTimeZone**元素中的时区  <br/> |
|**Exchange2007_SP1** <br/> |是  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |否  <br/> |是（ **MeetingTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |包含**MeetingTimeZone**元素的[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)元素中的元素被解释为**MeetingTimeZone**元素中的时区，其他所有人都解释为 UTC  <br/> |**MeetingTimeZone**元素中的时区  <br/> |
|**Exchange2007_SP1** <br/> |否  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
|**Exchange2010**及更高版本  <br/> |是  <br/> |是（ **StartTimeZone**和/或**EndTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |如果存在**StartTimeZone**元素，则[Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx)元素的值将被解释为**StartTimeZone**元素中的时区。 否则，这些元素的值将被解释为**TimeZoneContext**元素中的时区。  <br/> 如果存在**EndTimeZone**元素，则[Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)元素的值将被解释为**EndTimeZone**元素中的时区。 否则， **End**元素的值将被解释为**TimeZoneContext**元素中的时区。  <br/> [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)之外的元素被解释为**TimeZoneContext**元素中的时区。  <br/> |**StartTimeZone**元素中的时区（如果存在）、 **TimeZoneContext**元素中的时区（如果不存在）  <br/> |
|**Exchange2010**及更高版本  <br/> |是  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为**TimeZoneContext**元素中的时区  <br/> |**TimeZoneContext**元素中的时区  <br/> |
|**Exchange2010**及更高版本  <br/> |否  <br/> |是（ **StartTimeZone**和/或**EndTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |如果存在**StartTimeZone**元素，则[Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx)元素的值将被解释为**StartTimeZone**元素中的时区。 否则，这些元素的值将被解释为 UTC。  <br/> 如果存在**EndTimeZone**元素，则[Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)元素的值将被解释为**EndTimeZone**元素中的时区。 否则， **End**元素的值将被解释为 UTC。  <br/> [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)之外的元素被解释为 UTC。  <br/> |**StartTimeZone**元素中的时区（如果存在）、UTC （如果存在）  <br/> |
|**Exchange2010**及更高版本  <br/> |否  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
   
解释来自服务器的响应时，应始终检查每个元素的值，并相应地解释该值。 Exchange 将始终在值中包含时区（UTC 或特定时区）。
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>创建约会和会议时的其他时区注意事项

在创建约会或会议时，适用于开始时间的时区被视为约会的创建时区。 除了控制在创建约会或会议时如何解释日期/时间，创建时区对项目具有以下影响：
  
- 如果该项目是全天事件，则它可能会以意外的方式显示，如果从使用不同时区的客户端进行查看。 这是因为[在创建全天事件时](how-to-create-all-day-events-by-using-ews-in-exchange.md)，全天事件的开始和结束时间将调整为创建时区的午夜。 该时间将显示为不同时区中午夜之外的时间，因此该项目可能会跨越额外的天数。 因此，我们建议您使用为用户的主日历客户端配置的时区，以在可能时创建全天事件。
    
- 如果项目是会议，则创建时区将显示在与会者收到的会议请求的 Outlook 信息栏中（如果时区不同于其客户端的时区）。
    
## <a name="in-this-section"></a>本节内容

- [使用 Exchange 中的 EWS 在特定时区中创建约会](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 更新约会的时区](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Exchange 中的 EWS 架构版本](ews-schema-versions-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 Exchange 中的 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 创建全天事件](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [DateTime 结构](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx)
    
- [TimeZoneInfo 类](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

