---
title: SyncFolderHierarchy 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: b31916b1-bc6c-4451-a475-b7c5417f752d
description: SyncFolderHierarchy 操作将在运行 Microsoft Exchange Server 2010 的计算机和客户端之间同步文件夹。
ms.openlocfilehash: 1c7ad2413064161ba54e8a7a30bfcd6f23f218bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456428"
---
# <a name="syncfolderhierarchy-operation"></a><span data-ttu-id="459c1-103">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="459c1-103">SyncFolderHierarchy operation</span></span>

<span data-ttu-id="459c1-104">SyncFolderHierarchy 操作将在运行 Microsoft Exchange Server 2010 的计算机和客户端之间同步文件夹。</span><span class="sxs-lookup"><span data-stu-id="459c1-104">The SyncFolderHierarchy operation synchronizes folders between the computer that is running Microsoft Exchange Server 2010 and the client.</span></span>
  
> [!NOTE]
> <span data-ttu-id="459c1-105">当[UnreadCount](unreadcount.md)或[TotalCount](totalcount.md)属性发生更改时，SyncFolderHierarchy 操作不会返回文件夹。</span><span class="sxs-lookup"><span data-stu-id="459c1-105">The SyncFolderHierarchy operation does not return folders when the [UnreadCount](unreadcount.md) or [TotalCount](totalcount.md) properties have changed.</span></span> 
  
## <a name="syncfolderhierarchy-request-example"></a><span data-ttu-id="459c1-106">SyncFolderHierarchy 请求示例</span><span class="sxs-lookup"><span data-stu-id="459c1-106">SyncFolderHierarchy request example</span></span>

### <a name="description"></a><span data-ttu-id="459c1-107">Description</span><span class="sxs-lookup"><span data-stu-id="459c1-107">Description</span></span>

