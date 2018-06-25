---
title: CreateFolder Operation
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
description: CreateFolder 操作创建文件夹、 日历文件夹、 联系人文件夹、 任务文件夹和搜索文件夹。
ms.openlocfilehash: 97156d4a3747cacbdcf9563d21d93a0aa44c3358
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753642"
---
# <a name="createfolder-operation"></a><span data-ttu-id="5a1f5-103">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="5a1f5-103">CreateFolder operation</span></span>

<span data-ttu-id="5a1f5-104">CreateFolder 操作创建文件夹、 日历文件夹、 联系人文件夹、 任务文件夹和搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="5a1f5-105">CreateFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="5a1f5-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="5a1f5-106">说明</span><span class="sxs-lookup"><span data-stu-id="5a1f5-106">Description</span></span>

<span data-ttu-id="5a1f5-107">CreateFolder 请求的下面的示例演示如何以形成邮箱根目录创建两个新文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="5a1f5-108">代码</span><span class="sxs-lookup"><span data-stu-id="5a1f5-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="5a1f5-109">请求元素</span><span class="sxs-lookup"><span data-stu-id="5a1f5-109">Request elements</span></span>

<span data-ttu-id="5a1f5-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5a1f5-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5a1f5-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="5a1f5-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="5a1f5-112">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="5a1f5-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="5a1f5-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5a1f5-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="5a1f5-114">Folders</span><span class="sxs-lookup"><span data-stu-id="5a1f5-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="5a1f5-115">Folder</span><span class="sxs-lookup"><span data-stu-id="5a1f5-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="5a1f5-116">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5a1f5-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="5a1f5-117">介绍这些元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="5a1f5-118">若要查找的请求邮件 CreateFolder 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5a1f5-119">启动[CreateFolder](createfolder.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5a1f5-120">如果使用的**日历： 组织者**属性，可以与限制创建搜索文件夹，后续的 get 文件夹呼叫将返回与限制**消息： 从**所在的位置的属性。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="5a1f5-121">这两个属性映射到的相同的基础 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="5a1f5-122">CreateFolder 操作支持的自定义文件夹类创建仅当您使用的一般文件夹类型元素中创建文件夹并设置**FolderClass**元素。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="5a1f5-123">成功 CreateFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="5a1f5-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="5a1f5-124">说明</span><span class="sxs-lookup"><span data-stu-id="5a1f5-124">Description</span></span>

<span data-ttu-id="5a1f5-125">下面的示例演示对 CreateFolder 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="5a1f5-126">本示例中，响应返回新的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5a1f5-127">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5a1f5-128">代码</span><span class="sxs-lookup"><span data-stu-id="5a1f5-128">Code</span></span>

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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="5a1f5-129">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="5a1f5-129">Successful response elements</span></span>

<span data-ttu-id="5a1f5-130">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5a1f5-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5a1f5-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5a1f5-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5a1f5-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="5a1f5-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="5a1f5-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a1f5-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5a1f5-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a1f5-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="5a1f5-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5a1f5-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5a1f5-136">Folders</span><span class="sxs-lookup"><span data-stu-id="5a1f5-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="5a1f5-137">Folder</span><span class="sxs-lookup"><span data-stu-id="5a1f5-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="5a1f5-138">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="5a1f5-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="5a1f5-139">若要查找的响应消息 CreateFolder 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5a1f5-140">启动[CreateFolderResponse](createfolderresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="5a1f5-141">CreateFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="5a1f5-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="5a1f5-142">说明</span><span class="sxs-lookup"><span data-stu-id="5a1f5-142">Description</span></span>

<span data-ttu-id="5a1f5-143">下面的示例演示对 CreateFolder 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="5a1f5-144">代码</span><span class="sxs-lookup"><span data-stu-id="5a1f5-144">Code</span></span>

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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="5a1f5-145">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="5a1f5-145">Error response elements</span></span>

<span data-ttu-id="5a1f5-146">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5a1f5-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5a1f5-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5a1f5-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5a1f5-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="5a1f5-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="5a1f5-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a1f5-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5a1f5-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a1f5-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="5a1f5-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="5a1f5-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5a1f5-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5a1f5-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5a1f5-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5a1f5-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="5a1f5-154">Folders</span><span class="sxs-lookup"><span data-stu-id="5a1f5-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="5a1f5-155">若要查找错误响应消息的 CreateFolder 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5a1f5-156">启动[CreateFolderResponse](createfolderresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5a1f5-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a1f5-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5a1f5-157">See also</span></span>



[<span data-ttu-id="5a1f5-158">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="5a1f5-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="5a1f5-159">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="5a1f5-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="5a1f5-160">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="5a1f5-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="5a1f5-161">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5a1f5-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5a1f5-162">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="5a1f5-162">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

