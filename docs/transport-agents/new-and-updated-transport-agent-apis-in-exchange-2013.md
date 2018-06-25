---
title: 新增和经过更新的传输代理 Exchange 2013 中的 Api
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0a1ad73a-3085-4793-af4d-e4216484c93e
description: 找出哪些 Api 是新的或更新 Exchange 2013 中的传输代理。
ms.openlocfilehash: 0caafaf9629da1066d14357416862a7d67b961aa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753083"
---
# <a name="new-and-updated-transport-agent-apis-in-exchange-2013"></a><span data-ttu-id="ae1d2-103">新增和经过更新的传输代理 Exchange 2013 中的 Api</span><span class="sxs-lookup"><span data-stu-id="ae1d2-103">New and updated transport agent APIs in Exchange 2013</span></span>

<span data-ttu-id="ae1d2-104">找出哪些 Api 是新的或更新 Exchange 2013 中的传输代理。</span><span class="sxs-lookup"><span data-stu-id="ae1d2-104">Find out which APIs are new or updated in Exchange 2013 for transport agents.</span></span>

<span data-ttu-id="ae1d2-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae1d2-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="ae1d2-106">本文列出了类型的新的或更新 Exchange Server 2013 中影响传输代理。</span><span class="sxs-lookup"><span data-stu-id="ae1d2-106">This article lists types that are new or updated in Exchange Server 2013 that affect transport agents.</span></span> <span data-ttu-id="ae1d2-107">若要了解体系结构更改在 Exchange 2013 的影响传输代理，请参阅[传输代理概念在 Exchange 2013](transport-agent-concepts-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="ae1d2-107">To learn about architectural changes in Exchange 2013 that affect transport agents, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
  
## <a name="new-types-for-transport-agent-development-in-exchange-2013"></a><span data-ttu-id="ae1d2-108">在 Exchange 2013 中的传输代理开发的新类型</span><span class="sxs-lookup"><span data-stu-id="ae1d2-108">New types for transport agent development in Exchange 2013</span></span>

<span data-ttu-id="ae1d2-109">以下类型的新在 Exchange 2013:</span><span class="sxs-lookup"><span data-stu-id="ae1d2-109">The following types are new in Exchange 2013:</span></span>
  
- [<span data-ttu-id="ae1d2-110">NextHopCategory</span><span class="sxs-lookup"><span data-stu-id="ae1d2-110">NextHopCategory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.NextHopCategory.aspx)
    
- [<span data-ttu-id="ae1d2-111">RiskLevel</span><span class="sxs-lookup"><span data-stu-id="ae1d2-111">RiskLevel</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RiskLevel.aspx)
    
## <a name="updated-types-for-transport-agent-development-in-exchange-2013"></a><span data-ttu-id="ae1d2-112">更新的类型的传输代理开发在 Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ae1d2-112">Updated types for transport agent development in Exchange 2013</span></span>

<span data-ttu-id="ae1d2-113">Exchange 2013 中更新了以下类型：</span><span class="sxs-lookup"><span data-stu-id="ae1d2-113">The following types have been updated in Exchange 2013:</span></span>
  
- [<span data-ttu-id="ae1d2-114">ExchangeConfigurationException</span><span class="sxs-lookup"><span data-stu-id="ae1d2-114">ExchangeConfigurationException</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ExchangeConfigurationException.aspx)
    
- [<span data-ttu-id="ae1d2-115">CalendarWriter</span><span class="sxs-lookup"><span data-stu-id="ae1d2-115">CalendarWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx)
    
- [<span data-ttu-id="ae1d2-116">TnefReader</span><span class="sxs-lookup"><span data-stu-id="ae1d2-116">TnefReader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx)
    
- [<span data-ttu-id="ae1d2-117">TnefWriter</span><span class="sxs-lookup"><span data-stu-id="ae1d2-117">TnefWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx)
    
- [<span data-ttu-id="ae1d2-118">AddressHeader</span><span class="sxs-lookup"><span data-stu-id="ae1d2-118">AddressHeader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.AddressHeader.aspx)
    
- [<span data-ttu-id="ae1d2-119">ComplexHeader</span><span class="sxs-lookup"><span data-stu-id="ae1d2-119">ComplexHeader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.ComplexHeader.aspx)
    
- [<span data-ttu-id="ae1d2-120">EncodingFlags</span><span class="sxs-lookup"><span data-stu-id="ae1d2-120">EncodingFlags</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.EncodingFlags.aspx)
    
