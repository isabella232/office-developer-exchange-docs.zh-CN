---
title: 时区和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: 找出如何时区使用 EWS 托管 API 和 EWS 在 Exchange。
ms.openlocfilehash: fcc8b00acf2b63de04718e13b82191de95bbf2b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753021"
---
# <a name="time-zones-and-ews-in-exchange"></a>时区和 Exchange 中的 EWS

找出如何时区使用 EWS 托管 API 和 EWS 在 Exchange。
  
时区不会多数人授予得多灵感到。 但是，指定日期和时间使用 EWS 托管 API 或 EWS 是一个重要概念。 处理不当 EWS 托管 API 或 EWS 中的时区应用程序可以产生意外的结果。 正确处理时区非常简单，只要您知道如何。
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>处理 EWS 托管 API 中的时区

如果您正在使用 EWS 托管 API，时区，大多数情况下，为您自动处理。 不需要在您的部件的任何显式操作，API 使用的客户端计算机的本地时区，如何处理在后台所有必要的转换。 这是所需的效果，但您有其他选项时，这是很好。
  
一个选项设置[ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性。 此属性控制的所有请求执行 EWS 托管 API 所在的时区。 此属性为只读;将其设置的唯一方法是通过类构造函数。 如果您使用[ExchangeService(System.TimeZoneInfo)](http://msdn.microsoft.com/en-us/library/dd635875%28v=exchg.80%29.aspx)或[ExchangeService （ExchangeVersion、 System.TimeZoneInfo）](http://msdn.microsoft.com/en-us/library/dd636248%28v=exchg.80%29.aspx)构造函数，您可以指定特定的时区作为[System.TimeZoneInfo](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx)对象。 如果您使用不带**何时**对象作为参数的其他构造函数之一， **ExchangeService**类将**TimeZone**属性设置的客户端计算机当前的时区。 
  
**TimeZone**属性表示时区中表示您设置特定的时区还是将其保留为所在的时区的客户端计算机，所有的日期和时间。 EWS 托管 API 公开为[System.DateTime](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx)结构的所有日期/时间属性。 因此，如果设置日期/时间的任何属性，请注意，根据上的**DateTime**对象的[DateTime.Kind](http://msdn.microsoft.com/en-us/library/system.datetime.kind%28v=vs.110%29.aspx)属性值解释您指定的时间。 如果**类型**属性的值设置为**未指定**的**DateTime**值将被解释为在**TimeZone**属性指定的时区。 如果您正在阅读日期/时间属性，用该时区表示所有**DateTime**属性。 
  
如果您是[创建新的约会或会议](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)或[更新现有约会或会议](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)，必须能够重写为新的[约会](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的**TimeZone**中指定的时区。 但是，完全内容，可以覆盖取决于您的目标[EWS 架构版本](ews-schema-versions-in-exchange.md)。 对于所有[ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性的值，您可以设置[Appointment.StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx)要用于该约会或会议的某个特定的时区。 如果您使用的值大于**Exchange2007_SP1** **ExchangeService.RequestedServerVersion**属性，您还可以设置[Appointment.EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx)属性，从而使您可以指定[时区Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx)属性。 但是，记住这些属性只影响创建请求的日期/时间的解释。 如果检索约会，开始和结束时间将仍以表示**TimeZone**属性指定的时区。 
  
如果您正在更新现有约会或会议，您可以通过设置**StartTimeZone**属性和/或**EndTimeZone**属性更改**约会**对象所在的时区。 这样做将使相应 shift 适用次数。 如果已设置为**Exchange2007_SP1** **ExchangeService.RequestedServerVersion** ，无法设置您的**EndTimeZone**属性。将在其位置使用**StartTimeZone**属性的值。 
  
**表 1。EWS 托管 API 中的时区属性**

|**时区属性**|**服务器的最低请求版本**|**说明**|
|:-----|:-----|:-----|
|[TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |如果未设置通过**ExchangeService**类的构造函数，该属性设置为客户端计算机所在的时区。 用此所在的时区表示所有**DateTime**属性创建项目和检索现有项目时。 此时可以重写区域中创建约会和会议请求设置**Appointment.StartTimeZone**和/或**Appointment.EndTimeZone**属性。 如果没有重写**Appointment.StartTimeZone**属性，此时被视为约会和会议创建的时区。  <br/> |
|[StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |如果在新的**约会**对象上设置，此所在的时区用于解释[Appointment.Start](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx)和[Appointment.ReminderDueBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx)属性。 此所在的时区是也将被视为**Appointment**对象创建的时区。  <br/> 当检索现有项目，此属性才信息。 在现有约会的**DateTime**属性的值总是用**ExchangeService.TimeZone**属性指定的时区。  <br/> |
|[EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |如果在新的**约会**对象上设置，此所在的时区用于解释[Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx)属性。  <br/> 当检索现有项目，此属性才信息。 在现有约会的**DateTime**属性的值总是用**ExchangeService.TimeZone**属性指定的时区。  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>处理 EWS 中的时区

如果您正在使用 EWS，时区不会为您自动处理和更复杂的事项。 时区对 EWS 请求和响应的影响取决于多种因素：
  
- [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素中指定的 Exchange 版本 
    
- （如果存在） [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素中指定的时区 
    
- （如果约会或会议上存在） [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)、 [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)或[EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素中指定的时区 
    
- （如果有），XML **dateTime**元素中指定的时区 
    
**DateTime**元素的值指定的时区可以采用三种形式。 您可以阅读中的所有详细信息[XML 架构第 2 部分： 数据类型的第二版](http://www.w3.org/TR/xmlschema-2/#dateTime)，但来解答问题：
  
- **协调世界时 (UTC):** 指定 Z。 例如，`2014-06-06T19:00:00.000Z`
    
- **特定所在的时区：** 指定 + 或-跟小时和分钟数。 例如，`2014-06-06T19:00:00.000-08:00`
    
- **任何时区：** 指定不存在任何时区。 例如，`2014-06-06T19:00:00.000`
    
如果存在于**dateTime**值 （UTC 或特定时区） 中某个时区，该值是始终解释为该所在的时区。 如果存在此参数不时区，然后解释的值取决于其他时区相关元素的特定组合。 
  
**表 2。EWS 和其效果中的时区元素**

|**RequestServerVersion**|**TimeZoneContext 存在？**|**MeetingTimeZone、 StartTimeZone 或存在 EndTimeZone （日历项目和仅 MeetingRequest）？**|**采用 UTC 的日期时间**|**在特定的时区的日期时间**|**不时区的日期时间**|**约会和会议创建所在的时区**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |是  <br/> |是 ( **MeetingTimeZone** )  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)元素包含**MeetingTimeZone**元素中的元素解释为**MeetingTimeZone**元素，其他所有解释为 UTC 时区  <br/> |**MeetingTimeZone**元素中的时区  <br/> |
|**Exchange2007_SP1** <br/> |是  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |否  <br/> |是 ( **MeetingTimeZone** )  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)元素包含**MeetingTimeZone**元素中的元素解释为**MeetingTimeZone**元素，其他所有解释为 UTC 时区  <br/> |**MeetingTimeZone**元素中的时区  <br/> |
|**Exchange2007_SP1** <br/> |否  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
|**Exchange2010**及更高版本  <br/> |是  <br/> |是 （ **StartTimeZone**和/或**EndTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |如果**StartTimeZone**元素存在，[启动](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx)元素的值将被解释为**StartTimeZone**元素中的时区。 否则，这些元素的值被解释为**TimeZoneContext**元素中的时区。  <br/> 如果**EndTimeZone**元素存在，[启动](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)元素的值将被解释为**EndTimeZone**元素中的时区。 否则的**End**元素的值被解释为**TimeZoneContext**元素中的时区。  <br/> 元素之外的[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)被解释为**TimeZoneContext**元素中的时区。  <br/> |如果存在此参数，则为**StartTimeZone**元素中所在的时区中**TimeZoneContext**元素如果没有所在的时区  <br/> |
|**Exchange2010**及更高版本  <br/> |是  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为**TimeZoneContext**元素中的时区  <br/> |**TimeZoneContext**元素中的时区  <br/> |
|**Exchange2010**及更高版本  <br/> |否  <br/> |是 （ **StartTimeZone**和/或**EndTimeZone** ）  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |如果**StartTimeZone**元素存在，[启动](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx)元素的值将被解释为**StartTimeZone**元素中的时区。 否则，这些元素的值被解释为 UTC。  <br/> 如果**EndTimeZone**元素存在，[启动](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)元素的值将被解释为**EndTimeZone**元素中的时区。 否则的**End**元素的值被解释为 UTC。  <br/> 元素之外的[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)或[MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)被解释为 UTC。  <br/> |如果存在此参数，则为**StartTimeZone**元素中所在的时区如果不需要的 UTC  <br/> |
|**Exchange2010**及更高版本  <br/> |否  <br/> |否  <br/> |解释为 UTC  <br/> |解释为值中指示的时区  <br/> |解释为 UTC  <br/> |UTC  <br/> |
   
解释来自服务器的响应，应始终检查每个元素的值并相应地解释值。 Exchange 始终将值中包含某个时区 （UTC 或特定时区）。
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>创建约会和会议时的附加时区注意事项

创建约会或会议时，将应用于的开始时间的时区被视为约会创建所在的时区。 除了控制如何解释 date/times 创建约会或会议时，创建所在的时区具有项上的以下效果：
  
- 如果项目位于全天事件，它可能显示按预期方式如果查看从客户端使用不同的时区比创建所在的时区。 这是时区的因为为创建所在的午夜调整全天事件[创建全天事件的时间](how-to-create-all-day-events-by-using-ews-in-exchange.md)、 开始和结束时间。 该时间将显示在不同的时区的午夜以外的时间形式，所以该项目可能看起来跨越额外天数。 因此，我们建议使用配置用户的主日历客户端的时区来创建全天事件时可能。
    
- 如果项目位于会议，创建所在的时区将显示在接收到的与会者，会议请求的 Outlook 信息栏中如果该时区不同于他们的客户端的时区。
    
## <a name="in-this-section"></a>本节内容

- [通过在 Exchange 使用 EWS 特定时区中创建约会](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 更新约会所在的时区](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Exchange 中的 EWS 架构版本](ews-schema-versions-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 中创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [在 Exchange 使用 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 中创建全天事件](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [DateTime 结构](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx)
    
- [何时类](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

