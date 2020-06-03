---
title: 使用 Exchange 中的 EWS 设置 x 标头
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 设置邮箱的 x 标头。
ms.openlocfilehash: 409ddb944bbac7a60242de39cdf7ae13b17cc76a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527766"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a><span data-ttu-id="b16c9-103">使用 Exchange 中的 EWS 设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="b16c9-103">Provision x-headers by using EWS in Exchange</span></span>

<span data-ttu-id="b16c9-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 设置邮箱的 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-104">Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b16c9-105">X 标头是添加到电子邮件的头集合以传达信息的非标准标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-105">X-headers are non-standard headers that are added to the header collection of an email to communicate information.</span></span> <span data-ttu-id="b16c9-106">例如，Exchange 将带有**X-MS** --SCL 标头的邮件标记为表示电子邮件的垃圾邮件可信度（SCL）。</span><span class="sxs-lookup"><span data-stu-id="b16c9-106">For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email.</span></span> <span data-ttu-id="b16c9-107">Outlook 等电子邮件客户端可以使用该信息来确定对电子邮件执行的操作类型（例如，Outlook 可以阻止显示图像，除非用户采取了措施）。</span><span class="sxs-lookup"><span data-stu-id="b16c9-107">Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action).</span></span> 
  
<span data-ttu-id="b16c9-108">Exchange 会在邮箱架构中添加传入的 x 头作为命名属性，这是第一次收到该 x 标头的电子邮件时。</span><span class="sxs-lookup"><span data-stu-id="b16c9-108">Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header.</span></span> <span data-ttu-id="b16c9-109">X 头值不保存在第一封电子邮件上;但是，它会保存在包含 x 标头的所有后续电子邮件上。</span><span class="sxs-lookup"><span data-stu-id="b16c9-109">The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header.</span></span> <span data-ttu-id="b16c9-110">因此，您的应用程序应预配 x 标头，然后再预期使用它们。</span><span class="sxs-lookup"><span data-stu-id="b16c9-110">For this reason, your application should provision x-headers before you expect to use them.</span></span> <span data-ttu-id="b16c9-111">在电子邮件到邮箱的传输传递过程中出现命名属性和 x 标头之间的映射。</span><span class="sxs-lookup"><span data-stu-id="b16c9-111">The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox.</span></span> <span data-ttu-id="b16c9-112">这意味着，您需要通过传输传递来接收电子邮件;您不能只保存包含 x 头的电子邮件到邮箱，以创建到命名属性的映射。</span><span class="sxs-lookup"><span data-stu-id="b16c9-112">This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b16c9-113">如果发现不保存 x 标头，请确定[传输代理](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a)或[头防火墙](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)在到达邮箱之前是否筛选出您的 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-113">If you find that x-headers aren't being saved, determine whether a [transport agent](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox.</span></span> <span data-ttu-id="b16c9-114">r</span><span class="sxs-lookup"><span data-stu-id="b16c9-114">r</span></span>
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a><span data-ttu-id="b16c9-115">使用 EWS 托管 API 设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="b16c9-115">Provision an x-header by using the EWS Managed API</span></span>
<span data-ttu-id="b16c9-116"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="b16c9-116"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="b16c9-117">下面的代码示例演示如何使用 EWS 托管 API [EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)方法来设置邮箱的 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-117">The following code example shows how to use the EWS Managed API [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox.</span></span> <span data-ttu-id="b16c9-118">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，且目标邮箱尚未超过[命名属性的配额](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b16c9-118">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx).</span></span>
  
```cs
private static void ProvisionCustomXHeaderByEmail(ExchangeService service)
{
    // Create a definition for an extended property that will represent a custom x-header. X-headers must be created in the
    // InternetHeaders property set. The x-header name must match the name of the x-header sent in the subsequent emails so
    // the x-header and value are saved on the email.
    ExtendedPropertyDefinition xExperimentalHeader = new ExtendedPropertyDefinition(DefaultExtendedPropertySet.InternetHeaders,
                                                                                            "X-Experimental",
                                                                                            MapiPropertyType.String);
    // Create an item that is used to provision the custom x-header.
    EmailMessage email = new EmailMessage(service);
    email.ToRecipients.Add("user@contoso.com");
    email.SetExtendedProperty(xExperimentalHeader, "Provision X-Experimental Internet message header");
    try
    {
        // The mapping of the named property happens in transport delivery.
        email.Send();
        if (service.ServerInfo.MajorVersion == 12)
        {
            Console.WriteLine("Provisioned the X-Experimental across the mailbox database that hosts the user's mailbox.");
        }
        else // For versions of Exchange starting with Exchange 2010
        {
            Console.WriteLine("Provisioned the X-Experimental for the user's mailbox. You will need to run this " +
                                "for each mailbox that needs to process this x-header.");
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error: {0}", ex.Message);
    }
}
```