- [<span data-ttu-id="ae1d2-121">HeaderId</span><span class="sxs-lookup"><span data-stu-id="ae1d2-121">HeaderId</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.HeaderId.aspx)
    
- [<span data-ttu-id="ae1d2-122">HeaderList</span><span class="sxs-lookup"><span data-stu-id="ae1d2-122">HeaderList</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.HeaderList.aspx)
    
- [<span data-ttu-id="ae1d2-123">MimeComplianceStatus</span><span class="sxs-lookup"><span data-stu-id="ae1d2-123">MimeComplianceStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeComplianceStatus.aspx)
    
- [<span data-ttu-id="ae1d2-124">MimeGroup</span><span class="sxs-lookup"><span data-stu-id="ae1d2-124">MimeGroup</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeGroup.aspx)
    
- [<span data-ttu-id="ae1d2-125">MimeNode</span><span class="sxs-lookup"><span data-stu-id="ae1d2-125">MimeNode</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.aspx)
    
- [<span data-ttu-id="ae1d2-126">MimePart.PartSubtree</span><span class="sxs-lookup"><span data-stu-id="ae1d2-126">MimePart.PartSubtree</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimePart.PartSubtree.aspx)
    
- [<span data-ttu-id="ae1d2-127">MimePart.SubtreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="ae1d2-127">MimePart.SubtreeEnumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimePart.SubtreeEnumerator.aspx)
    
