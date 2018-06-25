---
title: EWS 应用程序和 Exchange 体系结构
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c10f308a-65bb-4a0b-8fdd-b4a61503f0fd
description: 了解 EWS 方式内 Exchange 体系结构，并找出哪些 EWS 依赖的协议。
ms.openlocfilehash: 1fbc1e68edbca829555fbbf1b9f0bc4723da9524
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752727"
---
# <a name="ews-applications-and-the-exchange-architecture"></a>EWS 应用程序和 Exchange 体系结构

了解 EWS 方式内 Exchange 体系结构，并找出哪些 EWS 依赖的协议。
  
Exchange Web Services (EWS) 是一个跨平台 API，使应用程序访问邮箱项目，如电子邮件、 会议和联系人从 Exchange Online 中，Exchange Online 作为 Office 365 的一部分或本地版本的 Exchange 开头Exchange Server 2007。 [EWS 应用程序](ews-application-types.md)可以通过在 SOAP 基于 XML 邮件中发送的请求访问邮箱项目本地或远程。 嵌入到 SOAP 消息时应用程序和服务器，这意味着，只要您的应用程序可以发布通过 HTTP 的 XML，它可以使用 EWS 访问 Exchange 之间发送的 HTTP 消息中。 
  
## <a name="exchange-architecture-overview"></a>Exchange 体系结构概述
<a name="bk_techarch"> </a>

下图显示的身份验证方法和 EWS 应用程序与 Exchange 2013 和 Exchange Online 进行通信时使用的通信路径。 从 EWS 应用程序的角度来看，是相同的通信路径和身份验证方法只会略有不同;主要区别是 Exchange 后端到您具有的可见性。
  
**图 1。EWS 应用程序和 Exchange 内部部署体系结构**

![此插图显示 Exchange 本地体系结构情境中的 EWS 应用程序。若要获取此图中组件的说明，请参阅本图和下图下方文本的第 1 至 8 条。](media/Ex2013_ArchitecturesOverview.png)
  
图 2 显示了在与 Exchange Online 进行通信时使用的 EWS 应用程序图 1 中所示的相同的通信路径。
  
**图 2。EWS 应用程序和 Exchange Online 体系结构**

![此插图显示适用于 EWS 应用程序的 Exchange Online 体系结构情境中的 EWS 应用程序。若要获取此图中组件的说明，请参阅本图像下方文本的第 1、2、3、6 和 9 条。](media/Ex2013_Architectures_Online.png)
  
以下是图所示的组件：
  
1. EWS 应用程序 — 这可以是[客户端、 门户或服务应用程序](ews-application-types.md)而可以将安装在客户端或 Exchange 内部部署客户端访问服务器上。 如果您使用 EWS 托管 API 开发的 EWS 应用程序，将 EWS 托管 API 的程序集必须安装在客户端和[您的应用程序重新分配](redistribution-requirements-for-the-ews-managed-api.md)。
    
2. SOAP XML 消息 — XML 消息，SOAP 信封中, 嵌入到客户端访问服务器上的 Services.wsdl 文件符合 HTTP/S 邮件中。 HTTPS 建议 Exchange 内部部署和 Exchange Online 的需要。 
    
3. 身份验证方法 — EWS 消息包括基本，作为 HTTP 负载的一部分的 NTLM （集成 Windows 身份验证） 或 OAuth 身份验证信息。 
    
4. 负载平衡器 — 负载平衡器分发客户端访问服务器阵列中的客户端访问服务器的邮件。 Exchange 内部部署体系结构中将仅显示此组件。
    
5. 客户端访问服务器阵列 — 客户端访问服务器均分成各种名为客户端访问服务器阵列的负载平衡的组。 单个客户端访问服务器提供身份验证、 有限的重定向和代理服务。 客户端访问服务器本身不执行任何数据呈现和排入队列或存储在客户端访问服务器上的任何数据-精简并无状态;它只是对请求进行身份验证，执行自动发现查找，然后代理对邮箱服务器的请求。 客户端访问服务器维护承载用户的数据的邮箱服务器 1:1 关系。 客户端访问服务器和邮箱服务器之间使用 HTTP 协议 （通过使用自签名的证书的 SSL 安全）。 Exchange 内部部署体系结构中将仅显示此组件。
    
6. 自动发现服务 — 自动发现服务执行发现服务通过访问 Active Directory 域服务 (AD DS) 来检索邮箱版本和邮箱服务器托管主动副本的用户的数据的位置。
    
