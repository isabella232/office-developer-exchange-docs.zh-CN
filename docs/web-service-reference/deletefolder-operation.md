---
title: DeleteFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: b0f92682-4895-4bcf-a4a1-e4c2e8403979
description: DeleteFolder 操作从邮箱中删除文件夹。
ms.openlocfilehash: e9bb9199027c2af2cbbb664ef7ad4fa70b7ef718
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455742"
---
# <a name="deletefolder-operation"></a><span data-ttu-id="a4578-103">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a4578-103">DeleteFolder operation</span></span>

<span data-ttu-id="a4578-104">**DeleteFolder**操作从邮箱中删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="a4578-104">The **DeleteFolder** operation deletes folders from a mailbox.</span></span> 
  
## <a name="deletefolder-request-example"></a><span data-ttu-id="a4578-105">DeleteFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="a4578-105">DeleteFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="a4578-106">说明</span><span class="sxs-lookup"><span data-stu-id="a4578-106">Description</span></span>

<span data-ttu-id="a4578-107">下面的**DeleteFolder**请求示例演示如何在表单中组成删除文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="a4578-107">This following example of a **DeleteFolder** request shows how to form a request to delete a folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a4578-108">代码</span><span class="sxs-lookup"><span data-stu-id="a4578-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a4578-109">备注</span><span class="sxs-lookup"><span data-stu-id="a4578-109">Comments</span></span>

<span data-ttu-id="a4578-110">本示例对文件夹执行硬删除。</span><span class="sxs-lookup"><span data-stu-id="a4578-110">This example performs a hard delete on the folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a4578-111">文件夹 ID 已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="a4578-111">The folder ID has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="a4578-112">Request 元素</span><span class="sxs-lookup"><span data-stu-id="a4578-112">Request elements</span></span>

<span data-ttu-id="a4578-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a4578-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a4578-114">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="a4578-114">DeleteFolder</span></span>](deletefolder.md)
    
- [<span data-ttu-id="a4578-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="a4578-115">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="a4578-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="a4578-116">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="a4578-117">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a4578-117">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="a4578-118">若要查找**DeleteFolder**操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a4578-118">To find other options for the request message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a4578-119">从[DeleteFolder](deletefolder.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a4578-119">Start at the [DeleteFolder](deletefolder.md) element.</span></span> 
  
## <a name="successful-deletefolder-response"></a><span data-ttu-id="a4578-120">成功的 DeleteFolder 响应</span><span class="sxs-lookup"><span data-stu-id="a4578-120">Successful DeleteFolder response</span></span>

### <a name="description"></a><span data-ttu-id="a4578-121">说明</span><span class="sxs-lookup"><span data-stu-id="a4578-121">Description</span></span>

<span data-ttu-id="a4578-122">下面的示例演示对**DeleteFolder**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a4578-122">The following example shows a successful response to the **DeleteFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a4578-123">代码</span><span class="sxs-lookup"><span data-stu-id="a4578-123">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="a4578-124">Response 元素</span><span class="sxs-lookup"><span data-stu-id="a4578-124">Response elements</span></span>

<span data-ttu-id="a4578-125">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a4578-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a4578-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a4578-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a4578-127">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a4578-127">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="a4578-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a4578-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a4578-129">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a4578-129">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="a4578-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a4578-130">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="a4578-131">若要查找**DeleteFolder**操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a4578-131">To find other options for the response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a4578-132">从[DeleteFolderResponse](deletefolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a4578-132">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="deletefolder-error-response"></a><span data-ttu-id="a4578-133">DeleteFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="a4578-133">DeleteFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="a4578-134">说明</span><span class="sxs-lookup"><span data-stu-id="a4578-134">Description</span></span>

<span data-ttu-id="a4578-135">下面的示例演示对**DeleteFolder**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="a4578-135">The following example shows an error response to a **DeleteFolder** request.</span></span> <span data-ttu-id="a4578-136">此错误是由于请求删除邮箱中不存在的文件夹所致。</span><span class="sxs-lookup"><span data-stu-id="a4578-136">The error was caused by a request to delete a folder that was not present in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a4578-137">代码</span><span class="sxs-lookup"><span data-stu-id="a4578-137">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a4578-138">备注</span><span class="sxs-lookup"><span data-stu-id="a4578-138">Comments</span></span>

<span data-ttu-id="a4578-139">不能在可分辨文件夹上使用**DeleteFolder**操作。</span><span class="sxs-lookup"><span data-stu-id="a4578-139">The **DeleteFolder** operation cannot be used on distinguished folders.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="a4578-140">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="a4578-140">Error response elements</span></span>

<span data-ttu-id="a4578-141">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a4578-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a4578-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a4578-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a4578-143">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a4578-143">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="a4578-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a4578-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a4578-145">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a4578-145">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="a4578-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="a4578-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a4578-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a4578-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a4578-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a4578-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="a4578-149">若要查找**DeleteFolder**操作的错误响应消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a4578-149">To find other options for the error response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a4578-150">从[DeleteFolderResponse](deletefolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a4578-150">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4578-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a4578-151">See also</span></span>

- [<span data-ttu-id="a4578-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a4578-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="a4578-153">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="a4578-153">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