## <a name="provision-an-x-header-by-using-ews"></a><span data-ttu-id="b16c9-119">使用 EWS 设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="b16c9-119">Provision an x-header by using EWS</span></span>
<span data-ttu-id="b16c9-120"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="b16c9-120"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="b16c9-121">下面的代码示例演示如何使用 EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)操作创建并发送电子邮件，以设置具有 x 标头的邮箱。</span><span class="sxs-lookup"><span data-stu-id="b16c9-121">The following code example shows how to use the EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header.</span></span> <span data-ttu-id="b16c9-122">这是通过[使用 Ews 托管 Api 设置 x 标头](#bk_example1)时由 EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="b16c9-122">This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendOnly">
      <m:Items>
        <t:Message>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="InternetHeaders"
                                PropertyName="X-Experimental"
                                PropertyType="String" />
            <t:Value>Provision X-Experimental Internet message header</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>user@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

## <a name="version-differences"></a><span data-ttu-id="b16c9-123">版本差异</span><span class="sxs-lookup"><span data-stu-id="b16c9-123">Version differences</span></span>
<span data-ttu-id="b16c9-124"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="b16c9-124"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="b16c9-125">首次在 Exchange Online 中设置 x 标头，将 Exchange Online 作为 Office 365 的一部分，或从 Exchange Server 2010 开始的本地 Exchange 版本，将不会将新的自定义 x 标头的值写入到存储的邮件中。</span><span class="sxs-lookup"><span data-stu-id="b16c9-125">The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message.</span></span> <span data-ttu-id="b16c9-126">这是因为必须首先将 x 标头映射到用户邮箱中的命名属性。</span><span class="sxs-lookup"><span data-stu-id="b16c9-126">This is because the x-header must first be mapped to a named property in the user's mailbox.</span></span> <span data-ttu-id="b16c9-127">映射发生在首次请求添加命名属性时。</span><span class="sxs-lookup"><span data-stu-id="b16c9-127">The mapping occurs upon the first request to add the named properties.</span></span> <span data-ttu-id="b16c9-128">当后续请求创建命名属性时，属性和值存储在邮件上。</span><span class="sxs-lookup"><span data-stu-id="b16c9-128">When a subsequent request to create the named property occurs, the property and value are stored on the message.</span></span> <span data-ttu-id="b16c9-129">在 Exchange 2007 中，第一次将 x 标头写入邮箱数据库时，会在邮箱数据库中为 x 标头创建一个映射，这是一个命名属性。</span><span class="sxs-lookup"><span data-stu-id="b16c9-129">In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database.</span></span> <span data-ttu-id="b16c9-130">在后续请求创建命名属性时，将对 Exchange 2007 数据库中的任何邮箱处理和存储 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-130">When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="b16c9-131">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b16c9-131">Next steps</span></span>
<span data-ttu-id="b16c9-132"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="b16c9-132"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="b16c9-133">本文介绍如何通过向用户发送电子邮件来为单个邮箱设置 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-133">This article shows you how to provision an x-header for a single mailbox by sending an email to a user.</span></span> <span data-ttu-id="b16c9-134">您还可以通过将[批处理电子邮件发送到](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)呼叫者组织中的收件人列表，为多个用户预配 x 标头。</span><span class="sxs-lookup"><span data-stu-id="b16c9-134">You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b16c9-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b16c9-135">See also</span></span>


- [<span data-ttu-id="b16c9-136">属性和交换中的 EWS 中的扩展的属性</span><span class="sxs-lookup"><span data-stu-id="b16c9-136">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="b16c9-137">Exchange 2013：以编程方式设置自定义 X 标头</span><span class="sxs-lookup"><span data-stu-id="b16c9-137">Exchange 2013: Provision custom X-headers programmatically</span></span>](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [<span data-ttu-id="b16c9-138">命名属性、X 标头和您</span><span class="sxs-lookup"><span data-stu-id="b16c9-138">Named Properties, X-Headers, and You</span></span>](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [<span data-ttu-id="b16c9-139">命名属性，圆形2：提前</span><span class="sxs-lookup"><span data-stu-id="b16c9-139">Named Properties, Round 2: What lies Ahead</span></span>](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [<span data-ttu-id="b16c9-140">标头防火墙</span><span class="sxs-lookup"><span data-stu-id="b16c9-140">Header Firewall</span></span>](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="b16c9-141">EWS、MIME 和缺少的 Internet 邮件头</span><span class="sxs-lookup"><span data-stu-id="b16c9-141">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [<span data-ttu-id="b16c9-142">使用 Exchange 中的 EWS 批量处理电子邮件</span><span class="sxs-lookup"><span data-stu-id="b16c9-142">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

