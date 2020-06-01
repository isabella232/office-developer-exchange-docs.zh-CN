---
title: CreateFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: CreateFolder 操作将创建文件夹、日历文件夹、联系人文件夹、任务文件夹和搜索文件夹。
ms.openlocfilehash: 125a6d212e5eaf85ace71c048de809f3a05ba9b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457548"
---
# <a name="createfolder-operation"></a><span data-ttu-id="2fe08-103">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2fe08-103">CreateFolder operation</span></span>

<span data-ttu-id="2fe08-104">CreateFolder 操作将创建文件夹、日历文件夹、联系人文件夹、任务文件夹和搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="2fe08-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="2fe08-105">CreateFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="2fe08-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="2fe08-106">说明</span><span class="sxs-lookup"><span data-stu-id="2fe08-106">Description</span></span>

<span data-ttu-id="2fe08-107">以下示例的 CreateFolder 请求显示如何在邮箱根目录中形成创建两个新文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2fe08-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="2fe08-108">代码</span><span class="sxs-lookup"><span data-stu-id="2fe08-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="2fe08-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="2fe08-109">Request elements</span></span>

<span data-ttu-id="2fe08-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fe08-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2fe08-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2fe08-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="2fe08-112">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="2fe08-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="2fe08-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2fe08-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="2fe08-114">Folders</span><span class="sxs-lookup"><span data-stu-id="2fe08-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="2fe08-115">Folder</span><span class="sxs-lookup"><span data-stu-id="2fe08-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="2fe08-116">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="2fe08-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="2fe08-117">描述这些元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2fe08-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="2fe08-118">若要查找 CreateFolder 操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="2fe08-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2fe08-119">从[CreateFolder](createfolder.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="2fe08-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fe08-120">如果使用**calendar：管理器**属性创建具有限制的搜索文件夹，后续的 get 文件夹调用将返回限制，并显示邮件的位置 **： from**属性。</span><span class="sxs-lookup"><span data-stu-id="2fe08-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="2fe08-121">这两个属性映射到相同的基础 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="2fe08-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="2fe08-122">仅当使用通用文件夹 type 元素创建文件夹并设置**FolderClass**元素时，CreateFolder 操作才支持创建自定义文件夹类。</span><span class="sxs-lookup"><span data-stu-id="2fe08-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="2fe08-123">成功的 CreateFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="2fe08-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="2fe08-124">说明</span><span class="sxs-lookup"><span data-stu-id="2fe08-124">Description</span></span>

<span data-ttu-id="2fe08-125">下面的示例演示对 CreateFolder 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="2fe08-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="2fe08-126">在此示例中，响应返回新文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="2fe08-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2fe08-127">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="2fe08-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2fe08-128">代码</span><span class="sxs-lookup"><span data-stu-id="2fe08-128">Code</span></span>

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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="2fe08-129">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="2fe08-129">Successful response elements</span></span>

<span data-ttu-id="2fe08-130">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fe08-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2fe08-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2fe08-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2fe08-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2fe08-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="2fe08-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2fe08-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2fe08-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2fe08-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="2fe08-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2fe08-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2fe08-136">Folders</span><span class="sxs-lookup"><span data-stu-id="2fe08-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="2fe08-137">Folder</span><span class="sxs-lookup"><span data-stu-id="2fe08-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="2fe08-138">FolderId</span><span class="sxs-lookup"><span data-stu-id="2fe08-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="2fe08-139">若要查找 CreateFolder 操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="2fe08-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2fe08-140">从[CreateFolderResponse](createfolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="2fe08-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="2fe08-141">CreateFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="2fe08-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="2fe08-142">说明</span><span class="sxs-lookup"><span data-stu-id="2fe08-142">Description</span></span>

<span data-ttu-id="2fe08-143">下面的示例演示对 CreateFolder 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="2fe08-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="2fe08-144">代码</span><span class="sxs-lookup"><span data-stu-id="2fe08-144">Code</span></span>

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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="2fe08-145">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="2fe08-145">Error response elements</span></span>

<span data-ttu-id="2fe08-146">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fe08-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="2fe08-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2fe08-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2fe08-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2fe08-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="2fe08-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2fe08-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2fe08-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2fe08-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="2fe08-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="2fe08-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2fe08-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2fe08-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2fe08-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2fe08-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="2fe08-154">Folders</span><span class="sxs-lookup"><span data-stu-id="2fe08-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="2fe08-155">若要查找 CreateFolder 操作的错误响应消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="2fe08-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2fe08-156">从[CreateFolderResponse](createfolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="2fe08-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fe08-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2fe08-157">See also</span></span>



[<span data-ttu-id="2fe08-158">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="2fe08-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="2fe08-159">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2fe08-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="2fe08-160">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="2fe08-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="2fe08-161">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2fe08-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2fe08-162">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="2fe08-162">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

