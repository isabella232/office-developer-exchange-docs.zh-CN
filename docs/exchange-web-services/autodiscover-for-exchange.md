---
title: Exchange 自动发现
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: da0f9402-4e35-42c7-a15e-1e9e4e966e8b
description: 了解 Exchange 中的自动发现服务。
ms.openlocfilehash: f56717eaced5db9028c556c6c2d9aa7794f4988e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752729"
---
# <a name="autodiscover-for-exchange"></a>Exchange 自动发现

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解 Exchange 中的自动发现服务。
  
Exchange 自动发现服务为客户端应用程序提供一种在尽量减少用户输入的情况下对自身进行配置的简单方式。大多数用户都知道自己的电子邮件地址和密码，通过这两项信息，您可以检索您启动和运行所需的所有其他详细信息。对于 Exchange Web 服务 (EWS) 客户端，自动发现通常用于查找 EWS 终结点 URL，但自动发现也可以提供信息，以配置使用其他协议的客户端。自动发现适用于位于防火墙内部或外部的客户端应用程序，并且可在资源林和多个林方案中运行。
  
## <a name="overview-of-the-autodiscover-process"></a>自动发现过程的概述
<a name="bk_Before"> </a>

自动发现过程基本分为三个阶段。在第一阶段，您生成潜在自动发现服务器列表，在第二阶段，您尝试列表中的每台服务器，直到您（有可能）收到成功的响应。如果您的候选服务器均未成功，您可以跳至第三阶段，这是查找自动发现终结点的"最后一招"。
  
EWS Managed API 中的 [ExchangeService.AutodiscoverUrl](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) 方法为您实施此过程的三个阶段，因此如果您使用 EWS Managed API，则无需担心需要自己实施自动发现。下图显示了自动发现过程的这三个阶段。 
  
**图 1. 自动发现过程的三个阶段**

![自动发现过程的说明，介绍了三个阶段：定义候选池、尝试终结点以及尝试其他选择。](media/Ex15_Autodiscover_Overview.png)
  
### <a name="phase-1-defining-the-candidate-pool"></a>阶段 1：定义候选池
<a name="bk_Phase1"> </a>

在使用自动发现之前，您必须为用户找到正确的自动发现服务器。幸运地是，自动发现定义了供您查找的有限数量的位置。如果找到多个候选服务器，自动发现还会定义[生成列表并进行优先排序的方式](how-to-generate-a-list-of-autodiscover-endpoints.md)。
  
**表 1：自动发现终结点候选源**

|**查找位置**|**您将找到的结果**|
|:-----|:-----|
|Active Directory 域服务 (AD DS)  <br/> |对于已加入域的客户端，这是要查找的第一个位置。Exchange 在 AD DS 中发布服务连接点 (SCP) 对象，这样就可以根据 Active Directory 站点将自动发现请求发送到服务器。[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)的结果应位于候选列表顶部。  <br/><br/>**注意**：SCP 查找不适用于未加入域或无权访问 Active Directory 服务器的客户端。 在这种情况下，应跳过 SCP 查找。 <br/>|
|用户的电子邮件地址域  <br/> | 自动发现可定义从用户电子邮件地址的域部分派生的两种标准终结点 URL 形式：  <br/>`"https://" + domain + "/autodiscover/autodiscover" +  *fileExtension*`  <br/>`"https://autodiscover." + domain + "/autodiscover/autodiscover" +  *fileExtension*`<br/><br/>  *文件扩展名*  的值取决于您使用的自动发现访问方法： [SOAP](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) 或 [POX](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)。SOAP 服务使用".svc"文件扩展名，POX 使用".xml"。  <br/> |
   
下图演示如何生成自动发现终结点列表。
  
**图 2. 生成自动发现终结点列表的过程**

![此说明显示生成自动发现终结点列表的过程。箭头表示终结点列表由 SCP 查找或用户的电子邮件地址派生。](media/Ex15_Autodiscover_Overview_Phase1.png)
  
### <a name="phase-2-trying-each-candidate"></a>阶段 2：尝试每个候选服务器
<a name="bk_Phase2"> </a>

生成潜在候选服务器的按顺序列表后，下一步是尝试列表中的每一台候选服务器，方法是[向 URL 发送请求](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)并验证结果，如图 3 中所示。收到成功的响应时，即表示您已大功告成！ 
  
**图 3. 按顺序尝试每个候选终结点**

![此说明显示服务器以优先级顺序尝试每个终结点，直到收到成功响应。](media/Ex15_Autodiscover_Overview_Phase2.png)
  
向候选服务器发送请求之前，确保其可信。请记住，您是在发送用户的凭据，因此务必确保仅与您信任的服务器共享。至少您应确认以下事项：
  
- 该终结点是 HTTPS 终结点。客户端应用程序不应进行身份验证，或将数据发送到非 SSL 终结点。
    
