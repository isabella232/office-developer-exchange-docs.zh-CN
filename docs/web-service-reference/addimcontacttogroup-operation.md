---
title: AddImContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: 查找信息 AddImContactToGroup EWS 操作。
ms.openlocfilehash: 669d798b6cabc1cab1fc057a3e18c565467440f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753104"
---
# <a name="addimcontacttogroup-operation"></a><span data-ttu-id="eac7d-103">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-103">AddImContactToGroup operation</span></span>

<span data-ttu-id="eac7d-104">查找有关**AddImContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="eac7d-104">Find information about the **AddImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="eac7d-105">**AddImContactToGroup** Exchange Web Services (EWS) 操作将现有的即时消息 (IM) 联系人添加到组。</span><span class="sxs-lookup"><span data-stu-id="eac7d-105">The **AddImContactToGroup** Exchange Web Services (EWS) operation adds an existing instant messaging (IM) contact to a group.</span></span> 
  
<span data-ttu-id="eac7d-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="eac7d-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimcontacttogroup-operation"></a><span data-ttu-id="eac7d-107">使用 AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-107">Using the AddImContactToGroup operation</span></span>

<span data-ttu-id="eac7d-108">**AddImContactToGroup**操作只能接受 IM 联系人。</span><span class="sxs-lookup"><span data-stu-id="eac7d-108">The **AddImContactToGroup** operation can only accept IM contacts.</span></span> <span data-ttu-id="eac7d-109">如果您想要将新的 IM 联系人添加到统一联系人存储库，使用[AddNewImContactToGroup](addnewimcontacttogroup-operation.md)操作。</span><span class="sxs-lookup"><span data-stu-id="eac7d-109">If you want to add a new IM contact to the Unified Contact Store, use the [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) operation.</span></span> 
  
<span data-ttu-id="eac7d-110">**AddImContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="eac7d-110">The **AddImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="eac7d-111">**表 1。AddImContactToGroup 操作 SOAP 标头**</span><span class="sxs-lookup"><span data-stu-id="eac7d-111">**Table 1. AddImContactToGroup operation SOAP headers**</span></span>

|<span data-ttu-id="eac7d-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="eac7d-112">**Header name**</span></span>|<span data-ttu-id="eac7d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="eac7d-113">**Element**</span></span>|<span data-ttu-id="eac7d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="eac7d-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eac7d-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="eac7d-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="eac7d-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="eac7d-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="eac7d-117">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="eac7d-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="eac7d-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="eac7d-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="eac7d-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="eac7d-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="eac7d-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="eac7d-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="eac7d-121">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="eac7d-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="eac7d-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="eac7d-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="eac7d-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="eac7d-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="eac7d-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="eac7d-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="eac7d-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="eac7d-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="eac7d-126">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="eac7d-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="eac7d-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="eac7d-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="eac7d-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="eac7d-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="eac7d-129">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="eac7d-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="eac7d-130">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="eac7d-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a><span data-ttu-id="eac7d-131">AddImContactToGroup 操作请求示例： 添加现有 IM 联系人的 IM 组</span><span class="sxs-lookup"><span data-stu-id="eac7d-131">AddImContactToGroup operation request example: Add an existing IM contact to an IM group</span></span>

<span data-ttu-id="eac7d-132">**AddImContactToGroup**操作请求的下面的示例演示如何添加的现有的 IM 联系人的 IM 组。</span><span class="sxs-lookup"><span data-stu-id="eac7d-132">The following example of an **AddImContactToGroup** operation request shows how to add an existing IM contact an IM group.</span></span> 
  
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
      <m:AddImContactToGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTc4Y2AA="
                      ChangeKey="EQAAABYAAABtF8oI7i"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkzzAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="eac7d-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eac7d-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eac7d-134">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="eac7d-134">AddImContactToGroup</span></span>](addimcontacttogroup.md)
    
- [<span data-ttu-id="eac7d-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="eac7d-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="eac7d-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="eac7d-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a><span data-ttu-id="eac7d-137">成功 AddImContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="eac7d-137">Successful AddImContactToGroup operation response</span></span>

<span data-ttu-id="eac7d-138">下面的示例演示对**AddImContactToGroup**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="eac7d-138">The following example shows a successful response to an **AddImContactToGroup** operation request.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Success" 
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </AddImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="eac7d-139">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eac7d-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eac7d-140">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="eac7d-140">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="eac7d-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eac7d-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="eac7d-142">AddImContactToGroup 操作 ErrorInvalidImContactId 错误响应</span><span class="sxs-lookup"><span data-stu-id="eac7d-142">AddImContactToGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="eac7d-143">下面的示例演示**AddImContactToGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="eac7d-143">The following example shows an error response to an **AddImContactToGroup** operation request.</span></span> <span data-ttu-id="eac7d-144">当尝试添加不是 IM 联系人的联系人时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="eac7d-144">The following error response occurs when an attempt is made to add a contact that is not an IM contact.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Error" 
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         </AddImContactToGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="eac7d-145">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eac7d-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eac7d-146">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="eac7d-146">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="eac7d-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="eac7d-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="eac7d-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eac7d-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="eac7d-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="eac7d-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="eac7d-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eac7d-150">See also</span></span>

- [<span data-ttu-id="eac7d-151">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-151">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="eac7d-152">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-152">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="eac7d-153">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-153">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="eac7d-154">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="eac7d-155">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="eac7d-155">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="eac7d-156">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="eac7d-156">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

