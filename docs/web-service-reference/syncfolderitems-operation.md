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
description: SyncFolderItems 操作同步 Exchange server 和客户端之间的项目。
ms.openlocfilehash: 6b2e4694ac793e17a2b7cb2edb2cb9e6a4a105ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838176"
---
# <a name="syncfolderitems-operation"></a><span data-ttu-id="dfeb0-103">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="dfeb0-103">SyncFolderItems operation</span></span>

<span data-ttu-id="dfeb0-104">SyncFolderItems 操作同步 Exchange server 和客户端之间的项目。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-104">The SyncFolderItems operation synchronizes items between the Exchange server and the client.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfeb0-105">注解</span><span class="sxs-lookup"><span data-stu-id="dfeb0-105">Remarks</span></span>

<span data-ttu-id="dfeb0-106">SyncFolderItems 操作将返回最多个 512 更改。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-106">The SyncFolderItems operation will return a maximum of 512 changes.</span></span> <span data-ttu-id="dfeb0-107">若要获取的其他更改，必须执行后续 SyncFolderItems 请求。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-107">Subsequent SyncFolderItems requests must be performed to get additional changes.</span></span> 
  
<span data-ttu-id="dfeb0-108">它不能返回正文或附件之类的属性，因此 SyncFolderItems 是类似于 FindItem 操作。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-108">SyncFolderItems is similar to the FindItem operation in that it cannot return properties like Body or Attachments.</span></span> <span data-ttu-id="dfeb0-109">如果 SyncFolderItems 操作不会返回所需的属性，您可以使用[GetItem 操作](getitem-operation.md)获取一组特定的属性，它由 SyncFolderItems 返回的每个项目。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-109">If the SyncFolderItems operation does not return the properties that you need, you can use the [GetItem operation](getitem-operation.md) to get a specific set of properties for each item that it returned by SyncFolderItems.</span></span> 
  
## <a name="syncfolderitems-request-example"></a><span data-ttu-id="dfeb0-110">SyncFolderItems 请求示例</span><span class="sxs-lookup"><span data-stu-id="dfeb0-110">SyncFolderItems request example</span></span>

### <a name="description"></a><span data-ttu-id="dfeb0-111">说明</span><span class="sxs-lookup"><span data-stu-id="dfeb0-111">Description</span></span>

<span data-ttu-id="dfeb0-112">SyncFolderItems 请求的下面的示例演示如何同步文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-112">The following example of a SyncFolderItems request shows how to synchronize items in a folder.</span></span> <span data-ttu-id="dfeb0-113">本示例演示不是第一个同步发生的已发送邮件文件夹的文件夹项目同步。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-113">This example shows a folder item's synchronization that is not the first synchronization to have occurred for the Sent Items folder.</span></span> <span data-ttu-id="dfeb0-114">首次尝试与 Exchange server 同步客户端的请求中不包括[SyncState](syncstate-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-114">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="dfeb0-115">同步文件夹层次结构中的项目的第一次尝试将返回所有项目在邮箱中排除[忽略](ignore.md)元素中标识的项目。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-115">The first attempt to synchronize the items in a folder hierarchy will return all the items in the mailbox, excluding items that are identified in the [Ignore](ignore.md) element.</span></span> <span data-ttu-id="dfeb0-116">此 SyncFolderItems 请求将尝试自上次同步同步到文件夹项目的所有更改。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-116">This SyncFolderItems request will try to synchronize all changes to the folder items since the last synchronization.</span></span> <span data-ttu-id="dfeb0-117">此请求将忽略尝试同步中的[忽略](ignore.md)元素标识一项。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-117">This request will ignore the attempt to synchronize the one item that is identified in the [Ignore](ignore.md) element.</span></span> 
  
### <a name="code"></a><span data-ttu-id="dfeb0-118">代码</span><span class="sxs-lookup"><span data-stu-id="dfeb0-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderItems xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="dfeb0-119">注释</span><span class="sxs-lookup"><span data-stu-id="dfeb0-119">Comments</span></span>

