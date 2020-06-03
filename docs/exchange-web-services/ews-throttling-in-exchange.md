---
title: Exchange 中的 EWS 限制
manager: sethgros
ms.date: 05/10/2019
ms.audience: Developer
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: 了解在使用 Exchange 时影响 EWS 的限制策略。
localization_priority: Priority
ms.openlocfilehash: 0c6ac49629ad4cdb4419cc8638d8e60ecb6509d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455399"
---
# <a name="ews-throttling-in-exchange"></a>Exchange 中的 EWS 限制

了解在使用 Exchange 时影响 EWS 的限制策略。

**提供者：** Glen 缩放;迈克尔• Mainer，Microsoft Corporation

本文提供了有关 Exchange Online 中的 EWS 限制、Exchange Online 作为 Office 365 的一部分以及从 Exchange 2010 开始的 Exchange 内部部署版本的信息。 Exchange 中的限制有助于通过限制单个用户或应用程序可以使用的服务器资源量来确保服务器的可靠性和正常运行时间。 限制是对过度使用系统资源（可能会影响服务可靠性和功能）的反应响应。 Exchange 会持续监视关键基础结构资源（如邮箱数据库）的运行状况。 如果检测到的高负载因子会降低这些资源的性能，则会根据每个呼叫者对此高负载条件的贡献量，成比例地限制 EWS 连接。 结果是，用户可能在其限制内处于限制状态，并且在资源的运行状况恢复为运营水平之前仍将遇到降低的速度。

Exchange 中的每个客户端访问协议（包括 EWS）都具有限制策略。 在设计使用 EWS 的应用程序时，请务必考虑限制策略，以帮助确保应用程序的可靠性和 Exchange 服务器的运行状况。 本文针对 EWS 确定了不同的限制策略和服务限制，无论您是面向 Exchange Online 还是从 Exchange Server 2010 开始的 Exchange 内部版本。 如果适用，本文还标识不同版本的 Exchange 中限制策略之间的差异。

> [!IMPORTANT]
> Exchange Online 和 Exchange 本地 Exchange 之间的默认限制策略、对限制策略的访问和限制策略配置有所不同。 特定限制设置值仅对 Exchange 的特定版本是准确的。 由于各个版本的设置值各不相同，并且 Exchange 管理员可以更改本地部署的默认限制策略，因此本文不提供默认的设置值。 更重要的是，要了解有关在限制限制内工作的应用程序的设计和对限制方案做出相应反应的考虑事项。

如果您是应用程序开发人员，则需要将限制因素转换为应用程序设计。 不同版本的 Exchange 具有不同的 EWS 限制参数的默认值。 用于访问不同 Exchange 版本的客户端和服务应用程序将需要考虑这些设置，无论这些设置是默认值、Exchange 管理员设置的自定义值，还是默认设置且不可检测到的 Exchange Online。 由于无法以编程方式发现限制参数值，因此客户端设计规范应包括应用程序适应不同潜在限制限制的计划。 当您设计将访问大量邮箱的多线程应用程序时，或者当多个客户端访问相同的邮箱时，请考虑默认策略适用于 Exchange 的并发性限制。

## <a name="throttling-policies-that-affect-ews"></a>影响 EWS 的限制策略

Exchange 中的限制策略不仅影响 EWS，还影响到 Exchange 服务器的所有客户端连接，包括 Office Outlook、Outlook Web App 和 Exchange ActiveSync 使用的协议。

当您运行 Exchange 2010 时， **CPUStartPercent**限制策略可能会影响 EWS 性能。 在客户端访问服务器上运行的 Exchange 进程的平均 CPU 使用率（包括但不限于 EWS 进程）超过此策略指定的值时，将延迟入站请求以降低 CPU 使用率。 您不能更改此策略的值，但知道它可以帮助您解决性能问题。 客户端访问服务器为此值执行的采样逻辑是10秒滚动时段的平均值。 这样一来，该过程可以适当地响应 CPU 使用率中的快速峰值。 超过此阈值时，到 EWS 的入站连接将延迟。 此延迟的上限为500毫秒（毫秒），每个 EWS 请求理论100% 的 CPU 使用率。 如果传递了获取100个项目的批处理 EWS 请求，则服务器将检查 CPU 使用100的次数（每个项目一次），最大延迟为50秒。 延迟时间与 CPU 使用率成正比。 在**CPUStartPercent**中，延迟为0（线程产生），并且它在100% 的 CPU 使用率下线性增加到500毫秒。 由于限制策略适用于所有 Exchange 用户，因此 CPU 使用率不太可能超过 Exchange 客户端访问服务器上的**CPUStartPercent**限制，因为单个用户或应用程序无法获得足够的 cpu 使用率来影响服务器操作。

