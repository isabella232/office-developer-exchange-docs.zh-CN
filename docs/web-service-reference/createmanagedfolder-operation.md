---
title: CreateManagedFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: CreateManagedFolder 操作在 Exchange 存储中创建一个托管文件夹。
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44444591"
---
# <a name="createmanagedfolder-operation"></a><span data-ttu-id="0529f-103">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0529f-103">CreateManagedFolder operation</span></span>

<span data-ttu-id="0529f-104">CreateManagedFolder 操作在 Exchange 存储中创建一个托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-104">The CreateManagedFolder operation creates a managed folder in the Exchange store.</span></span>
  
## <a name="using-the-createmanagedfolder-operation"></a><span data-ttu-id="0529f-105">使用 CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0529f-105">Using the CreateManagedFolder Operation</span></span>

<span data-ttu-id="0529f-106">CreateManagedFolder 操作将托管自定义文件夹添加到用户的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="0529f-106">The CreateManagedFolder operation adds a managed custom folder to a user's mailbox.</span></span> <span data-ttu-id="0529f-107">您可以使用 Exchange 命令行管理程序**get-managedfolder** cmdlet 查找要添加的可用托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-107">You can use the Exchange Management Shell **Get-ManagedFolder** cmdlet to find available managed folders to add.</span></span> <span data-ttu-id="0529f-108">虽然此 cmdlet 返回托管自定义文件夹和托管默认文件夹，但只能添加托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-108">Although this cmdlet returns both managed custom folders and managed default folders, only managed custom folders can be added.</span></span> <span data-ttu-id="0529f-109">托管自定义文件夹由 ManagedCustomFolder 文件夹类型标识。</span><span class="sxs-lookup"><span data-stu-id="0529f-109">Managed custom folders are identified by the ManagedCustomFolder folder type.</span></span> <span data-ttu-id="0529f-110">System.directoryservices 命名空间还包含可用于发现可用托管文件夹的名称的类型。</span><span class="sxs-lookup"><span data-stu-id="0529f-110">The System.DirectoryServices namespace also includes types that can be used to discover the names of available managed folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0529f-111">您不能使用 Exchange Web 服务查找要添加到邮箱中的可用托管文件夹的名称。</span><span class="sxs-lookup"><span data-stu-id="0529f-111">You cannot use Exchange Web Services to find the names of available managed folders to add to a mailbox.</span></span> 
  
<span data-ttu-id="0529f-112">您可以使用 FindFolder 和 GetFolder 操作来访问托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-112">You can use the FindFolder and GetFolder operations to access managed folders.</span></span> <span data-ttu-id="0529f-113">FindFolder 用于搜索指定父文件夹中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-113">FindFolder is used to search for folders in a specified parent folder.</span></span> <span data-ttu-id="0529f-114">可以使用此操作，以便在尝试将重复的托管自定义文件夹添加到同一目录中之前，可以在文件夹中发现托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-114">This can be used so that managed folders can be discovered in a folder before trying to add a duplicate managed custom folder to the same directory.</span></span> <span data-ttu-id="0529f-115">GetFolder 在 FindFolder 操作之后使用，以获取有关托管自定义文件夹的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0529f-115">GetFolder is used after the FindFolder operation to get more information about a managed custom folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0529f-116">备注</span><span class="sxs-lookup"><span data-stu-id="0529f-116">Remarks</span></span>