- [<span data-ttu-id="ae1d2-128">BinHexEncoder</span><span class="sxs-lookup"><span data-stu-id="ae1d2-128">BinHexEncoder</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [<span data-ttu-id="ae1d2-129">ConverterStream</span><span class="sxs-lookup"><span data-stu-id="ae1d2-129">ConverterStream</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx)
    
- [<span data-ttu-id="ae1d2-130">ConverterWriter</span><span class="sxs-lookup"><span data-stu-id="ae1d2-130">ConverterWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx)
    
- [<span data-ttu-id="ae1d2-131">HtmlReader</span><span class="sxs-lookup"><span data-stu-id="ae1d2-131">HtmlReader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlReader.aspx)
    
- [<span data-ttu-id="ae1d2-132">HtmlTagContext.AttributeCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-132">HtmlTagContext.AttributeCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlTagContext.AttributeCollection.aspx)
    
- [<span data-ttu-id="ae1d2-133">HtmlWriter</span><span class="sxs-lookup"><span data-stu-id="ae1d2-133">HtmlWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlWriter.aspx)
    
- [<span data-ttu-id="ae1d2-134">HtmlWriter</span><span class="sxs-lookup"><span data-stu-id="ae1d2-134">HtmlWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlWriter.aspx)
    
- [<span data-ttu-id="ae1d2-135">AcceptedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-135">AcceptedDomainCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.AcceptedDomainCollection.aspx)
    
- [<span data-ttu-id="ae1d2-136">EnvelopeRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-136">EnvelopeRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.EnvelopeRecipientCollection.aspx)
    
- [<span data-ttu-id="ae1d2-137">EnvelopeRecipientCollection.Enumerator</span><span class="sxs-lookup"><span data-stu-id="ae1d2-137">EnvelopeRecipientCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.EnvelopeRecipientCollection.Enumerator.aspx)
    
- [<span data-ttu-id="ae1d2-138">MailItem</span><span class="sxs-lookup"><span data-stu-id="ae1d2-138">MailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.MailItem.aspx)
    
- [<span data-ttu-id="ae1d2-139">PermissionCheckResults</span><span class="sxs-lookup"><span data-stu-id="ae1d2-139">PermissionCheckResults</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.PermissionCheckResults.aspx)
    
- [<span data-ttu-id="ae1d2-140">ReadOnlyEnvelopeRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-140">ReadOnlyEnvelopeRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.ReadOnlyEnvelopeRecipientCollection.aspx)
    
- [<span data-ttu-id="ae1d2-141">RecipientType</span><span class="sxs-lookup"><span data-stu-id="ae1d2-141">RecipientType</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RecipientType.aspx)
    
- [<span data-ttu-id="ae1d2-142">RemoteDomainCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-142">RemoteDomainCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RemoteDomainCollection.aspx)
    
- [<span data-ttu-id="ae1d2-143">RoutingAddress</span><span class="sxs-lookup"><span data-stu-id="ae1d2-143">RoutingAddress</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingAddress.aspx)
    
- [<span data-ttu-id="ae1d2-144">RoutingDomain</span><span class="sxs-lookup"><span data-stu-id="ae1d2-144">RoutingDomain</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingDomain.aspx)
    
- [<span data-ttu-id="ae1d2-145">路由主机</span><span class="sxs-lookup"><span data-stu-id="ae1d2-145">RoutingHost</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingHost.aspx)
    
- [<span data-ttu-id="ae1d2-146">RoutingOverride</span><span class="sxs-lookup"><span data-stu-id="ae1d2-146">RoutingOverride</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingOverride.aspx)
    
- [<span data-ttu-id="ae1d2-147">AttachmentCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-147">AttachmentCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.AttachmentCollection.aspx)
    
- [<span data-ttu-id="ae1d2-148">AttachmentCollection.Enumerator</span><span class="sxs-lookup"><span data-stu-id="ae1d2-148">AttachmentCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.AttachmentCollection.Enumerator.aspx)
    
- [<span data-ttu-id="ae1d2-149">EmailRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="ae1d2-149">EmailRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailRecipientCollection.aspx)
    
- [<span data-ttu-id="ae1d2-150">EmailRecipientCollection.Enumerator</span><span class="sxs-lookup"><span data-stu-id="ae1d2-150">EmailRecipientCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailRecipientCollection.Enumerator.aspx)
    
- [<span data-ttu-id="ae1d2-151">QueuedMessageEventSource</span><span class="sxs-lookup"><span data-stu-id="ae1d2-151">QueuedMessageEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.QueuedMessageEventSource.aspx)
    
- [<span data-ttu-id="ae1d2-152">RecipientExpansionInfo</span><span class="sxs-lookup"><span data-stu-id="ae1d2-152">RecipientExpansionInfo</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RecipientExpansionInfo.aspx)
    
- [<span data-ttu-id="ae1d2-153">ResolvedMessageEventHandler</span><span class="sxs-lookup"><span data-stu-id="ae1d2-153">ResolvedMessageEventHandler</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.ResolvedMessageEventHandler.aspx)
    
- [<span data-ttu-id="ae1d2-154">ResolvedMessageEventSource</span><span class="sxs-lookup"><span data-stu-id="ae1d2-154">ResolvedMessageEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.ResolvedMessageEventSource.aspx)
    
- [<span data-ttu-id="ae1d2-155">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="ae1d2-155">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    
- [<span data-ttu-id="ae1d2-156">ConnectEventArgs</span><span class="sxs-lookup"><span data-stu-id="ae1d2-156">ConnectEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.ConnectEventArgs.aspx)
    
- [<span data-ttu-id="ae1d2-157">DisconnectReason</span><span class="sxs-lookup"><span data-stu-id="ae1d2-157">DisconnectReason</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.DisconnectReason.aspx)
    
- [<span data-ttu-id="ae1d2-158">EhloCommandEventArgs</span><span class="sxs-lookup"><span data-stu-id="ae1d2-158">EhloCommandEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.EhloCommandEventArgs.aspx)
    
- [<span data-ttu-id="ae1d2-159">MailCommandEventArgs</span><span class="sxs-lookup"><span data-stu-id="ae1d2-159">MailCommandEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.MailCommandEventArgs.aspx)
    
- [<span data-ttu-id="ae1d2-160">ReceiveEventSource</span><span class="sxs-lookup"><span data-stu-id="ae1d2-160">ReceiveEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.ReceiveEventSource.aspx)
    
- [<span data-ttu-id="ae1d2-161">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="ae1d2-161">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    
- [<span data-ttu-id="ae1d2-162">SmtpResponse</span><span class="sxs-lookup"><span data-stu-id="ae1d2-162">SmtpResponse</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpResponse.aspx)
    
- [<span data-ttu-id="ae1d2-163">SmtpSession</span><span class="sxs-lookup"><span data-stu-id="ae1d2-163">SmtpSession</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpSession.aspx)
    
## <a name="see-also"></a><span data-ttu-id="ae1d2-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae1d2-164">See also</span></span>

- [<span data-ttu-id="ae1d2-165">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="ae1d2-165">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)  
- [<span data-ttu-id="ae1d2-166">创建 Exchange 2013 的传输代理</span><span class="sxs-lookup"><span data-stu-id="ae1d2-166">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)  
- [<span data-ttu-id="ae1d2-167">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="ae1d2-167">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