下表列出了影响使用 EWS 的应用程序的限制策略参数。

**表1：影响 EWS 的限制策略参数**

|**限制策略参数名称**|**应用于**|**说明**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可以同时拥有的并发发现搜索连接数。  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可在发现搜索中包含的最大关键字数。  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定要为其显示统计信息的关键字的数目。  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定用户可在发现搜索中包含的源邮箱的最大数量。  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定在就地电子数据展示搜索中可以搜索的最大邮箱数，不能查看统计信息。  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |指定电子数据展示搜索预览响应中返回的邮件数。  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |在完全阻止用户在特定组件上执行操作之前，为 EWS 用户定义资源消耗量限制。  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |定义在限制时，EWS 用户可使用已提升资源量的时间量。 此值以毫秒为单位计量。 每个组件的此值会分别设置。  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |定义在预算时间中，EWS 用户的预算为补给（预算增长率）的速率。  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义用户可一次在特定客户端访问服务器上拥有的活动推送、请求和流式处理通知订阅的最大数量。 对于不同的 Exchange 版本，这是不同的预算。  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |定义通过在 EWS 停止之前使用 EWS 中的 Exchange 搜索进行快速搜索所进行的时间量（以秒为单位）。Fast 搜索是使用[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)中的高级查询语法（AQS）查询字符串进行的搜索。  <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义一个用户可在客户端访问服务器上的内存中一次同时存在的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)或[FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)中的最大项目数。 此属性的默认值为1000。 此值的[回退值](https://technet.microsoft.com/library/dd297964%28v=exchg.141%29.aspx#fallback)为1000。  <br/> 在 exchange Online 和 Exchange 内部部署版本中，从 Exchange 2013 开始，不能通过 cmdlet 查询或配置此限制策略。 在 exchange Online 和 Exchange 内部部署版本中，从 Exchange 2013 开始， [AQS 搜索](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)的 EWSFindCountLimit 和任何具有限制的 Exchange 搜索都是250结果。 没有限制的 Exchange 搜索将返回最大为1000的结果。  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |定义特定用户可以执行 Active Directory 请求的时间百分比（以分钟为单位）。  <br/> |
|**Ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas** <br/> |Exchange 2010  <br/> |定义特定用户可以执行客户端访问服务器代码的每分钟时间的百分比。  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |定义特定用户可以执行邮箱 RPC 请求的时间百分比（以分钟为单位）  <br/> |
|**限制** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义特定用户在一次使用 EWS 的 Exchange 服务器可以对其进行的并发打开连接数。 Exchange 2010 的默认值为10。 Exchange 2013 和 Exchange Online 的默认值为27。  <br/> 此策略适用于除流通知之外的所有操作。 流式通知使用**HangingConnectionLimit**指示可用的打开流事件连接的数量。 有关详细信息，请参阅[我需要考虑哪些限制值？](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义每分钟可以提交的邮件数。  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义在24小时内用户可以处理的收件人数的限制。  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |定义24小时内收件箱转发/重定向操作的收件人数限制。  <br/> |
|**ConcurrentSyncCalls** <br/> |Exchange 2019  <br/> Exchange 2016  <br/> Exchange Online  <br/> |定义对用户的并发同步调用（SyncFolderHierarchy、SyncFolderItems）数量的限制。 <br/> |

> [!CAUTION]
> 不要将限制策略设置为**null**。 这会将策略设置为等于无限制，这表示不设置限制策略。

## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>显示应用于 Exchange 邮箱的策略

Exchange 本地部署提供了可用于设置和获取限制策略的 Exchange 命令行管理程序 cmdlet。 Exchange Online 不提供对限制策略 cmdlet 的访问权限。

您可以使用以下 cmdlet 来显示本地 Exchange Server 部署的限制策略：

- **ThrottlingPolicy** —获取一个或多个限制策略的客户端限制设置。 有关详细信息，请参阅 TechNet 上[的 ThrottlingPolicy](https://technet.microsoft.com/library/dd351264.aspx) 。

- **Set-throttlingpolicyassociation** —使您能够查看对象与其关联的限制策略之间的关系。 该对象可以是具有邮箱的用户、没有邮箱的用户或联系人。 有关详细信息，请参阅 TechNet 上[的 set-throttlingpolicyassociation](https://technet.microsoft.com/library/ff459241.aspx) 。

使用以下命令显示 Exchange 2010 的默认限制策略。

**ThrottlingPolicy |其中-对象 {$ _。IsDefault-eq "True"} |格式-列表**

使用以下命令在 Exchange 2013 中显示全局限制策略（相当于 Exchange 2010 中的默认限制策略）。

**ThrottlingPolicy |其中-对象 {$ _。ThrottlingPolicyScope-eq "Global"} |格式-列表**

使用以下命令可显示与 Exchange 2010 或 Exchange 2013 中的用户关联的限制策略。 将用户名 john@contoso.com 替换为要获取其限制策略信息的目标用户的用户名。

**Set-throttlingpolicyassociation john@contoso.com |格式-列表**

在 Exchange 命令行管理程序中运行此命令会生成与以下内容类似的输出。

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
> 如果**ThrottlingPolicyId**属性为空，则会将默认策略应用于邮箱。

您可以使用[ThrottlingPolicy](https://technet.microsoft.com/library/dd298094.aspx)和[Set-throttlingpolicyassociation](https://technet.microsoft.com/library/ff459231.aspx) cmdlet 在 Exchange 服务器上设置限制策略。 您可以使用[ThrottlingPolicy](https://technet.microsoft.com/library/dd351045.aspx)和[ThrottlingPolicy](https://technet.microsoft.com/library/dd351178.aspx) cmdlet 创建和删除非默认限制策略。

> [!TIP]
> 建议您将应用程序设计为遵循默认限制策略。 如果客户端应用程序设计无法容纳默认策略，则仅对默认限制策略进行更改。 请注意，限制较少的限制策略可能会对服务可靠性产生负面影响。

## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>使用 EWS 模拟的应用程序的限制注意事项

[模拟](impersonation-and-ews-in-exchange.md)是一种允许单个帐户访问多个帐户的授权方法。 当服务帐户模拟用户时，它将充当用户，因此假定分配给这些用户的权限。 日志文件以模拟用户的形式记录访问权限。 管理员使用基于角色的访问控制（RBAC）通过 Exchange 命令行管理程序配置模拟。

使用模拟时，所有限制阈值的预算将根据 Exchange 版本的不同而有所不同。 预算是依据模拟的帐户或服务帐户计算得出的。 如果您的应用程序是多线程的，并对多个邮箱进行了并发请求，则应考虑限制阈值将如何影响应用程序的性能。 通常，在创建使用模拟访问所有邮箱的基于服务的应用程序时，请注意服务帐户的以下限制：

- 使用模拟时，服务帐户对以下策略参数具有单独的预算：

  - **限制**

  - **EWSPercentTimeInAD**

  - **Ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**

  - **EWSPercentTimeInMailboxRPC**

  - **EWSMaxSubscriptions**

  - **EWSFastSearchTimeoutInSeconds**

  - **EWSFindCountLimit**

- **限制**预算对服务帐户和模拟的帐户进行共享，以供早于 Exchange 2010 service Pack 2 （SP2）更新汇总4（RU4）的 exchange 版本的所有连接。 从 Exchange 2010 SP2 RU4 （包括 Exchange Online）开始，服务帐户访问使用来自用户**限制**预算的单独预算。 有关对 EWS 的 Exchange 并发连接限制策略的更新的详细信息，请参阅[Exchange Server 2010 Service Pack 2 更新汇总4说明](https://support.microsoft.com/kb/2706690)。

    从 exchange 2010 开始的 Exchange 版本中的 EWS 流通知（包括 Exchange Online）具有来自所有其他 EWS 客户端连接的其他克隆的**限制**预算。 与所有其他 EWS 操作相比，流通知连接与单独的预算进行计数。 流式通知最大并发预算实际上是两个不同的预算：一个预算适用于所有服务帐户，而一个预算用于模拟的帐户。 Exchange Online 中的流通知和从 Exchange 2013 开始的 Exchange 版本使用[HangingConnectionLimit](#throttling-considerations-for-ews-notification-applications)来限制连接数。

    例如，假设**限制**等于5。 用户可以具有5个打开的拉取通知连接，而服务帐户可以同时为用户的邮箱提供五个并发的拉取通知连接。

- 下表标识了如何在服务帐户与要模拟的帐户之间计算**EWSMaxSubscriptions**限制预算。

   **表2： EWSMaxSubscriptions 预算记帐**

   |**Exchange 版本**|**EWSMaxSubscriptions 限制预算记帐**|
   |:-----|:-----|
   |Exchange Online  <br/> |针对目标邮箱收费。  <br/> |
   |Exchange 2013  <br/> |针对目标邮箱收费。  <br/> |
   |Exchange 2010 SP3  <br/> |针对目标邮箱收费。  <br/> |
   |Exchange 2010 SP2  <br/> |针对呼叫帐户收费。 从 Exchange 2010 SP2 RU4 开始，将针对目标邮箱对预算进行计费。  <br/> |
   |Exchange 2010 SP1  <br/> |针对呼叫帐户收费。  <br/> |
   |Exchange 2010  <br/> |针对呼叫帐户收费。  <br/> |

- 由于**EWSMaxSubscriptions**限制预算针对所模拟的帐户进行了计费，因此，只要使用模拟，服务帐户的邮箱数就无限制即可订阅和接收流式通知。 对于要模拟的帐户，每个目标邮箱的并发请求数不能超过_n_个，其中_n_是**EWSMaxSubscriptions**值。 如果您没有使用模拟，则同一个服务帐户的并发请求总数不能超过_n_个。 因此，好处在于是通过对服务帐户使用模拟，以指数方式增加可服务的邮箱数。 有关详细信息，请参阅[维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)。

- **EWSPercentTimeInMailboxRPC**、 **ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**和**EWSPercentTimeInAD**策略参数是指由单个线程执行的操作。 当应用程序执行多个并发操作时，应考虑这些操作对用户资源预算的累积影响。

## <a name="throttling-implications-for-ews-batch-requests"></a>EWS 批处理请求的限制影响

EWS 使您可以将多个项目请求成批转换为客户端访问服务器执行的单个请求。 这样可以提高效率和性能。 当 Exchange 服务器执行批请求时，它会在批处理中的每个项目执行后检查用户的预算。 如果应用程序超出预算，则在批处理中对下一项的处理将延迟到该用户的预算已补给。 若要确保使用批处理操作的应用程序成功运行，请限制单个批处理中可包含的项目请求数，并将大型批次分成多个较小的批次，以提高结果的可靠性。 批处理操作对特定限制阈值的影响取决于请求的类型、要处理的项目的大小（例如，在**UploadItems**或**ExportItems**操作中）和邮箱内容。 限制策略通过使请求的处理时间较长而影响批处理操作。 因此，调用方将需要等待更长时间进行响应，因为 EWS 将批处理请求的执行时间限制为一分钟，所以调用可能会超时。

若要确定应用程序的最佳批处理大小，请使用各种输入集执行单元测试，以确保应用程序不会在生产环境中遇到任何错误。

## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>影响 EWS 搜索操作的限制策略参数

[EWS 中的搜索操作](search-and-ews-in-exchange.md)可能需要大量的时间和资源，具体取决于搜索的运行方式以及请求的信息。 若要控制搜索期间的资源使用情况，两个策略参数将生效： **EWSFastSearchTimeoutInSeconds**和**EWSFindCountLimit**。

**EWSFastSearchTimeoutInSeconds**策略参数指定 EWS 快速搜索（也称为内容索引搜索）在超时之前运行的时间量（以秒为单位）。Fast search 是在[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)中使用高级查询语法（AQS）查询字符串进行的搜索。

您可以通过以下两种方式搜索 Exchange 邮箱文件夹：

- 通过使用 Exchange 存储搜索，将对目标搜索范围内的所有邮件执行顺序扫描。

- 通过使用 Exchange 搜索服务（内容索引）。

这两种类型的搜索都可能导致超时。 如果可能，请使用 Exchange Search 服务，因为这些搜索通常针对邮箱索引进行定位，并使用 AQS 查询。 下面的示例演示如何使用 EWS 和 Exchange 搜索服务执行 AQS 的收件箱搜索。

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

如果不能使用 AQS 搜索，请避免使用过于复杂的搜索筛选器。 如果查询涉及扩展 MAPI 属性，还应尽量避免基于计算值创建搜索筛选器。 AQS 搜索是在 Exchange 2010 中引入的。

> [!NOTE]
> 第一次运行复杂的 Exchange 存储搜索查询时，它运行速度非常慢，并且可能会超时。之后，查询的响应速度会更快。 有关 Exchange 存储搜索查询过程中出现的后端 Exchange server 进程的详细信息，请参阅了解 TechNet 上的[高项目计数和受限视图对性能的影响](https://technet.microsoft.com/library/cc535025%28EXCHG.80%29.aspx)。 使用**过滤**创建一个动态限制，在将来可帮助进行类似的查询，但由于这些限制在本质上是动态的，因此它们不是永久性的或可靠的，并且在最多三天后被删除。

**EWSFindCountLimit**策略参数指定一个用户可以同时存在于客户端访问服务器上的内存中的**FindItem**或**FindFolder**操作结果中的最大项目数。 将**FindItem**或**FindFolder**请求中的 EWS 进程的每个项目或文件夹与**EWSFindCountLimit**元素中指定的预算进行计数。 将响应发送回请求者时，将释放当前呼叫的查找计数费用。 超出预算时，服务器返回给请求者的响应基于**RequestServerVersion**元素值，以及请求者是否指定分页。 当**RequestServerVersion**元素的值指示 exchange 2010 或早期版本的 exchange 时，服务器会发送错误代码为**ErrorServerBusy**的失败响应。 如果**RequestServerVersion**元素的值指示从 EXCHANGE 2010 SP1 或 exchange Online 开始的 exchange 版本，并且客户端使用分页，则 EWS 可能返回部分结果集而不是错误。 您的应用程序应预期 EWS 不会返回所有项目。 如果**IncludesLastItemInRange**元素的值为 false，应用程序应使用新的偏移量创建另一个**FindItem**或**FindFolder**请求，并继续操作，直到**IncludesLastItemInRange**元素返回 true。

在使用**FindItem**或**FindFolder**操作时，使用分页非常重要。 EWS 托管 API 强制使用分页，但如果您使用的是其他方法（如 EWS 代理对象或原始 SOAP），则需要显式设置分页。 下面的示例演示如何在 EWS 托管 API 中使用分页。

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> Exchange 中的默认策略将页面大小限制为1000个项目。 将页面大小设置为大于此数字的值不会产生实际效果。

应用程序还应考虑到这一点， _EWSFindCountLimit_限制参数值可能会导致为发出并发请求的应用程序返回部分结果集。 下面的示例演示如何在 EWS 托管 API 中使用**MoreAvailable**属性，以确保所有结果都包含在查询中。

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

Concurrency 指特定用户的连接数。 在收到请求后，才会将连接保留一段时间，直到向请求者发送响应。 如果用户尝试生成超过其策略允许的并发请求，则新连接尝试将失败。 但是，现有的连接仍然有效。 限制策略可通过多种不同的方式影响并发性。

**限制**限制策略参数设置特定用户一次可对 Exchange 服务器进行的并发连接数。 若要确定允许的最大并发连接数，请考虑 Outlook 客户端将使用的连接。 Outlook 2007 和 Outlook 2010 使用 EWS 访问可用性和外出（OOF）信息。 Mac Outlook 2011 使用 EWS 实现所有客户端访问功能。 根据主动连接到用户邮箱的 Outlook 客户端的数量，可用于用户的并发连接数可能会受到限制。 此外，如果您的应用程序必须在使用单个安全上下文时同时连接到多个邮箱，则务必要考虑**限制**策略的价值。 有关将单个安全上下文与并发连接一起使用的详细信息，请参阅本文前面的[使用 EWS 模拟的应用程序的限制注意事项](#throttling-considerations-for-applications-that-use-ews-impersonation)。

同时连接到多个邮箱的应用程序必须能够跟踪客户端上的资源使用情况。 由于 EWS 操作是基于请求/响应的，因此您可以通过跟踪请求的开始和收到的响应之间发生的连接数以及何时收到响应，从而确保您的应用程序在**限制**阈值中正常运行，并确保同时发生10个以上的打开请求。

**EWSFindCountLimit**策略参数指定**FindItem**或**FindFolder**操作可以同时在客户端访问服务器上为一个用户使用的最大结果大小。 如果某个应用程序（或潜在的多个应用程序）生成两个并发的 EWS **FindItem**请求，每个请求为特定用户返回100个项目，则对该特定用户的预算的**EWSFindCountLimit**费用将为200。 当第一个请求返回时，预算将下降到100，当第二个请求返回时，预算将下降到零。 如果同一应用程序同时为1000项目创建两个请求，则预算值将为2000个项目，超过了**EWSFindCountLimit**值。 如果用户的项目预算低于零，则下一个请求将导致错误，直到用户的预算 recharges 到一个或多个。

## <a name="throttling-considerations-for-ews-notification-applications"></a>EWS 通知应用程序的限制注意事项

如果要构建使用 push、pull 或流式通知的 EWS 通知应用程序，则应考虑**EWSMaxSubscriptions**和**限制**限制策略的含义以及**HangingConnectionLimit**。

**EWSMaxSubscriptions**策略参数指定用户可以同时在特定客户端访问服务器上具有的活动推送、请求和流式订阅的最大数量。 不同版本的 Exchange 对此参数具有不同的默认值。 用户可以通过使用**SubscribeToAllFolders**属性来订阅邮箱中的所有文件夹-这对**EWSMaxSubscriptions**预算使用单个订阅。 用户可以订阅单个文件夹，每个文件夹订阅数向**EWSMaxSubscriptions**预算（最多为**EWSMaxSubscriptions**参数的值设置的限制）（例如，如果**EWSMaxSubscriptions**设置为20，用户可以在不同邮箱中订阅20个日历文件夹）。

有关模拟和**EWSMaxSubscriptions**参数的信息，请参阅本文前面的[使用 EWS 模拟的应用程序的限制注意事项](#throttling-considerations-for-applications-that-use-ews-impersonation)。

**限制**策略参数也可能是 EWS 通知的问题;例如：

- 当 EWS 在通知由推送订阅生成时，将订阅的所有者的连接计数增加。

- 当应用程序设计为侦听多个用户的邮箱时，用户将收到发送到通讯组列表的邮件实例的同时通知。

如果通知应用程序是多线程的，并发出同时连接请求，以获取有关用户帐户收到的特定邮件的详细信息，则可以超出**限制**策略限制。 为此，请考虑监视应用程序中的并发连接，包括服务器可能使用的连接，以及在客户端上实现请求队列。

**HangingConnectionLimit**仅适用于流式通知。 此限制是在 web.config 文件中设置的，这意味着 Exchange 管理员可以在本地 Exchange 服务器上设置此值，但 Exchange Online 邮箱必须使用此限制的默认值，即 Exchange Online 和 Exchange 2013 的默认值为3。 若要了解详细信息，请参阅[我需要考虑哪些限制值？](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。

## <a name="throttling-policy-and-application-performance"></a>限制策略和应用程序性能

**PercentTimeIn**限制策略的以下三个参数影响 EWS 应用程序可在客户端访问服务器上使用的时间量：

- **EWSPercentTimeInAD**

- **Ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**

- **EWSPercentTimeInMailboxRPC**

**PercentTimeIn**策略参数中指定的值指示一个线程分配一个请求的时间量。 例如，假设**ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**值为90，如果一个进程发出两个在客户端访问服务器上运行的代码中使用54秒的并发请求，则进程在60秒窗口中使用108秒。 这表示**ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**参数值为180%。

> [!NOTE]
> **Ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**参数值是**EWSPercentTimeInAD**和**EWSPercentTimeInMailboxRPC**参数值的重叠超集。 这意味着客户端访问服务器处理时间中的支出将始终大于**EWSPercentTimeInAD**和**EWSPercentTimeInMailboxRPC**中的支出。 这是因为 Exchange 组件要进行 Active Directory 或 RPC 调用，它必须已运行客户端访问服务器代码。 此外，在发出 LDAP 或 RPC 调用时， **ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**的处理时间的支出不会停止。 尽管该请求可能会在等待 Active Directory 域服务（AD DS）或 Exchange 存储中的响应时同步，但该进程仍在使用服务器上的线程，因此该线程应继续为该用法收取费用。

在60秒期间应用程序可能需要执行的 CPU 时间量可能超过这些限制限制;因此，请务必考虑正在进行的请求的数量和类型。 例如，同时进行的一批大型**ResolveNames**操作可能会超过**EWSPercentTimeInAD**策略参数值。 默认限制策略中包含的策略值旨在允许大多数 EWS 应用程序正常运行，而不会出现问题。但是，当多线程高容量应用程序在一个特定客户端访问服务器上放置了大量请求时，这可能会导致出现问题。 若要避免这种情况，请考虑限制要对服务器执行的批处理的大小。

## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>限制策略和发送大量电子邮件的应用程序

默认限制策略包括三个速率限制策略参数，这些参数可以影响使用 EWS 发送大量邮件的应用程序，或在较短的一段时间内发送较多批量邮件。

> [!NOTE]
> 通常情况下，我们建议您不要使用 EWS 发送批量电子邮件。 使用专用于批量邮件服务的 SMTP 主机，以提交频繁的大量批量电子邮件。

**MessageRateLimit**策略参数指定任何 Exchange 客户端（包括 EWS）可提交的每分钟邮件数。 默认情况下，此策略设置为每分钟30封邮件。 对于普通用户，这通常就足够了。 但是，发送大量电子邮件的应用程序（例如，作为开票计划的一部分）可能会遇到问题。 超过此策略限制时，将延迟对邮箱的邮件传递。 具体来说，当用户或应用程序提交的邮件数大于**MessageRateLimit**参数指定的值时，邮件将在 "发件箱" 或 "草稿" 文件夹中显示较长的一段时间。 在开发送达跟踪系统时，请务必考虑这一点，尤其是当您的应用程序使用用户通过 Outlook 连接到的邮箱时。 将延迟的项目存储在 "发件箱" 或 "草稿" 文件夹中时，用户可能会将其解释为错误。

**RecipientRateLimit**策略参数指定用户可在24小时内处理的收件人数限制。 例如，如果此值设置为500，则意味着单个 Exchange 邮箱帐户每天可以向不超过500个收件人发送邮件。 此限制适用于组织内部和外部的收件人的邮件。 此默认限制可能导致一些执行月结束发票的业务线应用程序出现问题，并且需要将邮件发送到超过此数目的收件人。 可以使用外部服务启用邮件批处理或单独的本地出站中继解决方案，以解决此限制。

**ForwardeeLimit**策略参数指定邮件可通过收件箱规则转发或重定向到的最大收件人数。 此参数不会限制可转发或重定向到收件人的邮件数。

## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>超出限制限制时生成的错误

超过限制策略时，EWS 将生成下表中列出的错误之一。

**表3：限制限制错误**

|**Error**|**限制策略参数**|**说明**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**限制** <br/> |指示对服务器的并发请求数超过用户策略所允许的数量。  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |指示已超出用户的限制策略最大订阅数。  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |指示搜索操作调用已超过可返回的项目总数。  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC**         **ewsmaxconcurrencyewspercenttimeinadewspercenttimeincas**         **EWSPercentTimeInAD** <br/> |在服务器处于忙碌状态时发生。 使用 ErrorServerBusy 错误返回的 BackOffMilliseconds 值指示客户端在重新提交导致返回此错误代码的响应的请求之前应等待的时间。  <br/> |

下表列出了由限制错误返回的 HTTP 状态代码。

**表4：限制错误返回的 HTTP 状态代码**

|**HTTP 状态代码**|**说明**|
|:-----|:-----|
|HTTP 503  <br/> |指示 EWS 请求正在通过 IIS 排队。 客户端应延迟发送其他请求，直到以后再发送。  <br/> |
|HTTP 500  <br/> |指示内部服务器错误，并显示 ErrorServerBusy 错误代码。 这表示客户端应延迟发送更多请求，直到以后再发送。 响应中可能包含名为 BackOffMilliseconds 的后退提示。 如果存在，则在客户端重新提交请求之前，应将 BackOffMilliseconds 的值用作持续时间。  <br/> |
|HTTP 200  <br/> |包含带 ErrorInternalServerError 错误代码的基于 EWS 架构的错误响应。 可能存在内部 ErrorServerBusy 错误代码。 这表示客户端应延迟发送更多请求，直到以后再发送。  <br/> |

## <a name="see-also"></a>另请参阅

- [Exchange 工作负载管理](https://technet.microsoft.com/library/jj150503.aspx)
- [ThrottlingPolicy cmdlet](https://technet.microsoft.com/library/dd351045.aspx)
- [了解客户端限制策略](https://technet.microsoft.com/library/dd297964.aspx)
- [ThrottlingPolicy 类](https://msdn.microsoft.com/library/ff342496%28v=EXCHG.140%29.aspx)
- [限制策略和 EWSFindCountLimit](https://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [IIS 日志中的预算快照](https://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)

- [限制对 Exchange 2010 SP1 中的部署的影响](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Exchange 2010 SP1 中的限制策略关联](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [限制策略和 CPUStartPercent](https://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