<span data-ttu-id="0529f-117">有关如何设置邮件记录管理（MRM）策略的信息，请参阅[如何创建托管文件夹邮箱策略](https://go.microsoft.com/fwlink/?LinkId=100975)。</span><span class="sxs-lookup"><span data-stu-id="0529f-117">For information about how to set up messaging records management (MRM) policy, see [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).</span></span>
  
<span data-ttu-id="0529f-118">有关如何从邮箱中删除托管自定义文件夹的信息，请参阅[get-managedfolder](https://go.microsoft.com/fwlink/?LinkId=100976)。</span><span class="sxs-lookup"><span data-stu-id="0529f-118">For information about how to remove managed custom folders from a mailbox, see [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).</span></span>
  
## <a name="createmanagedfolder-request-example"></a><span data-ttu-id="0529f-119">CreateManagedFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="0529f-119">CreateManagedFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="0529f-120">Description</span><span class="sxs-lookup"><span data-stu-id="0529f-120">Description</span></span>

<span data-ttu-id="0529f-121">以下示例的 CreateManagedFolder 请求显示如何将名为 Test Managed Folder 的托管文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="0529f-121">The following example of a CreateManagedFolder request shows how to add a managed folder named Test Managed Folder to a mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0529f-122">您还可以使用代理访问来添加托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="0529f-122">You can also use delegate access to add managed custom folders.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0529f-123">代码</span><span class="sxs-lookup"><span data-stu-id="0529f-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="0529f-124">Request 元素</span><span class="sxs-lookup"><span data-stu-id="0529f-124">Request elements</span></span>

<span data-ttu-id="0529f-125">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0529f-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0529f-126">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="0529f-126">CreateManagedFolder</span></span>](createmanagedfolder.md)
    
- [<span data-ttu-id="0529f-127">FolderNames</span><span class="sxs-lookup"><span data-stu-id="0529f-127">FolderNames</span></span>](foldernames.md)
    
- [<span data-ttu-id="0529f-128">FolderName</span><span class="sxs-lookup"><span data-stu-id="0529f-128">FolderName</span></span>](foldername.md)
    
<span data-ttu-id="0529f-129">若要查找 CreateManagedFolder 操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="0529f-129">To find other options for the request message of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="0529f-130">从[CreateManagedFolder](createmanagedfolder.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="0529f-130">Start at the [CreateManagedFolder](createmanagedfolder.md) element.</span></span> 
  
## <a name="successful-createmanagedfolder-response"></a><span data-ttu-id="0529f-131">成功的 CreateManagedFolder 响应</span><span class="sxs-lookup"><span data-stu-id="0529f-131">Successful CreateManagedFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="0529f-132">Description</span><span class="sxs-lookup"><span data-stu-id="0529f-132">Description</span></span>

<span data-ttu-id="0529f-133">下面的代码示例演示对 CreateManagedFolder 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="0529f-133">The following code example shows a successful response to a CreateManagedFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0529f-134">为了保持可读性， **Id**和**ChangeKey**属性值已缩短。</span><span class="sxs-lookup"><span data-stu-id="0529f-134">The **Id** and **ChangeKey** attribute values have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0529f-135">代码</span><span class="sxs-lookup"><span data-stu-id="0529f-135">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="0529f-136">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="0529f-136">Successful response elements</span></span>

<span data-ttu-id="0529f-137">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0529f-137">The following elements are used in the response:</span></span> 
  
- [<span data-ttu-id="0529f-138">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0529f-138">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="0529f-139">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0529f-139">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0529f-140">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0529f-140">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="0529f-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0529f-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0529f-142">Folders</span><span class="sxs-lookup"><span data-stu-id="0529f-142">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0529f-143">Folder</span><span class="sxs-lookup"><span data-stu-id="0529f-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="0529f-144">FolderId</span><span class="sxs-lookup"><span data-stu-id="0529f-144">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="0529f-145">若要查找 CreateManagedFolder 操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="0529f-145">To find other options for the response messages of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="0529f-146">从[CreateManagedFolderResponse](createmanagedfolderresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="0529f-146">Start at the [CreateManagedFolderResponse](createmanagedfolderresponse.md) element.</span></span> 
  
## <a name="createmanagedfolder-error-response"></a><span data-ttu-id="0529f-147">CreateManagedFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="0529f-147">CreateManagedFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="0529f-148">Description</span><span class="sxs-lookup"><span data-stu-id="0529f-148">Description</span></span>

<span data-ttu-id="0529f-149">下面的代码示例演示对 CreateManagedFolder 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="0529f-149">The following code example shows an error response to a CreateManagedFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0529f-150">代码</span><span class="sxs-lookup"><span data-stu-id="0529f-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="0529f-151">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0529f-151">Error response elements</span></span>

<span data-ttu-id="0529f-152">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0529f-152">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0529f-153">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0529f-153">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="0529f-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0529f-154">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0529f-155">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0529f-155">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="0529f-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="0529f-156">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0529f-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0529f-157">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0529f-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0529f-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0529f-159">Folders</span><span class="sxs-lookup"><span data-stu-id="0529f-159">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="0529f-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0529f-160">See also</span></span>



[<span data-ttu-id="0529f-161">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0529f-161">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="0529f-162">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0529f-162">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="0529f-163">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="0529f-163">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="0529f-164">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="0529f-164">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

