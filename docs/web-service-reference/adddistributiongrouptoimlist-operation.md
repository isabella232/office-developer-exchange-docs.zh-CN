---
title: AddDistributionGroupToImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: 查找有关 AddDistributionGroupToImList EWS 操作的信息。
ms.openlocfilehash: e68e21b6994af5773f5cf991d55129e1db3367ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463690"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="09f03-103">AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="09f03-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="09f03-104">查找有关**AddDistributionGroupToImList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="09f03-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="09f03-105">**AddDistributionGroupToImList** Exchange Web 服务（EWS）操作将通讯组添加到统一联系人存储库中的即时消息（IM）列表中。</span><span class="sxs-lookup"><span data-stu-id="09f03-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="09f03-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="09f03-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="09f03-107">使用 AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="09f03-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="09f03-108">**AddDistributionGroupToImList**操作采用单个参数来标识要添加到 IM 列表中的通讯组。</span><span class="sxs-lookup"><span data-stu-id="09f03-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="09f03-109">此操作不会创建通讯组;必须已创建通讯组。</span><span class="sxs-lookup"><span data-stu-id="09f03-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="09f03-110">此操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="09f03-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="09f03-111">**表1。AddDistributionGroupToImList 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="09f03-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="09f03-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="09f03-112">**Header name**</span></span>|<span data-ttu-id="09f03-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="09f03-113">**Element**</span></span>|<span data-ttu-id="09f03-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="09f03-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09f03-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="09f03-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="09f03-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="09f03-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="09f03-117">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="09f03-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="09f03-118">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="09f03-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="09f03-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="09f03-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="09f03-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="09f03-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="09f03-121">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="09f03-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="09f03-122">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="09f03-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="09f03-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="09f03-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="09f03-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="09f03-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="09f03-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="09f03-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="09f03-126">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="09f03-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="09f03-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="09f03-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="09f03-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="09f03-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="09f03-129">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="09f03-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="09f03-130">这适用于响应。</span><span class="sxs-lookup"><span data-stu-id="09f03-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="09f03-131">AddDistributionGroupToImList 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="09f03-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="09f03-132">以下示例的**AddDistributionGroupToImList**操作请求显示如何将通讯组添加到 IM 列表。</span><span class="sxs-lookup"><span data-stu-id="09f03-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
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
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="09f03-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="09f03-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="09f03-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="09f03-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="09f03-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="09f03-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="09f03-136">成功的 AddDistributionGroupToImList 操作响应</span><span class="sxs-lookup"><span data-stu-id="09f03-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="09f03-137">下面的示例演示对**AddDistributionGroupToImList**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="09f03-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="09f03-138">成功的响应包含通讯组显示名称、通讯组的 Exchange 存储类以及新通讯组的 EWS 标识符。</span><span class="sxs-lookup"><span data-stu-id="09f03-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="09f03-139">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="09f03-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="09f03-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="09f03-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="09f03-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="09f03-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="09f03-142">ImGroup</span><span class="sxs-lookup"><span data-stu-id="09f03-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="09f03-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="09f03-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="09f03-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="09f03-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="09f03-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="09f03-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="09f03-146">AddDistributionGroupToImList 操作 ErrorInvalidImDistributionGroupSmtpAddress 错误响应</span><span class="sxs-lookup"><span data-stu-id="09f03-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="09f03-147">下面的示例演示对**AddDistributionGroupToImList**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="09f03-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="09f03-148">当尝试添加 Exchange 存储中不存在的通讯组时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="09f03-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
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
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="09f03-149">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="09f03-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="09f03-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="09f03-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="09f03-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="09f03-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="09f03-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="09f03-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="09f03-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09f03-153">See also</span></span>

- [<span data-ttu-id="09f03-154">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="09f03-154">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="09f03-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="09f03-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="09f03-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="09f03-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

