---
title: Exchange 2013 中的新的和更新的传输代理 Api
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0a1ad73a-3085-4793-af4d-e4216484c93e
description: 了解 Exchange 2013 中新的或更新的用于传输代理的 Api。
ms.openlocfilehash: 9cb099757512081347e23bc619c42417929f0f70
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461819"
---
# <a name="new-and-updated-transport-agent-apis-in-exchange-2013"></a><span data-ttu-id="d6f17-103">Exchange 2013 中的新的和更新的传输代理 Api</span><span class="sxs-lookup"><span data-stu-id="d6f17-103">New and updated transport agent APIs in Exchange 2013</span></span>

<span data-ttu-id="d6f17-104">了解 Exchange 2013 中新的或更新的用于传输代理的 Api。</span><span class="sxs-lookup"><span data-stu-id="d6f17-104">Find out which APIs are new or updated in Exchange 2013 for transport agents.</span></span>

<span data-ttu-id="d6f17-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6f17-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="d6f17-106">本文列出了在 Exchange Server 2013 中新增或更新的类型，这些类型会影响传输代理。</span><span class="sxs-lookup"><span data-stu-id="d6f17-106">This article lists types that are new or updated in Exchange Server 2013 that affect transport agents.</span></span> <span data-ttu-id="d6f17-107">若要了解影响传输代理的 Exchange 2013 中的体系结构更改，请参阅[exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f17-107">To learn about architectural changes in Exchange 2013 that affect transport agents, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
  
## <a name="new-types-for-transport-agent-development-in-exchange-2013"></a><span data-ttu-id="d6f17-108">Exchange 2013 中的传输代理开发的新类型</span><span class="sxs-lookup"><span data-stu-id="d6f17-108">New types for transport agent development in Exchange 2013</span></span>

<span data-ttu-id="d6f17-109">以下类型是 Exchange 2013 中的新类型：</span><span class="sxs-lookup"><span data-stu-id="d6f17-109">The following types are new in Exchange 2013:</span></span>
  
- [<span data-ttu-id="d6f17-110">NextHopCategory</span><span class="sxs-lookup"><span data-stu-id="d6f17-110">NextHopCategory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.NextHopCategory.aspx)
    
- [<span data-ttu-id="d6f17-111">RiskLevel</span><span class="sxs-lookup"><span data-stu-id="d6f17-111">RiskLevel</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RiskLevel.aspx)
    
## <a name="updated-types-for-transport-agent-development-in-exchange-2013"></a><span data-ttu-id="d6f17-112">Exchange 2013 中传输代理开发的更新类型</span><span class="sxs-lookup"><span data-stu-id="d6f17-112">Updated types for transport agent development in Exchange 2013</span></span>

<span data-ttu-id="d6f17-113">已在 Exchange 2013 中更新以下类型：</span><span class="sxs-lookup"><span data-stu-id="d6f17-113">The following types have been updated in Exchange 2013:</span></span>
  
- [<span data-ttu-id="d6f17-114">ExchangeConfigurationException</span><span class="sxs-lookup"><span data-stu-id="d6f17-114">ExchangeConfigurationException</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ExchangeConfigurationException.aspx)
    
- [<span data-ttu-id="d6f17-115">CalendarWriter</span><span class="sxs-lookup"><span data-stu-id="d6f17-115">CalendarWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx)
    
- [<span data-ttu-id="d6f17-116">TnefReader</span><span class="sxs-lookup"><span data-stu-id="d6f17-116">TnefReader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx)
    
- [<span data-ttu-id="d6f17-117">TnefWriter</span><span class="sxs-lookup"><span data-stu-id="d6f17-117">TnefWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx)
    
- [<span data-ttu-id="d6f17-118">AddressHeader</span><span class="sxs-lookup"><span data-stu-id="d6f17-118">AddressHeader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.AddressHeader.aspx)
    
- [<span data-ttu-id="d6f17-119">ComplexHeader</span><span class="sxs-lookup"><span data-stu-id="d6f17-119">ComplexHeader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.ComplexHeader.aspx)
    
- [<span data-ttu-id="d6f17-120">EncodingFlags</span><span class="sxs-lookup"><span data-stu-id="d6f17-120">EncodingFlags</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.EncodingFlags.aspx)
    
