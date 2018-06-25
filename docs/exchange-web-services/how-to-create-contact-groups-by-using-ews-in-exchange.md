---
title: 使用 EWS 在 Exchange 中创建联系人组
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建联系人组。
ms.openlocfilehash: b3357f24e07a9c1b3b37ccb63b0f4f0d0a1d6fcf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752760"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange 中创建联系人组

了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建联系人组。
  
您可以创建联系人组，这是一个私有[通讯组](distribution-groups-and-ews-in-exchange.md)，通过使用 EWS 托管 API 或 EWS。 若要创建联系人组，在[ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS 托管 API 类中，使用方法，或使用[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作。 
  
请注意，不能使用 EWS 托管 API 或 EWS 创建的通用通讯组或安全组。 若要创建的通用通讯组或安全组，您可以使用[New-distributiongroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)。 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建联系人组
<a name="bk_EWSMA"> </a>

若要创建联系人组，您只需几条信息： 组，并添加到组的成员的名称。 下面的示例演示如何创建简单的联系人组，其中包含几个组成员。
  
```cs
// Create a new contact group object.
ContactGroup myContactGroup = new ContactGroup(service);
// Give the group a name.
myContactGroup.DisplayName = "My Contact Group";
// Add some members to the group.
myContactGroup.Members.Add(new GroupMember("sadie@contoso.com"));
myContactGroup.Members.Add(new GroupMember("alfred@contoso.com"));
// Save the group.
myContactGroup.Save();

```

## <a name="create-a-contact-group-by-using-ews"></a>使用 EWS 创建联系人组
<a name="bk_EWSMA"> </a>

可能需要几行代码，但您可以使用[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作创建联系人组。 下面的 XML 请求示例演示如何创建联系人组。 这也是 XML 请求发送时您[使用 EWS 托管 API 创建联系人组](#bk_EWSMA)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

下面是对请求的成功 XML 响应的示例。 注意返回的值，包括新的联系人组和更改密钥，您可以使用其他代码中修改联系人组或展开要查看的成员的组的项 ID。 为便于阅读将被截项 ID。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                          Id="AAMkADBlY…" 
                          ChangeKey="EgAAABYAAAAD7hO1SJPWTbICFWZ4U3NMAABXzQiK" />
               </DistributionList>
            </Items>
         </CreateItemResponseMessage>
      </ResponseMessages>
   </CreateItemResponse>
```

## <a name="see-also"></a>另请参阅


- [通讯组和 Exchange 中的 EWS](distribution-groups-and-ews-in-exchange.md)
    
- [通过使用 EWS 在 Exchange 2013 中展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

