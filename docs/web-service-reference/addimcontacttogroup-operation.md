---
title: AddImContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: 查找有关 AddImContactToGroup EWS 操作的信息。
ms.openlocfilehash: a69ee0b355e78e1249383cab612a75bcda8d9e8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458409"
---
# <a name="addimcontacttogroup-operation"></a><span data-ttu-id="421b2-103">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-103">AddImContactToGroup operation</span></span>

<span data-ttu-id="421b2-104">查找有关**AddImContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="421b2-104">Find information about the **AddImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="421b2-105">**AddImContactToGroup** Exchange Web 服务（EWS）操作将现有的即时消息（IM）联系人添加到组中。</span><span class="sxs-lookup"><span data-stu-id="421b2-105">The **AddImContactToGroup** Exchange Web Services (EWS) operation adds an existing instant messaging (IM) contact to a group.</span></span> 
  
<span data-ttu-id="421b2-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="421b2-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimcontacttogroup-operation"></a><span data-ttu-id="421b2-107">使用 AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-107">Using the AddImContactToGroup operation</span></span>

<span data-ttu-id="421b2-108">**AddImContactToGroup**操作只能接受 IM 联系人。</span><span class="sxs-lookup"><span data-stu-id="421b2-108">The **AddImContactToGroup** operation can only accept IM contacts.</span></span> <span data-ttu-id="421b2-109">如果要将新的 IM 联系人添加到统一联系人存储中，请使用[AddNewImContactToGroup](addnewimcontacttogroup-operation.md)操作。</span><span class="sxs-lookup"><span data-stu-id="421b2-109">If you want to add a new IM contact to the Unified Contact Store, use the [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) operation.</span></span> 
  
<span data-ttu-id="421b2-110">**AddImContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="421b2-110">The **AddImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="421b2-111">**表1。AddImContactToGroup 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="421b2-111">**Table 1. AddImContactToGroup operation SOAP headers**</span></span>

|<span data-ttu-id="421b2-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="421b2-112">**Header name**</span></span>|<span data-ttu-id="421b2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="421b2-113">**Element**</span></span>|<span data-ttu-id="421b2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="421b2-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="421b2-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="421b2-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="421b2-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="421b2-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="421b2-117">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="421b2-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="421b2-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="421b2-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="421b2-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="421b2-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="421b2-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="421b2-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="421b2-121">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="421b2-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="421b2-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="421b2-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="421b2-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="421b2-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="421b2-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="421b2-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="421b2-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="421b2-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="421b2-126">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="421b2-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="421b2-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="421b2-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="421b2-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="421b2-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="421b2-129">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="421b2-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="421b2-130">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="421b2-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a><span data-ttu-id="421b2-131">AddImContactToGroup 操作请求示例：将现有 IM 联系人添加到 IM 组</span><span class="sxs-lookup"><span data-stu-id="421b2-131">AddImContactToGroup operation request example: Add an existing IM contact to an IM group</span></span>

<span data-ttu-id="421b2-132">以下示例的**AddImContactToGroup**操作请求显示如何添加现有 im 联系人的 im 组。</span><span class="sxs-lookup"><span data-stu-id="421b2-132">The following example of an **AddImContactToGroup** operation request shows how to add an existing IM contact an IM group.</span></span> 
  
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

<span data-ttu-id="421b2-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="421b2-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="421b2-134">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="421b2-134">AddImContactToGroup</span></span>](addimcontacttogroup.md)
    
- [<span data-ttu-id="421b2-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="421b2-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="421b2-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="421b2-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a><span data-ttu-id="421b2-137">成功的 AddImContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="421b2-137">Successful AddImContactToGroup operation response</span></span>

<span data-ttu-id="421b2-138">下面的示例演示对**AddImContactToGroup**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="421b2-138">The following example shows a successful response to an **AddImContactToGroup** operation request.</span></span> 
  
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

<span data-ttu-id="421b2-139">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="421b2-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="421b2-140">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="421b2-140">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="421b2-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="421b2-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="421b2-142">AddImContactToGroup 操作 ErrorInvalidImContactId 错误响应</span><span class="sxs-lookup"><span data-stu-id="421b2-142">AddImContactToGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="421b2-143">下面的示例演示对**AddImContactToGroup**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="421b2-143">The following example shows an error response to an **AddImContactToGroup** operation request.</span></span> <span data-ttu-id="421b2-144">当尝试添加不是 IM 联系人的联系人时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="421b2-144">The following error response occurs when an attempt is made to add a contact that is not an IM contact.</span></span> 
  
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

<span data-ttu-id="421b2-145">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="421b2-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="421b2-146">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="421b2-146">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="421b2-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="421b2-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="421b2-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="421b2-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="421b2-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="421b2-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="421b2-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="421b2-150">See also</span></span>

- [<span data-ttu-id="421b2-151">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-151">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="421b2-152">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-152">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="421b2-153">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-153">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="421b2-154">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="421b2-155">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="421b2-155">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="421b2-156">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="421b2-156">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

