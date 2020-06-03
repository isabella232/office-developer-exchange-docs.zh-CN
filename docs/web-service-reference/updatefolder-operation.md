---
title: UpdateFolder 操作
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: UpdateFolder 操作用于修改 Exchange 存储中现有项的属性。 每个 UpdateFolder 操作都包含以下内容：
ms.openlocfilehash: fb894d9f42358b67f81e9fe8ae41ba61e6f46460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467359"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="451b8-104">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="451b8-104">UpdateFolder operation</span></span>

<span data-ttu-id="451b8-105">UpdateFolder 操作用于修改 Exchange 存储中现有项的属性。</span><span class="sxs-lookup"><span data-stu-id="451b8-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="451b8-106">每个 UpdateFolder 操作都包含以下内容：</span><span class="sxs-lookup"><span data-stu-id="451b8-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="451b8-107">一个[FolderId](folderid.md)元素，指定要更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="451b8-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="451b8-108">文件夹中元素的内部路径，由 folder 形状指定，该路径指定要更新的数据。</span><span class="sxs-lookup"><span data-stu-id="451b8-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="451b8-109">包含更新的域的新值的文件夹（如果更新不是删除）。</span><span class="sxs-lookup"><span data-stu-id="451b8-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="451b8-110">备注</span><span class="sxs-lookup"><span data-stu-id="451b8-110">Remarks</span></span>

<span data-ttu-id="451b8-111">可以对项目执行三个基本的更新操作。</span><span class="sxs-lookup"><span data-stu-id="451b8-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="451b8-112">下表中列出了这些操作。</span><span class="sxs-lookup"><span data-stu-id="451b8-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="451b8-113">**操作**</span><span class="sxs-lookup"><span data-stu-id="451b8-113">**Action**</span></span>|<span data-ttu-id="451b8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="451b8-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="451b8-115">Append</span><span class="sxs-lookup"><span data-stu-id="451b8-115">Append</span></span>  <br/> |<span data-ttu-id="451b8-116">Append 操作将数据添加到现有属性中。</span><span class="sxs-lookup"><span data-stu-id="451b8-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="451b8-117">它保留当前在其中的数据。</span><span class="sxs-lookup"><span data-stu-id="451b8-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="451b8-118">Append 不适用于所有属性。</span><span class="sxs-lookup"><span data-stu-id="451b8-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="451b8-119">Set</span><span class="sxs-lookup"><span data-stu-id="451b8-119">Set</span></span>  <br/> |<span data-ttu-id="451b8-120">如果属性包含数据，则 set 操作将替换该属性的数据，或者创建该属性并设置其值（如果不存在）。</span><span class="sxs-lookup"><span data-stu-id="451b8-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="451b8-121">Set 操作仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="451b8-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="451b8-122">Delete</span><span class="sxs-lookup"><span data-stu-id="451b8-122">Delete</span></span>  <br/> |<span data-ttu-id="451b8-123">"删除" 操作从文件夹中删除属性。</span><span class="sxs-lookup"><span data-stu-id="451b8-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="451b8-124">这与将其设置为空值不同。</span><span class="sxs-lookup"><span data-stu-id="451b8-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="451b8-125">完成后，该文件夹的属性不存在。</span><span class="sxs-lookup"><span data-stu-id="451b8-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="451b8-126">删除仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="451b8-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="451b8-127">UpdateFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="451b8-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="451b8-128">Description</span><span class="sxs-lookup"><span data-stu-id="451b8-128">Description</span></span>

<span data-ttu-id="451b8-129">以下示例的 UpdateFolder 请求显示如何更新文件夹显示名称。</span><span class="sxs-lookup"><span data-stu-id="451b8-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="451b8-130">代码</span><span class="sxs-lookup"><span data-stu-id="451b8-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AScA" ChangeKey="GO3u/"/>
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName"/>
              <t:Folder>
                <t:DisplayName>NewFolderName</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </FolderChanges>
    </UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="451b8-131">备注</span><span class="sxs-lookup"><span data-stu-id="451b8-131">Comments</span></span>

