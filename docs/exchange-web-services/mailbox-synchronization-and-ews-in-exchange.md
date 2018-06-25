---
title: 邮箱同步和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: 了解当您使用 EWS 访问 Exchange 邮箱同步的工作原理。
ms.openlocfilehash: 7bca2f7b754dcceee99e4bc24519f6e4f6423ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752929"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>邮箱同步和 Exchange 中的 EWS

了解当您使用 EWS 访问 Exchange 邮箱同步的工作原理。
  
Exchange 中的 EWS 使用两种类型的同步检索邮箱内容，并更改为邮箱内容：
  
- 文件夹同步
    
- 项目同步
    
在本文中，您将了解有关同时同步类型、 同步的工作原理、 同步设计模式和同步的最佳实践。
  
## <a name="folder-and-item-synchronization"></a>文件夹和项目同步
<a name="bk_typesofsyncs"> </a>

文件夹同步同步文件夹结构或文件夹层次结构。 项目同步同步文件夹内的项目。 在同步项目时，您必须单独同步的邮箱中每个文件夹。 可以使用 EWS 或 EWS 托管 API 应用程序中实现文件夹和项目同步。
  
**表 1。EWS 操作和用于同步文件夹和项目的 EWS 托管 API 方法**

|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
范围内发生的同步不同，具体取决于它是初始或正在进行同步，，如下所示：
  
- 初始同步同步所有文件夹或客户端到服务器上的项目。 初始同步后，客户端有它存储将来同步的同步状态。 同步状态表示服务器传送给客户端的服务器上的所有更改。
    
- 正在进行同步同步任何项目或文件夹的已添加、 删除或上一次同步后更改。 服务器使用的同步状态计算更改要报告给客户端期间每个正在执行的同步循环。
    
每个同步方法或操作返回更改，而不实际文件夹或更改的邮件的列表。 通过以下更改类型报告项目和文件夹对的更改：
  
- 创建 — 指示应在客户端上创建一个新项目或文件夹。
    
- Update — 指示应在客户端上更改项目或文件夹。
    
- 删除 — 指示项目或文件夹应删除的客户端上。
    
- EWS 或 EWS 托管 API 的 ReadFlagChange ReadStateChange — 指示的项目的读取的状态已更改，从未读读取，或读取为未读。
    
在 Exchange Online 中，为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2010 SP2，Exchange Online 项目和文件夹从降序顺序返回。 在以前版本的 Exchange，项目和文件夹从返回最早到最新。
  
## <a name="how-does-ews-synchronization-work"></a>EWS 同步的工作方式
<a name="bk_howdoesitwork"> </a>

简而言之，如果您第一次同步邮箱，使用过程，如图 1 中所示。 尽管您可以使用其他[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)，建议可扩展应用程序的此方法。
  
**图 1。初始同步设计模式**

![此插图显示初始同步设计模式。客户端调用 SyncFolderHierarchy 和 Load 或 GetItem，获取文件夹，然后调用 SyncFolderItems 和 LoadPropertiesForItems 或 GetItem，获取每个文件夹中的项目。](media/Exchange2013_SyncInitial.png)
  
如果您使用的客户端上现有的同步状态同步邮箱，我们建议您实现的设计模式，如图 2 中所示。 
  
**图 2。正在执行的同步设计模式**

