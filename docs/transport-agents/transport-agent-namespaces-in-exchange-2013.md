---
title: Exchange 2013 中的传输代理命名空间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: 了解可用于.NET Framework 2013 自定义传输代理的 Exchange 类和成员。
ms.openlocfilehash: 076ddb8e2ccbdfa195a68aca6b296337a2876b55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537128"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Exchange 2013 中的传输代理命名空间

了解可用于.NET Framework 2013 自定义传输代理的 Exchange 类和成员。
  
**适用于：Exchange Server** 2013 
  
本文提供有关命名空间的信息，其中包含可用于为 Exchange Server 2013 创建传输代理的参考信息。 它还介绍了传输代理可用于读取和修改通过传输管道的电子邮件的类。
  
## <a name="transport-agent-class-library"></a>传输代理类库

以下命名空间包含可用于创建和扩展传输代理的类型。

**表 1..NET Framework命名空间**

|**命名空间**|**说明**|
|:-----|:-----|
|[Microsoft。Exchange。数据](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |包含指定数据和配置异常的类型。  <br/> |
|[Microsoft。Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |包含支持本地化和错误处理的类型。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |包含使您能够读取和写入 iCalendar 数据的类型。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |包含使您能够读取和写入 TNEF 数据的类型。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |包含使您能够读取和写入 vCard 数据的类型。  <br/> |
|[Microsoft。Exchange。Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |包含使您能够处理区域性和字符集以生成本地化内容的类型。  <br/> |
|[Microsoft。Exchange。Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |包含使您能够读取和写入 MIME 数据的类型。  <br/> |
|[Microsoft。Exchange。Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |包含使您能够对 MIME 数据进行编码和解码的类型。  <br/> |
|[Microsoft。Exchange。Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |包含使您可以使用不同文本格式读取和写入数据以及从这些格式转换数据的类型。  <br/> |
|[Microsoft。Exchange。Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |包含使您能够访问有关传输管道的路由、主机和域信息的类型。  <br/> |
|[Microsoft。Exchange。Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |包含支持 2013 Exchange代理扩展的类型。  <br/> |
|[Microsoft。Exchange。Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |包含支持创建、读取、写入和修改电子邮件的类型。  <br/> |
|[Microsoft。Exchange。Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |包含支持 2013 传输Exchange扩展的类型。  <br/> |
|[Microsoft。Exchange。Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |包含支持 2013 传输 SMTP Exchange扩展的类型。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)   
- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Exchange 的服务器 API 参考](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)
    

