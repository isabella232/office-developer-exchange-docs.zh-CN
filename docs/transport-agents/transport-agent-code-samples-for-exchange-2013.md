---
title: Exchange 2013 的传输代理代码示例
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: 查找有关可用于 Exchange 2013 的示例传输代理的信息。
ms.openlocfilehash: 56334f661947cffceaf18eb257feeb6504a71ecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545707"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Exchange 2013 的传输代理代码示例

查找有关可用于 Exchange 2013 的示例传输代理的信息。
  
**适用于：Exchange Server** 2013
  
您可以使用 2013 年 Exchange Server中包含的 API 来开发扩展传输功能的代理。 本文提供有关示例代理的信息，这些代理可帮助您了解如何以编程方式扩展传输行为。 示例代理包括每个组件的源代码。 
  
下表列出了 2013 年 Exchange代理。
  
**表 1.传输代理示例**

|**示例名称**|**说明**|
|:-----|:-----|
|[Exchange 2013：生成防病毒传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |此代理响应 [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) 和 [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) 事件，并将传入邮件发送到进程外服务器，该服务器异步检查邮件并返回修改的版本。  <br/> |
|[Exchange 2013：构建带宽日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |此代理响应 [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) 和 [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) 事件，捕获指定收件人的带宽使用情况，将带宽使用率信息记录到文本文件。  <br/> |
|[Exchange 2013：构建正文转换传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |此代理通过确定传入邮件的格式并确定是否必须执行筛选来筛选电子邮件中的脚本。 如果需要筛选，内容将转换为 HTML，经过筛选，然后转换回源格式。  <br/> |
|[Exchange 2013：构建 SMTP 日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |此代理响应 [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) 事件，并异步将消息记录到本地硬盘上的文件。  <br/> |
|[Exchange 2013：构建临时阻止发件人的传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |此代理响应 [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) 和 [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) 事件，并确定邮件发件人之前是否已将邮件发送到前端传输服务。 如果发件人之前未向前端传输服务发送邮件，则发件人将添加到发件人列表中，邮件将被拒绝，并响应通知客户端稍后重试 (也称为灰色列表) 。 如果发件人在以前的发件人列表中，则代理不会拒绝该邮件。  <br/> |
|[Exchange 2013：生成邮箱服务器日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |此代理响应 [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) 传输管道事件，并同步将邮件记录到本地硬盘上的文件。  <br/> |
|[Exchange 2013：生成 X 标头传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |此代理响应 [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) 事件，并读取和修改邮件中的 X 标头。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)    
- [为 Exchange 2013 创建 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [为 Exchange 2013 创建 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [为 Exchange 2013 创建 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

