---
title: MarkAsJunk 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: 查找有关 MarkAsJunk EWS 操作的信息。
ms.openlocfilehash: b165b415ce9380846b49d15dd321bfddba72b749
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524733"
---
# <a name="markasjunk-operation"></a>MarkAsJunk 操作

查找有关 **MarkAsJunk** EWS 操作的信息。 
  
**MarkAsJunk** 操作在阻止的电子邮件列表中添加和删除用户，并将电子邮件移动到"垃圾邮件"文件夹。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-markasjunk-operation"></a>使用 MarkAsJunk 操作

**MarkAsJunk** 操作包含两个布尔选项，用于指示是否应该将电子邮件发件人添加到阻止的发件人列表，以及目标电子邮件应移动到默认的垃圾邮件文件夹或收件箱文件夹。 操作由 **IsJunk** 和 **MoveItem** 属性的值确定。 以下是根据 **IsJunk** 和 **MoveItem** 属性的值组合可能的操作： 
  
- 如果 **IsJunk** 属性设置为 **true，** 并且 **MoveItem** 属性设置为 **true，** 则目标电子邮件的发件人将添加到阻止的发件人列表中，并且电子邮件将移动到"垃圾邮件"文件夹。
    
- 如果 **IsJunk** 属性设置为 **true，** 并且 **MoveItem** 属性设置为 **false，** 则目标电子邮件的发件人将添加到阻止的发件人列表中，并且不会从文件夹移动该电子邮件。
    
- 如果 **IsJunk** 属性设置为 **false，** 并且 **MoveItem** 属性设置为 **true，** 则目标电子邮件的发件人将从阻止的发件人列表中删除，并且电子邮件将移动到收件箱文件夹。
    
- 如果 **IsJunk** 属性设置为 **false，** 并且 **MoveItem** 属性设置为 **false，** 则目标电子邮件的发件人将从阻止的发件人列表中删除，并且不会从文件夹中移动该电子邮件。
    
> [!IMPORTANT]
> 阻止的发件人列表的内容无法从 EWS 中发现。 如果将发件人添加到阻止的发件人列表中，则需要保留阻止发件人发送的电子邮件的副本，以在将来取消阻止发件人。 
  
### <a name="markasjunk-operation-soap-headers"></a>MarkAsJunk 操作 SOAP 标头

**MarkAsJunk** 操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序正在模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的区域性，如 RFC 3066"语言标识标记"中的定义。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>MarkAsJunk 操作请求示例：将发件人添加到阻止的发件人列表

**MarkAsJunk** 操作请求的以下示例显示如何将电子邮件的发件人添加到阻止的发件人列表，以及如何将电子邮件移动到垃圾邮件文件夹。 **MarkAsJunk** 操作接受唯一的电子邮件标识符，以标识用于引用添加到阻止发件人列表的发件人的电子邮件。 
  
> [!NOTE]
> 本文中所有项标识符和更改键已缩短，以保持可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
        <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a>MarkAsJunk 操作响应成功

以下示例显示对 **MarkAsJunk** 操作请求的成功响应，该请求将发件人添加到阻止的发件人列表，以及将电子邮件移动到"垃圾邮件"文件夹。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>MarkAsJunk 操作请求示例：从阻止的发件人列表中删除发件人

**MarkAsJunk** 操作请求的以下示例显示如何从阻止的发件人列表中删除电子邮件的发件人，以及如何将电子邮件移动到收件箱文件夹。 您需要保留阻止发件人发送的电子邮件，以将发件人从阻止的发件人列表中删除。 发件人的电子邮件地址与发件人发送的电子邮件相关联。 如果引用电子邮件在用户的邮箱中不再存在，则从阻止的发件人列表中删除发件人将失败。 用于将电子邮件与其发件人关联的项目标识符必须与电子邮件邮箱中已存在Exchange相关联。 我们建议您创建一个隐藏文件夹来存储以前阻止的发件人发送的项目，以便发件人可以从客户端应用程序取消阻止。 如果项目已从 Exchange 邮箱中删除，管理员必须使用此 Exchange 管理控制台 访问阻止的发件人列表，以从列表中删除发件人。 有关如何使用 Exchange 管理控制台 取消阻止用户的信息，请参阅如何在 Office 365 中配置安全发件人和[阻止发件人Office 365。](https://support.microsoft.com/kb/2545137)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
    </soap:Header>
    <soap:Body>
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

从阻止发件人列表中删除发件人的成功响应与将发件人添加到阻止发件人列表的响应相同。
  
请求 SOAP 正文包含以下元素：
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>MarkAsJunk 操作错误响应

以下示例显示对 **MarkAsJunk** 操作请求的错误响应。 当邮箱中不再存在项目标识符指定的电子邮件时，这是对在阻止发件人列表中添加或删除发件人的请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)
    
- [GetItem 操作](getitem-operation.md) GetItem 操作 
    
- [FindItem 操作](finditem-operation.md)
    

