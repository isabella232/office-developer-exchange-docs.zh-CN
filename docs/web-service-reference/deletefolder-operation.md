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
ms.openlocfilehash: 0fd7c9d4b04a706dcdb83f41087eaa4f3d45f129
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753801"
---
# <a name="deletefolder-operation"></a><span data-ttu-id="b36c9-103">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="b36c9-103">DeleteFolder operation</span></span>

<span data-ttu-id="b36c9-104">**DeleteFolder**操作从邮箱中删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="b36c9-104">The **DeleteFolder** operation deletes folders from a mailbox.</span></span> 
  
## <a name="deletefolder-request-example"></a><span data-ttu-id="b36c9-105">DeleteFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="b36c9-105">DeleteFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="b36c9-106">说明</span><span class="sxs-lookup"><span data-stu-id="b36c9-106">Description</span></span>

<span data-ttu-id="b36c9-107">**DeleteFolder**请求的此下面的示例演示如何删除文件夹的请求的表单。</span><span class="sxs-lookup"><span data-stu-id="b36c9-107">This following example of a **DeleteFolder** request shows how to form a request to delete a folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b36c9-108">代码</span><span class="sxs-lookup"><span data-stu-id="b36c9-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b36c9-109">注释</span><span class="sxs-lookup"><span data-stu-id="b36c9-109">Comments</span></span>

<span data-ttu-id="b36c9-110">本示例对文件夹执行硬删除。</span><span class="sxs-lookup"><span data-stu-id="b36c9-110">This example performs a hard delete on the folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b36c9-111">已缩短文件夹 ID 以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b36c9-111">The folder ID has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="b36c9-112">请求元素</span><span class="sxs-lookup"><span data-stu-id="b36c9-112">Request elements</span></span>

<span data-ttu-id="b36c9-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b36c9-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b36c9-114">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="b36c9-114">DeleteFolder</span></span>](deletefolder.md)
    
- [<span data-ttu-id="b36c9-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="b36c9-115">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="b36c9-116">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="b36c9-116">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="b36c9-117">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b36c9-117">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="b36c9-118">若要查找的请求邮件**DeleteFolder**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="b36c9-118">To find other options for the request message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b36c9-119">启动[DeleteFolder](deletefolder.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b36c9-119">Start at the [DeleteFolder](deletefolder.md) element.</span></span> 
  
## <a name="successful-deletefolder-response"></a><span data-ttu-id="b36c9-120">成功的 DeleteFolder 响应</span><span class="sxs-lookup"><span data-stu-id="b36c9-120">Successful DeleteFolder response</span></span>

### <a name="description"></a><span data-ttu-id="b36c9-121">说明</span><span class="sxs-lookup"><span data-stu-id="b36c9-121">Description</span></span>

<span data-ttu-id="b36c9-122">下面的示例演示对**DeleteFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b36c9-122">The following example shows a successful response to the **DeleteFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b36c9-123">代码</span><span class="sxs-lookup"><span data-stu-id="b36c9-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="b36c9-124">响应元素</span><span class="sxs-lookup"><span data-stu-id="b36c9-124">Response elements</span></span>

<span data-ttu-id="b36c9-125">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b36c9-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b36c9-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b36c9-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b36c9-127">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="b36c9-127">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="b36c9-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b36c9-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b36c9-129">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b36c9-129">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="b36c9-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b36c9-130">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="b36c9-131">若要查找的响应消息**DeleteFolder**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="b36c9-131">To find other options for the response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b36c9-132">启动[DeleteFolderResponse](deletefolderresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b36c9-132">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="deletefolder-error-response"></a><span data-ttu-id="b36c9-133">DeleteFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="b36c9-133">DeleteFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="b36c9-134">说明</span><span class="sxs-lookup"><span data-stu-id="b36c9-134">Description</span></span>

<span data-ttu-id="b36c9-135">下面的示例演示对**DeleteFolder**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="b36c9-135">The following example shows an error response to a **DeleteFolder** request.</span></span> <span data-ttu-id="b36c9-136">删除不存在的邮箱中的文件夹的请求导致出现错误。</span><span class="sxs-lookup"><span data-stu-id="b36c9-136">The error was caused by a request to delete a folder that was not present in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b36c9-137">代码</span><span class="sxs-lookup"><span data-stu-id="b36c9-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="b36c9-138">注释</span><span class="sxs-lookup"><span data-stu-id="b36c9-138">Comments</span></span>

<span data-ttu-id="b36c9-139">**DeleteFolder**操作不能用于可分辨文件夹。</span><span class="sxs-lookup"><span data-stu-id="b36c9-139">The **DeleteFolder** operation cannot be used on distinguished folders.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="b36c9-140">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="b36c9-140">Error response elements</span></span>

<span data-ttu-id="b36c9-141">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b36c9-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="b36c9-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b36c9-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b36c9-143">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="b36c9-143">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="b36c9-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b36c9-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b36c9-145">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b36c9-145">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="b36c9-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="b36c9-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b36c9-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b36c9-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b36c9-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b36c9-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="b36c9-149">若要查找错误响应消息的**DeleteFolder**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="b36c9-149">To find other options for the error response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b36c9-150">启动[DeleteFolderResponse](deletefolderresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b36c9-150">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b36c9-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b36c9-151">See also</span></span>

- [<span data-ttu-id="b36c9-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b36c9-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="b36c9-153">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="b36c9-153">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

