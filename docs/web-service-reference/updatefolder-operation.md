---
title: UpdateFolder Operation
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
description: UpdateFolder 操作用于修改 Exchange 存储中现有项目的属性。 每个 UpdateFolder 操作由以下内容组成：
ms.openlocfilehash: b33937bb09f0dcbe3d3ed61bbf5233423f320d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838372"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="646b1-104">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="646b1-104">UpdateFolder operation</span></span>

<span data-ttu-id="646b1-105">UpdateFolder 操作用于修改 Exchange 存储中现有项目的属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="646b1-106">每个 UpdateFolder 操作由以下内容组成：</span><span class="sxs-lookup"><span data-stu-id="646b1-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="646b1-107">指定要更新的文件夹的[文件夹 Id](folderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="646b1-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="646b1-108">在文件夹中，指定该文件夹形状，它指定要更新的数据元素的内部路径。</span><span class="sxs-lookup"><span data-stu-id="646b1-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="646b1-109">包含新值更新字段中，如果更新不删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="646b1-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="646b1-110">注解</span><span class="sxs-lookup"><span data-stu-id="646b1-110">Remarks</span></span>

<span data-ttu-id="646b1-111">可对项目执行三个基本 update 操作。</span><span class="sxs-lookup"><span data-stu-id="646b1-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="646b1-112">下表列出了这些操作。</span><span class="sxs-lookup"><span data-stu-id="646b1-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="646b1-113">**操作**</span><span class="sxs-lookup"><span data-stu-id="646b1-113">**Action**</span></span>|<span data-ttu-id="646b1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="646b1-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="646b1-115">追加</span><span class="sxs-lookup"><span data-stu-id="646b1-115">Append</span></span>  <br/> |<span data-ttu-id="646b1-116">Append 操作将数据添加到现有属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="646b1-117">它保留了当前存在的数据。</span><span class="sxs-lookup"><span data-stu-id="646b1-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="646b1-118">追加不适用于所有属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="646b1-119">设置</span><span class="sxs-lookup"><span data-stu-id="646b1-119">Set</span></span>  <br/> |<span data-ttu-id="646b1-120">如果它包含的数据，或创建属性并设置其值，如果它不存在，则设置操作将替换属性的数据。</span><span class="sxs-lookup"><span data-stu-id="646b1-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="646b1-121">设置操作仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="646b1-122">Delete</span><span class="sxs-lookup"><span data-stu-id="646b1-122">Delete</span></span>  <br/> |<span data-ttu-id="646b1-123">删除操作从文件夹中删除属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="646b1-124">这是不同于设置为空值。</span><span class="sxs-lookup"><span data-stu-id="646b1-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="646b1-125">完成后，该属性不存在的文件夹。</span><span class="sxs-lookup"><span data-stu-id="646b1-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="646b1-126">删除才适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="646b1-127">UpdateFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="646b1-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="646b1-128">说明</span><span class="sxs-lookup"><span data-stu-id="646b1-128">Description</span></span>

<span data-ttu-id="646b1-129">UpdateFolder 请求的下面的示例演示如何更新文件夹显示名称。</span><span class="sxs-lookup"><span data-stu-id="646b1-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="646b1-130">代码</span><span class="sxs-lookup"><span data-stu-id="646b1-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="646b1-131">注释</span><span class="sxs-lookup"><span data-stu-id="646b1-131">Comments</span></span>

<span data-ttu-id="646b1-132">此示例更改为 NewFolderName 文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="646b1-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="646b1-133">为便于阅读，具有已缩短的**Id**值和[文件夹 Id](folderid.md)元素的**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="646b1-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="646b1-134">请求元素</span><span class="sxs-lookup"><span data-stu-id="646b1-134">Request elements</span></span>

<span data-ttu-id="646b1-135">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="646b1-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="646b1-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="646b1-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="646b1-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="646b1-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="646b1-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="646b1-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="646b1-139">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="646b1-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="646b1-140">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="646b1-140">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="646b1-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="646b1-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="646b1-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="646b1-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="646b1-143">Folder</span><span class="sxs-lookup"><span data-stu-id="646b1-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="646b1-144">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="646b1-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="646b1-145">请参阅可用于窗体的 UpdateFolder 请求的其他元素的架构。</span><span class="sxs-lookup"><span data-stu-id="646b1-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="646b1-146">架构的默认位置是安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="646b1-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="646b1-147">UpdateFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="646b1-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="646b1-148">说明</span><span class="sxs-lookup"><span data-stu-id="646b1-148">Description</span></span>

<span data-ttu-id="646b1-149">下面的示例演示对 UpdateFolder 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="646b1-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="646b1-150">本示例中，新的更改密钥返回以反映更新的状态的文件夹。</span><span class="sxs-lookup"><span data-stu-id="646b1-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="646b1-151">代码</span><span class="sxs-lookup"><span data-stu-id="646b1-151">Code</span></span>

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
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="646b1-152">注释</span><span class="sxs-lookup"><span data-stu-id="646b1-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="646b1-153">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="646b1-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="646b1-154">响应中返回的文件夹 ID 表示已更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="646b1-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="646b1-155">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="646b1-155">Successful response elements</span></span>

<span data-ttu-id="646b1-156">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="646b1-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="646b1-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="646b1-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="646b1-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="646b1-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="646b1-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="646b1-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="646b1-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="646b1-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="646b1-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="646b1-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="646b1-162">Folders</span><span class="sxs-lookup"><span data-stu-id="646b1-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="646b1-163">Folder</span><span class="sxs-lookup"><span data-stu-id="646b1-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="646b1-164">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="646b1-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="646b1-165">UpdateFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="646b1-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="646b1-166">说明</span><span class="sxs-lookup"><span data-stu-id="646b1-166">Description</span></span>

<span data-ttu-id="646b1-167">下面的示例演示 UpdateFolder 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="646b1-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="646b1-168">代码</span><span class="sxs-lookup"><span data-stu-id="646b1-168">Code</span></span>

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
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="646b1-169">注释</span><span class="sxs-lookup"><span data-stu-id="646b1-169">Comments</span></span>

<span data-ttu-id="646b1-170">本示例显示错误响应导致的请求中的**更改密钥**属性无效。</span><span class="sxs-lookup"><span data-stu-id="646b1-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="646b1-171">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="646b1-171">Error response elements</span></span>

<span data-ttu-id="646b1-172">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="646b1-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="646b1-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="646b1-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="646b1-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="646b1-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="646b1-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="646b1-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="646b1-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="646b1-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="646b1-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="646b1-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="646b1-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="646b1-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="646b1-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="646b1-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="646b1-180">文件夹</span><span class="sxs-lookup"><span data-stu-id="646b1-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="646b1-181">另请参阅</span><span class="sxs-lookup"><span data-stu-id="646b1-181">See also</span></span>



- [<span data-ttu-id="646b1-182">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="646b1-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