<span data-ttu-id="459c1-108">以下示例的 SyncFolderHierarchy 请求显示如何将客户端文件夹层次结构与 Exchange 服务器同步。</span><span class="sxs-lookup"><span data-stu-id="459c1-108">The following example of a SyncFolderHierarchy request shows how to synchronize a client folder hierarchy with the Exchange server.</span></span> <span data-ttu-id="459c1-109">此示例显示至少已同步一次的文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="459c1-109">This example shows a folder hierarchy that has already been synchronized at least one time.</span></span> <span data-ttu-id="459c1-110">在第一次尝试将客户端与 Exchange 服务器同步时，请求中不包含[SyncState](syncstate-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="459c1-110">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="459c1-111">第一个请求将返回邮箱中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="459c1-111">The first request will return all the folders in the mailbox.</span></span> <span data-ttu-id="459c1-112">[SyncState](syncstate-ex15websvcsotherref.md)元素将在[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)中返回。</span><span class="sxs-lookup"><span data-stu-id="459c1-112">The [SyncState](syncstate-ex15websvcsotherref.md) element will be returned in the [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md).</span></span> <span data-ttu-id="459c1-113">此元素用于同步后续 SyncFolderHierarchy 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="459c1-113">This element is used to synchronize the state for subsequent SyncFolderHierarchy requests.</span></span>
  
### <a name="code"></a><span data-ttu-id="459c1-114">代码</span><span class="sxs-lookup"><span data-stu-id="459c1-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="459c1-115">备注</span><span class="sxs-lookup"><span data-stu-id="459c1-115">Comments</span></span>

<span data-ttu-id="459c1-116">[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="459c1-116">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="459c1-117">Request 元素</span><span class="sxs-lookup"><span data-stu-id="459c1-117">Request elements</span></span>

<span data-ttu-id="459c1-118">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="459c1-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="459c1-119">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="459c1-119">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md)
    
- [<span data-ttu-id="459c1-120">FolderShape</span><span class="sxs-lookup"><span data-stu-id="459c1-120">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="459c1-121">BaseShape</span><span class="sxs-lookup"><span data-stu-id="459c1-121">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="459c1-122">SyncState</span><span class="sxs-lookup"><span data-stu-id="459c1-122">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> <span data-ttu-id="459c1-123">描述这些元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="459c1-123">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-syncfolderhierarchy-response"></a><span data-ttu-id="459c1-124">成功的 SyncFolderHierarchy 响应</span><span class="sxs-lookup"><span data-stu-id="459c1-124">Successful SyncFolderHierarchy Response</span></span>

### <a name="description"></a><span data-ttu-id="459c1-125">Description</span><span class="sxs-lookup"><span data-stu-id="459c1-125">Description</span></span>

<span data-ttu-id="459c1-126">下面的示例演示对 SyncFolderHierarchy 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="459c1-126">The following example shows a successful response to the SyncFolderHierarchy request.</span></span> <span data-ttu-id="459c1-127">在此示例中，已同步一个新文件夹。</span><span class="sxs-lookup"><span data-stu-id="459c1-127">In this example, a new folder has been synchronized.</span></span>
  
### <a name="code"></a><span data-ttu-id="459c1-128">代码</span><span class="sxs-lookup"><span data-stu-id="459c1-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AQApAHR=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQApA=" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>NewFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="459c1-129">备注</span><span class="sxs-lookup"><span data-stu-id="459c1-129">Comments</span></span>

<span data-ttu-id="459c1-130">[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和文件夹标识符数据已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="459c1-130">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the folder identifier data have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="459c1-131">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="459c1-131">Successful response elements</span></span>

<span data-ttu-id="459c1-132">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="459c1-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="459c1-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="459c1-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="459c1-134">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="459c1-134">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="459c1-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="459c1-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="459c1-136">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="459c1-136">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="459c1-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="459c1-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="459c1-138">SyncState</span><span class="sxs-lookup"><span data-stu-id="459c1-138">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="459c1-139">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="459c1-139">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
- [<span data-ttu-id="459c1-140">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="459c1-140">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
    
- [<span data-ttu-id="459c1-141">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="459c1-141">Create (FolderSync)</span></span>](create-foldersync.md)
    
- [<span data-ttu-id="459c1-142">Folder</span><span class="sxs-lookup"><span data-stu-id="459c1-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="459c1-143">FolderId</span><span class="sxs-lookup"><span data-stu-id="459c1-143">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="459c1-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="459c1-144">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="459c1-145">FolderClass</span><span class="sxs-lookup"><span data-stu-id="459c1-145">FolderClass</span></span>](folderclass.md)
    
- [<span data-ttu-id="459c1-146">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="459c1-146">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="459c1-147">TotalCount</span><span class="sxs-lookup"><span data-stu-id="459c1-147">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="459c1-148">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="459c1-148">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="459c1-149">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="459c1-149">UnreadCount</span></span>](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a><span data-ttu-id="459c1-150">SyncFolderHierarchy 错误响应</span><span class="sxs-lookup"><span data-stu-id="459c1-150">SyncFolderHierarchy error response</span></span>

### <a name="description"></a><span data-ttu-id="459c1-151">Description</span><span class="sxs-lookup"><span data-stu-id="459c1-151">Description</span></span>

<span data-ttu-id="459c1-152">下面的示例演示对 SyncFolderHierarchy 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="459c1-152">The following example shows an error response to a SyncFolderHierarchy request.</span></span> <span data-ttu-id="459c1-153">此错误是由无效的 SyncState 所致。</span><span class="sxs-lookup"><span data-stu-id="459c1-153">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="459c1-154">代码</span><span class="sxs-lookup"><span data-stu-id="459c1-154">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupted or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="459c1-155">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="459c1-155">Error response elements</span></span>

<span data-ttu-id="459c1-156">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="459c1-156">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="459c1-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="459c1-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="459c1-158">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="459c1-158">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="459c1-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="459c1-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="459c1-160">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="459c1-160">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="459c1-161">MessageText</span><span class="sxs-lookup"><span data-stu-id="459c1-161">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="459c1-162">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="459c1-162">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="459c1-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="459c1-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="459c1-164">SyncState</span><span class="sxs-lookup"><span data-stu-id="459c1-164">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="459c1-165">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="459c1-165">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
## <a name="see-also"></a><span data-ttu-id="459c1-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="459c1-166">See also</span></span>



- [<span data-ttu-id="459c1-167">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="459c1-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

