---
title: 传输代理 Exchange 2013 中的命名空间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: 了解有关的.NET Framework 类和成员的可用来创建 Exchange 2013 的自定义传输代理。
ms.openlocfilehash: a8189ca9915312b64fefda3091f8f81e51271ad6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753088"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>传输代理 Exchange 2013 中的命名空间

了解有关的.NET Framework 类和成员的可用来创建 Exchange 2013 的自定义传输代理。
  
**适用于：** Exchange Server 2013 
  
本文提供了有关包含可用于创建传输代理的 Exchange Server 2013 的参考信息的命名空间的信息。 该参数还描述可用于读取和修改通过传输管道传递的电子邮件传输代理的类。
  
## <a name="transport-agent-class-library"></a>传输代理类库

以下命名空间包含可用于创建和扩展传输代理的类型。

**表 1。.NET framework 命名空间**

|**命名空间**|**说明**|
|:-----|:-----|
|[Microsoft.Exchange.Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |包含指定数据和配置例外的类型。  <br/> |
|[Microsoft.Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |包含支持本地化和错误处理的类型。  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |包含使您能够读取和写入 iCalendar 数据的类型。  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |包含使您能够读取和写入 TNEF 数据的类型。  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |包含使您能够读取和写入 vCard 数据的类型。  <br/> |
|[Microsoft.Exchange.Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |包含使您能够使用区域性和字符集以生成本地化的内容的类型。  <br/> |
|[Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |包含使您能够读取和写入 MIME 数据的类型。  <br/> |
|[Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |包含使您能够进行编码和解码 MIME 数据的类型。  <br/> |
|[Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |包含使您能够读取和写入数据使用不同的文本格式，并与这些格式转换数据类型。  <br/> |
|[Microsoft.Exchange.Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |包含使您能够访问路由、 主机和传输管道的域信息的类型。  <br/> |
|[Microsoft.Exchange.Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |包含支持 Exchange 2013 传递代理的扩展的类型。  <br/> |
|[Microsoft.Exchange.Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |包含支持创建、 读取、 写入，并修改电子邮件的类型。  <br/> |
|[Microsoft.Exchange.Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |包含支持的扩展的 Exchange 2013 传输路由行为的类型。  <br/> |
|[Microsoft.Exchange.Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |包含支持的扩展的 Exchange 2013 传输 SMTP 行为的类型。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在 Exchange 传输代理](transport-agents-in-exchange-2013.md)   
- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md) 
- [Exchange server API 参考](http://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)
    

