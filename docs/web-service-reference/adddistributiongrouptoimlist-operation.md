---
title: AddDistributionGroupToImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: 查找信息 AddDistributionGroupToImList EWS 操作。
ms.openlocfilehash: 7c562c317890a4cffb9e5844ea41c1096a8595b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753103"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="b8197-103">AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="b8197-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="b8197-104">查找有关**AddDistributionGroupToImList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="b8197-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="b8197-105">**AddDistributionGroupToImList** Exchange Web Services (EWS) 操作将通讯组添加到即时消息 (IM) 列表统一联系人存储库中。</span><span class="sxs-lookup"><span data-stu-id="b8197-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="b8197-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="b8197-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="b8197-107">使用 AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="b8197-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="b8197-108">**AddDistributionGroupToImList**操作所需的单个参数，标识将添加到 IM 列表的通讯组。</span><span class="sxs-lookup"><span data-stu-id="b8197-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="b8197-109">此操作不会创建通讯组;必须已创建通讯组。</span><span class="sxs-lookup"><span data-stu-id="b8197-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="b8197-110">此操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="b8197-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="b8197-111">**表 1。AddDistributionGroupToImList 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="b8197-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="b8197-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="b8197-112">**Header name**</span></span>|<span data-ttu-id="b8197-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b8197-113">**Element**</span></span>|<span data-ttu-id="b8197-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b8197-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8197-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="b8197-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="b8197-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="b8197-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="b8197-117">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="b8197-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="b8197-118">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="b8197-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b8197-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="b8197-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="b8197-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b8197-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="b8197-121">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="b8197-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="b8197-122">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="b8197-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b8197-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="b8197-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="b8197-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b8197-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="b8197-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="b8197-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="b8197-126">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="b8197-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b8197-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="b8197-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="b8197-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b8197-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="b8197-129">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="b8197-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="b8197-130">这是适用于响应。</span><span class="sxs-lookup"><span data-stu-id="b8197-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="b8197-131">AddDistributionGroupToImList 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="b8197-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="b8197-132">**AddDistributionGroupToImList**操作请求的下面的示例演示如何将通讯组添加到 IM 列表。</span><span class="sxs-lookup"><span data-stu-id="b8197-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b8197-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="b8197-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b8197-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b8197-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="b8197-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b8197-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="b8197-136">成功 AddDistributionGroupToImList 操作响应</span><span class="sxs-lookup"><span data-stu-id="b8197-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="b8197-137">下面的示例演示对**AddDistributionGroupToImList**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b8197-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="b8197-138">成功的响应中包含的通讯组的显示名称、 通讯组，并新建通讯组的 EWS 标识符的 Exchange 存储类。</span><span class="sxs-lookup"><span data-stu-id="b8197-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <s:Header>
      <t:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"/>
   </s:Header>
   <s:Body>
      <m:AddDistributionGroupToImListResponse ResponseClass="Success">
         <m:ResponseCode>NoError</m:ResponseCode>
         <m:ImGroup>
            <t:DisplayName>distributionlist1@example.com</t:DisplayName>
            <t:GroupType>IPM.DistList.MOC.DG</t:GroupType>
            <t:ExchangeStoreId Id="AAMkAGQ1MjJjAA=" 
                             ChangeKey="EgAAAA=="/>
      </m:ImGroup>
      </m:AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="b8197-139">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="b8197-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b8197-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="b8197-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="b8197-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b8197-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b8197-142">ImGroup</span><span class="sxs-lookup"><span data-stu-id="b8197-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="b8197-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="b8197-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="b8197-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="b8197-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="b8197-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="b8197-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="b8197-146">AddDistributionGroupToImList 操作 ErrorInvalidImDistributionGroupSmtpAddress 错误响应</span><span class="sxs-lookup"><span data-stu-id="b8197-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="b8197-147">下面的示例演示**AddDistributionGroupToImList**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="b8197-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="b8197-148">尝试 Exchange 存储中不存在的通讯组添加时发生了以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="b8197-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="b8197-149">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="b8197-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b8197-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="b8197-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="b8197-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="b8197-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b8197-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b8197-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="b8197-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8197-153">See also</span></span>

- [<span data-ttu-id="b8197-154">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="b8197-154">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="b8197-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="b8197-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="b8197-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="b8197-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

