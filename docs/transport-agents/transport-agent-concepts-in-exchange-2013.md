---
title: Exchange 2013 中的传输代理概念
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: 查找有关 Exchange 2013 中的传输代理管道和服务器角色体系结构如何影响传输代理开发的信息，以及可用于开发传输代理的类。
ms.openlocfilehash: 9116c9b7811958a2479421a642052df3cee24e34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537159"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Exchange 2013 中的传输代理概念

查找有关 Exchange 2013 中的传输代理管道和服务器角色体系结构如何影响传输代理开发的信息，以及可用于开发传输代理的类。 
  
**适用于：Exchange Server** 2013 
  
您可以使用 Exchange Server 2013 中提供的类库来实现注册事件并针对通过传输管道传递的邮件采取操作的传输代理。 您还可以使用传输代理修改邮件和转换内容。 
  
本文提供有关传输代理和传输管道体系结构的信息。 了解传输管道的体系结构非常重要，这样您才能修改传输行为以满足组织的需求。 本文还提供了有关 Exchange 2013 体系结构中影响传输代理和可用于开发传输代理的类的更改的信息。 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>传输管道中的传输代理
<a name="Pipeline"> </a>

传输代理派生自以下三个类之一：
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
传输管道是指 2013 组织边界内的邮件Exchange流。 管道由下表中列出的服务组成。
  
**表 1.传输管道服务**

