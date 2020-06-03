---
title: 邮箱同步和交换中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: 了解当您使用 EWS 访问 Exchange 时，邮箱同步的工作方式。
localization_priority: Priority
ms.openlocfilehash: 5dc700c7feb9fce6121a27ee73fc1a58e88e643a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456255"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>邮箱同步和交换中的 EWS

了解当您使用 EWS 访问 Exchange 时，邮箱同步的工作方式。
  
Exchange 中的 EWS 使用两种类型的同步来检索邮箱内容和对邮箱内容所做的更改：
  
- 文件夹同步
    
- 项目同步
    
在本文中，您将了解这两种类型的同步、同步的工作方式、同步设计模式和同步最佳实践。
  
## <a name="folder-and-item-synchronization"></a>文件夹和项目同步
<a name="bk_typesofsyncs"> </a>

文件夹同步同步文件夹结构或文件夹层次结构。 项目同步将同步文件夹中的项目。 在同步项目时，您必须单独同步邮箱中的每个文件夹。 您可以在应用程序中使用 EWS 或 EWS 托管 API 来实现文件夹和项目同步。
  
**表1。用于同步文件夹和项目的 EWS 操作和 EWS 托管 API 方法**

|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
发生的同步的范围因是初始同步还是持续同步而有所不同，如下所示：
  
- 初始同步将服务器上的所有文件夹或项目同步到客户端。 初始同步之后，客户端将拥有存储的同步状态以供将来同步。 同步状态表示服务器与客户端通信的所有更改。
    
- 正在进行的同步同步自上次同步以来添加、删除或更改的任何项目或文件夹。 在每个正在进行的同步循环期间，服务器使用同步状态计算要报告给客户端的更改。
    
每个同步方法或操作都会返回更改的列表，而不是实际更改的文件夹或邮件。 对项目和文件夹所做的更改通过以下更改类型进行报告：
  
- 创建—指示应在客户端上创建一个新的项目或文件夹。
    
- Update-指示应在客户端上更改项目或文件夹。
    
- 删除—指示应在客户端上删除某个项目或文件夹。
    
- ReadStateChange for EWS 或 ReadFlagChange for EWS 托管 API —指示项目的读取状态已更改，可以从 "已读" 更改为 "已读"，也可以读取为 "未读"。
    
在 Exchange Online 中，作为 Office 365 的一部分的 Exchange Online 和从 Exchange 2010 SP2 开始的 Exchange 版本，将按从新到旧的顺序返回项目和文件夹。 在早期版本的 Exchange 中，项目和文件夹从最旧到最新返回。
  
## <a name="how-does-ews-synchronization-work"></a>EWS 同步的工作原理是什么？
<a name="bk_howdoesitwork"> </a>

简言之，如果您是第一次同步邮箱，请使用图1中所示的过程。 虽然您可以使用其他[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)，但我们建议对可伸缩应用程序使用此方法。
  
**图1。初始同步设计模式**

![此插图显示初始同步设计模式。客户端调用 SyncFolderHierarchy 和 Load 或 GetItem，获取文件夹，然后调用 SyncFolderItems 和 LoadPropertiesForItems 或 GetItem，获取每个文件夹中的项目。](media/Exchange2013_SyncInitial.png)
  
如果您在客户端上使用现有同步状态来同步邮箱，我们建议您实现设计模式，如图2中所示。 
  
**图2。持续的同步设计模式**

