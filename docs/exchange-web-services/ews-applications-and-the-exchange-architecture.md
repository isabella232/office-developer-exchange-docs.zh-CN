---
title: EWS 应用程序和 Exchange 体系结构
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c10f308a-65bb-4a0b-8fdd-b4a61503f0fd
description: 了解 EWS 在 Exchange 体系结构中的工作方式，并找出 EWS 所依赖的协议。
localization_priority: Priority
ms.openlocfilehash: 15f396664ea46e53a4603a617c9bf679400af160
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456075"
---
# <a name="ews-applications-and-the-exchange-architecture"></a>EWS 应用程序和 Exchange 体系结构

了解 EWS 在 Exchange 体系结构中的工作方式，并找出 EWS 所依赖的协议。
  
Exchange Web 服务（EWS）是跨平台 API，它使应用程序能够访问邮箱项目，例如来自 Exchange Online 的电子邮件、会议和联系人、exchange Online （作为 Office 365 的一部分）或 Exchange Online 版（从 Exchange Server 2007 开始）。 [EWS 应用程序](ews-application-types.md)可以通过在基于 SOAP 的 XML 消息中发送请求，在本地或远程访问邮箱项。 在应用程序和服务器之间发送时，将在 HTTP 消息中嵌入 SOAP 消息，这意味着只要您的应用程序可以通过 HTTP 发布 XML，它就可以使用 EWS 访问 Exchange。 
  
## <a name="exchange-architecture-overview"></a>Exchange 体系结构概述
<a name="bk_techarch"> </a>

下图显示了在与 Exchange 2013 和 Exchange Online 通信时，EWS 应用程序使用的身份验证方法和通信路径。 从 EWS 应用程序的角度来看，通信路径完全相同，身份验证方法仅略有不同;主要区别是您对 Exchange 后端的可见性。
  
**图1。EWS 应用程序和 Exchange 本地体系结构**

![此插图显示 Exchange 本地体系结构情境中的 EWS 应用程序。若要获取此图中组件的说明，请参阅本图和下图下方文本的第 1 至 8 条。](media/Ex2013_ArchitecturesOverview.png)
  
图2显示了图1中所示的相同通信路径，与 Exchange Online 通信时，由 EWS 应用程序使用。
  
**图2。EWS 应用程序和 Exchange Online 体系结构**

![此插图显示适用于 EWS 应用程序的 Exchange Online 体系结构情境中的 EWS 应用程序。若要获取此图中组件的说明，请参阅本图像下方文本的第 1、2、3、6 和 9 条。](media/Ex2013_Architectures_Online.png)
  
图中显示了以下组件：
  
1. EWS 应用程序—这可以是[客户端、门户或服务应用程序](ews-application-types.md)，也可以安装在客户端或 Exchange 本地客户端访问服务器上。 如果使用 EWS 托管 API 开发 EWS 应用程序，则必须在客户端上安装 EWS 托管 API 程序集，并[由应用程序](redistribution-requirements-for-the-ews-managed-api.md)对其进行重新分配。
    
2. Soap XML 消息（SOAP 信封中的 XML 消息）嵌入在 HTTP/S 消息中，该消息符合客户端访问服务器上的服务 .wsdl 文件。 建议对 Exchange 内部部署使用 HTTPS，对于 Exchange Online，此为必需。 
    
3. 身份验证方法— EWS 邮件包括基本、NTLM （Windows 集成身份验证）或作为 HTTP 有效负载一部分的 OAuth 身份验证信息。 
    
4. 负载平衡器—负载平衡器将邮件分发到客户端访问服务器阵列中的客户端访问服务器。 此组件仅在 Exchange 内部部署体系结构中可见。
    
5. 客户端访问服务器阵列-客户端访问服务器被组织到一个称为客户端访问服务器阵列的负载平衡组中。 单个客户端访问服务器提供身份验证、有限重定向和代理服务。 客户端访问服务器本身不会进行任何数据呈现，也不会在客户端访问服务器上对数据进行排队或存储-它是瘦且无状态的;它只是对请求进行身份验证，执行自动发现查找，然后将请求代理到邮箱服务器。 客户端访问服务器与承载用户数据的邮箱服务器之间维护的关系为1:1。 在客户端访问服务器和邮箱服务器之间使用 HTTP 协议（通过使用自签名证书的 SSL 进行了安全保护）。 此组件仅在 Exchange 内部部署体系结构中可见。
    
6. 自动发现服务—自动发现服务通过访问 Active Directory 域服务（AD DS）来检索邮箱版本以及承载用户数据的主动副本的邮箱服务器的位置，从而执行服务发现。
    
