---
title: MarkAsJunk 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: 查找有关 MarkAsJunk EWS 操作的信息。
ms.openlocfilehash: 25d6b01dfff64c4e45f3382223311219d349c165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468570"
---
# <a name="markasjunk-operation"></a>MarkAsJunk 操作

查找有关**MarkAsJunk** EWS 操作的信息。 
  
**MarkAsJunk**操作在阻止的电子邮件列表中添加和删除用户，并将电子邮件移动到 "垃圾邮件" 文件夹。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-markasjunk-operation"></a>使用 MarkAsJunk 操作

**MarkAsJunk**操作包含两个布尔选项，用于指示是否应将电子邮件发件人添加到 "阻止的发件人" 列表以及是否应将目标电子邮件移动到默认的 "垃圾邮件" 文件夹或 "收件箱" 文件夹。 操作由**IsJunk**和**MoveItem**属性的值决定。 以下是基于**IsJunk**和**MoveItem**属性的值组合的可能操作： 
  
- 如果**IsJunk**属性设置为**True**，并且**MoveItem**属性设置为**true**，则目标电子邮件的发件人将添加到 "阻止的发件人" 列表中，并将电子邮件移动到 "垃圾 Dmail" 文件夹中。
    
- 如果将**IsJunk**属性设置为**true**，并将**MoveItem**属性设置为**false**，则目标电子邮件的发件人将添加到 "阻止的发件人" 列表中，并且不会从文件夹中移动电子邮件。
    
- 如果将**IsJunk**属性设置为**false**，并将**MoveItem**属性设置为**true**，则目标电子邮件 messageis 的发件人将从阻止的发件人列表中删除，并且电子邮件将移至 "收件箱" 文件夹。
    
- 如果将**IsJunk**属性设置为**false**，并将**MoveItem**属性设置为**false**，则会从阻止的发件人列表中删除目标电子邮件的发件人，并且不会将电子邮件从文件夹中移出。
    
> [!IMPORTANT]
> 阻止的发件人列表的内容不能从 EWS 中检测到。 如果将发件人添加到 "阻止的发件人" 列表中，则需要保留被阻止的发件人发送的电子邮件的副本，以在将来取消阻止该发件人。 
  
### <a name="markasjunk-operation-soap-headers"></a>MarkAsJunk 操作 SOAP 标头

**MarkAsJunk**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 此标头适用于响应。  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>MarkAsJunk 操作请求示例：将发件人添加到阻止的发件人列表

以下示例的**MarkAsJunk**操作请求显示如何将电子邮件的发件人添加到 "阻止的发件人" 列表中并将电子邮件移动到 "垃圾邮件" 文件夹。 **MarkAsJunk**操作接受唯一的电子邮件标识符，以标识用于引用添加到 "阻止的发件人" 列表中的发件人的电子邮件。 
  
> [!NOTE]
> 本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。 
  
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
    
## <a name="successful-markasjunk-operation-response"></a>成功的 MarkAsJunk 操作响应

以下示例显示了对**MarkAsJunk**操作请求的成功响应，以将发件人添加到阻止的发件人列表并将电子邮件移动到 "垃圾邮件" 文件夹。 
  
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

以下示例的**MarkAsJunk**操作请求显示如何从阻止的发件人列表中删除电子邮件的发件人，并将电子邮件移动到 "收件箱" 文件夹。 您需要保留被阻止的发件人发送的电子邮件，以从阻止的发件人列表中删除发件人。 发件人的电子邮件地址与发件人发送的电子邮件相关联。 如果参考电子邮件不再存在于用户的邮箱中，则从阻止的发件人列表中删除发件人将不会成功。 用于将电子邮件与其发件人相关联的项目标识符必须与 Exchange 邮箱中存在的项目相关联。 我们建议您创建一个隐藏文件夹来存储由以前被阻止的发件人发送的项目，以便可以从客户端应用程序取消阻止这些发件人。 如果已从 Exchange 邮箱中删除某个项目，则管理员必须使用 Exchange 管理控制台访问阻止的发件人列表，以从列表中删除发件人。 有关如何使用 Exchange 管理控制台取消阻止用户的信息，请参阅[如何在 Office 365 中配置安全发件人和阻止的发件人设置](https://support.microsoft.com/kb/2545137)。
  
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

从阻止的发件人列表中删除发件人的成功响应与将发件人添加到阻止的发件人列表的响应相同。
  
请求 SOAP 正文包含以下元素：
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>MarkAsJunk 操作错误响应

下面的示例演示对**MarkAsJunk**操作请求的错误响应。 这是在由项目标识符指定的电子邮件不再存在于邮箱中时，对向阻止的发件人列表添加或删除发件人的请求的响应。 
  
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

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
    
- [GetItem 操作](getitem-operation.md)GetItem 操作 
    
- [FindItem 操作](finditem-operation.md)
    

