---
title: RemoveDistributionGroupFromImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: 查找有关 RemoveDistributionGroupFromImList EWS 操作的信息。
ms.openlocfilehash: 66220f0cab99f404e17136bbb7836ca13d569b53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459600"
---
# <a name="removedistributiongroupfromimlist-operation"></a>RemoveDistributionGroupFromImList 操作

查找有关**RemoveDistributionGroupFromImList** EWS 操作的信息。 
  
当 Lync 使用联系人存储库的 Exchange 时， **RemoveDistributionGroupFromImList**操作将从 lync 即时消息（IM）列表中删除通讯组。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a>使用 RemoveDistributionGroupFromImList 操作

**RemoveDistributionGroupFromImList**操作接受单个参数，该参数标识要从存储在 Exchange 服务器上的 Lync IM 列表中删除的通讯组。 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a>RemoveDistributionGroupFromImList 操作 SOAP 标头

**RemoveDistributionGroupFromImList**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 此标头适用于响应。  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a>RemoveDistributionGroupFromImList 操作请求示例：从 IM 列表中删除通讯组

下面的**RemoveDistributionGroupFromImList**操作请求示例演示如何从 IM 组中删除通讯组。 **RemoveDistributionGroupFromImList**操作接受唯一的组标识符，以标识要从 IM 列表中删除的通讯组。 在[GetImItemList 操作](getimitemlist-operation.md)和[AddDistributionGroupToImList 操作](adddistributiongrouptoimlist-operation.md)的响应中返回的[EXCHANGESTOREID](exchangestoreid.md)元素标识可从 IM 列表中删除的通讯组。 
  
> [!NOTE]
> 本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

请求 SOAP 正文中使用以下元素：
  
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a>成功的 RemoveDistributionGroupFromImList 操作响应

下面的示例演示对从 IM 组中删除通讯组的**RemoveDistributionGroupFromImList**操作请求的成功响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文中使用以下元素：
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a>RemoveDistributionGroupFromImList 操作错误响应示例

下面的示例演示对**RemoveDistributionGroupFromImList**操作请求的错误响应。 这是对删除已从邮箱中删除的通讯组的请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文中使用以下元素：
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
    
- [GetImItemList 操作](getimitemlist-operation.md)
    
- [AddDistributionGroupToImList 操作](adddistributiongrouptoimlist-operation.md)
    
- [人员和 Exchange 中的 EWS 中的联系人](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