- 服务器提供的 SSL 证书有效且来自受信任的颁发机构。
    
> [!NOTE]
> [!注释] 这些只是基本的安全建议。只要您使用身份验证，就应确保您的代码满足组织的安全要求。 
  
您发送的请求类型取决于您访问自动发现服务的方式。
  
**表 2. 自动发现请求的类型**

|**如果您使用…**|**通过以下方式发送请求…**|
|:-----|:-----|
|EWS Managed API  <br/> |[GetUserSettings](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) 方法。  <br/> |
|SOAP 自动发现服务  <br/> |[GetUserSettings](http://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) 操作。  <br/> |
|POX 自动发现服务  <br/> |具有[自动发现请求正文](http://msdn.microsoft.com/library/75671b1d-f35b-497b-8d8c-706f3f2535fd%28Office.15%29.aspx)的 HTTP POST。  <br/> |
   
### <a name="phase-3-trying-other-alternatives"></a>阶段 3：尝试其他选择
<a name="bk_Phase3"> </a>

在某些情况下，您可能尝试了列表中的所有终结点，但却发现所有终结点均返回错误。在放弃之前，您可以多尝试几种方法：您可以发送一个未经身份验证的 GET 请求，或者查询 DNS 以查找 SRV 记录。如果这些尝试都没有结果，则无法联系自动发现服务。
  
**阶段 4：尝试其他选择**

![此说明显示通过未经身份验证的 GET 请求和 DNS 请求生成的其他终结点。](media/Ex15_Autodiscover_Overview_Phase3.png)
  
#### <a name="sending-an-unauthenticated-get-request"></a>发送未经身份验证的 GET 请求

尝试的第一件事就是向从用户电子邮件地址派生的终结点发送一个未经身份验证的 GET 请求。该终结点的格式为 "http://autodiscover." + 域 + "/autodiscover/autodiscover.xml"。请注意，这不是 SSL 终结点。如果 服务器返回 302 间接响应，您可以尝试向响应的位置头中的终结点 URL [重新发送自动发现请求](handling-autodiscover-error-messages.md#bk_ResendRequest)。 
  
#### <a name="querying-dns-for-an-srv-record"></a>查询 DNS 以查找 SRV 记录

如果未经身份验证的 GET 请求不起作用，最后一件事是进行 DNS 查询以查找自动发现服务的 SRV 记录。记录格式将为 "_autodiscover._tcp." + 域。该查询可能返回多条记录，但您应该仅使用指向 SSL 终结点且具有最高优先级和权重的记录。
  
## <a name="options-for-using-autodiscover"></a>使用自动发现的选项
<a name="bk_Options"> </a>

您可以通过使用 SOAP 或 POX Web 服务访问自动发现。您使用的方法取决于您的要求和环境。但是，我们建议您尽可能使用 SOAP Web 服务。EWS Managed API 也是一个选项。它实施 SOAP 和 POX 自动发现服务的客户端部分。
  
**表 3：访问自动发现的选项**

|**选项**|**优点**|**缺点**|
|:-----|:-----|:-----|
|[EWS Managed API](get-started-with-ews-managed-api-client-applications.md) <br/> | 为您实施自动发现过程。<br/><br/>使用 SOAP 和 POX 自动发现服务。<br/><br/>适用于 Exchange Online、作为 Office 365 一部分的 Exchange Online 或从 Exchange 2007 SP1 起的 Exchange 版本。<br/><br/>易于使用。  <br/> | 限制为 [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx) 枚举中可用的用户设置。<br/><br/>仅适用于 .NET Framework 应用程序。  <br/> |
|[SOAP 自动发现](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) <br/> | 独立于平台。<br/><br/>使您可以只请求您感兴趣的设置。  <br/> | 在 Exchange 2007 中不可用。  <br/> |
|[POX 自动发现](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx) <br/> | 独立于平台。<br/><br/>在 Exchange Online 中以及从 Exchange 2007 SP1 起的所有 Exchange 版本中受支持。  <br/> | 不允许您请求特定设置。  <br/> |
   
## <a name="in-this-section"></a>本节内容

- [通过使用 Exchange 中的 SCP 查找来找到自动发现终结点](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)
    
- [使用自动发现查找连接点](how-to-use-autodiscover-to-find-connection-points.md)
    
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [获取来自 Exchange 服务器的域设置](how-to-get-domain-settings-from-an-exchange-server.md)
    
- [使用自动发现刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [使用 Exchange 自动发现时提升性能](improving-performance-when-using-autodiscover-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)    
- [Exchange 2013：使用自动发现获取用户设置](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e)
- [自动发现检查器示例](http://code.msdn.microsoft.com/exchange/Autodiscover-Checker-e1ebca42)  
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