|**服务**|**说明**|**支持的类**|
|:-----|:-----|:-----|
|前端传输  <br/> |在所有客户端[访问服务器上运行](https://technet.microsoft.com/library/dd298114%28v=exchg.150%29.aspx)，并充当 Exchange 2013 组织的所有入站和出站外部 SMTP 通信的无状态代理。 前端传输服务不检查邮件内容或在本地对邮件进行排队。 它与邮箱服务器的传输 [服务通信](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx)。  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |在所有邮箱服务器上运行，类似于 Exchange Server 2010 中的集线器传输服务器角色。 [](https://technet.microsoft.com/library/bb123494%28v=exchg.141%29.aspx) 传输服务在自身与邮箱传输和前端传输服务之间路由邮件。 此服务不直接与邮箱数据库通信。  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|邮箱传输  <br/> |在所有邮箱服务器上运行，由两个单独的服务组成：邮箱传输提交和邮箱传输传递。 邮箱传输传递从传输服务接收 SMTP 邮件，然后使用 Exchange 远程过程调用 (RPC) 连接到邮箱数据库以传递邮件。 邮箱传输提交使用 RPC 连接到邮箱数据库以检索邮件，然后通过 SMTP 将邮件提交到传输服务。  <br/> |无。  <br/> |
   
### <a name="transport-events"></a>传输事件
<a name="Events"> </a>

通过先注册事件，然后在触发该事件时采取操作来实现传输代理。 这三种代理类型都可以注册不同的事件集。
  
下图显示了传输管道传输代理可以在哪里注册事件。
  
**图 1.传输事件**

![此图显示通过传输管道的邮件流，以及每个代理可以为其注册的事件，首先是 SmtpReceivedAgent 的 Smtp 事件，然后是 RoutingAgent 的 Categorizor 事件，最后是为 DeliveryAgent 提供的事件。](media/TAConceptsFig1.png)
  
当邮件进入传输管道时，派生自 [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) 类的传输代理可以在代理注册的任何 SMTP 事件期间对邮件执行操作。 从 [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) 类派生的代理可以处理已注册的四个分类程序事件中的任意一个。 从 [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) 类派生的代理可以在已注册的任何传递事件期间对邮件执行操作。 
  
## <a name="transport-agents-and-server-roles"></a>传输代理和服务器角色
<a name="ServerRoles"> </a>

2013 年 2 月Exchange服务器角色体系结构的更改会影响传输代理和传输代理可以执行哪些操作。 Exchange 2013 包括以下服务器角色：
  
- 邮箱服务器 — 包括客户端访问协议、传输服务、邮箱数据库和统一消息组件。 邮箱服务器直接与 Active Directory 域服务 (AD DS) 、客户端访问服务器和邮件客户端（如 Outlook）。
    
- 客户端访问服务器 — 提供身份验证、有限重定向、代理服务和客户端访问协议，如 HTTP、POP、IMAP 和 SMTP。
    
- 边缘传输服务器 — 将电子邮件路由到组织内部或组织外。 边缘传输服务器通常位于边缘Exchange外围。
    
此合并结构减少了需要在 Exchange 2013 环境中部署的服务器数量。 管理员不再需要在包括邮箱服务器的每个 Active Directory 站点中部署集线器传输服务器和客户端访问服务器，并且他们不再需要更新所有服务器角色以利用新功能。
  
对服务器角色体系结构的这些更改可能会影响代理在管道中可以响应事件的地方。 如果为 Exchange 2013 之前版本的 Exchange 创建了传输代理，请务必查看体系结构更改以确定是否需要对代理进行更改。
  
下图显示了 2013 年 Exchange中的体系结构更改如何产生简化的合并传输管道。 在此图中，客户端访问服务器标记为 CAS。 邮箱服务器标记为 MBX。
  
**图 2.Exchange 2013 服务器角色体系结构**

![此图显示通过左侧外部防火墙和边缘传输的客户端流量，它将流量从第 4 层负载平衡传递到右侧数据库可访问性组中的整合 CAS 数组和一组邮箱服务器。](media/Transport_Agent_Concepts_Fig_3.png)
  
下图显示了 Exchange 2013 服务器角色之间的交互。
  
**图 3.邮箱和客户端访问服务器交互**

![此图显示的互动箭头起始端为客户端流量，这些流量通过的第 4 层负载平衡在 CAS 中包含 4 个目标：IIS/HTTP 代理、POP/IMAP、SMTP 和 UM。箭头跳转到其在邮箱存储中的免费目标。](media/Transport_Agent_Concepts_Fig_4.png)
  
有关 Exchange 2013 服务器角色体系结构更改详细信息，请参阅[what's New in Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)中的[Exchange](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) 2013 体系结构。 
  
## <a name="transport-agent-classes"></a>传输代理类
<a name="Create"> </a>

传输代理派生自的类决定了代理可以注册的事件。 代理通常包含代理类、代理工厂、一个或多个事件处理程序以及执行您希望代理采取的操作的代码。
  
下表列出了每种代理类型派生自的类。
  
**表 2.代理类**

||||
|:-----|:-----|:-----|
|代理类型  <br/> |工厂基类  <br/> |代理基类  <br/> |
|SMTP 接收  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|路由  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Delivery  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
这些工厂和代理基类提供可用于访问传输事件和邮件的属性和方法。 在代理中实现继承自这些类的类。 在代理工厂派生类中，重写 **CreateAgent** 方法，以便它返回代理类的新实例。 
  
传递给事件的参数可以包含 [EmailMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) 类的实例，您可以使用该实例更改基础邮件的属性和内容。 并非所有邮件信息都可用于每个事件。 您必须确定哪个代理以及哪个事件最适合要完成的任务。 
  
以下命名空间包含可用于读取、写入和修改传输管道中的邮件的类型：
  
- [Microsoft。Exchange。Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft。Exchange。Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft。Exchange。Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft。Exchange。Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft。Exchange。Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
编写传输代理后，可以使用命令行管理[](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx)程序安装和管理Exchange代理。 有关详细信息，请参阅 Creating [transport agents for Exchange 2013](creating-transport-agents-for-exchange-2013.md)。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)   
- [读取和修改 Exchange 2013 传输管道中的邮件](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [2013 年 Exchange 的新增功能](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)   
- [Exchange 2013 服务器角色体系结构](https://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [邮箱服务器和客户端访问服务器](https://technet.microsoft.com/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013 邮件Flow](https://technet.microsoft.com/library/aa996349.aspx)
- [Exchange Server 2013 邮件路由](https://technet.microsoft.com/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange ServerPowerShell (Exchange命令行管理程序) ](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