![此插图显示正在进行的同步设计模式。客户端收到通知，然后调用 SyncFolderHierarchy 或 SyncFolderItems，获取属性，然后更新客户端，或者只更新客户端中的读取标记。](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>同步设计模式
<a name="bk_syncpatterns"> </a>

您可以使用两种同步设计模式之一应用程序中保留您的邮箱的最新： 基于通知的同步或仅同步方法。
  
基于通知的同步，如[图 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork)中所示依赖于通知，以通知客户端向 EWS 托管 API [SyncFolderItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)或[SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法或 EWS [SyncFolderHierarchy 发起呼叫](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)或[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作。 此类型的同步，通常建议对于可扩展应用程序，但它可能不是让每个人的最佳方法。 基于通知的同步具有以下优点： 
  
- 通知进行优化以减少对后端 Exchange 数据库调用。 事件队列和订阅管理通过邮箱服务器 （或 Exchange 2010 和 Exchange 2007 中的客户端访问服务器）;但是的事件和订阅管理使用替代方法，这是更频繁地与 Exchange 数据库的同步呼叫比较少的资源。 此外，Exchange 具有特定[限制策略](ews-throttling-in-exchange.md)的通知和订阅，以保护占用的资源。 
    
但是，也有一些缺点使用基于通知的同步：
  
- 因为大多数的方案涉及的一个用户意图的多个通知，通知是噪音太大。 这是尤为的日历文件夹。 例如，当收到一个会议请求时，多个项目和文件夹创建通知，包括通知创建项目，另一个用于修改项。 一种方法，以缓解此缺点是向[负载](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx)、 [LoadPropertiesForItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)、 [GetItem](http://msdn.microsoft.com/en-us/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)或[GetFolder](http://msdn.microsoft.com/en-us/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx)调用构建几秒钟的延迟。 对于会议请求中，如果您立即调用**GetItem**操作，您可能必须创建项目并修改项目的另一个呼叫。 相反，通过延迟呼叫，可以调用一次**GetItem**操作，并获取包括创建和修改项目的同时更改。 
    
- 在邮箱服务器上排队通知和邮箱服务器上保存订阅。 如果管理订阅的邮箱服务器不可用，会丢失任何新的通知，邮箱不同步，以及您将需要重新订阅通知。
    
- 您需要规划缓解策略的事件通知失败。 在这种方式，第二种方法，仅同步设计模式中，是更具弹性比基于通知的同步，因为它只要求客户端维护的同步状态 — 不存在具有关联到邮箱服务器问题管理订阅。
    
如果实现所推荐，，依赖基于通知的订阅设计模式： 
  
- 通知，以确定*何时*更改的数据。 
    
- EWS 托管 API **SyncFolderHierarchy** **SyncFolderItems**方法或 EWS **SyncFolderHierarchy**或**SyncFolderItems**操作来确定*哪些*更改，优化的 sync 事件返回数量。 新项目已在创建、 更新或删除？ 这是您需要知道从这些方法，不依赖于它们的更改的属性列表。 （不做**GetItem**或**LoadPropertiesForItems**呼叫的所有项目或文件夹返回）。 
    
- 若要从服务器根据需要检索属性，组织批处理的请求基于和使用 EWS 托管 API 或 EWS **GetItem**操作中的**负载**或**LoadPropertiesForItems**方法来确定*如何*数据更改在将返回的数据量。 这后跟属性的比较客户端和只返回从服务器，并最终创建、 删除或修改的项或客户端上的文件夹。 
    
仅同步方法完全依赖于**SyncFolderItems**和**SyncFolderHierarchy** EWS 托管 API 方法，或者**SyncFolderHierarchy**或**SyncFolderItems** EWS 操作，您可以呼叫连续或作为定时事件。 有优点和缺点，以及此选项。 仅同步方法是更具弹性，因为在邮箱级别客户端上存储的同步状态和唯一的关系，以及任何之间的同步状态维护通知订阅的邮箱服务器不需要。 同步方法可以排除邮箱故障转移，因为其独立性从邮箱服务器。 但是，同步方法会增加延迟用户因为规定或间歇性逐个同步项目 — 不在实时收到邮件时。 此方法还提供了更多消耗大量资金，因为您要发起呼叫与 Exchange 数据库时可能不发生任何更改。 
  
## <a name="synchronization-best-practices"></a>同步的最佳实践
<a name="bk_bestpractices"> </a>

对于高度可扩展应用程序，我们建议您应用以下最佳实践同步您的应用程序中的邮箱：
  
- 当调用 EWS 托管 API **SyncFolderItems**或**SyncFolderHierarchy**方法使用_IdOnly_值的_属性集_参数，或当使用 EWS **SyncFolderHierarchy**或**SyncFolderItems**操作使用[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)值的**IdOnly**值以减少与 Exchange 数据库的呼叫。 更多的属性设置的属性的**SyncFolderItems**或**SyncFolderHierarchy**中请求呼叫，请创建呼叫的多个后端。 新 RPC 调用的请求，每个属性值而只有一个 RPC 调用来检索所有**ItemIds**请求-无论到报表的结果数。 以便**IdOnly**请求结果在一个数据库调用中，而产生的三个数据库调用的属性包请求的主题和发件人： 一个用于**主题**、**发件人**，和**ItemId**。
    
- 不要调用 EWS 托管 API**负载**或**LoadPropertiesForItems**方法或 EWS **GetItem** **GetFolder**操作，对同步响应中的每个项目。 相反，分析结果;查找不需要要检索的所有属性的更改 like 阅读状态更改。 如果响应包括读取的状态更改，只需更新客户端上的标志，并且您完成;不是需要获取项目的所有属性。 并确保您不重复通过从同一客户端中进行产生的更改的工作量。 例如，如果同步响应包含删除的项目，并删除本地客户端上发生了变化，您无需再次删除邮件，或获取该项目的所有属性。 
    
- 避免获取限制，通过执行以下操作：
    
  - 当执行调用 EWS 托管 API **LoadPropertiesForItems**方法或 EWS **GetItem**操作获取一个批次中的项时，不批处理请求; 中的项过多否则，您可能有[限制](ews-throttling-in-exchange.md)。 我们建议您包含 10 个每批项目。
    
  - 不在太短时间内进行过多的请求。 这将还使限制和增加的响应时间，而不将其缩短。 
    
  - 批处理项目时，如果批处理[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素的所有项目**Id**和**更改密钥**属性相同的值。 
    
  - 如果您执行获取限制，停止发送请求。 重新发送请求将延长恢复工作。 相反，等待的时间过期，关闭后，然后尝试再次发送同步请求。
    
- 根据收到[通知事件](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes)的类型： 
    
  - **NewMail**或**修改**事件调用的 EWS 托管 API **SyncFolderItems**方法或 EWS **SyncFolderItems**操作因为通知不提供**更改密钥**，并且通知不会调用出读状态更改。
    
  - 对于**Deleted**事件，如果通知订阅处于活动状态之前以前同步，只需删除本地的事件。 不需要调用 EWS 托管 API **SyncFolderItems**方法或立即后删除 EWS **SyncFolderItems**操作。 
    
  - 如果**修改**事件由读取的状态更改引起的不调用 EWS 托管 API **LoadPropertiesForItems**方法或 EWS **GetItem**操作，只需更改项目上的标志。 
    
- 同步日历数据时, 继续，如下所示：
    
  - 使用类似于基于通知的同步的方法。 因为**SyncFolderItem**不包括任何日历逻辑，使用 EWS 托管 API [FindAppointments](http://msdn.microsoft.com/en-us/library/dd633767%28v=exchg.80%29.aspx)方法或 EWS [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素来查看两个日期之间的约会，然后呼叫的 EWS 托管 API **LoadPropertiesForItems**方法或要检索的日历项目的项目属性的 EWS **GetItem**操作。 
    
  - 不轮询**CalendarView**元素中使用 EWS 托管 API **FindAppointments**方法或 EWS **FindItem**操作。 
    
- 时同步处理搜索文件夹：
    
  - 使用类似于基于通知的同步的方法。 
    
  - 使用通知来确定数据更改时。
    
  - 因为您无法使用搜索文件夹**SyncFolderItem** ，使用排序和分页 EWS 托管 API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法或 EWS **FindItem**操作[FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)和[SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)元素集，以确定更改内容。 
    
  - 使用 EWS 托管 API **LoadPropertiesForItems**方法或 EWS **GetItem**操作可以检索数据。 
    
## <a name="filtered-synchronization"></a>经筛选的同步
<a name="bk_filteredsync"> </a>

EWS 托管 API **SyncFolderItems**方法和 EWS **SyncFolderItems**操作，可以忽略特定项，通过将_ignoreItemIds_参数设置 EWS 托管 API 或[忽略](http://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx)中基于其 ItemIds，EWS 中的元素。 这是理想时，如个人开始所有答复电子邮件发送到公司中的每个人。 
  
您可能想知道，是否可以筛选我的通知 （并因此仅触发同步） 如果特定属性更改？ 尽管这样看上去合理，因为通知订阅基于更改的类型 （创建、 更新、 删除），而不要更新的属性，您不能筛选这种方式通知。 相反，您可以执行以下操作：
  
- 使用基于通知的订阅设计模式。
    
- 使用_属性集_参数设置为_IdOnly_以使同步状态当前重复调用 EWS 托管 API **SyncFolderItems**和**SyncFolderHierarchy**方法。 或如果使用 EWS，呼叫**SyncFolderHierarchy**和**SyncFolderItems**操作反复**BaseShape**值设置为**IdOnly**。 
    
- 放弃响应 （不分析它，或执行任何属性在比较）。
    
- 使用 EWS 托管 API **FindItems**方法或 EWS **FindItem**操作和排序和页预填充您关注的筛选范围中的项目。 
    
- 使用您的同步状态可以继续调用 EWS 托管 API **SyncFolderItems**方法或 EWS **SyncFolderItems**操作，但仅监视筛选的项目集合中的更改。 如果创建新项，您必须以查看这些新项目是否在您筛选出的范围内。 
    
## <a name="in-this-section"></a>本节内容
<a name="bk_filteredsync"> </a>

- [使用 EWS 在 Exchange 同步文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 同步的项目](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 处理同步相关 EWS 中的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [SyncFolderItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy 操作](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [SyncFolderItems 操作](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

