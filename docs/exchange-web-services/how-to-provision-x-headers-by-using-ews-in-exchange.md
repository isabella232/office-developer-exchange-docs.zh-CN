---
title: 使用 EWS 在 Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 设置邮箱的 x 标头。
ms.openlocfilehash: e60092e0d40d5815cdf3fd4ed588e2f74978c245
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521114"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 设置邮箱的 x 标头。
  
X 标头是添加到电子邮件头集合中的非标准标头，用于传达信息。 例如，Exchange **使用 X-MS-Exchange-Organization-SCL** 标头标记邮件，以指示 (SCL) 的垃圾邮件可信度。 电子邮件客户端（如 Outlook）可以使用该信息来确定对电子邮件执行哪种类型的操作 (例如，Outlook 可以阻止显示图像，除非用户执行) 。 
  
Exchange第一次收到包含该 x 标头的电子邮件时，将传入的 x 标头作为命名属性添加到邮箱架构中。 x 标头值不会保存在第一封电子邮件上;但是，它将保存在包含 x 标头的所有后续电子邮件中。 因此，应用程序应在你预期使用 x 标头之前预配 x 标头。 命名属性和 x 标头之间的映射发生在电子邮件到邮箱的传输传递中。 这意味着你需要通过传输传递接收电子邮件;不能只将包含 x 标头的电子邮件保存到邮箱，以创建到命名属性的映射。
  
> [!NOTE]
> 如果发现 x 标头未保存，请确定传输代理或邮件头防火墙[](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a)是否在到达邮箱[](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)之前筛选出 x 标头。 r
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 预配 x 标头
<a name="bk_example1"> </a>

以下代码示例演示如何使用 EWS 托管 API [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) 方法设置邮箱的 x 标头。 此示例 **假定服务是有效的** [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且目标邮箱没有超出命名 [属性的配额](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx)。
  
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

## <a name="provision-an-x-header-by-using-ews"></a>使用 EWS 预配 x 标头
<a name="bk_example1"> </a>

以下代码示例演示如何使用 EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 操作创建和发送电子邮件来设置具有 x 标头的邮箱。 这是当您使用 EWS 托管 API 预配 [x 标头时，EWS 托管 API 发送的 XML 请求](#bk_example1)。
  
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

第一次在 Exchange Online 中预配 x 标头、将 Exchange Online 作为 Office 365 的一部分或 Exchange 本地版本（从 Exchange Server 2010 开始）时，不会将新的自定义 x 标头的值写入存储的邮件。 这是因为必须先将 x 标头映射到用户邮箱中的命名属性。 该映射发生在第一次请求添加命名属性时。 当创建命名属性的后续请求发生时，该属性和值将存储在邮件上。 在 Exchange 2007 中，第一次将 x 标头写入邮箱数据库时，会为 x 标头创建到邮箱数据库中的命名属性的映射。 当创建命名属性的后续请求发生时，x 标头将处理和存储到 Exchange 2007 数据库中。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_example1"> </a>

本文演示如何通过向用户发送电子邮件来设置单个邮箱的 x 标头。 您还可以通过向呼叫者的组织中收件人列表发送批处理电子邮件，[](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)为许多用户设置 x 标头。 
  
## <a name="see-also"></a>另请参阅


- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013：以编程方式预配自定义 X 标头](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [命名属性、X-Header 和 You](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [命名属性，第 2 轮：前面是什么](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [邮件头防火墙](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS、MIME 和缺少的 Internet 邮件头](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [使用 Exchange 中的 EWS 批量处理电子邮件](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

