---
title: MarkAllItemsAsRead 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: 查找有关 MarkAllItemsAsRead EWS 操作的信息。
ms.openlocfilehash: aeeacea1cd5eed723f93027dd1ef75b34605fdfd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530528"
---
# <a name="markallitemsasread-operation"></a>MarkAllItemsAsRead 操作

查找有关**MarkAllItemsAsRead** EWS 操作的信息。 
  
**MarkAllItemsAsRead**操作设置一个或多个文件夹中所有项目的[IsRead](isread.md)属性，以指示所有项目都已读或未读。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-markallitemsasread-operation"></a>使用 MarkAllItemsAsRead 操作

**MarkAllItemsAsRead**操作可以设置文件夹中的所有项目的[IsRead](isread.md)属性，这些项目由 EXCHANGE Web 服务（EWS）文件夹标识符或默认 Exchange 文件夹名称标识。 **MarkAllItemsAsRead**操作还可以禁止发送标记为 "已读" 的项目的已读回执。 
  
### <a name="markallitemsasread-operation-soap-headers"></a>MarkAllItemsAsRead 操作 SOAP 标头

**MarkAllItemsAsRead**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 此标头适用于响应。  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a>MarkAllItemsAsRead 操作请求示例：将文件夹中的所有项目标记为已读

以下示例的**MarkAllItemsAsRead**操作请求显示如何将文件夹中所有项目的[IsRead](isread.md)属性（也称为 "读取" 标志）设置为**true** 。 此示例还显示了在响应任何已读回执请求时不会发送 "已读" 回执。 
  
> [!NOTE]
> 本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。 此操作不需要更改键。 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>true</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

请求 SOAP 正文包含以下元素：
  
- [MarkAllItemsAsRead](markallitemsasread.md)
    
- [ReadFlag](readflag.md)
    
- [SuppressReadReceipts](suppressreadreceipts.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a>成功的 MarkAllItemsAsRead 操作响应

下面的示例演示对**MarkAllItemsAsRead**操作请求的成功响应，以将文件夹中的所有项目标记为已读。 
  
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
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [MarkAllItemsAsReadResponse](markallitemsasreadresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAllItemsAsReadResponseMessage](markallitemsasreadresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a>MarkAllItemsAsRead 操作请求示例：将文件夹中的所有项目标记为未读

下面的**MarkAllItemsAsRead**操作请求示例演示如何在文件夹中的所有项目上将[IsRead](isread.md)属性设置为**false** 。 此示例还显示了在响应任何已读回执请求时不会发送 "已读" 回执。 
  
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
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>false</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

对将所有项目标记为已读的请求的成功响应与对将所有项目标记为未读的请求的响应相同。
  
请求 SOAP 正文包含以下元素：
  
- [MarkAllItemsAsRead](markallitemsasread.md)
    
- [ReadFlag](readflag.md)
    
- [SuppressReadReceipts](suppressreadreceipts.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a>MarkAllItemsAsRead 操作错误响应

下面的示例演示对**MarkAllItemsAsRead**操作请求的错误响应，以便将文件夹中的所有项目标记为已读或未读（当该文件夹在邮箱中不存在时）。 
  
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
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Error">
               <m:MessageText>The specified object was not found in the store.</m:MessageText>
               <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>

```

错误响应 SOAP 正文包含以下元素：
  
- [MarkAllItemsAsReadResponse](markallitemsasreadresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAllItemsAsReadResponseMessage](markallitemsasreadresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
    
- [FindFolder Operation](findfolder-operation.md)
    

