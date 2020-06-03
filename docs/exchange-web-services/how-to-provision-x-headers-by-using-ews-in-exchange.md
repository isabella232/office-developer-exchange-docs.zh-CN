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
# <a name="provision-x-headers-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 设置 x 标头

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 设置邮箱的 x 标头。
  
X 标头是添加到电子邮件的头集合以传达信息的非标准标头。 例如，Exchange 将带有**X-MS** --SCL 标头的邮件标记为表示电子邮件的垃圾邮件可信度（SCL）。 Outlook 等电子邮件客户端可以使用该信息来确定对电子邮件执行的操作类型（例如，Outlook 可以阻止显示图像，除非用户采取了措施）。 
  
Exchange 会在邮箱架构中添加传入的 x 头作为命名属性，这是第一次收到该 x 标头的电子邮件时。 X 头值不保存在第一封电子邮件上;但是，它会保存在包含 x 标头的所有后续电子邮件上。 因此，您的应用程序应预配 x 标头，然后再预期使用它们。 在电子邮件到邮箱的传输传递过程中出现命名属性和 x 标头之间的映射。 这意味着，您需要通过传输传递来接收电子邮件;您不能只保存包含 x 头的电子邮件到邮箱，以创建到命名属性的映射。
  
> [!NOTE]
> 如果发现不保存 x 标头，请确定[传输代理](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a)或[头防火墙](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)在到达邮箱之前是否筛选出您的 x 标头。 r
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 设置 x 标头
<a name="bk_example1"> </a>

下面的代码示例演示如何使用 EWS 托管 API [EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)方法来设置邮箱的 x 标头。 此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，且目标邮箱尚未超过[命名属性的配额](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx)。
  
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

## <a name="provision-an-x-header-by-using-ews"></a>使用 EWS 设置 x 标头
<a name="bk_example1"> </a>

下面的代码示例演示如何使用 EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)操作创建并发送电子邮件，以设置具有 x 标头的邮箱。 这是通过[使用 Ews 托管 Api 设置 x 标头](#bk_example1)时由 EWS 托管 api 发送的 XML 请求。
  
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

## <a name="version-differences"></a>版本差异
<a name="bk_example1"> </a>

首次在 Exchange Online 中设置 x 标头，将 Exchange Online 作为 Office 365 的一部分，或从 Exchange Server 2010 开始的本地 Exchange 版本，将不会将新的自定义 x 标头的值写入到存储的邮件中。 这是因为必须首先将 x 标头映射到用户邮箱中的命名属性。 映射发生在首次请求添加命名属性时。 当后续请求创建命名属性时，属性和值存储在邮件上。 在 Exchange 2007 中，第一次将 x 标头写入邮箱数据库时，会在邮箱数据库中为 x 标头创建一个映射，这是一个命名属性。 在后续请求创建命名属性时，将对 Exchange 2007 数据库中的任何邮箱处理和存储 x 标头。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_example1"> </a>

本文介绍如何通过向用户发送电子邮件来为单个邮箱设置 x 标头。 您还可以通过将[批处理电子邮件发送到](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)呼叫者组织中的收件人列表，为多个用户预配 x 标头。 
  
## <a name="see-also"></a>另请参阅


- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013：以编程方式设置自定义 X 标头](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [命名属性、X 标头和您](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [命名属性，圆形2：提前](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [标头防火墙](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS、MIME 和缺少的 Internet 邮件头](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [使用 Exchange 中的 EWS 批量处理电子邮件](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

