---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: 查找信息 MarkAsJunk EWS 操作。
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826353"
---
# <a name="markasjunk-operation"></a>MarkAsJunk Operation

查找有关**MarkAsJunk** EWS 操作的信息。 
  
**MarkAsJunk**操作添加和用户从列表中删除阻止的电子邮件并将电子邮件移动到垃圾邮件文件夹。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-markasjunk-operation"></a>使用 MarkAsJunk 操作

**MarkAsJunk**操作包含两个布尔选项，以指示是否应将电子邮件发件人添加到阻止发件人列表以及是否应该将目标电子邮件移动到默认垃圾邮件文件夹或收件箱文件夹。 操作**IsJunk**和**MoveItem**属性的值由决定。 以下是可能的操作基于**IsJunk**和**MoveItem**属性的值组合： 
  
- 如果**IsJunk**属性设置为**true**，并且**MoveItem**属性设置为**true**，则目标电子邮件的发件人添加到阻止发件人列表和电子邮件移动到垃圾 Dmail 文件夹。
    
- 如果**IsJunk**属性设置为**true**，并且**MoveItem**属性设置为**false**，目标电子邮件的发件人添加到阻止发件人列表和电子邮件也不会移动从文件夹。
    
- 如果**IsJunk**属性设置为**false**，且**MoveItem**属性设置为**true**，从阻止发件人列表中删除目标电子邮件 messageis 发件人和电子邮件移动到收件箱文件夹。
    
- 如果**IsJunk**属性设置为**false**，并且**MoveItem**属性设置为**false**，从阻止发件人列表中删除的目标电子邮件发件人和电子邮件也不会移动从文件夹。
    
> [!IMPORTANT]
> 阻止发件人列表的内容不从 EWS 可供搜索。 如果发件人添加到阻止发件人列表中，您需要保留一份阻止发件人发送将来取消阻止发件人的电子邮件。 
  
### <a name="markasjunk-operation-soap-headers"></a>MarkAsJunk 操作 SOAP 标头

**MarkAsJunk**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。 适用于请求此标头。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。 适用于请求此标头。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 适用于请求此标头。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 适用于响应此标头。  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a>MarkAsJunk 操作请求示例： 将发件人添加到阻止发件人列表

**MarkAsJunk**操作请求的下面的示例演示如何将电子邮件发件人添加到阻止发件人列表并将电子邮件移动到垃圾邮件文件夹。 **MarkAsJunk**操作接受标识用于引用添加到阻止发件人列表中的发件人的电子邮件的唯一电子邮件消息标识符。 
  
> [!NOTE]
> 所有项目标识符，本文中的更改项具有已截短要保留可读性。 
  
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
    
## <a name="successful-markasjunk-operation-response"></a>成功 MarkAsJunk 操作响应

下面的示例演示对**MarkAsJunk**操作请求将发件人添加到阻止发件人列表并将电子邮件移动到垃圾邮件文件夹的成功响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

响应 SOAP 正文中包含以下元素：
  
- [MarkAsJunkResponse](markasjunkresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [MovedItemId](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a>MarkAsJunk 操作请求示例： 从阻止发件人列表中删除发件人

**MarkAsJunk**操作请求的下面的示例演示如何从阻止发件人列表中删除电子邮件的发件人，并将电子邮件移动到收件箱文件夹。 您需要保留从阻止发件人列表中删除发件人被阻止发件人发送一封电子邮件。 与电子邮件已发送发件人的发件人的电子邮件地址。 如果引用电子邮件不再存在用户的邮箱中，不会成功从阻止发件人列表中删除发件人。 用于将电子邮件的发件人为相关联的项标识符必须与 Exchange 邮箱中存在的项相关联。 我们建议您创建一个隐藏的文件夹，用于存储项目，以便可以从客户端应用程序的阻止发件人发送的以前阻止发件人。 中的项已从 Exchange 邮箱，管理员必须使用 Exchange 管理控制台访问要从列表中删除发件人的阻止发件人列表。 有关如何使用 Exchange 管理控制台取消阻止用户的信息，请参阅[如何配置的安全发件人和阻止发件人在 Office 365 中的设置](http://support.microsoft.com/kb/2545137)。
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

将发件人添加到阻止发件人列表的响应相同的阻止发件人列表中移除发件人的成功响应。
  
请求 SOAP 正文包含以下元素：
  
- [MarkAsJunk](markasjunk.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a>MarkAsJunk 操作错误响应

下面的示例演示对**MarkAsJunk**操作请求错误响应。 这是要添加或移除阻止发件人列表发件人时指定的项标识符的电子邮件不再存在的邮箱中请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
    

