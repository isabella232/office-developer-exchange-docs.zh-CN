---
title: SetImGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d48aa07-8152-4c3d-a519-061253e80174
description: 查找有关 SetImGroup EWS 操作的信息。
ms.openlocfilehash: 37b290559fff0b2de57669741547ba4b1b56c28c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44438073"
---
# <a name="setimgroup-operation"></a><span data-ttu-id="f02ad-103">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f02ad-103">SetImGroup operation</span></span>

<span data-ttu-id="f02ad-104">查找有关**SetImGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="f02ad-104">Find information about the **SetImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="f02ad-105">**SetImGroup**操作更改即时消息（IM）组的显示名称。</span><span class="sxs-lookup"><span data-stu-id="f02ad-105">The **SetImGroup** operation changes the display name of an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="f02ad-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="f02ad-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setimgroup-operation"></a><span data-ttu-id="f02ad-107">使用 SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f02ad-107">Using the SetImGroup operation</span></span>

<span data-ttu-id="f02ad-108">**SetImGroup**操作仅采用一个显示名称参数。</span><span class="sxs-lookup"><span data-stu-id="f02ad-108">The **SetImGroup** operation only takes a single display name argument.</span></span> 
  
### <a name="setimgroup-operation-soap-headers"></a><span data-ttu-id="f02ad-109">SetImGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f02ad-109">SetImGroup operation SOAP headers</span></span>

<span data-ttu-id="f02ad-110">**SetImGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f02ad-110">The **SetImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f02ad-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="f02ad-111">**Header name**</span></span>|<span data-ttu-id="f02ad-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="f02ad-112">**Element**</span></span>|<span data-ttu-id="f02ad-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="f02ad-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f02ad-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="f02ad-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f02ad-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f02ad-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f02ad-116">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="f02ad-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f02ad-117">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f02ad-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f02ad-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f02ad-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f02ad-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f02ad-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f02ad-120">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="f02ad-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f02ad-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f02ad-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f02ad-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f02ad-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f02ad-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f02ad-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f02ad-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f02ad-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f02ad-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f02ad-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f02ad-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f02ad-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f02ad-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f02ad-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f02ad-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="f02ad-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f02ad-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="f02ad-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setimgroup-operation-request-example"></a><span data-ttu-id="f02ad-130">SetImGroup 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="f02ad-130">SetImGroup operation request example</span></span>

<span data-ttu-id="f02ad-131">以下示例的**SetImGroup**操作请求显示如何将 IM 组显示名称更改为 "MyNewGroupName"。</span><span class="sxs-lookup"><span data-stu-id="f02ad-131">The following example of a **SetImGroup** operation request shows how to change an IM group display name to "MyNewGroupName".</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f02ad-132">已缩短 Exchange 存储标识符以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="f02ad-132">The Exchange store identifier has been shortened to preserve readability.</span></span> 
  
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
      <m:SetImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
         <m:NewDisplayName>MyNewGroupName</m:NewDisplayName>
      </m:SetImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f02ad-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f02ad-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f02ad-134">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="f02ad-134">SetImGroup</span></span>](setimgroup.md)
    
- [<span data-ttu-id="f02ad-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="f02ad-135">GroupId</span></span>](groupid.md)
    
- [<span data-ttu-id="f02ad-136">NewDisplayName</span><span class="sxs-lookup"><span data-stu-id="f02ad-136">NewDisplayName</span></span>](newdisplayname.md)
    
## <a name="successful-setimgroup-operation-response"></a><span data-ttu-id="f02ad-137">成功的 SetImGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="f02ad-137">Successful SetImGroup operation response</span></span>

<span data-ttu-id="f02ad-138">下面的示例演示对**SetImGroup**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="f02ad-138">The following example shows a successful response to a **SetImGroup** operation request.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         </SetImGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="f02ad-139">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f02ad-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f02ad-140">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f02ad-140">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="f02ad-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f02ad-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="setimgroup-operation-error-response"></a><span data-ttu-id="f02ad-142">SetImGroup 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="f02ad-142">SetImGroup operation error response</span></span>

<span data-ttu-id="f02ad-143">下面的示例演示对**SetImGroup**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="f02ad-143">The following example shows an error response to a **SetImGroup** operation request.</span></span> <span data-ttu-id="f02ad-144">当尝试将组显示名称更改为现有的组显示名称时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="f02ad-144">The following error response occurs when an attempt is made to change the group display name to the existing group display name.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>An IM group with the specified display name already exists.</MessageText>
         <ResponseCode>ErrorImGroupDisplayNameAlreadyExists</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f02ad-145">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f02ad-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f02ad-146">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f02ad-146">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="f02ad-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="f02ad-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f02ad-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f02ad-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f02ad-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f02ad-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f02ad-150">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="f02ad-150">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f02ad-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f02ad-151">See also</span></span>

- [<span data-ttu-id="f02ad-152">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="f02ad-152">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="f02ad-153">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f02ad-153">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="f02ad-154">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="f02ad-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    

