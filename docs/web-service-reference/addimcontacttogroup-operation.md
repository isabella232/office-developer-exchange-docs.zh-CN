---
title: AddImContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: 查找有关 AddImContactToGroup EWS 操作的信息。
ms.openlocfilehash: 2f3cfa35662251fdcd449876af466bd5c066ec62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525407"
---
# <a name="addimcontacttogroup-operation"></a>AddImContactToGroup 操作

查找有关 **AddImContactToGroup** EWS 操作的信息。 
  
**AddImContactToGroup** Exchange EWS (EWS) 操作会将现有的即时消息 (IM) 联系人添加到组中。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-addimcontacttogroup-operation"></a>使用 AddImContactToGroup 操作

**AddImContactToGroup** 操作只能接受 IM 联系人。 如果要将新的 IM 联系人添加到统一联系人存储，请使用 [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) 操作。 
  
**AddImContactToGroup** 操作可以使用下表中列出的 SOAP 标头。 
  
**表 1.AddImContactToGroup 操作 SOAP 标头**

|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序正在模拟的用户。 此标头适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的区域性，如 RFC 3066"语言标识标记"中的定义。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a>AddImContactToGroup 操作请求示例：向 IM 组添加现有 IM 联系人

**AddImContactToGroup** 操作请求的以下示例显示如何添加现有 IM 联系人 IM 组。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:AddImContactToGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTc4Y2AA="
                      ChangeKey="EQAAABYAAABtF8oI7i"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkzzAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

请求 SOAP 正文包含以下元素：
  
- [AddImContactToGroup](addimcontacttogroup.md)
    
- [ContactId](contactid.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a>成功的 AddImContactToGroup 操作响应

以下示例显示对 **AddImContactToGroup** 操作请求的成功响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddImContactToGroupResponse ResponseClass="Success" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </AddImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [AddImContactToGroupResponse](addimcontacttogroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a>AddImContactToGroup 操作 ErrorInvalidImContactId 错误响应

以下示例显示对 **AddImContactToGroup** 操作请求的错误响应。 当尝试添加非 IM 联系人的联系人时，将发生以下错误响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddImContactToGroupResponse ResponseClass="Error" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         </AddImContactToGroupResponse>
      </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [AddImContactToGroupResponse](addimcontacttogroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅

- [AddImGroup 操作](addimgroup-operation.md)
    
- [AddNewImContactToGroup 操作](addnewimcontacttogroup-operation.md)
    
- [SetImGroup 操作](setimgroup-operation.md)
    
- [RemoveImGroup 操作](removeimgroup-operation.md)
    
- [GetImItemList 操作](getimitemlist-operation.md)
    
- [人员和 Exchange 中的 EWS 中的联系人](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