<span data-ttu-id="dfeb0-120">已缩短[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和[ItemId](itemid.md)元素的**Id**属性，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-120">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="dfeb0-121">请求元素</span><span class="sxs-lookup"><span data-stu-id="dfeb0-121">Request elements</span></span>

<span data-ttu-id="dfeb0-122">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="dfeb0-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="dfeb0-123">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="dfeb0-123">SyncFolderItems</span></span>](syncfolderitems.md)
    
- [<span data-ttu-id="dfeb0-124">ItemShape</span><span class="sxs-lookup"><span data-stu-id="dfeb0-124">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="dfeb0-125">BaseShape</span><span class="sxs-lookup"><span data-stu-id="dfeb0-125">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="dfeb0-126">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="dfeb0-126">SyncFolderId</span></span>](syncfolderid.md)
    
- [<span data-ttu-id="dfeb0-127">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="dfeb0-127">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="dfeb0-128">SyncState</span><span class="sxs-lookup"><span data-stu-id="dfeb0-128">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="dfeb0-129">忽略</span><span class="sxs-lookup"><span data-stu-id="dfeb0-129">Ignore</span></span>](ignore.md)
    
- [<span data-ttu-id="dfeb0-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="dfeb0-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="dfeb0-131">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="dfeb0-131">MaxChangesReturned</span></span>](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a><span data-ttu-id="dfeb0-132">成功的 SyncFolderItems 响应</span><span class="sxs-lookup"><span data-stu-id="dfeb0-132">Successful SyncFolderItems Response</span></span>

### <a name="description"></a><span data-ttu-id="dfeb0-133">说明</span><span class="sxs-lookup"><span data-stu-id="dfeb0-133">Description</span></span>

<span data-ttu-id="dfeb0-134">下面的示例演示对 SyncFolderItems 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-134">The following example shows a successful response to the SyncFolderItems request.</span></span> <span data-ttu-id="dfeb0-135">本示例中，从已发送邮件文件夹同步会议请求。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-135">In this example, a meeting request is synchronized from the Sent Items folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="dfeb0-136">代码</span><span class="sxs-lookup"><span data-stu-id="dfeb0-136">Code</span></span>

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
    <SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="dfeb0-137">注释</span><span class="sxs-lookup"><span data-stu-id="dfeb0-137">Comments</span></span>

<span data-ttu-id="dfeb0-138">已缩短[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和[ItemId](itemid.md)元素的**Id**属性，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-138">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="dfeb0-139">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="dfeb0-139">Successful response elements</span></span>

<span data-ttu-id="dfeb0-140">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="dfeb0-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="dfeb0-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dfeb0-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="dfeb0-142">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="dfeb0-142">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="dfeb0-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dfeb0-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="dfeb0-144">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dfeb0-144">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="dfeb0-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dfeb0-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dfeb0-146">SyncState</span><span class="sxs-lookup"><span data-stu-id="dfeb0-146">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="dfeb0-147">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="dfeb0-147">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
- [<span data-ttu-id="dfeb0-148">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="dfeb0-148">Changes (Items)</span></span>](changes-items.md)
    
- [<span data-ttu-id="dfeb0-149">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="dfeb0-149">Create (ItemSync)</span></span>](create-itemsync.md)
    
- [<span data-ttu-id="dfeb0-150">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="dfeb0-150">MeetingRequest</span></span>](meetingrequest.md)
    
- [<span data-ttu-id="dfeb0-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="dfeb0-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="dfeb0-152">Subject</span><span class="sxs-lookup"><span data-stu-id="dfeb0-152">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="dfeb0-153">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="dfeb0-153">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="dfeb0-154">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="dfeb0-154">IsOutOfDate</span></span>](isoutofdate.md)
    
- [<span data-ttu-id="dfeb0-155">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="dfeb0-155">HasBeenProcessed</span></span>](hasbeenprocessed.md)
    
- [<span data-ttu-id="dfeb0-156">ResponseType</span><span class="sxs-lookup"><span data-stu-id="dfeb0-156">ResponseType</span></span>](responsetype.md)
    
- [<span data-ttu-id="dfeb0-157">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="dfeb0-157">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md)
    
- [<span data-ttu-id="dfeb0-158">Start</span><span class="sxs-lookup"><span data-stu-id="dfeb0-158">Start</span></span>](start.md)
    
- [<span data-ttu-id="dfeb0-159">结束</span><span class="sxs-lookup"><span data-stu-id="dfeb0-159">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="dfeb0-160">位置</span><span class="sxs-lookup"><span data-stu-id="dfeb0-160">Location</span></span>](location.md)
    
- [<span data-ttu-id="dfeb0-161">Organizer</span><span class="sxs-lookup"><span data-stu-id="dfeb0-161">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="dfeb0-162">Mailbox</span><span class="sxs-lookup"><span data-stu-id="dfeb0-162">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="dfeb0-163">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="dfeb0-163">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="dfeb0-164">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="dfeb0-164">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="dfeb0-165">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="dfeb0-165">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a><span data-ttu-id="dfeb0-166">SyncFolderItems 错误响应</span><span class="sxs-lookup"><span data-stu-id="dfeb0-166">SyncFolderItems error response</span></span>

### <a name="description"></a><span data-ttu-id="dfeb0-167">说明</span><span class="sxs-lookup"><span data-stu-id="dfeb0-167">Description</span></span>

<span data-ttu-id="dfeb0-168">下面的示例演示对 SyncFolderItems 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-168">The following example shows an error response to a SyncFolderItems request.</span></span> <span data-ttu-id="dfeb0-169">无效的 SyncState 导致出现此错误。</span><span class="sxs-lookup"><span data-stu-id="dfeb0-169">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="dfeb0-170">代码</span><span class="sxs-lookup"><span data-stu-id="dfeb0-170">Code</span></span>

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
    <SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="dfeb0-171">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="dfeb0-171">Error response elements</span></span>

<span data-ttu-id="dfeb0-172">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="dfeb0-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="dfeb0-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dfeb0-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="dfeb0-174">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="dfeb0-174">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="dfeb0-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dfeb0-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="dfeb0-176">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dfeb0-176">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="dfeb0-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="dfeb0-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="dfeb0-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dfeb0-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dfeb0-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dfeb0-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="dfeb0-180">SyncState</span><span class="sxs-lookup"><span data-stu-id="dfeb0-180">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="dfeb0-181">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="dfeb0-181">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
## <a name="see-also"></a><span data-ttu-id="dfeb0-182">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfeb0-182">See also</span></span>



- [<span data-ttu-id="dfeb0-183">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dfeb0-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

