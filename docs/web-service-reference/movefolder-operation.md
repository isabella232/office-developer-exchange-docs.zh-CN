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
description: MoveFolder 操作将从指定的文件夹的文件夹，并将其放入另一个文件夹。
ms.openlocfilehash: 5da6929f11ce9ba74db190db6d799f25974d2192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826490"
---
# <a name="movefolder-operation"></a><span data-ttu-id="afb51-103">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="afb51-103">MoveFolder operation</span></span>

<span data-ttu-id="afb51-104">MoveFolder 操作将从指定的文件夹的文件夹，并将其放入另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="afb51-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afb51-105">备注</span><span class="sxs-lookup"><span data-stu-id="afb51-105">Remarks</span></span>

<span data-ttu-id="afb51-106">MoveFolder 操作类似于 CopyFolder 操作。</span><span class="sxs-lookup"><span data-stu-id="afb51-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="afb51-107">不能移动可分辨的文件夹。</span><span class="sxs-lookup"><span data-stu-id="afb51-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="afb51-108">您可以将多个文件夹一次移动到目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="afb51-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="afb51-109">MoveFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="afb51-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="afb51-110">说明</span><span class="sxs-lookup"><span data-stu-id="afb51-110">Description</span></span>

<span data-ttu-id="afb51-111">MoveFolder 请求的下面的示例演示如何以形成移动由[文件夹 Id](folderid.md)标识的文件夹和将文件夹放入垃圾邮件的可分辨文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="afb51-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="afb51-112">代码</span><span class="sxs-lookup"><span data-stu-id="afb51-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="afb51-113">注释</span><span class="sxs-lookup"><span data-stu-id="afb51-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="afb51-114">为便于阅读缩短了[文件夹 Id](folderid.md)元素的 ID 属性的值。</span><span class="sxs-lookup"><span data-stu-id="afb51-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="afb51-115">请求元素</span><span class="sxs-lookup"><span data-stu-id="afb51-115">Request elements</span></span>

<span data-ttu-id="afb51-116">此 MoveFolder 请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="afb51-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="afb51-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="afb51-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="afb51-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="afb51-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="afb51-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="afb51-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="afb51-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="afb51-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="afb51-121">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="afb51-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="afb51-122">请参阅可用于表单 MoveFolder 请求的其他元素的架构。</span><span class="sxs-lookup"><span data-stu-id="afb51-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="afb51-123">架构的默认位置是安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="afb51-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="afb51-124">成功 MoveFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="afb51-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="afb51-125">说明</span><span class="sxs-lookup"><span data-stu-id="afb51-125">Description</span></span>

<span data-ttu-id="afb51-126">下面的示例演示对 MoveFolder 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="afb51-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="afb51-127">代码</span><span class="sxs-lookup"><span data-stu-id="afb51-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="afb51-128">注释</span><span class="sxs-lookup"><span data-stu-id="afb51-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="afb51-129">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="afb51-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="afb51-130">响应中返回文件夹 Id 代表已文件夹移至新的文件夹位置。</span><span class="sxs-lookup"><span data-stu-id="afb51-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="afb51-131">响应元素</span><span class="sxs-lookup"><span data-stu-id="afb51-131">Response elements</span></span>

<span data-ttu-id="afb51-132">MoveFolder 响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="afb51-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="afb51-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="afb51-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="afb51-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="afb51-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="afb51-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="afb51-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="afb51-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="afb51-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="afb51-137">Folders</span><span class="sxs-lookup"><span data-stu-id="afb51-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="afb51-138">Folder</span><span class="sxs-lookup"><span data-stu-id="afb51-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="afb51-139">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="afb51-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="afb51-140">MoveFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="afb51-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="afb51-141">说明</span><span class="sxs-lookup"><span data-stu-id="afb51-141">Description</span></span>

<span data-ttu-id="afb51-142">下面的示例演示当您尝试移动可分辨的文件夹时，发生此事件出现错误响应。</span><span class="sxs-lookup"><span data-stu-id="afb51-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="afb51-143">代码</span><span class="sxs-lookup"><span data-stu-id="afb51-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="afb51-144">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="afb51-144">Error response elements</span></span>

<span data-ttu-id="afb51-145">MoveFolder 错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="afb51-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="afb51-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="afb51-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="afb51-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="afb51-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="afb51-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="afb51-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="afb51-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="afb51-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="afb51-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="afb51-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="afb51-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="afb51-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="afb51-152">文件夹</span><span class="sxs-lookup"><span data-stu-id="afb51-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="afb51-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afb51-153">See also</span></span>



[<span data-ttu-id="afb51-154">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="afb51-154">CopyFolder operation</span></span>](copyfolder-operation.md)

