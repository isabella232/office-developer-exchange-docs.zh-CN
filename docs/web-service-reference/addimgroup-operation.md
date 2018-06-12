---
title: AddImGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: 查找信息 AddImGroup EWS 操作。
ms.openlocfilehash: 91236f9ad2236b3f6bee600b9d57bcf736090ed7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753109"
---
# <a name="addimgroup-operation"></a><span data-ttu-id="d0fa3-103">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="d0fa3-103">AddImGroup operation</span></span>

<span data-ttu-id="d0fa3-104">查找有关**AddImGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-104">Find information about the **AddImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="d0fa3-105">**AddImGroup** Exchange Web Services (EWS) 操作将新的即时消息 (IM) 组添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-105">The **AddImGroup** Exchange Web Services (EWS) operation adds a new instant messaging (IM) group to a mailbox.</span></span> 
  
<span data-ttu-id="d0fa3-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimgroup-operation"></a><span data-ttu-id="d0fa3-107">使用 AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="d0fa3-107">Using the AddImGroup operation</span></span>

<span data-ttu-id="d0fa3-108">**AddImGroup**操作只需一个显示名称参数。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-108">The **AddImGroup** operation only takes a single display name argument.</span></span> 
  
<span data-ttu-id="d0fa3-109">此操作返回的显示名称、 组类型和 Exchange 存储的新组的标识符。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-109">This operation returns the display name, group type, and Exchange store identifier of the new group.</span></span>
  
<span data-ttu-id="d0fa3-110">**AddImGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-110">The **AddImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="d0fa3-111">**表 1。AddImGroup 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-111">**Table 1. AddImGroup operation SOAP headers**</span></span>

|<span data-ttu-id="d0fa3-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-112">**Header name**</span></span>|<span data-ttu-id="d0fa3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-113">**Element**</span></span>|<span data-ttu-id="d0fa3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0fa3-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d0fa3-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d0fa3-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d0fa3-117">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d0fa3-118">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d0fa3-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d0fa3-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d0fa3-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d0fa3-121">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d0fa3-122">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d0fa3-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d0fa3-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d0fa3-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d0fa3-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d0fa3-126">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d0fa3-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d0fa3-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d0fa3-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d0fa3-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d0fa3-129">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d0fa3-130">这是适用于响应。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a><span data-ttu-id="d0fa3-131">AddImGroup 操作请求示例： 创建新的 IM 组</span><span class="sxs-lookup"><span data-stu-id="d0fa3-131">AddImGroup operation request example: Create a new IM group</span></span>

<span data-ttu-id="d0fa3-132">**AddImGroup**操作请求的下面的示例演示如何创建一个名为 MyCustomerGroup 的 IM 组。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-132">The following example of an **AddImGroup** operation request shows how to create an IM group named MyCustomerGroup.</span></span> 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d0fa3-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d0fa3-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d0fa3-134">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="d0fa3-134">AddImGroup</span></span>](addimgroup.md)
    
- [<span data-ttu-id="d0fa3-135">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="d0fa3-135">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a><span data-ttu-id="d0fa3-136">成功 AddImGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="d0fa3-136">Successful AddImGroup operation response</span></span>

<span data-ttu-id="d0fa3-137">下面的示例演示对**AddImGroup**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-137">The following example shows a successful response to an **AddImGroup** operation request.</span></span> 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d0fa3-138">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d0fa3-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d0fa3-139">AddImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="d0fa3-139">AddImGroupResponse</span></span>](addimgroupresponse.md)
    
- [<span data-ttu-id="d0fa3-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d0fa3-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d0fa3-141">ImGroup</span><span class="sxs-lookup"><span data-stu-id="d0fa3-141">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="d0fa3-142">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="d0fa3-142">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d0fa3-143">GroupType</span><span class="sxs-lookup"><span data-stu-id="d0fa3-143">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="d0fa3-144">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="d0fa3-144">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a><span data-ttu-id="d0fa3-145">AddImGroup 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="d0fa3-145">AddImGroup operation error response</span></span>

<span data-ttu-id="d0fa3-146">下面的示例演示**AddImGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-146">The following example shows an error response to an **AddImGroup** operation request.</span></span> <span data-ttu-id="d0fa3-147">这是对包含一个字符，不能使用中的显示名称的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-147">This is a response to a request that contains a character that cannot be used in a display name.</span></span> <span data-ttu-id="d0fa3-148">请注意，这是 SOAP 错误和不基于架构的错误消息。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-148">Note that this is a SOAP fault and not a schema-based error message.</span></span> <span data-ttu-id="d0fa3-149">提交请求中的显示名称是 ~ ！ @# $%^&amp;，并且上出现了错误&amp;字符。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-149">The display name submitted in the request is ~!@#$%^&amp;, and the error occurs on the &amp; character.</span></span> <span data-ttu-id="d0fa3-150">&amp;中请求负载的 11 行和 33rd 字符上发生的字符。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-150">The &amp; character occurred on the 11th line and 33rd character in the request payload.</span></span> <span data-ttu-id="d0fa3-151">响应 HTTP 500 代码返回。</span><span class="sxs-lookup"><span data-stu-id="d0fa3-151">The response was returned with an HTTP 500 code.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d0fa3-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0fa3-152">See also</span></span>

- [<span data-ttu-id="d0fa3-153">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="d0fa3-153">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="d0fa3-154">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="d0fa3-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="d0fa3-155">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="d0fa3-155">SetImGroup</span></span>](setimgroup.md)
    

