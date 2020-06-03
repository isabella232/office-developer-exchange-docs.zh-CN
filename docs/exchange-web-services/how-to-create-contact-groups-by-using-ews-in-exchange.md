---
title: 使用 Exchange 中的 EWS 创建联系人组
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建联系人组。
ms.openlocfilehash: 1da876bbda72f5bea08fd9855aa3f554135d54aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528137"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 创建联系人组

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建联系人组。
  
您可以使用 EWS 托管 API 或 EWS 创建一个私有[通讯组](distribution-groups-and-ews-in-exchange.md)的联系人组。 若要创建联系人组，请使用[ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS 托管 API 类中的方法，或使用[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作。 
  
请注意，不能使用 EWS 托管 API 或 EWS 创建通用通讯组或安全组。 若要创建通用通讯组或安全组，您可以使用[New-distributiongroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange 命令行管理程序 cmdlet](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)。 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建联系人组
<a name="bk_EWSMA"> </a>

若要创建联系人组，只需提供以下几条信息：组的名称和要添加到组的成员。 下面的示例演示如何创建包含两个组成员的简单联系人组。
  
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

它可能需要几行代码，但您可以通过使用[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作来创建联系人组。 下面的 XML 请求示例演示如何创建联系人组。 这也是当您[使用 EWS 托管 API 创建联系人组](#bk_EWSMA)时发送的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

下面的示例演示了对请求的成功的 XML 响应。 请注意，返回的值包括新联系人组的项 ID，以及可以在其他代码中用来修改联系人组或展开组以查看成员的更改密钥。 为了提高可读性，项目 ID 被缩短。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
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
    
- [使用 Exchange 2013 中的 EWS 展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

