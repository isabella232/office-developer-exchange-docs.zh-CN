---
title: 传输代理 Exchange 2013 中的概念
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: 查找有关如何传输代理管道和服务器角色体系结构在 Exchange 2013 影响传输代理开发，以及可用于开发传输代理的类的信息。
ms.openlocfilehash: 6f7a03e16b260117c6ee27b86ec0e55b5346e301
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353705"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>传输代理 Exchange 2013 中的概念

查找有关如何传输代理管道和服务器角色体系结构在 Exchange 2013 影响传输代理开发，以及可用于开发传输代理的类的信息。 
  
**适用于：** Exchange Server 2013 
  
提供在 Exchange Server 2013 类库可用于实现的注册事件和执行对邮件的操作，当通过传输管道传输代理。 您还可以使用传输代理修改邮件并将内容转换。 
  
本文提供了有关传输代理的信息和传输管道体系结构。 务必要了解传输管道的体系结构，以便您可以修改传输行为以满足您组织的需求。 本文还提供了有关影响传输代理的 Exchange 2013 体系结构和可用于开发传输代理的类中的更改的信息。 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>传输管道中的传输代理
<a name="Pipeline"> </a>

从以下三类之一派生传输代理：
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
传输管道是指数据流 Exchange 2013 组织的边界内的邮件。 管道包含下表中列出的服务。
  
**表 1。传输管道服务**

