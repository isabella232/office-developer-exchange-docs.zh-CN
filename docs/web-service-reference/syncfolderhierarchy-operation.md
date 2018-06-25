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
description: SyncFolderHierarchy 操作将同步的计算机的运行 Microsoft Exchange Server 2010 和客户端之间的文件夹。
ms.openlocfilehash: 33c886d5eec64a9ff2ccc667eedfc2d4cc8dcfd5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838169"
---
# <a name="syncfolderhierarchy-operation"></a><span data-ttu-id="6a954-103">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="6a954-103">SyncFolderHierarchy operation</span></span>

<span data-ttu-id="6a954-104">SyncFolderHierarchy 操作将同步的计算机的运行 Microsoft Exchange Server 2010 和客户端之间的文件夹。</span><span class="sxs-lookup"><span data-stu-id="6a954-104">The SyncFolderHierarchy operation synchronizes folders between the computer that is running Microsoft Exchange Server 2010 and the client.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6a954-105">SyncFolderHierarchy 操作不返回文件夹时的[UnreadCount](unreadcount.md)或[TotalCount](totalcount.md)属性已更改。</span><span class="sxs-lookup"><span data-stu-id="6a954-105">The SyncFolderHierarchy operation does not return folders when the [UnreadCount](unreadcount.md) or [TotalCount](totalcount.md) properties have changed.</span></span> 
  
## <a name="syncfolderhierarchy-request-example"></a><span data-ttu-id="6a954-106">SyncFolderHierarchy 请求示例</span><span class="sxs-lookup"><span data-stu-id="6a954-106">SyncFolderHierarchy request example</span></span>

### <a name="description"></a><span data-ttu-id="6a954-107">说明</span><span class="sxs-lookup"><span data-stu-id="6a954-107">Description</span></span>