<span data-ttu-id="451b8-132">本示例将文件夹的显示名称更改为 NewFolderName。</span><span class="sxs-lookup"><span data-stu-id="451b8-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="451b8-133">为了提高可读性， [FolderId](folderid.md)元素的**Id**和**ChangeKey**属性的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="451b8-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="451b8-134">Request 元素</span><span class="sxs-lookup"><span data-stu-id="451b8-134">Request elements</span></span>

<span data-ttu-id="451b8-135">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="451b8-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="451b8-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="451b8-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="451b8-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="451b8-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="451b8-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="451b8-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="451b8-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="451b8-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="451b8-140">Updates 文件夹</span><span class="sxs-lookup"><span data-stu-id="451b8-140">Updates (Folder)</span></span>](updates-folder.md)
    
- [<span data-ttu-id="451b8-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="451b8-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="451b8-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="451b8-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="451b8-143">Folder</span><span class="sxs-lookup"><span data-stu-id="451b8-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="451b8-144">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="451b8-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="451b8-145">有关可用于形成 UpdateFolder 请求的其他元素，请参阅架构。</span><span class="sxs-lookup"><span data-stu-id="451b8-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="451b8-146">架构的默认位置在安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="451b8-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="451b8-147">UpdateFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="451b8-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="451b8-148">Description</span><span class="sxs-lookup"><span data-stu-id="451b8-148">Description</span></span>

<span data-ttu-id="451b8-149">下面的示例演示对 UpdateFolder 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="451b8-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="451b8-150">在此示例中，将返回新的更改密钥，以反映该文件夹的更新状态。</span><span class="sxs-lookup"><span data-stu-id="451b8-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="451b8-151">代码</span><span class="sxs-lookup"><span data-stu-id="451b8-151">Code</span></span>

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
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFVz" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="451b8-152">备注</span><span class="sxs-lookup"><span data-stu-id="451b8-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="451b8-153">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="451b8-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="451b8-154">响应中返回的文件夹 ID 表示更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="451b8-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="451b8-155">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="451b8-155">Successful response elements</span></span>

<span data-ttu-id="451b8-156">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="451b8-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="451b8-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="451b8-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="451b8-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="451b8-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="451b8-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="451b8-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="451b8-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="451b8-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="451b8-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="451b8-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="451b8-162">Folders</span><span class="sxs-lookup"><span data-stu-id="451b8-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="451b8-163">Folder</span><span class="sxs-lookup"><span data-stu-id="451b8-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="451b8-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="451b8-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="451b8-165">UpdateFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="451b8-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="451b8-166">Description</span><span class="sxs-lookup"><span data-stu-id="451b8-166">Description</span></span>

<span data-ttu-id="451b8-167">下面的示例演示对 UpdateFolder 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="451b8-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="451b8-168">代码</span><span class="sxs-lookup"><span data-stu-id="451b8-168">Code</span></span>

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
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="451b8-169">备注</span><span class="sxs-lookup"><span data-stu-id="451b8-169">Comments</span></span>

<span data-ttu-id="451b8-170">此示例显示了由请求中的无效**ChangeKey**属性导致的错误响应。</span><span class="sxs-lookup"><span data-stu-id="451b8-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="451b8-171">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="451b8-171">Error response elements</span></span>

<span data-ttu-id="451b8-172">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="451b8-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="451b8-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="451b8-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="451b8-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="451b8-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="451b8-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="451b8-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="451b8-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="451b8-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="451b8-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="451b8-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="451b8-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="451b8-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="451b8-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="451b8-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="451b8-180">Folders</span><span class="sxs-lookup"><span data-stu-id="451b8-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="451b8-181">另请参阅</span><span class="sxs-lookup"><span data-stu-id="451b8-181">See also</span></span>



- [<span data-ttu-id="451b8-182">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="451b8-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