![此插图显示正在进行的同步设计模式。客户端收到通知，然后调用 SyncFolderHierarchy 或 SyncFolderItems，获取属性，然后更新客户端，或者只更新客户端中的读取标记。](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>同步设计模式
<a name="bk_syncpatterns"> </a>

您可以在应用程序中使用两种同步设计模式之一，使邮箱保持最新：基于通知的同步或仅同步方法。
  
基于通知的同步（如[图 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork)中所示）依赖于通知客户端以调用 EWS 托管 API [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)或[SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法或 EWS [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)或[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作的通知。 此类型的同步通常建议用于可伸缩应用程序，但它可能不是每个人的最佳方法。 基于通知的同步具有以下优点： 
  
- 对通知进行了优化，以减少对后端 Exchange 数据库的调用。 事件队列和订阅由邮箱服务器（或 Exchange 2010 中的客户端访问服务器和 Exchange 2007）管理;但是，事件和订阅的管理使用的资源比替代方案更少，这是对 Exchange 数据库的更频繁的同步调用。 此外，Exchange 具有针对通知和订阅的特定[限制策略](ews-throttling-in-exchange.md)，以保护资源的消耗。 
    
但是，使用基于通知的同步还有一些缺点：
  
- 通知会发出干扰，因为大多数方案都涉及针对一个用户意图的多个通知。 对于 "日历" 文件夹，尤其如此。 例如，当收到单个会议请求时，将创建多个项目和文件夹通知，包括通知以创建该项目以及另一个用于修改项目的通知。 缓解此缺点的一种方法是在[Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx)、 [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)、 [GetItem](https://msdn.microsoft.com/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)或[GetFolder](https://msdn.microsoft.com/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx)调用中构建几秒钟的延迟。 在会议请求的情况下，如果您立即调用**GetItem**操作，您可能会有一个调用来创建该项目，另一个则用于修改项目。 相反，通过延迟调用，可以一次调用**GetItem**操作，并同时获取同时包含创建和修改项的更改。 
    
- 在邮箱服务器上对通知进行排队，并将订阅保存在邮箱服务器上。 如果管理订阅的邮箱服务器不可用，则会丢失任何新通知，邮箱将不会同步，并且必须重新订阅通知。
    
- 当通知失败时，您需要规划缓解策略。 这样一来，第二种方法（仅同步设计模式）比基于通知的同步更具弹性，因为它只要求客户端保持同步状态，因此与管理订阅的邮箱服务器之间没有任何相关性问题。
    
如果按建议实现，基于通知的订阅设计模式依赖于： 
  
- 用于确定数据更改*时间*的通知。 
    
- EWS 托管 API **SyncFolderHierarchy**或**SyncFolderItems**方法，或 ews **SyncFolderHierarchy**或**SyncFolderItems**操作来确定已更改的*内容*，并优化返回的同步事件数。 是创建、更新还是删除了新项？ 这就是这些方法所需了解的全部，而不依赖于它们的更改属性列表。 （不要在返回的所有项目或文件夹中执行**GetItem**或**LoadPropertiesForItems**调用）。 
    
- 使用 EWS 托管 API 中的**Load**或**LoadPropertiesForItems**方法，或 ews **GetItem**操作来确定数据更改的*方式*，并根据需要从服务器检索属性，根据返回的数据量组织批处理请求。 接下来是比较客户端上的属性和刚刚从服务器返回的属性，最后是在客户端上创建、删除或修改项目或文件夹。 
    
仅同步方法完全依赖于**SyncFolderItems**和**SYNCFOLDERHIERARCHY** ews 托管 API 方法，或者是**SyncFolderHierarchy**或**SyncFolderItems** ews 操作，可以连续调用，也可以作为定时事件调用。 此选项也有优缺点。 仅同步方法更具弹性，因为同步状态存储在邮箱级别的客户端上，而同步状态和维护通知订阅的任何邮箱服务器之间的唯一关系则不是必需的。 同步方法可经受邮箱故障转移，因为它独立于邮箱服务器。 但是，同步方法会增加用户的延迟时间，因为项目会定期同步，而不是在项目到达时实时同步。 此方法的成本也更高，因为在可能发生任何更改时，您正在调用 Exchange 数据库。 
  
## <a name="synchronization-best-practices"></a>同步最佳实践
<a name="bk_bestpractices"> </a>

对于高度可伸缩的应用程序，我们建议您遵循以下最佳实践来同步您的应用程序中的邮箱：
  
- 调用 EWS 托管 API **SyncFolderItems**或**SyncFolderHierarchy**方法时，使用_propertySet_参数的_IdOnly_值，或者在使用 EWS **SyncFolderHierarchy**或**SyncFolderItems**操作时使用 IdOnly 值的**BaseShape**值来减少[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)对 Exchange 数据库的调用。 您在**SyncFolderItems**或**SyncFolderHierarchy**调用的属性集中请求的属性越多，创建的后端调用就越多。 对每个请求的属性值进行一次新的 RPC 调用，而只进行一个用于检索请求的所有**ItemIds**的 rpc 调用-无论要报告的结果数是多少。 因此， **IdOnly**请求将导致一个数据库调用，而主题和发件人的属性包请求将导致三个数据库调用：一个用于一个**主题**，一个用于**发件人**，另一个用于**ItemId**。
    
- 请勿在同步响应中的每个项目上调用 EWS 托管 API **Load**或**LoadPropertiesForItems**方法，或者 ews **GetItem**或**GetFolder**操作。 而是分析结果;查找不需要检索所有属性的更改，如读取状态更改。 如果响应包括读取状态更改，只需更新客户端上的标志，即可完成操作;无需获取所有项目属性。 并确保您不会通过进行来自同一客户端的更改来重复工作。 例如，如果同步响应包括删除项目，并且在本地客户端上进行了删除，则无需再次删除邮件或获取该项目的所有属性。 
    
- 通过执行以下操作，避免受到限制：
    
  - 当您调用 EWS 托管 API **LoadPropertiesForItems**方法或 ews **GetItem**操作以获取批次中的项时，在请求中的项目不会过多。否则，您可能会受到[限制](ews-throttling-in-exchange.md)。 建议每批次包含10个项目。
    
  - 请勿在过短的时间内进行太多请求。 这也将导致限制，并延长响应时间，而不是缩短它。 
    
  - 如果要批处理项目，请使用与[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素的**Id**和**ChangeKey**属性相同的值对所有项目进行批处理。 
    
  - 如果确实受到限制，请停止发送请求。 重新发送请求将延长恢复工作量。 而是等待后端关闭时间过期，然后再次尝试发送同步请求。
    
- 根据收到的[通知事件](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes)的类型： 
    
  - 对于**NewMail**或**修改**的事件，请调用 ews Managed API **SyncFolderItems**方法或 EWS **SyncFolderItems**操作，因为通知不提供**ChangeKey**，并且通知不会调用读取状态更改。
    
  - 对于**已删除**事件，如果通知订阅在之前的同步之前处于活动状态，则只需在本地删除该事件即可。 您无需在删除后立即调用 EWS Managed API **SyncFolderItems**方法或 ews **SyncFolderItems**操作。 
    
  - 如果**修改**的事件是由读取状态更改导致的，请勿调用 EWS 托管 API **LOADPROPERTIESFORITEMS**方法或 ews **GetItem**操作，只需更改项目上的标志即可。 
    
- 同步日历数据时，请执行以下操作：
    
  - 使用类似于基于通知的同步的方法。 由于**SyncFolderItem**不包含任何日历逻辑，请使用 EWS 托管 api [FindAppointments](https://msdn.microsoft.com/library/dd633767%28v=exchg.80%29.aspx)方法，或使用包含[CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素的 ews [FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)查看两个日期之间的约会，然后调用 EWS 托管 API **LoadPropertiesForItems**方法，或使用 ews **GetItem**操作检索日历项目的项目属性。 
    
  - 请勿使用 EWS 托管 API **FindAppointments**方法进行轮询，或使用**CALENDARVIEW**元素进行 ews **FindItem**操作。 
    
- 同步搜索文件夹时：
    
  - 使用类似于基于通知的同步的方法。 
    
  - 使用通知确定数据更改的时间。
    
  - 由于无法在搜索文件夹中使用**SyncFolderItem** ，因此请使用已排序和分页的 EWS 托管 API [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法，或使用[FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)和[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)元素集的 ews **FindItem**操作来确定已更改的内容。 
    
  - 使用 EWS 托管 API **LoadPropertiesForItems**方法或 ews **GetItem**操作检索数据。 
    
## <a name="filtered-synchronization"></a>筛选的同步
<a name="bk_filteredsync"> </a>

EWS Managed API **SyncFolderItems**方法和 ews **SyncFolderItems**操作使您能够通过在 EWS 托管 API 或 ews 中的[ignore](https://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx)元素中设置_ignoreItemIds_参数，来忽略特定项目（基于其 ItemIds）。 例如，当个人开始答复发送给公司中每个人的电子邮件时，这是理想的选择。 
  
您可能会想，如果特定属性发生更改，是否可以筛选通知（从而仅触发同步）？ 虽然这似乎是合理的，但由于通知订阅是基于更改的类型（创建、更新、删除），而不是基于要更新的属性，因此无法通过这种方式筛选通知。 相反，您可以执行以下操作：
  
- 使用基于通知的订阅设计模式。
    
- 在将_propertySet_参数设置为_IdOnly_时，反复调用 EWS 托管 API **SyncFolderItems**和**SyncFolderHierarchy**方法，以使同步状态成为当前同步状态。 或者，如果使用 EWS，则在**BaseShape**值设置为**IdOnly**的情况下重复调用**SyncFolderHierarchy**和**SyncFolderItems**操作。 
    
- 放弃响应（不要对其进行分析或进行任何属性比较）。
    
- 使用 EWS 托管 API **FindItems**方法或 ews **FindItem**操作和排序和页面预填充所关注的筛选作用域中的项目。 
    
- 使用您的同步状态可继续调用 EWS 托管 API **SyncFolderItems**方法或 ews **SyncFolderItems**操作，但只监视已筛选的项目集中的更改。 如果创建了新项目，则必须查看这些新项目是否在筛选过的范围内。 
    
## <a name="in-this-section"></a>本节内容
<a name="bk_filteredsync"> </a>

- [使用 Exchange 中的 EWS 同步文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 同步项目](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [SyncFolderItems 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy 操作](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [SyncFolderItems 操作](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

