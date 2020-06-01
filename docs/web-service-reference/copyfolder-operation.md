---
title: CopyFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: CopyFolder 操作会复制邮箱中的文件夹。
ms.openlocfilehash: 1f9a7a3f3ede2d3cf8f9d41677d8ce0487266f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468892"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="a072f-103">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a072f-103">CopyFolder operation</span></span>

<span data-ttu-id="a072f-104">CopyFolder 操作会复制邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a072f-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="a072f-105">使用 CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a072f-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="a072f-106">CopyFolder 操作类似于[MoveFolder 操作](movefolder-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="a072f-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="a072f-107">它会复制标识的文件夹，并返回已复制文件夹的**Id**和**ChangeKey** 。</span><span class="sxs-lookup"><span data-stu-id="a072f-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="a072f-108">CopyFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="a072f-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="a072f-109">说明</span><span class="sxs-lookup"><span data-stu-id="a072f-109">Description</span></span>

<span data-ttu-id="a072f-110">以下示例的 CopyFolder 请求显示如何将文件夹复制到 "收件箱" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="a072f-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a072f-111">为了提高可读性， [FolderId](folderid.md)元素的**Id**属性值已缩短。</span><span class="sxs-lookup"><span data-stu-id="a072f-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a072f-112">代码</span><span class="sxs-lookup"><span data-stu-id="a072f-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a072f-113">备注</span><span class="sxs-lookup"><span data-stu-id="a072f-113">Comments</span></span>

<span data-ttu-id="a072f-114">可以通过[DistinguishedFolderId](distinguishedfolderid.md)元素或[FolderId](folderid.md)元素标识文件夹，以便在[ToFolderId](tofolderid.md)或[FolderIds](folderids.md)元素中使用。</span><span class="sxs-lookup"><span data-stu-id="a072f-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="a072f-115">Request 元素</span><span class="sxs-lookup"><span data-stu-id="a072f-115">Request elements</span></span>

<span data-ttu-id="a072f-116">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a072f-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a072f-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="a072f-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="a072f-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="a072f-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="a072f-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a072f-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="a072f-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="a072f-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="a072f-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="a072f-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="a072f-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a072f-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="a072f-123">若要查找 CopyFolder 操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a072f-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a072f-124">从[CopyFolder](copyfolder.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a072f-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="a072f-125">成功的 CopyFolder 响应</span><span class="sxs-lookup"><span data-stu-id="a072f-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="a072f-126">说明</span><span class="sxs-lookup"><span data-stu-id="a072f-126">Description</span></span>

<span data-ttu-id="a072f-127">下面的示例演示对 CopyFolder 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a072f-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a072f-128">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="a072f-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a072f-129">代码</span><span class="sxs-lookup"><span data-stu-id="a072f-129">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="a072f-130">评论</span><span class="sxs-lookup"><span data-stu-id="a072f-130">Comment</span></span>

<span data-ttu-id="a072f-131">响应中返回的[FolderId](folderid.md)元素表示在新文件夹位置中复制的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a072f-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="a072f-132">Response 元素</span><span class="sxs-lookup"><span data-stu-id="a072f-132">Response elements</span></span>

<span data-ttu-id="a072f-133">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a072f-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a072f-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a072f-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a072f-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a072f-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="a072f-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a072f-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a072f-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a072f-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="a072f-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a072f-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a072f-139">Folders</span><span class="sxs-lookup"><span data-stu-id="a072f-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a072f-140">Folder</span><span class="sxs-lookup"><span data-stu-id="a072f-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="a072f-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="a072f-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="a072f-142">若要查找 CopyFolder 操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a072f-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a072f-143">从[CopyFolderResponse](copyfolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a072f-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="a072f-144">CopyFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="a072f-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="a072f-145">说明</span><span class="sxs-lookup"><span data-stu-id="a072f-145">Description</span></span>

<span data-ttu-id="a072f-146">下面的示例演示对 CopyFolder 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="a072f-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="a072f-147">出现此错误的原因是已经存在具有相同显示名称的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a072f-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="a072f-148">代码</span><span class="sxs-lookup"><span data-stu-id="a072f-148">Code</span></span>

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
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="a072f-149">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="a072f-149">Error response elements</span></span>

<span data-ttu-id="a072f-150">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a072f-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a072f-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a072f-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="a072f-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a072f-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a072f-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a072f-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="a072f-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="a072f-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a072f-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a072f-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a072f-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a072f-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="a072f-157">Folders</span><span class="sxs-lookup"><span data-stu-id="a072f-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="a072f-158">若要查找 CopyFolder 操作的错误响应消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a072f-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a072f-159">从[CopyFolderResponse](copyfolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a072f-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a072f-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a072f-160">See also</span></span>

- [<span data-ttu-id="a072f-161">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a072f-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="a072f-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a072f-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

