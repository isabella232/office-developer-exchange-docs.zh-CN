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
# <a name="transport-agent-namespaces-in-exchange-2013"></a><span data-ttu-id="c0b76-103">Exchange 2013 中的传输代理命名空间</span><span class="sxs-lookup"><span data-stu-id="c0b76-103">Transport agent namespaces in Exchange 2013</span></span>

<span data-ttu-id="c0b76-104">了解可用于创建 Exchange 2013 的自定义传输代理的 .NET Framework 类和成员。</span><span class="sxs-lookup"><span data-stu-id="c0b76-104">Learn about the .NET Framework classes and members that you can use to create custom transport agents for Exchange 2013.</span></span>
  
<span data-ttu-id="c0b76-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b76-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="c0b76-106">本文提供有关命名空间的信息，这些命名空间包含可用于为 Exchange Server 2013 创建传输代理的参考信息。</span><span class="sxs-lookup"><span data-stu-id="c0b76-106">This article provides information about the namespaces that contain reference information that you can use to create transport agents for Exchange Server 2013.</span></span> <span data-ttu-id="c0b76-107">此外，它还介绍了您的传输代理可用于读取和修改通过传输管道的电子邮件的类。</span><span class="sxs-lookup"><span data-stu-id="c0b76-107">It also describes the classes that your transport agents can use to read and modify email messages that pass through the transport pipeline.</span></span>
  
## <a name="transport-agent-class-library"></a><span data-ttu-id="c0b76-108">传输代理类库</span><span class="sxs-lookup"><span data-stu-id="c0b76-108">Transport agent class library</span></span>

<span data-ttu-id="c0b76-109">以下命名空间包含可用于创建和扩展传输代理的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-109">The following namespaces contain types that you can use to create and extend transport agents.</span></span>

<span data-ttu-id="c0b76-110">**表1。.NET Framework 命名空间**</span><span class="sxs-lookup"><span data-stu-id="c0b76-110">**Table 1. .NET Framework namespaces**</span></span>

|<span data-ttu-id="c0b76-111">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="c0b76-111">**Namespace**</span></span>|<span data-ttu-id="c0b76-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0b76-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0b76-113">Microsoft. Data</span><span class="sxs-lookup"><span data-stu-id="c0b76-113">Microsoft.Exchange.Data</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |<span data-ttu-id="c0b76-114">包含指定数据和配置异常的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-114">Contains types that specify data and configuration exceptions.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-115">Microsoft. 常见</span><span class="sxs-lookup"><span data-stu-id="c0b76-115">Microsoft.Exchange.Data.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |<span data-ttu-id="c0b76-116">包含支持本地化和错误处理的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-116">Contains types that support localization and error handling.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-117">ContentTypes 的数据。</span><span class="sxs-lookup"><span data-stu-id="c0b76-117">Microsoft.Exchange.Data.ContentTypes.iCalendar</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |<span data-ttu-id="c0b76-118">包含使您能够读取和写入 iCalendar 数据的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-118">Contains types that enable you to read and write iCalendar data.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-119">"ContentTypes"。</span><span class="sxs-lookup"><span data-stu-id="c0b76-119">Microsoft.Exchange.Data.ContentTypes.Tnef</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |<span data-ttu-id="c0b76-120">包含使您能够读取和写入 TNEF 数据的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-120">Contains types that enable you to read and write TNEF data.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-121">ContentTypes 的电子名片</span><span class="sxs-lookup"><span data-stu-id="c0b76-121">Microsoft.Exchange.Data.ContentTypes.vCard</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |<span data-ttu-id="c0b76-122">包含使您能够读取和写入电子名片数据的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-122">Contains types that enable you to read and write vCard data.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-123">Microsoft. 全球数据</span><span class="sxs-lookup"><span data-stu-id="c0b76-123">Microsoft.Exchange.Data.Globalization</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |<span data-ttu-id="c0b76-124">包含使您能够使用区域性和字符集生成本地化内容的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-124">Contains types that enable you to work with cultures and character sets to produce localized content.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-125">Microsoft. 数据 Mime</span><span class="sxs-lookup"><span data-stu-id="c0b76-125">Microsoft.Exchange.Data.Mime</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |<span data-ttu-id="c0b76-126">包含使您能够读取和写入 MIME 数据的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-126">Contains types that enable you to read and write MIME data.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-127">（即，模拟编码器）</span><span class="sxs-lookup"><span data-stu-id="c0b76-127">Microsoft.Exchange.Data.Mime.Encoders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |<span data-ttu-id="c0b76-128">包含使您能够对 MIME 数据进行编码和解码的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-128">Contains types that enable you to encode and decode MIME data.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-129">Microsoft TextConverters</span><span class="sxs-lookup"><span data-stu-id="c0b76-129">Microsoft.Exchange.Data.TextConverters</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |<span data-ttu-id="c0b76-130">包含使您能够读取和写入具有不同文本格式的数据，并可将数据与这些格式相互转换的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-130">Contains types that enable you to read and write data with different text formats, and convert data to and from those formats.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-131">. 数据传输</span><span class="sxs-lookup"><span data-stu-id="c0b76-131">Microsoft.Exchange.Data.Transport</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |<span data-ttu-id="c0b76-132">包含使您能够访问传输管道的路由、主机和域信息的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-132">Contains types that enable you to access routing, host, and domain information about the transport pipeline.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-133">Microsoft. 传输数据</span><span class="sxs-lookup"><span data-stu-id="c0b76-133">Microsoft.Exchange.Data.Transport.Delivery</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |<span data-ttu-id="c0b76-134">包含支持 Exchange 2013 传递代理扩展的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-134">Contains types that support the extension of Exchange 2013 delivery agents.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-135">Microsoft. 电子邮件</span><span class="sxs-lookup"><span data-stu-id="c0b76-135">Microsoft.Exchange.Data.Transport.Email</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |<span data-ttu-id="c0b76-136">包含支持创建、读取、写入和修改电子邮件的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-136">Contains types that support creating, reading, writing, and modifying email messages.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-137">Microsoft. 传输路由</span><span class="sxs-lookup"><span data-stu-id="c0b76-137">Microsoft.Exchange.Data.Transport.Routing</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |<span data-ttu-id="c0b76-138">包含支持 Exchange 2013 传输路由行为扩展的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-138">Contains types that support the extension of the Exchange 2013 transport routing behavior.</span></span>  <br/> |
|[<span data-ttu-id="c0b76-139">Microsoft. 传输. Smtp</span><span class="sxs-lookup"><span data-stu-id="c0b76-139">Microsoft.Exchange.Data.Transport.Smtp</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |<span data-ttu-id="c0b76-140">包含支持 Exchange 2013 传输 SMTP 行为的扩展的类型。</span><span class="sxs-lookup"><span data-stu-id="c0b76-140">Contains types that support the extension of the Exchange 2013 transport SMTP behavior.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0b76-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0b76-141">See also</span></span>

- [<span data-ttu-id="c0b76-142">Exchange 中的传输代理</span><span class="sxs-lookup"><span data-stu-id="c0b76-142">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)   
- [<span data-ttu-id="c0b76-143">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="c0b76-143">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md) 
- <span data-ttu-id="c0b76-144">
  [Exchange 的服务器 API 参考](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0b76-144">[Server API reference for Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)</span></span>
- [<span data-ttu-id="c0b76-145">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="c0b76-145">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)
    

