---
title: SyncFolderItems 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 7f0de089-8876-47ec-a871-df118ceae75d
description: SyncFolderItems 操作在 Exchange 服务器和客户端之间同步项目。
ms.openlocfilehash: 1a28d895eda11dd43f77ec2662a60a426cfc463c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468143"
---
# <a name="syncfolderitems-operation"></a><span data-ttu-id="0bdff-103">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="0bdff-103">SyncFolderItems operation</span></span>

<span data-ttu-id="0bdff-104">SyncFolderItems 操作在 Exchange 服务器和客户端之间同步项目。</span><span class="sxs-lookup"><span data-stu-id="0bdff-104">The SyncFolderItems operation synchronizes items between the Exchange server and the client.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0bdff-105">备注</span><span class="sxs-lookup"><span data-stu-id="0bdff-105">Remarks</span></span>

<span data-ttu-id="0bdff-106">SyncFolderItems 操作将返回最多512个更改。</span><span class="sxs-lookup"><span data-stu-id="0bdff-106">The SyncFolderItems operation will return a maximum of 512 changes.</span></span> <span data-ttu-id="0bdff-107">必须执行后续的 SyncFolderItems 请求以获取其他更改。</span><span class="sxs-lookup"><span data-stu-id="0bdff-107">Subsequent SyncFolderItems requests must be performed to get additional changes.</span></span> 
  
<span data-ttu-id="0bdff-108">SyncFolderItems 类似于 FindItem 操作，因为它无法返回正文或附件等属性。</span><span class="sxs-lookup"><span data-stu-id="0bdff-108">SyncFolderItems is similar to the FindItem operation in that it cannot return properties like Body or Attachments.</span></span> <span data-ttu-id="0bdff-109">如果 SyncFolderItems 操作不返回所需的属性，则可以使用[GetItem 操作](getitem-operation.md)获取 SyncFolderItems 返回的每个项目的特定属性集。</span><span class="sxs-lookup"><span data-stu-id="0bdff-109">If the SyncFolderItems operation does not return the properties that you need, you can use the [GetItem operation](getitem-operation.md) to get a specific set of properties for each item that it returned by SyncFolderItems.</span></span> 
  
## <a name="syncfolderitems-request-example"></a><span data-ttu-id="0bdff-110">SyncFolderItems 请求示例</span><span class="sxs-lookup"><span data-stu-id="0bdff-110">SyncFolderItems request example</span></span>

### <a name="description"></a><span data-ttu-id="0bdff-111">说明</span><span class="sxs-lookup"><span data-stu-id="0bdff-111">Description</span></span>

<span data-ttu-id="0bdff-112">下面的 SyncFolderItems 请求示例演示如何同步文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="0bdff-112">The following example of a SyncFolderItems request shows how to synchronize items in a folder.</span></span> <span data-ttu-id="0bdff-113">本示例显示 "已发送邮件" 文件夹中未发生的第一次同步的文件夹项目同步。</span><span class="sxs-lookup"><span data-stu-id="0bdff-113">This example shows a folder item's synchronization that is not the first synchronization to have occurred for the Sent Items folder.</span></span> <span data-ttu-id="0bdff-114">在第一次尝试将客户端与 Exchange 服务器同步时，请求中不包含[SyncState](syncstate-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="0bdff-114">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="0bdff-115">第一次尝试同步文件夹层次结构中的项时，将返回邮箱中的所有项，而不包括在[Ignore](ignore.md)元素中标识的项。</span><span class="sxs-lookup"><span data-stu-id="0bdff-115">The first attempt to synchronize the items in a folder hierarchy will return all the items in the mailbox, excluding items that are identified in the [Ignore](ignore.md) element.</span></span> <span data-ttu-id="0bdff-116">此 SyncFolderItems 请求将尝试同步自上次同步之后对文件夹项所做的所有更改。</span><span class="sxs-lookup"><span data-stu-id="0bdff-116">This SyncFolderItems request will try to synchronize all changes to the folder items since the last synchronization.</span></span> <span data-ttu-id="0bdff-117">此请求将忽略对[ignore](ignore.md)元素中标识的项进行同步的尝试。</span><span class="sxs-lookup"><span data-stu-id="0bdff-117">This request will ignore the attempt to synchronize the one item that is identified in the [Ignore](ignore.md) element.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0bdff-118">代码</span><span class="sxs-lookup"><span data-stu-id="0bdff-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderItems xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
      </ItemShape>
      <SyncFolderId>
        <t:DistinguishedFolderId Id="sentitems"/>
      </SyncFolderId>
      <SyncState>AEbJ94eMOAAA=</SyncState>
      <Ignore>
        <t:ItemId Id="AQApAHRAA==" ChangeKey="CQAAABY"/>
      </Ignore>
      <MaxChangesReturned>100</MaxChangesReturned>
    </SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0bdff-119">备注</span><span class="sxs-lookup"><span data-stu-id="0bdff-119">Comments</span></span>

