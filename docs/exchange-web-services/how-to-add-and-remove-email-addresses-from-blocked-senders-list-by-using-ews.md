---
title: 使用 Exchange 中的 EWS 在阻止的发件人列表中添加和删除电子邮件地址
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: 了解如何使用 EWS 托管 API 或 EWS 将电子邮件地址添加到阻止的发件人列表并将其从该列表中删除。
ms.openlocfilehash: 270613a739acba165c7bac1bd2c1ef275b5d3aca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528277"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 在阻止的发件人列表中添加和删除电子邮件地址

了解如何使用 EWS 托管 API 或 EWS 将电子邮件地址添加到阻止的发件人列表并将其从该列表中删除。
  
用户的 "垃圾邮件" 选项中的 "阻止发件人" 列表提供了将所有电子邮件从指定发件人移动到 "垃圾邮件" 文件夹的方法。 您可以启用您的 EWS 托管 API 或 EWS 应用程序，将电子邮件地址添加到阻止的发件人列表或从中删除它们。
  
请注意，来自电子邮件地址的邮件必须存在于用户的邮箱中，然后才能将电子邮件地址添加到阻止发件人列表或从阻止发件人列表中删除。 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法和[MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS 操作使用项目 id 的集合。 集合中的项目 Id 指示邮箱中应更改其垃圾邮件状态的邮件。 
  
您可以使用[set-mailboxjunkemailconfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx)和 Set-mailboxjunkemailconfiguration Exchange 命令行管理[程序](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx)cmdlet 直接访问阻止的发件人列表。 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 将电子邮件地址添加到阻止发件人列表或从阻止的发件人列表中删除
<a name="bk_AddRemoveEWSMA"> </a>

若要将电子邮件的发件人添加到阻止的发件人列表中，请使用**MarkAsJunk**方法并将**isJunk**参数设置为**true**。 若要从阻止的发件人列表中删除电子邮件的发件人，请将**isJunk**参数设置为**false**。
  
下面的示例演示如何使用**MarkAsJunk**方法更改邮件的垃圾邮件状态。 
  
```cs
private static void MarkMessageAsJunk(ExchangeService service, ItemId messageId, bool isJunk, bool moveItem)
{
    List<ItemId> junkItemIds = new List<ItemId>();
    junkItemIds.Add(messageId);
    ServiceResponseCollection<MarkAsJunkResponse> responseCollection = null;
    try
    {
        // If isJunk is true, the sender of the email message is added to 
        // the Blocked Senders List. If isJunk is false, the sender is removed
        // from the list (if present).
        responseCollection = service.MarkAsJunk(junkItemIds, isJunk, moveItem);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error marking item as junk: {0}", ex.ErrorCode);
        return;
    }
    foreach (MarkAsJunkResponse response in responseCollection)
    {
        if (response.Result == ServiceResult.Success)
        {
            Console.WriteLine("Successfully marked message as {0}junk.", isJunk ? "": "NOT ");
            if (moveItem)
            {
                Console.WriteLine("New item ID: {0}", response.MovedItemId.ToString());
            }
        }
        else
        {
            Console.WriteLine("[{0}]: {1}", response.Result.ToString(),
                response.ErrorCode.ToString());
        }
    }
}
```

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a>使用 EWS 将电子邮件地址添加到阻止发件人列表或从阻止的发件人列表中删除
<a name="bk_AddRemoveEWS"> </a>

下面的 EWS SOAP 请求通过将[MarkAsJunk](https://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx)元素上的**IsJunk**属性设置为**true**，将项标记为垃圾。 它还通过将**MarkAsJunk**元素上的**MoveItem**属性设置为**true**，将邮件移动到 "垃圾邮件" 文件夹。
  
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
    <m:MarkAsJunk IsJunk="true" MoveItem="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAENAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEuAAA=" 
            ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAADi" />
      </m:ItemIds>
    </m:MarkAsJunk>
  </soap:Body>
</soap:Envelope>
```

下面的 EWS SOAP 响应显示成功的响应。 响应中的[MovedItemId](https://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx)元素包含项目在移动后的项目 ID。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:MovedItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEbAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59DIAAA="
              ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59E+" />
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅

- [Inbox management and EWS in Exchange](inbox-management-and-ews-in-exchange.md)   
- [ExchangeService。 MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [MarkAsJunk 操作](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [Set-mailboxjunkemailconfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx)   
- [Set-mailboxjunkemailconfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) 
- [Exchange 命令行管理程序](../management/exchange-management-shell.md)
    

