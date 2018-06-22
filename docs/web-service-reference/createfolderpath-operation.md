---
title: CreateFolderPath 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: 查找信息 CreateFolderPath EWS 操作。
ms.openlocfilehash: 22561e5086c144e25d7e04b68ec6674b87c4718d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753645"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="bf1c0-103">CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="bf1c0-103">CreateFolderPath operation</span></span>

<span data-ttu-id="bf1c0-104">查找有关**CreateFolderPath** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="bf1c0-105">**CreateFolderPath**操作创建文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="bf1c0-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="bf1c0-107">使用 CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="bf1c0-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="bf1c0-108">**CreateFolderPath**操作请求所需的文件夹和父文件夹标识符数组，并创建文件夹层次结构根据数组中的文件夹的顺序。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="bf1c0-109">CreateFolderPath 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="bf1c0-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="bf1c0-110">**CreateFolderPath**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="bf1c0-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-111">**Header name**</span></span>|<span data-ttu-id="bf1c0-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-112">**Element**</span></span>|<span data-ttu-id="bf1c0-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf1c0-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="bf1c0-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="bf1c0-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="bf1c0-116">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="bf1c0-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bf1c0-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="bf1c0-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="bf1c0-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="bf1c0-120">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="bf1c0-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bf1c0-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="bf1c0-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bf1c0-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="bf1c0-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="bf1c0-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bf1c0-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="bf1c0-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bf1c0-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="bf1c0-128">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="bf1c0-129">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="bf1c0-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="bf1c0-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="bf1c0-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="bf1c0-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="bf1c0-132">标识**DateTime**属性的时区范围。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="bf1c0-133">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="bf1c0-134">CreateFolderPath 操作请求示例： 创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="bf1c0-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="bf1c0-135">**CreateFolderPath**操作请求的下面的示例演示如何创建三个文件夹的文件夹层次结构深度在默认收件箱文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bf1c0-136">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="bf1c0-137">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="bf1c0-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bf1c0-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="bf1c0-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="bf1c0-139">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="bf1c0-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="bf1c0-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="bf1c0-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="bf1c0-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="bf1c0-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="bf1c0-142">Folder</span><span class="sxs-lookup"><span data-stu-id="bf1c0-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="bf1c0-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="bf1c0-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="bf1c0-144">成功 CreateFolderPath 操作响应</span><span class="sxs-lookup"><span data-stu-id="bf1c0-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="bf1c0-145">下面的示例演示成功响应**CreateFolderPath**操作请求创建一个文件夹层次结构三文件夹深度在默认收件箱文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="bf1c0-146">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="bf1c0-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bf1c0-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="bf1c0-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="bf1c0-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf1c0-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bf1c0-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf1c0-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="bf1c0-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bf1c0-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bf1c0-151">Folders</span><span class="sxs-lookup"><span data-stu-id="bf1c0-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="bf1c0-152">Folder</span><span class="sxs-lookup"><span data-stu-id="bf1c0-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="bf1c0-153">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="bf1c0-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="bf1c0-154">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="bf1c0-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="bf1c0-155">TotalCount</span><span class="sxs-lookup"><span data-stu-id="bf1c0-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="bf1c0-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="bf1c0-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="bf1c0-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="bf1c0-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="bf1c0-158">CreateFolderPath 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="bf1c0-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="bf1c0-159">下面的示例演示对**CreateFolderPath**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="bf1c0-160">这是对请求创建两个文件夹，其中第一个不具有显示名称属性设置的响应。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="bf1c0-161">没有显示 name 属性，无法创建层次结构中的第一个文件夹且无法创建第二个文件夹，因为未创建层次结构中的父文件夹。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="bf1c0-162">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="bf1c0-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bf1c0-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="bf1c0-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="bf1c0-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf1c0-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bf1c0-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf1c0-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="bf1c0-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="bf1c0-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bf1c0-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bf1c0-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bf1c0-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bf1c0-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="bf1c0-169">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bf1c0-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="bf1c0-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="bf1c0-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="bf1c0-171">Folders</span><span class="sxs-lookup"><span data-stu-id="bf1c0-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="bf1c0-172">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="bf1c0-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf1c0-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf1c0-173">See also</span></span>

- [<span data-ttu-id="bf1c0-174">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="bf1c0-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="bf1c0-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="bf1c0-175">FindFolder operation</span></span>](findfolder-operation.md)
    

