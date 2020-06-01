---
title: Exchange 2013 中的传输代理命名空间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: 了解可用于创建 Exchange 2013 的自定义传输代理的 .NET Framework 类和成员。
ms.openlocfilehash: fc2d9108c910a730bb48c5be028797f0f15ad4ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461791"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Exchange 2013 中的传输代理命名空间

了解可用于创建 Exchange 2013 的自定义传输代理的 .NET Framework 类和成员。
  
**适用于：** Exchange Server 2013 
  
本文提供有关命名空间的信息，这些命名空间包含可用于为 Exchange Server 2013 创建传输代理的参考信息。 此外，它还介绍了您的传输代理可用于读取和修改通过传输管道的电子邮件的类。
  
## <a name="transport-agent-class-library"></a>传输代理类库

以下命名空间包含可用于创建和扩展传输代理的类型。

**表1。.NET Framework 命名空间**

|**命名空间**|**说明**|
|:-----|:-----|
|[Microsoft. Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |包含指定数据和配置异常的类型。  <br/> |
|[Microsoft. 常见](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |包含支持本地化和错误处理的类型。  <br/> |
|[ContentTypes 的数据。](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |包含使您能够读取和写入 iCalendar 数据的类型。  <br/> |
|["ContentTypes"。](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |包含使您能够读取和写入 TNEF 数据的类型。  <br/> |
|[ContentTypes 的电子名片](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |包含使您能够读取和写入电子名片数据的类型。  <br/> |
|[Microsoft. 全球数据](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |包含使您能够使用区域性和字符集生成本地化内容的类型。  <br/> |
|[Microsoft. 数据 Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |包含使您能够读取和写入 MIME 数据的类型。  <br/> |
|[（即，模拟编码器）](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |包含使您能够对 MIME 数据进行编码和解码的类型。  <br/> |
|[Microsoft TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |包含使您能够读取和写入具有不同文本格式的数据，并可将数据与这些格式相互转换的类型。  <br/> |
|[. 数据传输](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |包含使您能够访问传输管道的路由、主机和域信息的类型。  <br/> |
|[Microsoft. 传输数据](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |包含支持 Exchange 2013 传递代理扩展的类型。  <br/> |
|[Microsoft. 电子邮件](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |包含支持创建、读取、写入和修改电子邮件的类型。  <br/> |
|[Microsoft. 传输路由](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |包含支持 Exchange 2013 传输路由行为扩展的类型。  <br/> |
|[Microsoft. 传输. Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |包含支持 Exchange 2013 传输 SMTP 行为的扩展的类型。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)   
- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Exchange 的服务器 API 参考](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)
    

