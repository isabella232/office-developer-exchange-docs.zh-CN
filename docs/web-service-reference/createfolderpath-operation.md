---
title: CreateFolderPath 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: 查找有关 CreateFolderPath EWS 操作的信息。
ms.openlocfilehash: a8d42cbef854d900c5fb6b72c730dd1e2b903aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458899"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="c17d9-103">CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="c17d9-103">CreateFolderPath operation</span></span>

<span data-ttu-id="c17d9-104">查找有关**CreateFolderPath** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="c17d9-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="c17d9-105">**CreateFolderPath**操作将创建一个文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="c17d9-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="c17d9-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="c17d9-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="c17d9-107">使用 CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="c17d9-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="c17d9-108">**CreateFolderPath**操作请求采用文件夹和父文件夹标识符的数组，并根据数组中文件夹的顺序创建文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="c17d9-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="c17d9-109">CreateFolderPath 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="c17d9-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="c17d9-110">**CreateFolderPath**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c17d9-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c17d9-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="c17d9-111">**Header name**</span></span>|<span data-ttu-id="c17d9-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="c17d9-112">**Element**</span></span>|<span data-ttu-id="c17d9-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="c17d9-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c17d9-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="c17d9-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c17d9-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c17d9-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c17d9-116">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="c17d9-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c17d9-117">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c17d9-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c17d9-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c17d9-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c17d9-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c17d9-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c17d9-120">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="c17d9-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c17d9-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c17d9-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c17d9-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c17d9-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c17d9-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c17d9-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c17d9-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="c17d9-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c17d9-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c17d9-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c17d9-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c17d9-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c17d9-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c17d9-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c17d9-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="c17d9-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c17d9-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="c17d9-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="c17d9-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="c17d9-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="c17d9-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c17d9-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c17d9-132">标识**DateTime**属性的时区范围。</span><span class="sxs-lookup"><span data-stu-id="c17d9-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="c17d9-133">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c17d9-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="c17d9-134">CreateFolderPath 操作请求示例：创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="c17d9-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="c17d9-135">下面的**CreateFolderPath**操作请求示例演示如何在默认的 "收件箱" 文件夹中创建三个文件夹的文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="c17d9-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c17d9-136">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="c17d9-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:CreateFolderPath>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ParentFolderId>
         <m:RelativeFolderPath>
            <t:Folder>
               <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MySecondLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
            </t:Folder>
         </m:RelativeFolderPath>
      </m:CreateFolderPath>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="c17d9-137">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c17d9-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c17d9-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="c17d9-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="c17d9-139">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="c17d9-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="c17d9-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c17d9-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="c17d9-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="c17d9-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="c17d9-142">Folder</span><span class="sxs-lookup"><span data-stu-id="c17d9-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c17d9-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="c17d9-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="c17d9-144">成功的 CreateFolderPath 操作响应</span><span class="sxs-lookup"><span data-stu-id="c17d9-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="c17d9-145">下面的示例演示如何成功地响应在默认 "收件箱" 文件夹中创建文件夹层次结构深度为3个文件夹的**CreateFolderPath**操作请求。</span><span class="sxs-lookup"><span data-stu-id="c17d9-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExYisXAAA=" ChangeKey="AQAAABYAABq6Wxb"/>
                     <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExm4QrAABqxisYAAA=" ChangeKey="AQAAABYAAAm4QrAABq6Wxg"/>
                     <t:DisplayName>MySecondLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTAABqxisZAAA=" ChangeKey="AQAAABYAA6Wxl"/>
                     <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="c17d9-146">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c17d9-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c17d9-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="c17d9-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="c17d9-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c17d9-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c17d9-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c17d9-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="c17d9-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c17d9-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c17d9-151">Folders</span><span class="sxs-lookup"><span data-stu-id="c17d9-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c17d9-152">Folder</span><span class="sxs-lookup"><span data-stu-id="c17d9-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="c17d9-153">FolderId</span><span class="sxs-lookup"><span data-stu-id="c17d9-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="c17d9-154">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="c17d9-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c17d9-155">TotalCount</span><span class="sxs-lookup"><span data-stu-id="c17d9-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="c17d9-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="c17d9-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="c17d9-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c17d9-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="c17d9-158">CreateFolderPath 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="c17d9-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="c17d9-159">下面的示例演示对**CreateFolderPath**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="c17d9-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="c17d9-160">这是对创建两个文件夹的请求的响应，其中第一个文件夹没有显示名称属性集。</span><span class="sxs-lookup"><span data-stu-id="c17d9-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="c17d9-161">层次结构中的第一个文件夹不能在没有显示名称属性的情况下创建，并且无法创建第二个文件夹，因为层次结构中的父文件夹未创建。</span><span class="sxs-lookup"><span data-stu-id="c17d9-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The folder save operation failed due to invalid property values.</m:MessageText>
               <m:ResponseCode>ErrorFolderSavePropertyError</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:MessageXml>
                  <t:FieldURI FieldURI="folder:DisplayName"/>
               </m:MessageXml>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The specified parent folder could not be found.</m:MessageText>
               <m:ResponseCode>ErrorParentFolderNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="c17d9-162">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c17d9-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c17d9-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="c17d9-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="c17d9-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c17d9-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c17d9-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c17d9-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="c17d9-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="c17d9-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c17d9-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c17d9-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c17d9-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c17d9-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="c17d9-169">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c17d9-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="c17d9-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c17d9-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="c17d9-171">Folders</span><span class="sxs-lookup"><span data-stu-id="c17d9-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="c17d9-172">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="c17d9-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c17d9-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c17d9-173">See also</span></span>

- [<span data-ttu-id="c17d9-174">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="c17d9-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c17d9-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c17d9-175">FindFolder operation</span></span>](findfolder-operation.md)
    