<span data-ttu-id="6a954-108">SyncFolderHierarchy 请求的下面的示例演示如何同步客户端与 Exchange server 的文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a954-108">The following example of a SyncFolderHierarchy request shows how to synchronize a client folder hierarchy with the Exchange server.</span></span> <span data-ttu-id="6a954-109">本示例显示了已完成同步至少一次文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a954-109">This example shows a folder hierarchy that has already been synchronized at least one time.</span></span> <span data-ttu-id="6a954-110">首次尝试与 Exchange server 同步客户端的请求中不包括[SyncState](syncstate-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="6a954-110">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="6a954-111">第一个请求将返回的邮箱中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="6a954-111">The first request will return all the folders in the mailbox.</span></span> <span data-ttu-id="6a954-112">将在[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)返回[SyncState](syncstate-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="6a954-112">The [SyncState](syncstate-ex15websvcsotherref.md) element will be returned in the [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md).</span></span> <span data-ttu-id="6a954-113">此元素用于同步后续 SyncFolderHierarchy 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="6a954-113">This element is used to synchronize the state for subsequent SyncFolderHierarchy requests.</span></span>
  
### <a name="code"></a><span data-ttu-id="6a954-114">代码</span><span class="sxs-lookup"><span data-stu-id="6a954-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6a954-115">注释</span><span class="sxs-lookup"><span data-stu-id="6a954-115">Comments</span></span>

<span data-ttu-id="6a954-116">已缩短[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="6a954-116">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="6a954-117">请求元素</span><span class="sxs-lookup"><span data-stu-id="6a954-117">Request elements</span></span>

<span data-ttu-id="6a954-118">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a954-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6a954-119">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="6a954-119">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md)
    
- [<span data-ttu-id="6a954-120">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6a954-120">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="6a954-121">BaseShape</span><span class="sxs-lookup"><span data-stu-id="6a954-121">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="6a954-122">SyncState</span><span class="sxs-lookup"><span data-stu-id="6a954-122">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> <span data-ttu-id="6a954-123">介绍这些元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6a954-123">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-syncfolderhierarchy-response"></a><span data-ttu-id="6a954-124">成功的 SyncFolderHierarchy 响应</span><span class="sxs-lookup"><span data-stu-id="6a954-124">Successful SyncFolderHierarchy Response</span></span>

### <a name="description"></a><span data-ttu-id="6a954-125">说明</span><span class="sxs-lookup"><span data-stu-id="6a954-125">Description</span></span>

<span data-ttu-id="6a954-126">下面的示例演示对 SyncFolderHierarchy 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="6a954-126">The following example shows a successful response to the SyncFolderHierarchy request.</span></span> <span data-ttu-id="6a954-127">本示例中，已同步的新文件夹。</span><span class="sxs-lookup"><span data-stu-id="6a954-127">In this example, a new folder has been synchronized.</span></span>
  
### <a name="code"></a><span data-ttu-id="6a954-128">代码</span><span class="sxs-lookup"><span data-stu-id="6a954-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6a954-129">注释</span><span class="sxs-lookup"><span data-stu-id="6a954-129">Comments</span></span>

<span data-ttu-id="6a954-130">已缩短[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和文件夹标识符数据，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="6a954-130">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the folder identifier data have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="6a954-131">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="6a954-131">Successful response elements</span></span>

<span data-ttu-id="6a954-132">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a954-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="6a954-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6a954-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6a954-134">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="6a954-134">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="6a954-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6a954-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6a954-136">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6a954-136">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="6a954-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6a954-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6a954-138">SyncState</span><span class="sxs-lookup"><span data-stu-id="6a954-138">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6a954-139">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="6a954-139">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
- [<span data-ttu-id="6a954-140">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="6a954-140">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
    
- [<span data-ttu-id="6a954-141">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="6a954-141">Create (FolderSync)</span></span>](create-foldersync.md)
    
- [<span data-ttu-id="6a954-142">Folder</span><span class="sxs-lookup"><span data-stu-id="6a954-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="6a954-143">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="6a954-143">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="6a954-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="6a954-144">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="6a954-145">FolderClass</span><span class="sxs-lookup"><span data-stu-id="6a954-145">FolderClass</span></span>](folderclass.md)
    
- [<span data-ttu-id="6a954-146">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="6a954-146">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="6a954-147">TotalCount</span><span class="sxs-lookup"><span data-stu-id="6a954-147">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="6a954-148">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="6a954-148">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="6a954-149">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="6a954-149">UnreadCount</span></span>](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a><span data-ttu-id="6a954-150">SyncFolderHierarchy 错误响应</span><span class="sxs-lookup"><span data-stu-id="6a954-150">SyncFolderHierarchy error response</span></span>

### <a name="description"></a><span data-ttu-id="6a954-151">说明</span><span class="sxs-lookup"><span data-stu-id="6a954-151">Description</span></span>

<span data-ttu-id="6a954-152">下面的示例演示对 SyncFolderHierarchy 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="6a954-152">The following example shows an error response to a SyncFolderHierarchy request.</span></span> <span data-ttu-id="6a954-153">无效的 SyncState 导致出现此错误。</span><span class="sxs-lookup"><span data-stu-id="6a954-153">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="6a954-154">代码</span><span class="sxs-lookup"><span data-stu-id="6a954-154">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="6a954-155">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="6a954-155">Error response elements</span></span>

<span data-ttu-id="6a954-156">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a954-156">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="6a954-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6a954-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6a954-158">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="6a954-158">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="6a954-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6a954-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6a954-160">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6a954-160">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="6a954-161">MessageText</span><span class="sxs-lookup"><span data-stu-id="6a954-161">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="6a954-162">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6a954-162">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6a954-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6a954-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="6a954-164">SyncState</span><span class="sxs-lookup"><span data-stu-id="6a954-164">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6a954-165">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="6a954-165">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
## <a name="see-also"></a><span data-ttu-id="6a954-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a954-166">See also</span></span>



- [<span data-ttu-id="6a954-167">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6a954-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

