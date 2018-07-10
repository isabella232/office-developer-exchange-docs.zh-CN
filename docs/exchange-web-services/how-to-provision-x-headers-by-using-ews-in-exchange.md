---
title: 在 Exchange 使用 EWS 的设置 x 标头
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中设置邮箱的 x 标头。
ms.openlocfilehash: de572764921da432cfa203b3dcf166d1d34dd0cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752867"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a><span data-ttu-id="89f38-103">在 Exchange 使用 EWS 的设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="89f38-103">Provision x-headers by using EWS in Exchange</span></span>

<span data-ttu-id="89f38-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中设置邮箱的 x 标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-104">Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="89f38-105">X 标头都是添加到标头集合的电子邮件进行通信信息的非标准标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-105">X-headers are non-standard headers that are added to the header collection of an email to communicate information.</span></span> <span data-ttu-id="89f38-106">例如，Exchange 戳**X-MS-Exchange-组织的 SCL**标头的消息以指示电子邮件的垃圾邮件可信度 (SCL)。</span><span class="sxs-lookup"><span data-stu-id="89f38-106">For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email.</span></span> <span data-ttu-id="89f38-107">电子邮件客户端，如 Outlook 可以使用这些信息来确定要对电子邮件执行操作的类型 （例如，Outlook 可以阻止图像显示除非用户执行的操作）。</span><span class="sxs-lookup"><span data-stu-id="89f38-107">Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action).</span></span> 
  
<span data-ttu-id="89f38-108">Exchange 将传入 x 标头添加到邮箱架构，它会接收电子邮件的 x 标头的命名的属性第一个时间形式。</span><span class="sxs-lookup"><span data-stu-id="89f38-108">Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header.</span></span> <span data-ttu-id="89f38-109">X 标头值不会保存上的第一个电子邮件;但是，它将保存所有后续的电子邮件，包括 x 标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-109">The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header.</span></span> <span data-ttu-id="89f38-110">因此，您的应用程序应设置 x 标头之前您希望使用它们。</span><span class="sxs-lookup"><span data-stu-id="89f38-110">For this reason, your application should provision x-headers before you expect to use them.</span></span> <span data-ttu-id="89f38-111">电子邮件传输传递到邮箱中发生的命名的属性和 x 标头之间的映射。</span><span class="sxs-lookup"><span data-stu-id="89f38-111">The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox.</span></span> <span data-ttu-id="89f38-112">这意味着，您需要接收传输传递; 通过电子邮件只需无法保存电子邮件，其中包括 x 标头邮箱创建到命名属性的映射。</span><span class="sxs-lookup"><span data-stu-id="89f38-112">This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="89f38-113">如果您发现 x 标头不会保存，确定是否[传输代理](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a)或[标头防火墙](http://technet.microsoft.com/zh-cn/library/bb232136%28v=exchg.150%29.aspx)筛选出 x 标头到达邮箱之前。</span><span class="sxs-lookup"><span data-stu-id="89f38-113">If you find that x-headers aren't being saved, determine whether a [transport agent](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](http://technet.microsoft.com/zh-cn/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox.</span></span> 
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a><span data-ttu-id="89f38-114">使用 EWS 托管 API 设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="89f38-114">Provision an x-header by using the EWS Managed API</span></span>
<span data-ttu-id="89f38-115"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="89f38-115"></span></span>

<span data-ttu-id="89f38-116">下面的代码示例演示如何使用 EWS 托管 API [EmailMessage.Send](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)方法可设置邮箱的 x 标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-116">The following code example shows how to use the EWS Managed API [EmailMessage.Send](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox.</span></span> <span data-ttu-id="89f38-117">此示例假定该**服务**是有效[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和目标邮箱尚未超出[配额的命名属性](http://technet.microsoft.com/zh-cn/library/bb851492%28v=EXCHG.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="89f38-117">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](http://technet.microsoft.com/zh-cn/library/bb851492%28v=EXCHG.80%29.aspx).</span></span>
  
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

## <a name="provision-an-x-header-by-using-ews"></a><span data-ttu-id="89f38-118">使用 EWS 设置 x 标头</span><span class="sxs-lookup"><span data-stu-id="89f38-118">Provision an x-header by using EWS</span></span>
<span data-ttu-id="89f38-119"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="89f38-119"></span></span>