7. EWS 服务 — EWS 服务由三个文件描述： Services.wsdl、 Messages.xsd，Types.xsd，以及将 EWS 托管 API 的程序集。 Services.wsdl 介绍在客户端和服务器之间合同、 Messages.xsd 定义请求和响应 SOAP 消息，并 Types.xsd 定义的 SOAP 消息中使用的元素。 Messages.xsd 和 Types.xsd 始终包含架构的最新版本，尽管存在早期版本的架构。 请注意，Services.wsdl、 Messages.xsd 和 Types.xsd 可在客户端访问服务器上，但实际上并不用于的架构验证 — 它们仅供参考。 EWS 托管 API 的程序集提供的服务器端 EWS 客户端应用程序，并在所有 Exchange 服务器角色，而不仅仅是客户端访问服务器上部署。 Exchange 内部部署体系结构中将仅显示此组件。
    
    功能的可用性取决于 EWS 架构版本的应用程序的目标。 因为 EWS 架构和转发-兼容，如果您创建的应用程序面向早期架构版本，Exchange 2007 SP1，例如您的应用程序也适用的更高版本的架构版本，Exchange 2010 SP2 服务，如针对以及Exchange Online。 由于特性和功能更新驱动的架构，我们建议您在该目标您想要在客户端应用程序中实现的 EWS 功能使用最早的常见代码库。 多个应用程序可以目标 Exchange2007_SP1 版本，因为 Exchange 2007 SP1 架构包含几乎所有核心 Exchange 功能用于处理项目和 Exchange 存储中的文件夹。 有关详细信息，请参阅[EWS 客户端功能](ews-client-design-overview-for-exchange.md#EWSFeatures)。
    
8. 数据库可用性组 (DAG) — 高度可用的 DAG，可以在一个或多个数据中心中部署到组织的邮箱服务器。 邮箱服务器包含邮箱数据库，并处理该服务器上的活动邮箱的所有活动。 处理，呈现，并存储数据的所有组件都都在邮箱服务器上。 客户端不直接连接到邮箱服务器。由客户端访问服务器处理所有连接。 Exchange 内部部署体系结构中将仅显示此组件。
    
9. Exchange Online 和 Exchange Online 作为 Office 365 的一部分 — 托管作为基于云的服务提供 Exchange 功能的消息解决方案。
    
当 EWS 应用程序请求从 Exchange 存储的信息时，符合标准的 SOAP XML 请求消息创建并发送到 Exchange 服务器中。 Exchange 服务器接收请求时，它验证客户端提供的凭据，并自动分析所请求的数据的 XML。 然后，服务器建立 SOAP 响应，其中包含代表请求的强类型的对象及其属性的 XML 数据。 XML 数据发送回 HTTP 响应中的应用程序。 应用程序然后 XML 反序列化和使用数据修订的强类型的对象。
  
## <a name="protocols-and-standards-that-ews-applications-must-support"></a>协议和 EWS 应用程序必须支持的标准
<a name="bk_standards"> </a>

要与 Exchange 服务器通信，EWS 应用程序必须支持以下协议和标准。
  
**表 1。协议**

|**协议**|**如何使用它**|
|:-----|:-----|
|HTTP/S  <br/> |允许通过网络，无论客户端是否在 Internet 或 intranet 访问 Exchange 数据库数据 EWS 应用程序。  <br/> |
|SOAP 1.0  <br/> |窗体周围消息负载信封。 EWS 通过使用 SOAP 信封的不同部分实现不同的功能实现 SOAP 协议。 SOAP 标头用于模拟，并提供版本控制数据。 SOAP 主体提供有关要运行的操作和数据提交到该操作的信息。 SOAP 依赖于 WSDL 来描述要呼叫的操作。  <br/> |
|WSDL 1.0  <br/> |介绍绑定、 操作和用于 Services.wsdl 文件中调用 EWS 操作的属性。 此文件，以及被引用的架构文件，包括 EWS 应用程序和 Exchange 服务器之间的协定和通常用于供应商特定工具以及创建特定于平台的应用程序。 WSDL 文件位于 EWS 虚拟目录，它是网站的根目录。  <br/> |
|传输层安全性 (TLS) / SSL  <br/> |在 Internet 或 intranet 上提供安全的 web 通信。 TLS 使应用程序进行身份验证服务器或服务器进行身份验证 EWS 应用程序，（可选）。 它还提供一个安全通道，通过加密通信。 TLS 是安全套接字层 (SSL) 协议的最新版本。  <br/> |
|XML/XSD  <br/> |Exchange server 和客户端之间的信息的 exchange 提供通用消息的格式。 XML 可提供复杂 Exchange 数据库数据客户端应用程序，但在定义的结构。 XML 的优点在于，它允许的数据交换的 EWS 应用程序和服务器不共享一个共同平台，即使。  <br/> |
   
此外，EWS 应用程序必须支持以下身份验证标准：
  
- 基本身份验证使用 ssl，针对 Exchange Online 或 Exchange 内部部署的应用程序。
    
- NTLM 身份验证使用 ssl，支持 Exchange 内部部署的应用程序。
    
- OAuth 2.0 令牌身份验证，受信任的合作伙伴应用程序和 Lync Server 2013 和 SharePoint Server 2013 互操作性。
    
## <a name="see-also"></a>另请参阅


- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS 应用程序类型](ews-application-types.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

