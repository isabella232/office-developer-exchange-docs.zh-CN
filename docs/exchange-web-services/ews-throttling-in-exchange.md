---
title: 限制在 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: 了解如何使用 Exchange 时影响 EWS 的限制策略。
ms.openlocfilehash: 64393c173a6fc60cd4be969e8c7457d5b0109713
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354013"
---
# <a name="ews-throttling-in-exchange"></a>限制在 Exchange 中的 EWS

了解如何使用 Exchange 时影响 EWS 的限制策略。
  
**提供者：** Glen 标尺;Michael Mainer，Microsoft Corporation 
  
文章提供有关 EWS 限制在 Exchange Online，Exchange Online 作为 Office 365 的一部分的信息和内部部署 Exchange 2010 开头的 Exchange 版本。 在 Exchange 限制有助于确保通过限制的单个用户或应用程序可以使用的服务器资源数量的服务器的可靠性和正常运行时间。 限制是服务可靠性和功能可能会影响的系统资源过度使用的反应响应。 Exchange 持续监视关键基础结构的资源，如邮箱数据库的运行状况。 高负载因素检测到的降低这些资源的性能时, EWS 连接将受到控制按比例基于每个呼叫者有贡献此高负载条件的金额。 结果是用户可能会在其限制的限制内，仍然遇到瓶颈，直到资源的运行状况回操作级别。
  
在 Exchange，包括 EWS，每个客户端访问协议具有限制策略。 在设计使用 EWS 的应用程序时，务必帐户限制策略，以帮助确保应用程序的可靠性和您的 Exchange 服务器的运行状况。 本文 ews，标识的不同的限制策略和服务限制是否面向的 Exchange Online 或 Exchange 内部部署 Exchange Server 2010 开头的版本。 如果适用，本文还标识限制策略不同版本的 Exchange 中的差异。
  
> [!IMPORTANT]
> 默认限制策略、 Exchange Online 和 Exchange 内部部署的访问限制策略，并限制策略配置不同。 特定的限制设置值才准确的特定的 Exchange 版本。 由于设置值会有所不同跨版本，并且 Exchange 管理员可以更改默认限制策略的内部部署，本文不提供包含默认设置值。 很多重要为您要注意的设计的应用程序功能内节流限制结果，并适当地对限制方案时的注意事项。 
  
如果您是应用程序开发人员，您需要因素到应用程序设计限制。 不同版本的 Exchange 具有不同的默认值为 EWS 限制参数。 旨在访问不同版本的 Exchange 的客户端与服务应用程序将需要考虑这些设置，它们是默认值，Exchange 管理员，设置的自定义值还是，如 Exchange Online，默认情况下设置，而不可供搜索。 限制参数值不能以编程方式发现，因为您的客户端设计规范应包括规划适应节流限制的不同潜在的应用程序。 多线程访问应用程序将大量邮箱，在设计时或在多个客户端访问的同一邮箱时，考虑对默认策略应用于 Exchange 的并发的限制。 
  
## <a name="throttling-policies-that-affect-ews"></a>影响 EWS 的限制策略
<a name="bk_PolicyParameters"> </a>

限制策略在 Office Outlook、 Outlook Web App 和 Exchange ActiveSync 的 Exchange 影响不仅 EWS，而且所有有还客户端连接到 Exchange 服务器，包括协议使用。 
  
运行 Exchange 2010 时， **CPUStartPercent**限制策略可能会影响 EWS 性能。 当 Exchange 的平均 CPU 使用率处理客户端访问服务器上运行 — 包括但不是限于 EWS 过程 — 超过指定此策略的值，入站的请求将延迟以减少 CPU 使用率。 不能更改此策略的值，但了解有关该产品可帮助您解决性能问题。 客户端访问服务器执行此值采样逻辑平均通过滚动窗口 10 秒。 这样，正确响应快速高峰 CPU 利用率的过程。 当超过此阈值时，延迟为 EWS 的入站的连接。 在每次 EWS 请求理论 100 %cpu 使用率情况下，此延迟上限为 500 毫秒 （毫秒）。 如果传递批处理 EWS 请求以获取 100 个项目，则服务器将检查的 CPU 使用率 100 次 （一次每个项目） 的最大延迟为 50 秒。 线性向 CPU 的使用率成比例延迟时间。 在**CPUStartPercent**，延迟为 0 （线程收益），并且会增加线性达 500 毫秒在 100%的 CPU 使用率。 限制策略应用于所有的 Exchange 用户，因为不太可能的 CPU 使用率超过**CPUStartPercent**限制在 Exchange 客户端访问服务器上，因为各个用户或应用程序无法获得影响足够 CPU 使用率服务器操作。 
  
