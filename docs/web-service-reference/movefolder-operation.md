---
title: MoveFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: MoveFolder 操作将文件夹从指定文件夹移动，并将其放在另一个文件夹中。
ms.openlocfilehash: dc572130ca3b2f2b152abbb4a8b68cc6f67790e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460580"
---
# <a name="movefolder-operation"></a><span data-ttu-id="9d204-103">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9d204-103">MoveFolder operation</span></span>

<span data-ttu-id="9d204-104">MoveFolder 操作将文件夹从指定文件夹移动，并将其放在另一个文件夹中。</span><span class="sxs-lookup"><span data-stu-id="9d204-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d204-105">备注</span><span class="sxs-lookup"><span data-stu-id="9d204-105">Remarks</span></span>

<span data-ttu-id="9d204-106">MoveFolder 操作类似于 CopyFolder 操作。</span><span class="sxs-lookup"><span data-stu-id="9d204-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="9d204-107">无法移动可分辨文件夹。</span><span class="sxs-lookup"><span data-stu-id="9d204-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="9d204-108">您可以一次将多个文件夹移动到目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="9d204-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="9d204-109">MoveFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="9d204-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="9d204-110">说明</span><span class="sxs-lookup"><span data-stu-id="9d204-110">Description</span></span>

<span data-ttu-id="9d204-111">以下示例的 MoveFolder 请求显示如何形成一个请求，以移动[FolderId](folderid.md)标识的文件夹，并将该文件夹放在 "垃圾邮件" 可分辨文件夹中。</span><span class="sxs-lookup"><span data-stu-id="9d204-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9d204-112">代码</span><span class="sxs-lookup"><span data-stu-id="9d204-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9d204-113">备注</span><span class="sxs-lookup"><span data-stu-id="9d204-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="9d204-114">为了提高可读性， [FolderId](folderid.md)元素的 ID 属性值已缩短。</span><span class="sxs-lookup"><span data-stu-id="9d204-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="9d204-115">Request 元素</span><span class="sxs-lookup"><span data-stu-id="9d204-115">Request elements</span></span>

<span data-ttu-id="9d204-116">此 MoveFolder 请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="9d204-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="9d204-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="9d204-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="9d204-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="9d204-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="9d204-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9d204-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="9d204-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="9d204-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="9d204-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="9d204-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="9d204-122">有关可用于形成 MoveFolder 请求的其他元素，请参阅架构。</span><span class="sxs-lookup"><span data-stu-id="9d204-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9d204-123">架构的默认位置在安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9d204-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="9d204-124">成功的 MoveFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="9d204-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="9d204-125">说明</span><span class="sxs-lookup"><span data-stu-id="9d204-125">Description</span></span>

<span data-ttu-id="9d204-126">下面的示例演示对 MoveFolder 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="9d204-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9d204-127">代码</span><span class="sxs-lookup"><span data-stu-id="9d204-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9d204-128">备注</span><span class="sxs-lookup"><span data-stu-id="9d204-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="9d204-129">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="9d204-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="9d204-130">响应中返回的 FolderId 表示移动到新文件夹位置的文件夹。</span><span class="sxs-lookup"><span data-stu-id="9d204-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="9d204-131">Response 元素</span><span class="sxs-lookup"><span data-stu-id="9d204-131">Response elements</span></span>

<span data-ttu-id="9d204-132">MoveFolder 响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="9d204-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="9d204-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9d204-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="9d204-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9d204-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9d204-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9d204-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="9d204-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9d204-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9d204-137">Folders</span><span class="sxs-lookup"><span data-stu-id="9d204-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9d204-138">Folder</span><span class="sxs-lookup"><span data-stu-id="9d204-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="9d204-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="9d204-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="9d204-140">MoveFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="9d204-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="9d204-141">说明</span><span class="sxs-lookup"><span data-stu-id="9d204-141">Description</span></span>

<span data-ttu-id="9d204-142">下面的示例演示在尝试移动可分辨文件夹时发生的错误响应。</span><span class="sxs-lookup"><span data-stu-id="9d204-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="9d204-143">代码</span><span class="sxs-lookup"><span data-stu-id="9d204-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="9d204-144">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="9d204-144">Error response elements</span></span>

<span data-ttu-id="9d204-145">MoveFolder 错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="9d204-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="9d204-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9d204-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="9d204-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9d204-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9d204-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9d204-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="9d204-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="9d204-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9d204-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9d204-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9d204-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9d204-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9d204-152">Folders</span><span class="sxs-lookup"><span data-stu-id="9d204-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="9d204-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9d204-153">See also</span></span>



[<span data-ttu-id="9d204-154">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9d204-154">CopyFolder operation</span></span>](copyfolder-operation.md)

