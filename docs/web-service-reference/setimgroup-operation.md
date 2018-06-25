---
title: SetImGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d48aa07-8152-4c3d-a519-061253e80174
description: 查找信息 SetImGroup EWS 操作。
ms.openlocfilehash: 80980c25888ab3fcae0a761e115c3ac3d578a013
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827421"
---
# <a name="setimgroup-operation"></a><span data-ttu-id="5511e-103">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="5511e-103">SetImGroup operation</span></span>

<span data-ttu-id="5511e-104">查找有关**SetImGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="5511e-104">Find information about the **SetImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="5511e-105">**SetImGroup**操作将更改即时消息 (IM) 组的显示名称。</span><span class="sxs-lookup"><span data-stu-id="5511e-105">The **SetImGroup** operation changes the display name of an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="5511e-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="5511e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setimgroup-operation"></a><span data-ttu-id="5511e-107">使用 SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="5511e-107">Using the SetImGroup operation</span></span>

<span data-ttu-id="5511e-108">**SetImGroup**操作只需一个显示名称参数。</span><span class="sxs-lookup"><span data-stu-id="5511e-108">The **SetImGroup** operation only takes a single display name argument.</span></span> 
  
### <a name="setimgroup-operation-soap-headers"></a><span data-ttu-id="5511e-109">SetImGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="5511e-109">SetImGroup operation SOAP headers</span></span>

<span data-ttu-id="5511e-110">**SetImGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="5511e-110">The **SetImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="5511e-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="5511e-111">**Header name**</span></span>|<span data-ttu-id="5511e-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="5511e-112">**Element**</span></span>|<span data-ttu-id="5511e-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="5511e-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5511e-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="5511e-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="5511e-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="5511e-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="5511e-116">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="5511e-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="5511e-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5511e-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5511e-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="5511e-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="5511e-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="5511e-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="5511e-120">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="5511e-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="5511e-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5511e-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5511e-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="5511e-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="5511e-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5511e-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5511e-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="5511e-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="5511e-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5511e-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5511e-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="5511e-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="5511e-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5511e-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5511e-128">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="5511e-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="5511e-129">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="5511e-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setimgroup-operation-request-example"></a><span data-ttu-id="5511e-130">SetImGroup 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="5511e-130">SetImGroup operation request example</span></span>

<span data-ttu-id="5511e-131">**SetImGroup**操作请求的下面的示例演示如何将 IM 组的显示名称更改为"MyNewGroupName"。</span><span class="sxs-lookup"><span data-stu-id="5511e-131">The following example of a **SetImGroup** operation request shows how to change an IM group display name to "MyNewGroupName".</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5511e-132">Exchange 书店标识符已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="5511e-132">The Exchange store identifier has been shortened to preserve readability.</span></span> 
  
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
      <m:SetImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
         <m:NewDisplayName>MyNewGroupName</m:NewDisplayName>
      </m:SetImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="5511e-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5511e-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5511e-134">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="5511e-134">SetImGroup</span></span>](setimgroup.md)
    
- [<span data-ttu-id="5511e-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="5511e-135">GroupId</span></span>](groupid.md)
    
- [<span data-ttu-id="5511e-136">NewDisplayName</span><span class="sxs-lookup"><span data-stu-id="5511e-136">NewDisplayName</span></span>](newdisplayname.md)
    
## <a name="successful-setimgroup-operation-response"></a><span data-ttu-id="5511e-137">成功 SetImGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="5511e-137">Successful SetImGroup operation response</span></span>

<span data-ttu-id="5511e-138">下面的示例演示对**SetImGroup**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="5511e-138">The following example shows a successful response to a **SetImGroup** operation request.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         </SetImGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="5511e-139">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5511e-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5511e-140">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="5511e-140">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="5511e-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5511e-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="setimgroup-operation-error-response"></a><span data-ttu-id="5511e-142">SetImGroup 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="5511e-142">SetImGroup operation error response</span></span>

<span data-ttu-id="5511e-143">下面的示例演示对**SetImGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="5511e-143">The following example shows an error response to a **SetImGroup** operation request.</span></span> <span data-ttu-id="5511e-144">当尝试为现有组的显示名称更改组的显示名称时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="5511e-144">The following error response occurs when an attempt is made to change the group display name to the existing group display name.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Error" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>An IM group with the specified display name already exists.</MessageText>
         <ResponseCode>ErrorImGroupDisplayNameAlreadyExists</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="5511e-145">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5511e-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5511e-146">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="5511e-146">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="5511e-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="5511e-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5511e-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5511e-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5511e-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5511e-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="5511e-150">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="5511e-150">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5511e-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5511e-151">See also</span></span>

- [<span data-ttu-id="5511e-152">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="5511e-152">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="5511e-153">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="5511e-153">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="5511e-154">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="5511e-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    