7. EWS 服务-EWS 服务由三个文件： wsdl.exe、消息 .xsd 和类型 .xsd 以及 EWS 托管 API 程序集进行描述。 "Wsdl" 描述客户端和服务器之间的协定，消息 .xsd 定义请求和响应 SOAP 消息，类型 .xsd 定义在 SOAP 消息中使用的元素。 无论早期版本的架构是什么，xsd 和类型都始终包含架构的最新版本。 请注意，在客户端访问服务器上提供了服务 wsdl、消息 .xsd 和类型 .xsd，但实际上并不用于架构验证，仅提供这些功能仅供参考。 EWS 托管 API 程序集是为服务器端 EWS 客户端应用程序提供的，并且部署在所有 Exchange 服务器角色上，而不只是在客户端访问服务器上部署。 此组件仅在 Exchange 内部部署体系结构中可见。
    
    功能可用性基于应用程序的目标 EWS 架构版本。 由于 EWS 架构是向后和向前兼容的，因此，如果您创建一个面向早期架构版本的应用程序（如 Exchange 2007 SP1），则您的应用程序还将针对更高版本的架构版本（如 Exchange 2010 SP2 服务）以及 Exchange Online 运行。 由于功能和功能更新由架构驱动，因此我们建议使用针对要在客户端应用程序中实现的 EWS 功能的最早通用基本代码。 由于 Exchange 2007 SP1 架构包含几乎所有用于在 Exchange 存储中处理项目和文件夹的核心 Exchange 功能，因此许多应用程序可以面向 Exchange2007_SP1 版本。 有关详细信息，请参阅[EWS 客户端功能](ews-client-design-overview-for-exchange.md#EWSFeatures)。
    
8. 数据库可用性组（DAG）—邮箱服务器被组织到一个高度可用的 DAG 中，可在一个或多个数据中心部署。 邮箱服务器包含邮箱数据库，并处理该服务器上的活动邮箱的所有活动。 处理、呈现和存储数据的所有组件都位于邮箱服务器上。 客户端不直接连接到邮箱服务器;所有连接都由客户端访问服务器处理。 此组件仅在 Exchange 内部部署体系结构中可见。
    
9. Exchange Online 和 Exchange Online 作为 Office 365 的一部分—将 Exchange 功能作为基于云的服务提供的托管邮件解决方案。
    
当 EWS 应用程序请求来自 Exchange 存储的信息时，将创建符合 SOAP 标准的 XML 请求邮件并将其发送到 Exchange 服务器。 当 Exchange 服务器收到请求时，它会验证客户端提供的凭据，并自动分析请求的数据的 XML。 然后，服务器生成包含表示所请求的强类型对象及其属性的 XML 数据的 SOAP 响应。 将 XML 数据发送回 HTTP 响应中的应用程序。 然后，应用程序将 XML 反序列化并使用数据来重新对强类型对象进行改革。
  
## <a name="protocols-and-standards-that-ews-applications-must-support"></a>EWS 应用程序必须支持的协议和标准
<a name="bk_standards"> </a>

若要与 Exchange 服务器通信，EWS 应用程序必须支持以下协议和标准。
  
**表1。协议**

|**协议**|**如何使用**|
|:-----|:-----|
|HTTP/S  <br/> |使 EWS 应用程序可以通过网络访问 Exchange 数据库数据，而不管客户端是在 Internet 上还是在 intranet 上。  <br/> |
|SOAP 1。0  <br/> |在邮件传递负载周围形成信封。 EWS 通过使用 SOAP 信封的不同部分来实现 SOAP 协议，以启用不同的功能。 SOAP 标头用于模拟并提供版本控制数据。 SOAP body 提供有关要运行的操作和提交到操作的数据的信息。 SOAP 依赖 WSDL 来描述要调用的操作。  <br/> |
|WSDL 1。0  <br/> |介绍了在 wsdl.exe 文件中用于调用 EWS 操作的绑定、操作和属性。 此文件和引用的架构文件（包括 EWS 应用程序和 Exchange 服务器之间的协定），通常与供应商特定的工具一起使用，以创建特定于平台的应用程序。 WSDL 文件位于 EWS 虚拟目录中，该目录位于网站的根目录中。  <br/> |
|传输层安全性（TLS）/SSL  <br/> |在 Internet 或 intranet 上提供安全的 web 通信。 TLS 使应用程序能够对服务器进行身份验证，也可以选择通过服务器对 EWS 应用程序进行身份验证。 它还通过对通信进行加密来提供安全通道。 TLS 是安全套接字层 (SSL) 协议的最新版本。  <br/> |
|XML/XSD  <br/> |为 Exchange 服务器和客户端之间的信息交换提供通用邮件格式。 XML 向客户端应用程序提供复杂的 Exchange 数据库数据，但采用定义的结构。 XML 的优点是，即使 EWS 应用程序和服务器不共享一个通用平台，也可以对数据进行交换。  <br/> |
   
此外，EWS 应用程序必须支持以下身份验证标准：
  
- 基于 SSL 的基本身份验证，适用于面向 Exchange Online 或本地 Exchange 的应用程序。
    
- 通过 SSL 的 NTLM 身份验证，适用于支持本地 Exchange 的应用程序。
    
- 适用于受信任合作伙伴应用程序的 OAuth 2.0 令牌身份验证以及与 Lync Server 2013 和 SharePoint Server 2013 的互操作性。
    
## <a name="see-also"></a>另请参阅


- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
    
- [EWS 应用程序类型](ews-application-types.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

