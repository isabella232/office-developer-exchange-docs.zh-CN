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
# <a name="create-contact-groups-by-using-ews-in-exchange"></a><span data-ttu-id="fc2d8-103">使用 EWS 在 Exchange 中创建联系人组</span><span class="sxs-lookup"><span data-stu-id="fc2d8-103">Create contact groups by using EWS in Exchange</span></span>

<span data-ttu-id="fc2d8-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建联系人组。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-104">Learn how to create a contact group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="fc2d8-105">您可以创建联系人组，这是一个私有[通讯组](distribution-groups-and-ews-in-exchange.md)，通过使用 EWS 托管 API 或 EWS。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-105">You can create a contact group, which is a private [distribution group](distribution-groups-and-ews-in-exchange.md), by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="fc2d8-106">若要创建联系人组，在[ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS 托管 API 类中，使用方法，或使用[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-106">To create contact groups, use the methods in the [ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API class, or use the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="fc2d8-107">请注意，不能使用 EWS 托管 API 或 EWS 创建的通用通讯组或安全组。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-107">Note that you can't use the EWS Managed API or EWS to create a universal distribution group or security group.</span></span> <span data-ttu-id="fc2d8-108">若要创建的通用通讯组或安全组，您可以使用[New-distributiongroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-108">To create a universal distribution group or security group, you can use the [New-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx).</span></span> 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a><span data-ttu-id="fc2d8-109">使用 EWS 托管 API 创建联系人组</span><span class="sxs-lookup"><span data-stu-id="fc2d8-109">Create a contact group by using the EWS Managed API</span></span>
<span data-ttu-id="fc2d8-110"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="fc2d8-110"></span></span>

<span data-ttu-id="fc2d8-111">若要创建联系人组，您只需几条信息： 组，并添加到组的成员的名称。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-111">To create a contact group, you just need a couple pieces of information: a name for the group, and the members to add to the group.</span></span> <span data-ttu-id="fc2d8-112">下面的示例演示如何创建简单的联系人组，其中包含几个组成员。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-112">The following example shows how to create a simple contact group that contains a couple of group members.</span></span>
  
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

## <a name="create-a-contact-group-by-using-ews"></a><span data-ttu-id="fc2d8-113">使用 EWS 创建联系人组</span><span class="sxs-lookup"><span data-stu-id="fc2d8-113">Create a contact group by using EWS</span></span>
<span data-ttu-id="fc2d8-114"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="fc2d8-114"></span></span>

<span data-ttu-id="fc2d8-115">可能需要几行代码，但您可以使用[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作创建联系人组。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-115">It might take a few more lines of code, but you can create a contact group by using the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="fc2d8-116">下面的 XML 请求示例演示如何创建联系人组。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-116">The following XML request example shows how you can create a contact group.</span></span> <span data-ttu-id="fc2d8-117">这也是 XML 请求发送时您[使用 EWS 托管 API 创建联系人组](#bk_EWSMA)。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-117">This is also the XML request that is sent when you [use the EWS Managed API to create a contact group](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="fc2d8-118">下面是对请求的成功 XML 响应的示例。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-118">The following is an example of a successful XML response to the request.</span></span> <span data-ttu-id="fc2d8-119">注意返回的值，包括新的联系人组和更改密钥，您可以使用其他代码中修改联系人组或展开要查看的成员的组的项 ID。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-119">Notice that the values returned include an item ID for the new contact group and a change key that you can use in other code to modify the contact group or expand the group to see the members.</span></span> <span data-ttu-id="fc2d8-120">为便于阅读将被截项 ID。</span><span class="sxs-lookup"><span data-stu-id="fc2d8-120">The item ID is shortened for readability.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="fc2d8-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc2d8-121">See also</span></span>


- [<span data-ttu-id="fc2d8-122">通讯组和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="fc2d8-122">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="fc2d8-123">通过使用 EWS 在 Exchange 2013 中展开通讯组</span><span class="sxs-lookup"><span data-stu-id="fc2d8-123">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

