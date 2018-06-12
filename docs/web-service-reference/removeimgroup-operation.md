---
title: RemoveImGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e788016-68e0-4a3f-9243-03f6b6c6b389
description: 查找信息 RemoveImGroup EWS 操作。
ms.openlocfilehash: 85b312f0b156125a2d5395658ccea06d831abdde
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827097"
---
# <a name="removeimgroup-operation"></a><span data-ttu-id="f71e6-103">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f71e6-103">RemoveImGroup operation</span></span>

<span data-ttu-id="f71e6-104">查找有关**RemoveImGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="f71e6-104">Find information about the **RemoveImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="f71e6-105">**RemoveImGroup**操作从邮箱中删除一个即时消息 (IM) 组。</span><span class="sxs-lookup"><span data-stu-id="f71e6-105">The **RemoveImGroup** operation removes a single instant messaging (IM) group from a mailbox.</span></span> 
  
<span data-ttu-id="f71e6-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="f71e6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimgroup-operation"></a><span data-ttu-id="f71e6-107">使用 RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f71e6-107">Using the RemoveImGroup operation</span></span>

<span data-ttu-id="f71e6-108">**RemoveImGroup**操作只需一个组标识符参数。</span><span class="sxs-lookup"><span data-stu-id="f71e6-108">The **RemoveImGroup** operation only takes a single group identifier argument.</span></span> 
  
### <a name="removeimgroup-operation-soap-headers"></a><span data-ttu-id="f71e6-109">RemoveImGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f71e6-109">RemoveImGroup operation SOAP headers</span></span>

<span data-ttu-id="f71e6-110">**RemoveImGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f71e6-110">The **RemoveImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f71e6-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="f71e6-111">**Header name**</span></span>|<span data-ttu-id="f71e6-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="f71e6-112">**Element**</span></span>|<span data-ttu-id="f71e6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="f71e6-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f71e6-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="f71e6-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f71e6-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f71e6-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f71e6-116">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="f71e6-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f71e6-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="f71e6-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f71e6-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f71e6-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f71e6-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f71e6-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f71e6-120">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="f71e6-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f71e6-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="f71e6-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f71e6-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f71e6-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f71e6-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f71e6-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f71e6-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f71e6-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f71e6-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="f71e6-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f71e6-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f71e6-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f71e6-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f71e6-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f71e6-128">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="f71e6-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f71e6-129">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="f71e6-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimgroup-operation-request-example"></a><span data-ttu-id="f71e6-130">RemoveImGroup 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="f71e6-130">RemoveImGroup operation request example</span></span>

<span data-ttu-id="f71e6-131">**RemoveImGroup**操作请求的下面的示例演示如何删除 IM 组。</span><span class="sxs-lookup"><span data-stu-id="f71e6-131">The following example of a **RemoveImGroup** operation request shows how to remove an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f71e6-132">已缩短的组 ID 以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="f71e6-132">The group ID has been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5hQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f71e6-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f71e6-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f71e6-134">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="f71e6-134">RemoveImGroup</span></span>](removeimgroup.md)
    
- [<span data-ttu-id="f71e6-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="f71e6-135">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimgroup-operation-response"></a><span data-ttu-id="f71e6-136">成功 RemoveImGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="f71e6-136">Successful RemoveImGroup operation response</span></span>

<span data-ttu-id="f71e6-137">下面的示例演示对**RemoveImGroup**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="f71e6-137">The following example shows a successful response to a **RemoveImGroup** operation request.</span></span> 
  
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
      <RemoveImGroupResponse ResponseClass="Success" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f71e6-138">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f71e6-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f71e6-139">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f71e6-139">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="f71e6-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f71e6-140">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimgroup-operation-errorinvalidimgroupid-error-response"></a><span data-ttu-id="f71e6-141">RemoveImGroup 操作 ErrorInvalidImGroupId 错误响应</span><span class="sxs-lookup"><span data-stu-id="f71e6-141">RemoveImGroup operation ErrorInvalidImGroupId error response</span></span>

<span data-ttu-id="f71e6-142">下面的示例演示对**RemoveImGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="f71e6-142">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="f71e6-143">尝试删除不存在的邮箱中的组时发生了以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="f71e6-143">The following error response occurs when an attempt is made to remove a group that does not exist in the mailbox.</span></span> 
  
```XML
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
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Group Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImGroupId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f71e6-144">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f71e6-144">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f71e6-145">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f71e6-145">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="f71e6-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="f71e6-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f71e6-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f71e6-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f71e6-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f71e6-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f71e6-149">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="f71e6-149">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="removeimgroup-operation-errorinvalididmalformed-error-response"></a><span data-ttu-id="f71e6-150">RemoveImGroup 操作 ErrorInvalidIdMalformed 错误响应</span><span class="sxs-lookup"><span data-stu-id="f71e6-150">RemoveImGroup operation ErrorInvalidIdMalformed error response</span></span>

<span data-ttu-id="f71e6-151">下面的示例演示对**RemoveImGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="f71e6-151">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="f71e6-152">尝试删除格式不正确的组标识符组时发生了以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="f71e6-152">The following error response occurs when an attempt is made to remove a group with an incorrectly formatted group identifier.</span></span> 
  
```XML
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
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f71e6-153">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f71e6-153">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f71e6-154">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f71e6-154">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="f71e6-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="f71e6-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f71e6-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f71e6-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f71e6-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f71e6-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="f71e6-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f71e6-158">See also</span></span>

- [<span data-ttu-id="f71e6-159">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="f71e6-159">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="f71e6-160">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f71e6-160">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="f71e6-161">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f71e6-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    