- [<span data-ttu-id="d6f17-121">HeaderId</span><span class="sxs-lookup"><span data-stu-id="d6f17-121">HeaderId</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.HeaderId.aspx)
    
- [<span data-ttu-id="d6f17-122">HeaderList</span><span class="sxs-lookup"><span data-stu-id="d6f17-122">HeaderList</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.HeaderList.aspx)
    
- [<span data-ttu-id="d6f17-123">MimeComplianceStatus</span><span class="sxs-lookup"><span data-stu-id="d6f17-123">MimeComplianceStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeComplianceStatus.aspx)
    
- [<span data-ttu-id="d6f17-124">MimeGroup</span><span class="sxs-lookup"><span data-stu-id="d6f17-124">MimeGroup</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeGroup.aspx)
    
- [<span data-ttu-id="d6f17-125">MimeNode</span><span class="sxs-lookup"><span data-stu-id="d6f17-125">MimeNode</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.aspx)
    
- [<span data-ttu-id="d6f17-126">MimePart.PartSubtree</span><span class="sxs-lookup"><span data-stu-id="d6f17-126">MimePart.PartSubtree</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimePart.PartSubtree.aspx)
    
- [<span data-ttu-id="d6f17-127">MimePart.SubtreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="d6f17-127">MimePart.SubtreeEnumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimePart.SubtreeEnumerator.aspx)
    
