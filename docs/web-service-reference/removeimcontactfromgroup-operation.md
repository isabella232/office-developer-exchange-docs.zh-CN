---
title: RemoveImContactFromGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: 查找有关 RemoveImContactFromGroup EWS 操作的信息。
ms.openlocfilehash: 4750ef57794c3da540ac36baa8ef6ef093939ea1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466967"
---
# <a name="removeimcontactfromgroup-operation"></a><span data-ttu-id="05c2a-103">RemoveImContactFromGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-103">RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="05c2a-104">查找有关**RemoveImContactFromGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="05c2a-104">Find information about the **RemoveImContactFromGroup** EWS operation.</span></span> 
  
<span data-ttu-id="05c2a-105">**RemoveImContactFromGroup**操作从 im 组中删除单个 im 联系人。</span><span class="sxs-lookup"><span data-stu-id="05c2a-105">The **RemoveImContactFromGroup** operation removes a single IM contact from an IM group.</span></span> 
  
<span data-ttu-id="05c2a-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="05c2a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimcontactfromgroup-operation"></a><span data-ttu-id="05c2a-107">使用 RemoveImContactFromGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-107">Using the RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="05c2a-108">**RemoveImContactFromGroup**操作采用两个参数：联系人项目标识符，以及从中删除联系人的相应即时消息（IM）组。</span><span class="sxs-lookup"><span data-stu-id="05c2a-108">The **RemoveImContactFromGroup** operation takes two arguments: a contact item identifier, and the corresponding instant messaging (IM) group from which the contact is removed.</span></span> 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a><span data-ttu-id="05c2a-109">RemoveImContactFromGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="05c2a-109">RemoveImContactFromGroup operation SOAP headers</span></span>

<span data-ttu-id="05c2a-110">**RemoveImContactFromGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="05c2a-110">The **RemoveImContactFromGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="05c2a-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="05c2a-111">**Header name**</span></span>|<span data-ttu-id="05c2a-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="05c2a-112">**Element**</span></span>|<span data-ttu-id="05c2a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="05c2a-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05c2a-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="05c2a-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="05c2a-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="05c2a-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="05c2a-116">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="05c2a-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="05c2a-117">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="05c2a-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="05c2a-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="05c2a-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="05c2a-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="05c2a-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="05c2a-120">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="05c2a-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="05c2a-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="05c2a-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="05c2a-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="05c2a-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="05c2a-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="05c2a-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="05c2a-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="05c2a-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="05c2a-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="05c2a-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="05c2a-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="05c2a-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="05c2a-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="05c2a-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="05c2a-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="05c2a-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="05c2a-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="05c2a-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a><span data-ttu-id="05c2a-130">RemoveImContactFromGroup 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="05c2a-130">RemoveImContactFromGroup operation request example</span></span>

<span data-ttu-id="05c2a-131">下面的**RemoveImContactFromGroup**操作请求示例演示如何从 im 组中删除 im 联系人。</span><span class="sxs-lookup"><span data-stu-id="05c2a-131">The following example of a **RemoveImContactFromGroup** operation request shows how to remove an IM contact from an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="05c2a-132">组和联系人标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="05c2a-132">The group and contact identifiers have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="05c2a-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="05c2a-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="05c2a-134">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="05c2a-134">RemoveImContactFromGroup</span></span>](removeimcontactfromgroup.md)
    
- [<span data-ttu-id="05c2a-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="05c2a-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="05c2a-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="05c2a-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a><span data-ttu-id="05c2a-137">成功的 RemoveImContactFromGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="05c2a-137">Successful RemoveImContactFromGroup operation response</span></span>

<span data-ttu-id="05c2a-138">下面的示例演示对**RemoveImContactFromGroup**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="05c2a-138">The following example shows a successful response to a **RemoveImContactFromGroup** operation request.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="05c2a-139">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="05c2a-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="05c2a-140">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="05c2a-140">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="05c2a-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="05c2a-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="05c2a-142">RemoveImContactFromGroup 操作 ErrorInvalidImContactId 错误响应</span><span class="sxs-lookup"><span data-stu-id="05c2a-142">RemoveImContactFromGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="05c2a-143">下面的示例演示对**RemoveImContactFromGroup**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="05c2a-143">The following example shows an error response to a **RemoveImContactFromGroup** operation request.</span></span> <span data-ttu-id="05c2a-144">当尝试删除 IM 组中不存在的联系人项时，将发生以下错误响应。</span><span class="sxs-lookup"><span data-stu-id="05c2a-144">The following error response occurs when an attempt is made to remove a contact item that does not exist in the IM group.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="05c2a-145">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="05c2a-145">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="05c2a-146">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="05c2a-146">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="05c2a-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="05c2a-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="05c2a-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="05c2a-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="05c2a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="05c2a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="05c2a-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05c2a-150">See also</span></span>

- [<span data-ttu-id="05c2a-151">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="05c2a-151">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="05c2a-152">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="05c2a-152">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="05c2a-153">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="05c2a-153">AddImContactToGroup</span></span>](addimcontacttogroup-operation.md)
    
- [<span data-ttu-id="05c2a-154">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-154">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="05c2a-155">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-155">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="05c2a-156">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="05c2a-157">GetImItems</span><span class="sxs-lookup"><span data-stu-id="05c2a-157">GetImItems</span></span>](getimitems-operation.md)
    
- [<span data-ttu-id="05c2a-158">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="05c2a-158">RemoveContactFromImList</span></span>](removecontactfromimlist-operation.md)
    
- [<span data-ttu-id="05c2a-159">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="05c2a-159">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist-operation.md)
    
- [<span data-ttu-id="05c2a-160">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-160">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="05c2a-161">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="05c2a-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="05c2a-162">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="05c2a-162">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted-operation.md)
    