|**服务**|**说明**|**支持的类**|
|:-----|:-----|:-----|
|前端传输  <br/> |所有[客户端访问服务器](http://technet.microsoft.com/en-us/library/dd298114%28v=exchg.150%29.aspx)上运行并充当所有入站和出站外部 SMTP 流量 Exchange 2013 组织无状态代理。 前端传输服务不检查消息内容或队列本地任何消息。 在[邮箱服务器](http://technet.microsoft.com/en-us/library/jj150491%28v=exchg.150%29.aspx)上的传输服务通信。  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|传输  <br/> |在所有邮箱服务器上运行并且是类似于 Exchange Server 2010 中的[集线器传输服务器](http://technet.microsoft.com/en-us/library/bb123494%28v=exchg.141%29.aspx)角色。 传输服务路由本身和的邮箱传输和前端传输服务之间的邮件。 此服务不直接与邮箱数据库通信。  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|邮箱传输  <br/> |将所有邮箱服务器上运行并包含两个单独的服务： 邮箱传输提交和邮箱传输传递。 邮箱传输传递 SMTP 邮件接收的传输服务，并通过使用 Exchange 远程过程调用 (RPC) 将邮件传递到邮箱数据库连接。 邮箱传输提交连接到邮箱数据库 RPC 用于检索邮件，并提交通过 SMTP 邮件的传输服务。  <br/> |无。  <br/> |
   
### <a name="transport-events"></a>传输事件
<a name="Events"> </a>

通过先注册事件，并随后执行一个操作时，会触发该事件实现传输代理。 每个三个代理类型可以注册的一组不同的事件。
  
下图显示了在传输管道传输代理可以注册事件中的位置。
  
**图 1。传输事件**

![此图显示通过传输管道的邮件流，以及每个代理可以为其注册的事件，首先是 SmtpReceivedAgent 的 Smtp 事件，然后是 RoutingAgent 的 Categorizor 事件，最后是为 DeliveryAgent 提供的事件。](media/TAConceptsFig1.png)
  
当邮件进入传输管道时，从[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类派生的传输代理可以期间注册的代理的 SMTP 事件，作用于邮件。 在任何已注册的四个分类程序事件可充当[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类派生的代理。 从[DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)类派生代理可以在任何已注册的传递事件期间对邮件进行操作。 
  
## <a name="transport-agents-and-server-roles"></a>传输代理和服务器角色
<a name="ServerRoles"> </a>

对服务器角色体系结构更改在 Exchange 2013 影响传输代理以及传输代理可以执行哪些操作。 Exchange 2013 包括下列服务器角色：
  
- 邮箱服务器，包括客户端访问协议、 传输服务、 邮箱数据库和统一消息组件。 邮箱服务器直接与 Active Directory 域服务 (AD DS) 和客户端访问服务器，如 Outlook 的邮件客户端通信。
    
- 客户端访问服务器 — 提供身份验证、 有限的重定向、 代理服务和客户端访问协议，如 HTTP、 POP、 IMAP 和 SMTP。
    
- 边缘传输服务器 — 和注销组织的电子邮件路由。 在 Exchange 拓扑的外围通常 sit 边缘传输服务器。
    
此合并的结构减少了需要在 Exchange 2013 环境中部署的服务器的数量。 管理员不再需要部署包括一个邮箱服务器，每个 Active Directory 站点中的集线器传输和客户端访问服务器，它们不再需要更新所有服务器角色，以便充分利用新功能。
  
对服务器角色体系结构的这些更改可能会影响其中管道中您的代理可以响应事件。 如果您已创建的早于 Exchange 2013 版本的 Exchange 传输代理，请务必查看体系结构的更改，以确定是否需要对您的代理进行任何更改。
  
下图显示了如何在 Exchange 2013 中的体系结构更改导致简化、 合并传输管道。 在此图中，客户端访问服务器标记 CAS。 和邮箱服务器标记 MBX。
  
**图 2。Exchange 2013 服务器角色体系结构**

![此图显示通过左侧外部防火墙和边缘传输的客户端流量，它将流量从第 4 层负载平衡传递到右侧数据库可访问性组中的整合 CAS 数组和一组邮箱服务器。](media/Transport_Agent_Concepts_Fig_3.png)
  
下图显示了 Exchange 2013 服务器角色之间的交互。
  
**图 3。邮箱和客户端访问服务器交互**

![此图显示的互动箭头起始端为客户端流量，这些流量通过的第 4 层负载平衡在 CAS 中包含 4 个目标：IIS/HTTP 代理、POP/IMAP、SMTP 和 UM。箭头跳转到其在邮箱存储中的免费目标。](media/Transport_Agent_Concepts_Fig_4.png)
  
有关 Exchange 2013 服务器角色体系结构中的更改的详细信息，请参阅[What's New in Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx)中的[Exchange 2013 体系结构](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch)。 
  
## <a name="transport-agent-classes"></a>传输代理类
<a name="Create"> </a>

传输代理派生的类确定您的代理可为其注册的事件。 您的代理通常将包含一个代理类、 代理工厂、 一个或多个事件处理程序和执行希望您的代理程序执行的操作的代码。
  
下表列出了要从中派生每个代理类型的类。
  
**表 2。代理类**

||||
|:-----|:-----|:-----|
|代理类型  <br/> |中心基类  <br/> |代理基类  <br/> |
|SMTP 接收  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|路由  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|传递  <br/> |[DeliveryAgentFactory\<管理器\>](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
属性和方法可用于访问传输事件和消息，提供了这些中心和代理的基类。 在您从这些类继承的代理中实现类。 在代理工厂派生类中，重写**CreateAgent**方法，以便它返回代理类的新实例。 
  
传递给事件参数可以包含实例[EmailMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx)类中，您可以使用更改的属性和基础邮件的内容。 并非所有邮件的信息可以在每个事件。 您必须确定哪个代理，最适合您想要完成的任务的事件。 
  
以下命名空间包含可用于读取、 写入和修改传输管道中的邮件的类型：
  
- [Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
之后，您编写传输代理，您[安装和管理您的代理](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx)使用 Exchange 命令行管理程序。 有关详细信息，请参阅[Exchange 2013 创建传输代理](creating-transport-agents-for-exchange-2013.md)。 
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 传输代理](transport-agents-in-exchange-2013.md)    
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)   
- [读取和修改 Exchange 2013 传输管道中的邮件](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [What's New in Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx)   
- [Exchange 2013 服务器角色体系结构](http://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [邮箱和客户端访问服务器](http://technet.microsoft.com/en-us/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013 的邮件流](http://technet.microsoft.com/en-us/library/aa996349.aspx)
- [Exchange Server 2013 邮件路由](http://technet.microsoft.com/en-us/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

