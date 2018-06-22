---
title: GetFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: GetFolder 操作从 Exchange 存储中获取文件夹。
ms.openlocfilehash: 1d2806e4febb6059b8a866d585bc70f49befbdef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754568"
---
# <a name="getfolder-operation"></a><span data-ttu-id="80dfa-103">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="80dfa-103">GetFolder operation</span></span>

<span data-ttu-id="80dfa-104">**GetFolder**操作从 Exchange 存储中获取文件夹。</span><span class="sxs-lookup"><span data-stu-id="80dfa-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="80dfa-105">GetFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="80dfa-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="80dfa-106">说明</span><span class="sxs-lookup"><span data-stu-id="80dfa-106">Description</span></span>

<span data-ttu-id="80dfa-107">**GetFolder**请求的下面的示例演示如何获取文件夹标识符，显示文件夹中的名称、 的文件夹中的项计数、 的子文件夹计数和未读项目数。</span><span class="sxs-lookup"><span data-stu-id="80dfa-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="80dfa-108">代码</span><span class="sxs-lookup"><span data-stu-id="80dfa-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="80dfa-109">请求元素</span><span class="sxs-lookup"><span data-stu-id="80dfa-109">Request elements</span></span>

<span data-ttu-id="80dfa-110">此**GetFolder**请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="80dfa-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="80dfa-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="80dfa-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="80dfa-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="80dfa-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="80dfa-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="80dfa-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="80dfa-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="80dfa-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="80dfa-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="80dfa-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="80dfa-116">请参阅可用于表单**GetFolder**请求的其他元素的架构。</span><span class="sxs-lookup"><span data-stu-id="80dfa-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80dfa-117">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80dfa-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="80dfa-118">GetFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="80dfa-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="80dfa-119">说明</span><span class="sxs-lookup"><span data-stu-id="80dfa-119">Description</span></span>

<span data-ttu-id="80dfa-120">下面的简单对象访问协议 (SOAP) 正文示例演示对**GetFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="80dfa-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80dfa-121">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="80dfa-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="80dfa-122">代码</span><span class="sxs-lookup"><span data-stu-id="80dfa-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="80dfa-123">响应元素</span><span class="sxs-lookup"><span data-stu-id="80dfa-123">Response elements</span></span>

<span data-ttu-id="80dfa-124">此**GetFolder**响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="80dfa-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="80dfa-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="80dfa-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="80dfa-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="80dfa-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="80dfa-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="80dfa-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="80dfa-128">Folders</span><span class="sxs-lookup"><span data-stu-id="80dfa-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="80dfa-129">Folder</span><span class="sxs-lookup"><span data-stu-id="80dfa-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="80dfa-130">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="80dfa-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="80dfa-131">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="80dfa-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="80dfa-132">TotalCount</span><span class="sxs-lookup"><span data-stu-id="80dfa-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="80dfa-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="80dfa-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="80dfa-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="80dfa-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="80dfa-135">GetFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="80dfa-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="80dfa-136">说明</span><span class="sxs-lookup"><span data-stu-id="80dfa-136">Description</span></span>

<span data-ttu-id="80dfa-137">下面的 SOAP 正文示例演示请求中正确[文件夹 Id](folderid.md)导致出现错误响应。</span><span class="sxs-lookup"><span data-stu-id="80dfa-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="80dfa-138">代码</span><span class="sxs-lookup"><span data-stu-id="80dfa-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="80dfa-139">响应元素</span><span class="sxs-lookup"><span data-stu-id="80dfa-139">Response elements</span></span>

<span data-ttu-id="80dfa-140">此**GetFolder**错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="80dfa-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="80dfa-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="80dfa-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="80dfa-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="80dfa-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="80dfa-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="80dfa-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="80dfa-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="80dfa-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="80dfa-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="80dfa-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="80dfa-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="80dfa-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="80dfa-147">Folders</span><span class="sxs-lookup"><span data-stu-id="80dfa-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="80dfa-148">版本差异</span><span class="sxs-lookup"><span data-stu-id="80dfa-148">Version differences</span></span>

<span data-ttu-id="80dfa-149">应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="80dfa-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="80dfa-150">若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="80dfa-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80dfa-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80dfa-151">See also</span></span>



- [<span data-ttu-id="80dfa-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="80dfa-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

