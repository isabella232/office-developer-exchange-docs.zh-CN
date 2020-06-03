---
title: GetFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: GetFolder 操作从 Exchange 存储中获取文件夹。
localization_priority: Priority
ms.openlocfilehash: 9d511f309b9210fd9b5a49ff6c60bc7982992973
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459179"
---
# <a name="getfolder-operation"></a><span data-ttu-id="8a65d-103">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8a65d-103">GetFolder operation</span></span>

<span data-ttu-id="8a65d-104">**GetFolder**操作从 Exchange 存储中获取文件夹。</span><span class="sxs-lookup"><span data-stu-id="8a65d-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="8a65d-105">GetFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="8a65d-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="8a65d-106">Description</span><span class="sxs-lookup"><span data-stu-id="8a65d-106">Description</span></span>

<span data-ttu-id="8a65d-107">下面的**GetFolder**请求示例演示如何获取文件夹标识符、显示名称、该文件夹中的项目数、子文件夹数以及文件夹中未读项目的数量。</span><span class="sxs-lookup"><span data-stu-id="8a65d-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8a65d-108">代码</span><span class="sxs-lookup"><span data-stu-id="8a65d-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <FolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </FolderIds>
    </GetFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="8a65d-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="8a65d-109">Request elements</span></span>

<span data-ttu-id="8a65d-110">此**GetFolder**请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="8a65d-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="8a65d-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="8a65d-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="8a65d-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="8a65d-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="8a65d-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="8a65d-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="8a65d-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="8a65d-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="8a65d-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="8a65d-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="8a65d-116">有关可用于形成**GetFolder**请求的其他元素，请参阅架构。</span><span class="sxs-lookup"><span data-stu-id="8a65d-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8a65d-117">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a65d-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="8a65d-118">GetFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="8a65d-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="8a65d-119">Description</span><span class="sxs-lookup"><span data-stu-id="8a65d-119">Description</span></span>

<span data-ttu-id="8a65d-120">下面的简单对象访问协议（SOAP）正文示例显示了对**GetFolder**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8a65d-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8a65d-121">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8a65d-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8a65d-122">代码</span><span class="sxs-lookup"><span data-stu-id="8a65d-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AQApA=" ChangeKey="AQAAAB" />
              <t:DisplayName>Inbox</t:DisplayName>
              <t:TotalCount>2</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:UnreadCount>2</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="8a65d-123">Response 元素</span><span class="sxs-lookup"><span data-stu-id="8a65d-123">Response elements</span></span>

<span data-ttu-id="8a65d-124">此**GetFolder**响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="8a65d-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="8a65d-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8a65d-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="8a65d-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8a65d-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8a65d-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8a65d-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="8a65d-128">Folders</span><span class="sxs-lookup"><span data-stu-id="8a65d-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8a65d-129">Folder</span><span class="sxs-lookup"><span data-stu-id="8a65d-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="8a65d-130">FolderId</span><span class="sxs-lookup"><span data-stu-id="8a65d-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="8a65d-131">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="8a65d-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="8a65d-132">TotalCount</span><span class="sxs-lookup"><span data-stu-id="8a65d-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="8a65d-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="8a65d-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="8a65d-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="8a65d-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="8a65d-135">GetFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="8a65d-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="8a65d-136">Description</span><span class="sxs-lookup"><span data-stu-id="8a65d-136">Description</span></span>

<span data-ttu-id="8a65d-137">以下 SOAP 正文示例显示了由请求中的错误[FolderId](folderid.md)导致的错误响应。</span><span class="sxs-lookup"><span data-stu-id="8a65d-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8a65d-138">代码</span><span class="sxs-lookup"><span data-stu-id="8a65d-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="8a65d-139">Response 元素</span><span class="sxs-lookup"><span data-stu-id="8a65d-139">Response elements</span></span>

<span data-ttu-id="8a65d-140">此**GetFolder**错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="8a65d-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="8a65d-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8a65d-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="8a65d-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8a65d-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8a65d-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8a65d-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="8a65d-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="8a65d-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8a65d-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8a65d-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8a65d-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8a65d-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8a65d-147">Folders</span><span class="sxs-lookup"><span data-stu-id="8a65d-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="8a65d-148">版本差异</span><span class="sxs-lookup"><span data-stu-id="8a65d-148">Version differences</span></span>

<span data-ttu-id="8a65d-149">对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="8a65d-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="8a65d-150">若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="8a65d-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a65d-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a65d-151">See also</span></span>



- [<span data-ttu-id="8a65d-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a65d-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