下表列出了影响使用 EWS 的应用程序的限制策略参数。
  
**表 1： 限制影响 EWS 的策略参数**

|**限制策略参数名称**|**适用于**|**说明**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可同时拥有的并发发现搜索连接数。  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可在发现搜索在搜索中包括的关键字的最大数量。  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定要显示的统计信息的关键词数量。  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可在发现搜索在搜索中包括的源邮箱的最大数。  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定可以在就地电子数据展示搜索的邮箱的最大数目而不需要能够查看的统计信息的搜索。  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定电子数据展示搜索预览响应中返回的消息的数。  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |该用户从特定组件上执行操作完全被阻止之前，请定义 EWS 用户的资源消耗量限制。  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |定义 EWS 用户可以被阻止之前使用提升的资源数量的时间量。 这被以毫秒为单位。 此值将为每个组件的单独。  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |定义 EWS 用户的预算再充电频率的速率 （预算增长速率） 在预算时间。  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义 active 推送、 提取、 和流式处理用户可同时拥有特定客户端访问服务器的通知订阅的最大数目。 这是不同的 Exchange 版本不同预算。  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |以秒为单位的 fast 搜索所做的 EWS 中使用 Exchange 搜索继续之前它们超时定义的时间量。Fast 搜索是在[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)中使用高级查询语法 (AQS) 查询字符串进行搜索。  <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |一次一个用户的客户端访问服务器上的内存中定义从[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)或[FindFolder 操作](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)可存在的项的最大数目。 此属性的默认值为 1000年。 此值[回退值](http://technet.microsoft.com/en-us/library/dd297964%28v=exchg.141%29.aspx#fallback)为 1000年。  <br/> 在 Exchange Online 和 Exchange 开头 Exchange 2013 内部部署版本中，不能查询或通过 cmdlet 配置的此限制策略。 在 Exchange Online 和本地版本的 Exchange 开头 Exchange 2013、 [AQS](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)搜索 EWSFindCountLimit 和任何 Exchange 搜索带限制是 250 个结果。 无限制 Exchange 搜索将返回最多 1000年结果。  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |定义每分钟特定用户可以在此期间执行 Active Directory 请求的时间的百分比。  <br/> |
|**EWSPercentTimeInCAS** <br/> |Exchange 2010  <br/> |定义每分钟的特定用户可以在此期间执行客户端访问服务器代码的时间的百分比。  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |定义每分钟的特定用户可以在此期间执行邮箱 RPC 请求的时间的百分比  <br/> |
|**EWSMaxConcurrency** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义特定用户可以针对一次使用 EWS 的 Exchange server 的并发打开连接的数。 Exchange 2010 的默认值为 10。 Exchange 2013 和 Exchange Online 的默认值为 27。  <br/> 此策略应用于除流式处理通知的所有操作。 流式通知使用**HangingConnectionLimit**指示打开可用的流式事件连接数。 有关详细信息，请参阅[我需要考虑哪些限制值？](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义每分钟可以提交的消息的数。  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义为用户在 24 小时内可以解决的收件人数的限制。  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义对收件人的收件箱转接/重定向操作的数量在 24 小时内的限制。  <br/> |
   
> [!CAUTION]
> 未设置为**null**限制策略。 这将设置等于不受限制，这表明未设置限制策略的策略。 
  
## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>显示适用于 Exchange 邮箱的策略
<a name="bk_PolicyCmdlets"> </a>

Exchange 内部部署提供了可用于设置和获取限制策略的 Exchange 命令行管理程序 cmdlet。 Exchange Online 不提供对的限制策略 cmdlet 的访问。
  
您可以使用以下 cmdlet 以显示限制策略的内部部署 Exchange Server 部署：
  
- **Get-throttlingpolicy** — 获取限制设置为一个或多个客户端限制策略。 有关详细信息，请参阅 TechNet 上的[Get-throttlingpolicy](http://technet.microsoft.com/en-us/library/dd351264.aspx) 。 
    
- **Get ThrottlingPolicyAssociation** — 使您能够查看对象和其关联的限制策略之间的关系。 该对象可以是具有邮箱的用户、 没有邮箱或联系人的用户。 有关详细信息，请参阅 TechNet 上的[Get ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459241.aspx) 。 
    
使用以下命令以显示默认限制策略对于 Exchange 2010。
  
**Get-throttlingpolicy |Where-object {$_。IsDefault-eq"True"} |格式列表**
  
使用以下命令以显示 （这相当于默认限制策略在 Exchange 2010） 的全局限制策略在 Exchange 2013。
  
**Get-throttlingpolicy |Where-object {$_。ThrottlingPolicyScope-eq"全局"} |格式列表**
  
使用以下命令来显示限制策略与用户关联在 Exchange 2010 或 Exchange 2013。 用户名称 john@contoso.com 替换为您要为其获取限制策略信息的目标用户的用户名。
  
**Get ThrottlingPolicyAssociation john@contoso.com |格式列表**
  
运行此命令在 Exchange 命令行管理程序将导致类似于以下输出。
  
```powershell
PS C:\>Get-ThrottlingPolicyAssociation john@contoso.com
RunspaceId               : 72153d6-9dce-2fae-8dbd-5ca5f760g2df
ObjectId                 : john
ThrottlingPolicyId       :
Name                     : john
Identity                 : FHXB-28178dom.contoso.com/Users/john
IsValid                  : True
NeedsToSuppressPii       : False
ExchangeVersion          : 0.10 (15.0.0.0)
DistinguishedName        : CN=john,CN=Users,DC=FHXB-28178dom,DC=contoso,DC=com
Guid                     : 2c10dab6-de28-1937-ad8g-535832613a08
```

> [!NOTE]
> 空白**ThrottlingPolicyId**属性时，默认策略应用于邮箱。 
  
您可以设置使用[Set-throttlingpolicy](http://technet.microsoft.com/en-us/library/dd298094.aspx)和[设置 ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459231.aspx) cmdlet 限制 Exchange 服务器上的策略。 您可以创建和删除非默认限制策略使用[New-throttlingpolicy](http://technet.microsoft.com/en-us/library/dd351045.aspx)和[Remove-throttlingpolicy](http://technet.microsoft.com/en-us/library/dd351178.aspx) cmdlet。 
  
> [!TIP]
> 我们建议您设计遵守默认限制策略的应用程序。 仅对默认限制策略，如果客户端应用程序设计无法容纳默认策略进行更改。 注意限制较少的限制策略可能产生负面影响服务可靠性。 

<a name="bk_ThrottlingConsiderations"> </a>

## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>限制使用 EWS 模拟的应用程序的注意事项


[模拟](impersonation-and-ews-in-exchange.md)是使一个帐户以访问多个帐户的授权方法。 时的服务帐户模拟用户，它将充当用户并因此假定已分配给这些用户的权限。 日志文件以模拟用户记录访问。 管理员使用基于角色的访问控制 (RBAC) 来配置模拟通过 Exchange 命令行管理程序。 
  
使用模拟时，预算的所有限制阈值的 Exchange 版本根据不同的应用。 预算也模拟的帐户或服务帐户对计算。 如果您的应用程序是多线程和使针对多个邮箱的并发请求，则应考虑限制阈值将如何影响应用程序的性能。 通常，应注意以下限制对服务帐户，创建使用模拟访问所有邮箱的基于服务的应用程序时： 
  
- 使用模拟时，服务帐户具有一个单独的预算为下列策略参数：
    
  - **EWSMaxConcurrency**
    
  - **EWSPercentTimeInAD**
    
  - **EWSPercentTimeInCAS**
    
  - **EWSPercentTimeInMailboxRPC**
    
  - **EWSMaxSubscriptions**
    
  - **EWSFastSearchTimeoutInSeconds**
    
  - **EWSFindCountLimit**
    
- **EWSMaxConcurrency**预算共享的服务帐户和帐户被模拟为所有连接的 Exchange 版本早于 Exchange 2010 Service Pack 2 (SP2) 更新汇总 4 (RU4)。 开始 Exchange 2010 SP2 RU4，并包含 Exchange Online，服务帐户访问使用从用户**EWSMaxConcurrency**预算的一个单独的预算。 有关 EWS 的更新 Exchange 并发连接限制策略的详细信息，请参阅[说明的更新汇总 4 的 Exchange Server 2010 Service Pack 2](http://support.microsoft.com/kb/2706690)。
    
    流式处理版本的 Exchange 开始 Exchange 2010，并包含 Exchange Online 中的通知的 EWS 具有其他的克隆的**EWSMaxConcurrency**预算从所有其他 EWS 客户端连接。 对所有其他 EWS 操作比单独预算在内流式通知连接。 流式通知最大并发预算是实际两个不同预算： 的所有服务帐户，是一个预算，一个预算是正在模拟的帐户。 流式处理通知在 Exchange Online 和 Exchange 开头 Exchange 2013 版本使用[HangingConnectionLimit](ews-throttling-in-exchange.md#bk_ThrottlingNotifications)限制的连接数。 
    
    例如，假定**EWSMaxConcurrency**等于 5。 服务帐户可以五个并发拉通知连接具有对用户的邮箱，同时为用户时，用户可以具有五个 open 拉通知连接。 
    
- 下表标识**EWSMaxSubscriptions**限制预算之间的服务帐户和帐户模拟的计算方式。 
    
   **表 2: EWSMaxSubscriptions 预算记帐**

   |**Exchange 版本**|**EWSMaxSubscriptions 限制预算记帐**|
   |:-----|:-----|
   |Exchange Online  <br/> |领导针对目标邮箱。  <br/> |
   |Exchange 2013  <br/> |领导针对目标邮箱。  <br/> |
   |Exchange 2010 SP3  <br/> |领导针对目标邮箱。  <br/> |
   |Exchange 2010 SP2  <br/> |领导针对调用帐户。 从 Exchange 2010 SP2 RU4 开始，预算负责针对目标邮箱。  <br/> |
   |Exchange 2010 SP1  <br/> |领导针对调用帐户。  <br/> |
   |Exchange 2010  <br/> |领导针对调用帐户。  <br/> |
   
- 只要模拟是因为**EWSMaxSubscriptions**限制预算负责对正在模拟的帐户，已连接的邮箱的服务帐户可以订阅和接收，流通知数量没有限制正在使用。 正在模拟的帐户，您不能超过_n_并发请求每个目标邮箱，其中_n_是**EWSMaxSubscriptions**值。 如果您不使用模拟，相同的服务帐户可能没有超过_n_并发请求总数。 因此，主要是，通过使用模拟上的服务帐户，您成倍增加可服务的邮箱数。 有关详细信息，请参阅[在 Exchange 维护一组订阅和邮箱服务器之间的关联](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)。
    
- **EWSPercentTimeInMailboxRPC**、 **EWSPercentTimeInCAS**和**EWSPercentTimeInAD**策略参数引用单个线程执行操作。 当应用程序执行多个并发操作时，您应负责累积用户资源的预算进行这些操作的效果。 
    
## <a name="throttling-implications-for-ews-batch-requests"></a>限制的 EWS 批处理请求的影响
<a name="bk_ThrottlingBatch"> </a>

EWS 使您能够由客户端访问服务器执行单个请求到批处理多个项目请求。 这样可以更好的效率和性能。 当 Exchange 服务器执行批处理的请求时，它会检查用户的预算在批处理中的每个项目的执行后。 如果超过预算应用程序，直到该用户的预算具有再充电延迟处理的批次中的下一项。 若要确保使用批处理操作数的应用程序成功运行，限制可以包括在单一批次，并在多个较小的批次，以提高结果的可靠性之间划分大型批次的项目请求数。 批操作对特定限制阈值的效果取决于请求的类型、 项目处理 （例如在**UploadItems**或**ExportItems**操作） 和邮箱内容的大小。 限制策略影响需要更长时间的处理的请求，从而批处理操作数。 因此必须呼叫者将再等待响应，然后调用 EWS 限制为一分钟批处理请求的执行时间，因为无法超时。 
  
若要确定应用程序的最佳批次大小，单位测试使用各种输入执行设置以确保应用程序不会遇到生产环境中的任何错误。 
  
## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>影响 EWS 的限制策略参数搜索操作
<a name="bk_ThrottlingSearch"> </a>

[EWS 中的搜索操作](search-and-ews-in-exchange.md)可能需要大量的时间和资源，具体取决于搜索的运行方式和请求哪些信息。 若要控制搜索过程中的资源使用状况，两个策略参数，才会生效： **EWSFastSearchTimeoutInSeconds**和**EWSFindCountLimit**。 
  
**EWSFastSearchTimeoutInSeconds**策略参数指定的时间，以秒为单位，该 EWS fast 搜索 （也称为内容索引的搜索） 在超时之前运行。快速搜索是通过使用[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)中的高级查询语法 (AQS) 查询字符串进行搜索。
  
您可以通过以下两种搜索 Exchange 邮箱文件夹：
  
- 通过使用 Exchange 存储搜索，在目标搜索范围内执行的所有邮件的顺序扫描。
    
- 通过使用 Exchange 搜索服务 （内容索引）。
    
这两种类型的搜索会导致超时。 如果可能，请使用 Exchange 搜索服务，因为这些搜索通常针对邮箱索引，并使用 AQS 查询。 下面的示例演示如何使用 EWS 和 Exchange 搜索服务执行收件箱 AQS 搜索。
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

如果您不能使用 AQS 搜索，避免使用过于复杂的搜索筛选器。 尝试来避免创建基于计算值，如果查询涉及扩展的 MAPI 属性的搜索筛选器。 AQS 搜索是在 Exchange 2010 中引入的。
  
> [!NOTE]
> 首次运行复杂 Exchange 存储搜索查询，它运行速度很慢并可能超时时间。之后，查询将更快地响应。 有关 Exchange 的后端的详细信息交换期间发生的服务器进程存储搜索查询，请参阅 TechNet 上的[了解的性能影响的高项目计数和受限的视图](http://technet.microsoft.com/en-us/library/cc535025%28EXCHG.80%29.aspx)。 使用**SearchFilter**创建将来，帮助相似的查询的动态限制，但是这些限制是动态的性质，因为它们不是永久或可靠，并最长三天后删除。 
  
**EWSFindCountLimit** policy 参数指定为一个用户同时在客户端访问服务器上的内存**FindItem**或**FindFolder**操作可存在的结果中的项的最大数目。 每个项目或 EWS 处理**FindItem**或**FindFolder**请求中的文件夹是根据预算**EWSFindCountLimit**元素中指定计算在内。 当将响应发送回请求者时，当前呼叫查找计数收费被释放。 超过预算时，服务器将返回到请求者的响应基于**RequestServerVersion**元素的值和请求者是否指定分页。 如果**RequestServerVersion**元素的值表示 Exchange 2010 或更早版本 Exchange，服务器将发送错误代码**ErrorServerBusy**失败响应。 如果**RequestServerVersion**元素的值指示版本的 Exchange 开头 Exchange 2010 SP1 或 Exchange Online 和客户端使用分页，EWS 可能返回的部分结果集而不是一个错误。 您的应用程序应产生预期 EWS 可能不会返回所有项目。 如果**IncludesLastItemInRange**元素的值为 false，应用程序应使新的偏移量与另一个**FindItem**或**FindFolder**请求，并继续之前**IncludesLastItemInRange**元素，则返回 true。 
  
当您使用**FindItem**或**FindFolder**操作时，请务必使用分页。 EWS 托管 API 强制使用分页，但如果您使用其他方法，如 EWS 代理对象或原始 SOAP，您需要显式设置分页。 下面的示例演示如何使用 EWS 托管 API 中的页面。 
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> Exchange 中的默认策略限制为 1000年项目的页面大小。 将页面大小设置为一个值，超过此号码产生任何实际。 
  
应用程序还应负责这一事实_EWSFindCountLimit_限制参数值可能会导致设置的应用程序的并发请求返回的部分结果。 下面的示例演示如何使用 EWS 托管 API 在**MoreAvailable**属性来确保在查询中包含的所有结果。 
  
```cs
ItemView iv = new ItemView(1000);
service.TraceEnabled = false;
FindItemsResults<Item> fiResults = null;
Do 
{
    fiResults = service.FindItems(WellKnownFolderName.Inbox, iv);
    PropertySet itItemPropSet = new PropertySet(BasePropertySet.IdOnly) { EmailMessageSchema.Body };
    //Process Items in Result Set
    iv.Offset += fiResults.Items.Count;
}
while (fiResults.MoreAvailable == true);
```

## <a name="throttling-policies-and-concurrency"></a>限制策略和并发
<a name="bk_ThrottlingConcurrency"> </a>

并发指的特定用户的连接数。 连接保留从开始，直到响应发送给请求者收到的请求。 如果用户尝试进行更多并发请求多于其策略允许，新连接尝试失败。 但是，保持有效现有连接。 限制策略可以通过多种不同的方式影响并发。
  
**EWSMaxConcurrency**限制策略参数可设置特定用户可针对 Exchange 服务器一次拥有的并发连接的数。 若要确定的最大并发连接允许数，请考虑 Outlook 客户端将使用的连接。 Outlook 2007 和 Outlook 2010 使用 EWS 访问可用性和外出 (OOF) 信息。 Mac Outlook 2011 使用 EWS 的所有客户端访问功能。 正在连接到用户邮箱的 Outlook 客户端数，根据用户可用的并发连接数可能会受到限制。 此外，如果您的应用程序使用单个的安全性上下文时同时连接到多个邮箱，务必考虑**EWSMaxConcurrency**策略的值。 有关单一安全环境使用并发连接的详细信息，请参阅上文中的[应用程序使用 EWS 模拟的限制注意事项](#bk_ThrottlingConsiderations)。 
  
同时连接到多个邮箱的应用程序必须能够在客户端跟踪资源使用情况。 由于 EWS 操作是基于请求/响应，可确保您的应用程序函数也在**EWSMaxConcurrency**阈值内通过跟踪发生的请求和响应时开始之间的连接数收到的、 并且确保不超过 10 打开请求同时发生。 
  
**EWSFindCountLimit** policy 参数指定**FindItem**或**FindFolder**操作可用于客户端访问服务器一次一个用户的最大结果大小。 如果应用程序 （或具有潜在的多个应用程序） 使返回 100 个项目每个特定用户的两个并发 EWS **FindItem**请求，根据特定用户的预算**EWSFindCountLimit**费用将 200。 返回的第一个请求，预算将降至 100，并为零第二个请求返回时，将预算。 如果同一应用程序已进行 1000年个项的两个并发请求，预算值将为 2000年个项目，其超过**EWSFindCountLimit**值。 如果项目的用户的预算低于零下, 一个请求会导致错误之前用户的预算重新充电到一个或多。 

<a name="bk_ThrottlingNotifications"> </a>
  
## <a name="throttling-considerations-for-ews-notification-applications"></a>限制 EWS 通知应用程序的注意事项


如果您要构建 EWS 通知使用应用程序推送、 拉，或流式处理通知，您应考虑**EWSMaxSubscriptions** **EWSMaxConcurrency**限制策略和**的含义HangingConnectionLimit**。 
  
**EWSMaxSubscriptions**策略参数指定活动推送、 提取、 和用户可同时拥有特定客户端访问服务器的流式订阅的最大数量。 不同版本的 Exchange 具有不同的默认值为此参数。 用户可以订阅邮箱中的所有文件夹使用**SubscribeToAllFolders**属性-此服务使用单个订阅根据**EWSMaxSubscriptions**预算。 用户可以订阅单个文件夹，每个文件夹订阅计数达到**EWSMaxSubscriptions**预算，最多限制设置由**EWSMaxSubscriptions**参数的值 （例如，用户可以订阅 20 日历如果**EWSMaxSubscriptions**设为 20 的不同邮箱中文件夹）。 
  
有关模拟和**EWSMaxSubscriptions**参数的信息，请参阅上文中的[应用程序使用 EWS 模拟的限制注意事项](#bk_ThrottlingConsiderations)。 
  
**EWSMaxConcurrency** policy 参数也可以是 EWS 通知; 问题例如： 
  
- 当 EWS 递增订阅的所有者的连接数时通知由强制订阅生成。
    
- 在应用程序旨在收听多个用户的邮箱，并用户会收到一条消息，发送到通讯组列表实例的同时通知。
    
如果通知应用程序是多线程，并使同时连接请求以获取有关特定消息已接收的用户帐户的详细信息，则可能会超过**EWSMaxConcurrency**策略限制。 若要为此帐户，请考虑监控应用程序中的并发连接、 包括那些可能使用该服务器，以及实现请求队列的客户端上。 
  
**HangingConnectionLimit**才适用于流式传输通知。 此限制设置在 web.config 文件中，这意味着 Exchange 管理员可以在内部部署 Exchange 服务器上，设置此值，但 Exchange Online 邮箱必须为此限制，这是 3 的 Exchange Online 和 Exchange 2013 中使用的默认值。 若要了解详细信息，请参阅[我需要考虑哪些限制值？](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。
  
## <a name="throttling-policy-and-application-performance"></a>限制策略和应用程序性能
<a name="bk_PercentTimeIn"> </a>

限制策略**PercentTimeIn**以下三个参数会影响客户端访问服务器上的 EWS 应用程序可以使用的时间量： 
  
- **EWSPercentTimeInAD**
    
- **EWSPercentTimeInCAS**
    
- **EWSPercentTimeInMailboxRPC**
    
**PercentTimeIn**策略参数中指定的值指示分配了一个使一个请求的线程的时间量。 该过程假定**EWSPercentTimeInCAS**值为 90，如果一个过程将花费 54 秒的两个并发请求客户端访问服务器上的每个运行代码，例如，使用 108 秒 60 秒窗口。 这表示 180% **EWSPercentTimeInCAS**参数值。 
  
> [!NOTE]
> **EWSPercentTimeInCAS**参数值为**EWSPercentTimeInAD**和**EWSPercentTimeInMailboxRPC**参数的值的重叠超集。 这意味着在客户端访问服务器处理时间支出始终将大于**EWSPercentTimeInAD**和**EWSPercentTimeInMailboxRPC**中的支出。 这是因为进行 Active Directory 或 RPC 调用的 Exchange 组件，它必须已经在运行客户端访问服务器代码。 此外，在处理时间**EWSPercentTimeInCAS**支出不停止时 LDAP 或进行 RPC 调用。 尽管请求可能同步等待来自 Active Directory 域服务 (AD DS) 或 Exchange 存储的响应的进程仍占用的服务器上，线程，因此线程应继续会收取该用法。 
  
应用程序可能需要 60 秒内的 CPU 时间量可能会超过这些节流限制;因此，务必要考虑的数量和类型的正在进行的请求。 例如，同时进行的**ResolveNames**操作大批可能会超过**EWSPercentTimeInAD**策略参数值。 默认限制策略中包含的策略值旨在允许大多数 EWS 应用程序没有问题; 起作用但是，当多线程的高容量应用程序在一个特定的客户端访问服务器上放置大量请求，这可以创建问题。 若要避免此问题，请考虑将打算执行对服务器的批次大小限制。 
  
## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>限制策略和发送大量的电子邮件应用程序
<a name="bk_RateLimits"> </a>

默认限制策略包含三个速率限制策略参数会影响使用 EWS 发送大量邮件或短时间内中采用大型批次发送消息的应用程序。 
  
> [!NOTE]
> 通常情况下，建议您不要使用 EWS 发送批量电子邮件。 使用从事批量邮件服务，以提交常用大型批量电子邮件的 SMTP 主机。 
  
**MessageRateLimit**策略参数指定每分钟可以提交任何 Exchange 客户端，包括 EWS 的消息的数。 默认情况下，此策略设置为每分钟 30 封邮件。 对于一般用户，这通常已足够。 但是，作为一部分开票程序，例如发送电子邮件的大型批次的应用程序可以遇到问题。 当超过此策略限制时，邮箱的邮件传递延迟。 具体而言，邮件发件箱或草稿文件夹中显示的长时间时用户或应用程序提交比**MessageRateLimit**参数指定值的较大邮件数。 请务必考虑这一点尤其在您的应用程序使用的用户通过 Outlook 连接到邮箱开发跟踪系统，传递时。 当延迟的项目存储在发件箱或草稿文件夹中时，用户可能将的解释为错误。 
  
**RecipientRateLimit** policy 参数指定用户在 24 小时内可以解决的收件人数的限制。 例如，如果此值设置为 500，则表示一个 Exchange 邮箱帐户可以发送到不多于 500 个收件人天的邮件。 此限制适用于发送给组织内部和外部的收件人的邮件。 此默认限制可能会导致的一些业务线应用程序的执行结束的月份发票运行，需要将邮件发送到此收件人数超过的问题。 您可以使用启用批处理消息或单独的内部部署出站中继解决方案，以解决此限制的外部服务。 
  
**ForwardeeLimit**策略参数指定的最大收件人可以转发或重定向到通过收件箱规则的邮件数。 此参数不限制可转发或重定向到收件人的邮件数。 
  
## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>为在超出节流限制时生成的错误
<a name="bk_ThrottlingErrors"> </a>

超过了限制策略时，EWS 将生成下表中列出的错误之一。
  
**表 3： 限制限制错误**

|**Error**|**限制策略参数**|**说明**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**EWSMaxConcurrency** <br/> |指示根据服务器所允许的用户策略的更多并发请求。  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |指示用户的限制的策略已超出最大订阅计数。  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |指示搜索操作调用超过的可返回的项目总数。  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC**         **EWSPercentTimeInCAS**         **EWSPercentTimeInAD** <br/> |服务器正忙时发生。 返回与 ErrorServerBusy 错误的 BackOffMilliseconds 值指示客户端它应等待，直到它应重新提交请求的导致响应返回此错误代码的时间量。  <br/> |
   
下表列出了由限制错误返回的 HTTP 状态代码。
  
**返回的限制错误的表 4: HTTP 状态代码**

|**HTTP 状态代码**|**说明**|
|:-----|:-----|
|HTTP 503  <br/> |指示 EWS 请求队列 iis。 客户端应推迟到以后发送其他请求。  <br/> |
|HTTP 500  <br/> |指示内部服务器错误 ErrorServerBusy 错误代码。 这指示客户端应延迟发送到以后的其他请求。 响应可能包含后退调用 BackOffMilliseconds 的提示。 如果存在此参数，则 BackOffMilliseconds 的值应用作直到客户端重新提交请求的持续时间。  <br/> |
|HTTP 200  <br/> |包含与 ErrorInternalServerError 错误代码 EWS 基于架构的错误响应。 可能存在内部 ErrorServerBusy 错误代码。 这指示客户端应延迟发送到以后的其他请求。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 工作负载管理](http://technet.microsoft.com/en-us/library/jj150503.aspx)
- [新 ThrottlingPolicy cmdlet](http://technet.microsoft.com/en-us/library/dd351045.aspx)
- [了解客户端限制策略](http://technet.microsoft.com/en-us/library/dd297964.aspx)
- [ThrottlingPolicy 类](http://msdn.microsoft.com/en-us/library/ff342496%28v=EXCHG.140%29.aspx)
- [限制策略和 EWSFindCountLimit](http://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [在 IIS 日志预算快照](http://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)
- [限制在 Exchange 2010 SP1 中的部署的影响](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Exchange 2010 SP1 中的限制策略关联](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [限制策略和 CPUStartPercent](http://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
    

