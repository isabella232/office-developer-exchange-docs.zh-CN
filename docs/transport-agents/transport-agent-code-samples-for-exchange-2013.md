---
title: 传输代理的 Exchange 2013 的代码示例
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: 查找有关适用于 Exchange 2013 示例传输代理信息。
ms.openlocfilehash: 122a3351748fa6ffd823a51ce65ffb913332cb2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753084"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>传输代理的 Exchange 2013 的代码示例

查找有关适用于 Exchange 2013 示例传输代理信息。
  
**适用于：** Exchange Server 2013
  
您可以使用 Exchange Server 2013 开发的扩展功能传输代理中包含的 Api。 本文提供有关可用于帮助您了解如何以编程方式扩展传输行为示例代理信息。 示例代理包括每个组件的源代码。 
  
下表列出了示例代理 Exchange 2013。
  
**表 1。传输代理示例**

|**示例名称**|**说明**|
|:-----|:-----|
|[Exchange 2013： 生成防病毒传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |此代理响应[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)和[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件，并将传入邮件发送到进程外服务器将异步检查邮件，并返回的修改的版本。  <br/> |
|[Exchange 2013： 构建带宽日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |此代理响应[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)和[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件、 指定的收件人，捕获带宽使用情况和记录到文本文件的带宽使用情况信息。  <br/> |
|[Exchange 2013： 构建正文转换传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |此代理通过确定传入消息的格式，决定必须发生筛选筛选出电子邮件的脚本。 是否需要筛选时，内容转换为 HTML、 筛选，然后转换回源格式。  <br/> |
|[Exchange 2013： 生成 SMTP 日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |此代理响应[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)事件中，并异步将消息记录到本地硬盘上的文件。  <br/> |
|[Exchange 2013： 构建暂时阻止发件人的传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |此代理响应的[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx)和[OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx)事件，并确定是否发件人之前具有到前端传输服务发送消息。 如果发件人未以前发送一条消息，前端传输服务、 发件人添加到的发件人列表和一个通知客户端稍后重试的响应拒绝邮件 (也称为 graylisting)。 如果发件人的以前的发件人列表中，也代理不拒绝邮件。  <br/> |
|[Exchange 2013： 构建邮箱服务器日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |此代理响应[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)传输管道事件，并同步到本地硬盘上的文件中记录消息。  <br/> |
|[Exchange 2013： 生成 X 标头传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |此代理响应[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx)事件和阅读消息中修改 X 标头。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)    
- [创建 Exchange 2013 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [创建 Exchange 2013 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [创建 Exchange 2013 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