<span data-ttu-id="89f38-120">下面的代码示例演示如何使用 EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation，创建和发送电子邮件设置具有 x 标头的邮箱。</span><span class="sxs-lookup"><span data-stu-id="89f38-120">The following code example shows how to use the EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header.</span></span> <span data-ttu-id="89f38-121">这是 XML 请求发送的 EWS 托管 API 时您[设置使用 EWS 托管 API x 标头](#bk_example1)。</span><span class="sxs-lookup"><span data-stu-id="89f38-121">This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="version-differences"></a><span data-ttu-id="89f38-122">版本差异</span><span class="sxs-lookup"><span data-stu-id="89f38-122">Version differences</span></span>
<span data-ttu-id="89f38-123"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="89f38-123"></span></span>

<span data-ttu-id="89f38-124">在 Exchange 设置 x 标头的第一个时间 Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange Server 2010 的本地版本，新的自定义 x 标头的值将不写入到存储的邮件。</span><span class="sxs-lookup"><span data-stu-id="89f38-124">The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message.</span></span> <span data-ttu-id="89f38-125">这是因为 x 标头必须首先将映射到用户的邮箱中的命名属性。</span><span class="sxs-lookup"><span data-stu-id="89f38-125">This is because the x-header must first be mapped to a named property in the user's mailbox.</span></span> <span data-ttu-id="89f38-126">映射发生在首次请求来添加命名的属性。</span><span class="sxs-lookup"><span data-stu-id="89f38-126">The mapping occurs upon the first request to add the named properties.</span></span> <span data-ttu-id="89f38-127">创建命名的属性的后续请求时，邮件上存储的属性和值。</span><span class="sxs-lookup"><span data-stu-id="89f38-127">When a subsequent request to create the named property occurs, the property and value are stored on the message.</span></span> <span data-ttu-id="89f38-128">在 Exchange 2007，第一次 x 标头写入到的邮箱数据库，创建一个映射到命名属性的 x 标头跨邮箱数据库。</span><span class="sxs-lookup"><span data-stu-id="89f38-128">In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database.</span></span> <span data-ttu-id="89f38-129">创建命名的属性的后续请求时，x 标头处理和存储为 Exchange 2007 数据库中的任何邮箱。</span><span class="sxs-lookup"><span data-stu-id="89f38-129">When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="89f38-130">后续步骤</span><span class="sxs-lookup"><span data-stu-id="89f38-130">Next steps</span></span>
<span data-ttu-id="89f38-131"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="89f38-131"></span></span>

<span data-ttu-id="89f38-132">本文介绍如何通过向用户发送电子邮件设置的单个邮箱 x 标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-132">This article shows you how to provision an x-header for a single mailbox by sending an email to a user.</span></span> <span data-ttu-id="89f38-133">也可以通过呼叫者的组织中的[发送到的收件人列表的批量电子邮件](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)设置多个用户 x 标头。</span><span class="sxs-lookup"><span data-stu-id="89f38-133">You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89f38-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89f38-134">See also</span></span>


- [<span data-ttu-id="89f38-135">属性和交换中的 EWS 中的扩展的属性</span><span class="sxs-lookup"><span data-stu-id="89f38-135">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="89f38-136">Exchange 2013： 以编程方式设置自定义 X 标头</span><span class="sxs-lookup"><span data-stu-id="89f38-136">Exchange 2013: Provision custom X-headers programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [<span data-ttu-id="89f38-137">命名属性，X 标头，并且您</span><span class="sxs-lookup"><span data-stu-id="89f38-137">Named Properties, X-Headers, and You</span></span>](http://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [<span data-ttu-id="89f38-138">命名属性，Round 2： 内容位于提前</span><span class="sxs-lookup"><span data-stu-id="89f38-138">Named Properties, Round 2: What lies Ahead</span></span>](http://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [<span data-ttu-id="89f38-139">标头防火墙</span><span class="sxs-lookup"><span data-stu-id="89f38-139">Header Firewall</span></span>](http://technet.microsoft.com/zh-cn/library/bb232136%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="89f38-140">EWS、 MIME 和缺少的 Internet 邮件头</span><span class="sxs-lookup"><span data-stu-id="89f38-140">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [<span data-ttu-id="89f38-141">在 Exchange 中使用 EWS 的批次中的过程电子邮件</span><span class="sxs-lookup"><span data-stu-id="89f38-141">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