<span data-ttu-id="0bdff-120">[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和[ItemId](itemid.md)元素**Id**属性已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0bdff-120">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="0bdff-121">Request 元素</span><span class="sxs-lookup"><span data-stu-id="0bdff-121">Request elements</span></span>

<span data-ttu-id="0bdff-122">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0bdff-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0bdff-123">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="0bdff-123">SyncFolderItems</span></span>](syncfolderitems.md)
    
- [<span data-ttu-id="0bdff-124">ItemShape</span><span class="sxs-lookup"><span data-stu-id="0bdff-124">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="0bdff-125">BaseShape</span><span class="sxs-lookup"><span data-stu-id="0bdff-125">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="0bdff-126">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="0bdff-126">SyncFolderId</span></span>](syncfolderid.md)
    
- [<span data-ttu-id="0bdff-127">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0bdff-127">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="0bdff-128">SyncState</span><span class="sxs-lookup"><span data-stu-id="0bdff-128">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0bdff-129">忽略</span><span class="sxs-lookup"><span data-stu-id="0bdff-129">Ignore</span></span>](ignore.md)
    
- [<span data-ttu-id="0bdff-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="0bdff-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="0bdff-131">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="0bdff-131">MaxChangesReturned</span></span>](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a><span data-ttu-id="0bdff-132">成功的 SyncFolderItems 响应</span><span class="sxs-lookup"><span data-stu-id="0bdff-132">Successful SyncFolderItems Response</span></span>

### <a name="description"></a><span data-ttu-id="0bdff-133">说明</span><span class="sxs-lookup"><span data-stu-id="0bdff-133">Description</span></span>

<span data-ttu-id="0bdff-134">下面的示例演示对 SyncFolderItems 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="0bdff-134">The following example shows a successful response to the SyncFolderItems request.</span></span> <span data-ttu-id="0bdff-135">在此示例中，会议请求将从 "已发送邮件" 文件夹中同步。</span><span class="sxs-lookup"><span data-stu-id="0bdff-135">In this example, a meeting request is synchronized from the Sent Items folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="0bdff-136">代码</span><span class="sxs-lookup"><span data-stu-id="0bdff-136">Code</span></span>

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
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAA=</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:MeetingRequest>
                <t:ItemId Id="AQApAHRwA==" ChangeKey="CwAAABYA" />
                <t:Subject>Budget Q3</t:Subject>
                <t:Sensitivity>Normal</t:Sensitivity>
                <t:IsOutOfDate>false</t:IsOutOfDate>
                <t:HasBeenProcessed>true</t:HasBeenProcessed>
                <t:ResponseType>NoResponseReceived</t:ResponseType>
                <t:IntendedFreeBusyStatus>Busy</t:IntendedFreeBusyStatus>
                <t:Start>2006-08-02T17:30:00Z</t:Start>
                <t:End>2006-08-02T19:30:00Z</t:End>
                <t:Location>Conference Room 2</t:Location>
                <t:Organizer>
                  <t:Mailbox>
                    <t:Name>Dan Park</t:Name>
                    <t:EmailAddress>dpark@example.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                  </t:Mailbox>
                </t:Organizer>
              </t:MeetingRequest>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0bdff-137">备注</span><span class="sxs-lookup"><span data-stu-id="0bdff-137">Comments</span></span>

<span data-ttu-id="0bdff-138">[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和[ItemId](itemid.md)元素**Id**属性已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0bdff-138">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="0bdff-139">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="0bdff-139">Successful response elements</span></span>

<span data-ttu-id="0bdff-140">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0bdff-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0bdff-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0bdff-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0bdff-142">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="0bdff-142">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="0bdff-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0bdff-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0bdff-144">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0bdff-144">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="0bdff-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0bdff-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0bdff-146">SyncState</span><span class="sxs-lookup"><span data-stu-id="0bdff-146">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0bdff-147">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="0bdff-147">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
- [<span data-ttu-id="0bdff-148">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="0bdff-148">Changes (Items)</span></span>](changes-items.md)
    
- [<span data-ttu-id="0bdff-149">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="0bdff-149">Create (ItemSync)</span></span>](create-itemsync.md)
    
- [<span data-ttu-id="0bdff-150">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0bdff-150">MeetingRequest</span></span>](meetingrequest.md)
    
- [<span data-ttu-id="0bdff-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="0bdff-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="0bdff-152">主题</span><span class="sxs-lookup"><span data-stu-id="0bdff-152">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="0bdff-153">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="0bdff-153">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="0bdff-154">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="0bdff-154">IsOutOfDate</span></span>](isoutofdate.md)
    
- [<span data-ttu-id="0bdff-155">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="0bdff-155">HasBeenProcessed</span></span>](hasbeenprocessed.md)
    
- [<span data-ttu-id="0bdff-156">ResponseType</span><span class="sxs-lookup"><span data-stu-id="0bdff-156">ResponseType</span></span>](responsetype.md)
    
- [<span data-ttu-id="0bdff-157">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0bdff-157">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md)
    
- [<span data-ttu-id="0bdff-158">开始</span><span class="sxs-lookup"><span data-stu-id="0bdff-158">Start</span></span>](start.md)
    
- [<span data-ttu-id="0bdff-159">停止</span><span class="sxs-lookup"><span data-stu-id="0bdff-159">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0bdff-160">Location</span><span class="sxs-lookup"><span data-stu-id="0bdff-160">Location</span></span>](location.md)
    
- [<span data-ttu-id="0bdff-161">Organizer</span><span class="sxs-lookup"><span data-stu-id="0bdff-161">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="0bdff-162">邮箱</span><span class="sxs-lookup"><span data-stu-id="0bdff-162">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="0bdff-163">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0bdff-163">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="0bdff-164">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0bdff-164">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="0bdff-165">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="0bdff-165">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a><span data-ttu-id="0bdff-166">SyncFolderItems 错误响应</span><span class="sxs-lookup"><span data-stu-id="0bdff-166">SyncFolderItems error response</span></span>

### <a name="description"></a><span data-ttu-id="0bdff-167">说明</span><span class="sxs-lookup"><span data-stu-id="0bdff-167">Description</span></span>

<span data-ttu-id="0bdff-168">下面的示例演示对 SyncFolderItems 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="0bdff-168">The following example shows an error response to a SyncFolderItems request.</span></span> <span data-ttu-id="0bdff-169">此错误是由无效的 SyncState 所致。</span><span class="sxs-lookup"><span data-stu-id="0bdff-169">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="0bdff-170">代码</span><span class="sxs-lookup"><span data-stu-id="0bdff-170">Code</span></span>

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
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupt or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="0bdff-171">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0bdff-171">Error response elements</span></span>

<span data-ttu-id="0bdff-172">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0bdff-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0bdff-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0bdff-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0bdff-174">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="0bdff-174">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="0bdff-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0bdff-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0bdff-176">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0bdff-176">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="0bdff-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="0bdff-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0bdff-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0bdff-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0bdff-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0bdff-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0bdff-180">SyncState</span><span class="sxs-lookup"><span data-stu-id="0bdff-180">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0bdff-181">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="0bdff-181">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
## <a name="see-also"></a><span data-ttu-id="0bdff-182">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0bdff-182">See also</span></span>



- [<span data-ttu-id="0bdff-183">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0bdff-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