- [<span data-ttu-id="d6f17-128">BinHexEncoder</span><span class="sxs-lookup"><span data-stu-id="d6f17-128">BinHexEncoder</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [<span data-ttu-id="d6f17-129">ConverterStream</span><span class="sxs-lookup"><span data-stu-id="d6f17-129">ConverterStream</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx)
    
- [<span data-ttu-id="d6f17-130">ConverterWriter</span><span class="sxs-lookup"><span data-stu-id="d6f17-130">ConverterWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx)
    
- [<span data-ttu-id="d6f17-131">HtmlReader</span><span class="sxs-lookup"><span data-stu-id="d6f17-131">HtmlReader</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlReader.aspx)
    
- [<span data-ttu-id="d6f17-132">HtmlTagContext.AttributeCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-132">HtmlTagContext.AttributeCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlTagContext.AttributeCollection.aspx)
    
- [<span data-ttu-id="d6f17-133">HtmlWriter</span><span class="sxs-lookup"><span data-stu-id="d6f17-133">HtmlWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlWriter.aspx)
    
- [<span data-ttu-id="d6f17-134">HtmlWriter</span><span class="sxs-lookup"><span data-stu-id="d6f17-134">HtmlWriter</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlWriter.aspx)
    
- [<span data-ttu-id="d6f17-135">AcceptedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-135">AcceptedDomainCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.AcceptedDomainCollection.aspx)
    
- [<span data-ttu-id="d6f17-136">EnvelopeRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-136">EnvelopeRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.EnvelopeRecipientCollection.aspx)
    
- [<span data-ttu-id="d6f17-137">EnvelopeRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-137">EnvelopeRecipientCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.EnvelopeRecipientCollection.Enumerator.aspx)
    
- [<span data-ttu-id="d6f17-138">MailItem</span><span class="sxs-lookup"><span data-stu-id="d6f17-138">MailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.MailItem.aspx)
    
- [<span data-ttu-id="d6f17-139">PermissionCheckResults</span><span class="sxs-lookup"><span data-stu-id="d6f17-139">PermissionCheckResults</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.PermissionCheckResults.aspx)
    
- [<span data-ttu-id="d6f17-140">ReadOnlyEnvelopeRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-140">ReadOnlyEnvelopeRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.ReadOnlyEnvelopeRecipientCollection.aspx)
    
- [<span data-ttu-id="d6f17-141">RecipientType</span><span class="sxs-lookup"><span data-stu-id="d6f17-141">RecipientType</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RecipientType.aspx)
    
- [<span data-ttu-id="d6f17-142">RemoteDomainCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-142">RemoteDomainCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RemoteDomainCollection.aspx)
    
- [<span data-ttu-id="d6f17-143">RoutingAddress</span><span class="sxs-lookup"><span data-stu-id="d6f17-143">RoutingAddress</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingAddress.aspx)
    
- [<span data-ttu-id="d6f17-144">RoutingDomain</span><span class="sxs-lookup"><span data-stu-id="d6f17-144">RoutingDomain</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingDomain.aspx)
    
- [<span data-ttu-id="d6f17-145">RoutingHost</span><span class="sxs-lookup"><span data-stu-id="d6f17-145">RoutingHost</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingHost.aspx)
    
- [<span data-ttu-id="d6f17-146">RoutingOverride</span><span class="sxs-lookup"><span data-stu-id="d6f17-146">RoutingOverride</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.RoutingOverride.aspx)
    
- [<span data-ttu-id="d6f17-147">AttachmentCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-147">AttachmentCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.AttachmentCollection.aspx)
    
- [<span data-ttu-id="d6f17-148">AttachmentCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-148">AttachmentCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.AttachmentCollection.Enumerator.aspx)
    
- [<span data-ttu-id="d6f17-149">EmailRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-149">EmailRecipientCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailRecipientCollection.aspx)
    
- [<span data-ttu-id="d6f17-150">EmailRecipientCollection</span><span class="sxs-lookup"><span data-stu-id="d6f17-150">EmailRecipientCollection.Enumerator</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailRecipientCollection.Enumerator.aspx)
    
- [<span data-ttu-id="d6f17-151">QueuedMessageEventSource</span><span class="sxs-lookup"><span data-stu-id="d6f17-151">QueuedMessageEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.QueuedMessageEventSource.aspx)
    
- [<span data-ttu-id="d6f17-152">RecipientExpansionInfo</span><span class="sxs-lookup"><span data-stu-id="d6f17-152">RecipientExpansionInfo</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RecipientExpansionInfo.aspx)
    
- [<span data-ttu-id="d6f17-153">ResolvedMessageEventHandler</span><span class="sxs-lookup"><span data-stu-id="d6f17-153">ResolvedMessageEventHandler</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.ResolvedMessageEventHandler.aspx)
    
- [<span data-ttu-id="d6f17-154">ResolvedMessageEventSource</span><span class="sxs-lookup"><span data-stu-id="d6f17-154">ResolvedMessageEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.ResolvedMessageEventSource.aspx)
    
- [<span data-ttu-id="d6f17-155">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="d6f17-155">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    
- [<span data-ttu-id="d6f17-156">ConnectEventArgs</span><span class="sxs-lookup"><span data-stu-id="d6f17-156">ConnectEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.ConnectEventArgs.aspx)
    
- [<span data-ttu-id="d6f17-157">DisconnectReason</span><span class="sxs-lookup"><span data-stu-id="d6f17-157">DisconnectReason</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.DisconnectReason.aspx)
    
- [<span data-ttu-id="d6f17-158">EhloCommandEventArgs</span><span class="sxs-lookup"><span data-stu-id="d6f17-158">EhloCommandEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.EhloCommandEventArgs.aspx)
    
- [<span data-ttu-id="d6f17-159">MailCommandEventArgs</span><span class="sxs-lookup"><span data-stu-id="d6f17-159">MailCommandEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.MailCommandEventArgs.aspx)
    
- [<span data-ttu-id="d6f17-160">ReceiveEventSource</span><span class="sxs-lookup"><span data-stu-id="d6f17-160">ReceiveEventSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.ReceiveEventSource.aspx)
    
- [<span data-ttu-id="d6f17-161">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="d6f17-161">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    
- [<span data-ttu-id="d6f17-162">SmtpResponse</span><span class="sxs-lookup"><span data-stu-id="d6f17-162">SmtpResponse</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpResponse.aspx)
    
- [<span data-ttu-id="d6f17-163">SmtpSession</span><span class="sxs-lookup"><span data-stu-id="d6f17-163">SmtpSession</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpSession.aspx)
    
## <a name="see-also"></a><span data-ttu-id="d6f17-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d6f17-164">See also</span></span>

- [<span data-ttu-id="d6f17-165">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="d6f17-165">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)  
- [<span data-ttu-id="d6f17-166">创建 Exchange 2013 的传输代理</span><span class="sxs-lookup"><span data-stu-id="d6f17-166">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)  
- [<span data-ttu-id="d6f17-167">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="d6f17-167">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

