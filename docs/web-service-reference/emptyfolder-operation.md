---
title: EmptyFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: EmptyFolder 操作清空邮箱中的文件夹。 （可选） 通过此操作可删除指定的文件夹的子文件夹。 删除子文件夹后，将删除的子文件夹和子文件夹中的邮件。
ms.openlocfilehash: 0192744516c5a6d24b95915452bfcffecc2d92b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754094"
---
# <a name="emptyfolder-operation"></a><span data-ttu-id="35e83-105">EmptyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="35e83-105">EmptyFolder operation</span></span>

<span data-ttu-id="35e83-106">**EmptyFolder**操作清空邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="35e83-106">The **EmptyFolder** operation empties folders in a mailbox.</span></span> <span data-ttu-id="35e83-107">（可选） 通过此操作可删除指定的文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="35e83-107">Optionally, this operation enables you to delete the subfolders of the specified folder.</span></span> <span data-ttu-id="35e83-108">删除子文件夹后，将删除的子文件夹和子文件夹中的邮件。</span><span class="sxs-lookup"><span data-stu-id="35e83-108">When a subfolder is deleted, the subfolder and the messages within the subfolder are deleted.</span></span> 
  
## <a name="emptyfolder-request-example"></a><span data-ttu-id="35e83-109">EmptyFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="35e83-109">EmptyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="35e83-110">说明</span><span class="sxs-lookup"><span data-stu-id="35e83-110">Description</span></span>

<span data-ttu-id="35e83-111">**EmptyFolder**请求的此下面的示例演示如何以形成清空文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="35e83-111">This following example of an **EmptyFolder** request shows how to form a request to empty a folder.</span></span> <span data-ttu-id="35e83-112">本示例删除标识文件夹的所有子文件夹。</span><span class="sxs-lookup"><span data-stu-id="35e83-112">This example deletes all subfolders of the identified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="35e83-113">为便于阅读，具有已缩短的**Id**值和[文件夹 Id](folderid.md)元素的**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="35e83-113">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="35e83-114">代码</span><span class="sxs-lookup"><span data-stu-id="35e83-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
    </soap:Header>
    <soap:Body>
      <m:EmptyFolder DeleteType="HardDelete" DeleteSubFolders="true">
        <m:FolderIds>
          <t:FolderId Id="AQMkADhhOGU0"  ChangeKey="AQAAABYAAABsMB" />
        </m:FolderIds>
      </m:EmptyFolder>
    </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="35e83-115">注释</span><span class="sxs-lookup"><span data-stu-id="35e83-115">Comments</span></span>

<span data-ttu-id="35e83-116">本示例对文件夹执行硬删除。</span><span class="sxs-lookup"><span data-stu-id="35e83-116">This example performs a hard delete on the folder.</span></span>
  
<span data-ttu-id="35e83-117">可通过[DistinguishedFolderId](distinguishedfolderid.md)元素或[FolderIds](folderids.md)元素中使用的[文件夹 Id](folderid.md)元素标识文件夹。</span><span class="sxs-lookup"><span data-stu-id="35e83-117">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in the [FolderIds](folderids.md) element.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="35e83-118">请求元素</span><span class="sxs-lookup"><span data-stu-id="35e83-118">Request elements</span></span>

<span data-ttu-id="35e83-119">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="35e83-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="35e83-120">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="35e83-120">EmptyFolder</span></span>](emptyfolder.md)
    
- [<span data-ttu-id="35e83-121">FolderIds</span><span class="sxs-lookup"><span data-stu-id="35e83-121">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="35e83-122">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="35e83-122">FolderId</span></span>](folderid.md)
    
## <a name="successful-emptyfolder-response"></a><span data-ttu-id="35e83-123">成功的 EmptyFolder 响应</span><span class="sxs-lookup"><span data-stu-id="35e83-123">Successful EmptyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="35e83-124">说明</span><span class="sxs-lookup"><span data-stu-id="35e83-124">Description</span></span>

<span data-ttu-id="35e83-125">下面的示例演示对**EmptyFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="35e83-125">The following example shows a successful response to the **EmptyFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="35e83-126">代码</span><span class="sxs-lookup"><span data-stu-id="35e83-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:EmptyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="35e83-127">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="35e83-127">Successful response elements</span></span>

<span data-ttu-id="35e83-128">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="35e83-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="35e83-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="35e83-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="35e83-130">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="35e83-130">EmptyFolderResponse</span></span>](emptyfolderresponse.md)
    
- [<span data-ttu-id="35e83-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="35e83-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="35e83-132">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="35e83-132">EmptyFolderResponseMessage</span></span>](emptyfolderresponsemessage.md)
    
- [<span data-ttu-id="35e83-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="35e83-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="emptyfolder-error-response"></a><span data-ttu-id="35e83-134">EmptyFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="35e83-134">EmptyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="35e83-135">说明</span><span class="sxs-lookup"><span data-stu-id="35e83-135">Description</span></span>

<span data-ttu-id="35e83-136">下面的示例演示**Emptyfolder**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="35e83-136">The following example shows an error response to an **Emptyfolder** request.</span></span> <span data-ttu-id="35e83-137">创建错误，因为该操作尝试清空找不到的文件夹 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="35e83-137">The error was created because the operation tried to empty a folder that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="35e83-138">代码</span><span class="sxs-lookup"><span data-stu-id="35e83-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
            MinorVersion="1" 
            MajorBuildNumber="164" 
            MinorBuildNumber="0" 
            Version="Exchange2010_SP1" 
            xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="35e83-139">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="35e83-139">Error response elements</span></span>

<span data-ttu-id="35e83-140">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="35e83-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="35e83-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="35e83-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="35e83-142">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="35e83-142">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="35e83-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="35e83-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="35e83-144">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="35e83-144">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="35e83-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="35e83-145">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="35e83-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="35e83-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="35e83-147">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="35e83-147">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="35e83-148">文件夹</span><span class="sxs-lookup"><span data-stu-id="35e83-148">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="35e83-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35e83-149">See also</span></span>

- [<span data-ttu-id="35e83-150">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35e83-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

