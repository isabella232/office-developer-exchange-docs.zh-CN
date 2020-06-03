---
title: FindFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: FindFolder 操作使用 Exchange Web 服务查找已标识文件夹的子文件夹，并返回一组用于描述子文件夹集的属性。
ms.openlocfilehash: f1cc199bdaf684d8d74687ed7f064eb66fee48ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462582"
---
# <a name="findfolder-operation"></a><span data-ttu-id="ccdce-103">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="ccdce-103">FindFolder operation</span></span>

<span data-ttu-id="ccdce-104">**FindFolder**操作使用 Exchange Web 服务查找已标识文件夹的子文件夹，并返回一组用于描述子文件夹集的属性。</span><span class="sxs-lookup"><span data-stu-id="ccdce-104">The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ccdce-105">备注</span><span class="sxs-lookup"><span data-stu-id="ccdce-105">Remarks</span></span>

<span data-ttu-id="ccdce-106">FindFolder 仅返回任何 streamable 属性的前512个字节。</span><span class="sxs-lookup"><span data-stu-id="ccdce-106">FindFolder returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="ccdce-107">对于 Unicode，它通过使用以 null 结尾的 Unicode 字符串返回前255个字符。</span><span class="sxs-lookup"><span data-stu-id="ccdce-107">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span>
  
<span data-ttu-id="ccdce-108">无法对公用文件夹执行深度遍历查询。</span><span class="sxs-lookup"><span data-stu-id="ccdce-108">Deep traversal queries cannot be performed on public folders.</span></span>
  
<span data-ttu-id="ccdce-109">限制是允许的，并且应仅使用文件夹属性，而不应使用项目属性。</span><span class="sxs-lookup"><span data-stu-id="ccdce-109">Restrictions are permitted and should use only the folder properties, not the item properties.</span></span> <span data-ttu-id="ccdce-110">排序功能对**FindFolder**响应不可用。</span><span class="sxs-lookup"><span data-stu-id="ccdce-110">Sorting functionality is not available for **FindFolder** responses.</span></span> <span data-ttu-id="ccdce-111">分组查询不适用于**FindFolder**查询。</span><span class="sxs-lookup"><span data-stu-id="ccdce-111">Grouped queries are not available for **FindFolder** queries.</span></span> 
  
 <span data-ttu-id="ccdce-112">**注释\*\*\*\*FindFolder**操作还用于查找托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="ccdce-112">**Note** The **FindFolder** operation is also used to find managed folders.</span></span> 
  
### <a name="soap-headers"></a><span data-ttu-id="ccdce-113">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="ccdce-113">SOAP Headers</span></span>

<span data-ttu-id="ccdce-114">**FindFolder**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="ccdce-114">The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="ccdce-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="ccdce-115">**Header**</span></span>|<span data-ttu-id="ccdce-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccdce-116">**Element**</span></span>|<span data-ttu-id="ccdce-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccdce-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccdce-118">模拟</span><span class="sxs-lookup"><span data-stu-id="ccdce-118">Impersonation</span></span>  <br/> |[<span data-ttu-id="ccdce-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ccdce-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ccdce-120">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="ccdce-120">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="ccdce-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ccdce-121">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="ccdce-122">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ccdce-122">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ccdce-123">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="ccdce-123">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="ccdce-124">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="ccdce-124">RequestVersion</span></span>  <br/> |[<span data-ttu-id="ccdce-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ccdce-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ccdce-126">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="ccdce-126">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="ccdce-127">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ccdce-127">ServerVersion</span></span>  <br/> |[<span data-ttu-id="ccdce-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccdce-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ccdce-129">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="ccdce-129">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="ccdce-130">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="ccdce-130">TimeZoneContext</span></span>  <br/> |[<span data-ttu-id="ccdce-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="ccdce-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="ccdce-132">标识要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="ccdce-132">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="findfolder-request-example"></a><span data-ttu-id="ccdce-133">FindFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="ccdce-133">FindFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="ccdce-134">Description</span><span class="sxs-lookup"><span data-stu-id="ccdce-134">Description</span></span>

<span data-ttu-id="ccdce-135">下面的**FindFolder**请求示例演示如何在请求中查找位于收件箱中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="ccdce-135">The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccdce-136">代码</span><span class="sxs-lookup"><span data-stu-id="ccdce-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ccdce-137">备注</span><span class="sxs-lookup"><span data-stu-id="ccdce-137">Comments</span></span>

<span data-ttu-id="ccdce-138">通过使用[BaseShape](baseshape.md)的默认值，响应将返回文件夹名称、文件夹 ID、子文件夹数、文件夹中找到的子文件夹数以及未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="ccdce-138">Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ccdce-139">Request 元素</span><span class="sxs-lookup"><span data-stu-id="ccdce-139">Request elements</span></span>

<span data-ttu-id="ccdce-140">此**FindFolder**请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="ccdce-140">This **FindFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccdce-141">FindFolder</span><span class="sxs-lookup"><span data-stu-id="ccdce-141">FindFolder</span></span>](findfolder.md)
    
- [<span data-ttu-id="ccdce-142">FolderShape</span><span class="sxs-lookup"><span data-stu-id="ccdce-142">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="ccdce-143">BaseShape</span><span class="sxs-lookup"><span data-stu-id="ccdce-143">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="ccdce-144">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="ccdce-144">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="ccdce-145">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="ccdce-145">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
 <span data-ttu-id="ccdce-146">有关其他**FindFolder**请求元素，请参阅架构。</span><span class="sxs-lookup"><span data-stu-id="ccdce-146">For additional **FindFolder** request elements, see the schema.</span></span> 
  
## <a name="findfolder-response-example"></a><span data-ttu-id="ccdce-147">FindFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="ccdce-147">FindFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="ccdce-148">Description</span><span class="sxs-lookup"><span data-stu-id="ccdce-148">Description</span></span>

<span data-ttu-id="ccdce-149">下面的简单对象访问协议（SOAP）正文示例显示了对**FindFolder**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="ccdce-149">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request.</span></span> <span data-ttu-id="ccdce-150">响应包含在使用[BaseShape](baseshape.md)的默认值时返回的元素。</span><span class="sxs-lookup"><span data-stu-id="ccdce-150">The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ccdce-151">文件夹 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="ccdce-151">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccdce-152">代码</span><span class="sxs-lookup"><span data-stu-id="ccdce-152">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="ccdce-153">Response 元素</span><span class="sxs-lookup"><span data-stu-id="ccdce-153">Response elements</span></span>

<span data-ttu-id="ccdce-154">在响应中返回的属性由[BaseShape](baseshape.md)和[AdditionalProperties](additionalproperties.md) （如果使用它们）决定。</span><span class="sxs-lookup"><span data-stu-id="ccdce-154">The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used.</span></span> <span data-ttu-id="ccdce-155">成功的**FindFolder**响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="ccdce-155">A successful **FindFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccdce-156">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccdce-156">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ccdce-157">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ccdce-157">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="ccdce-158">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccdce-158">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccdce-159">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ccdce-159">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
    
- [<span data-ttu-id="ccdce-160">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccdce-160">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ccdce-161">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="ccdce-161">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="ccdce-162">Folders</span><span class="sxs-lookup"><span data-stu-id="ccdce-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ccdce-163">Folder</span><span class="sxs-lookup"><span data-stu-id="ccdce-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ccdce-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="ccdce-164">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ccdce-165">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="ccdce-165">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ccdce-166">TotalCount</span><span class="sxs-lookup"><span data-stu-id="ccdce-166">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="ccdce-167">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="ccdce-167">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="ccdce-168">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="ccdce-168">UnreadCount</span></span>](unreadcount.md)
    
### <a name="comments"></a><span data-ttu-id="ccdce-169">备注</span><span class="sxs-lookup"><span data-stu-id="ccdce-169">Comments</span></span>

 <span data-ttu-id="ccdce-170">对具有**AllProperties**响应形状的请求的**FindFolder**响应不会返回公用文件夹搜索的[TotalCount](totalcount.md)和[UnreadCount](unreadcount.md)元素。</span><span class="sxs-lookup"><span data-stu-id="ccdce-170">**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.</span></span> 
  
## <a name="findfolder-error-response-example"></a><span data-ttu-id="ccdce-171">FindFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="ccdce-171">FindFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="ccdce-172">Description</span><span class="sxs-lookup"><span data-stu-id="ccdce-172">Description</span></span>

<span data-ttu-id="ccdce-173">下面的 SOAP 正文示例显示当您搜索由格式错误的文件夹标识符标识的文件夹时发生的错误响应。</span><span class="sxs-lookup"><span data-stu-id="ccdce-173">The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="ccdce-174">代码</span><span class="sxs-lookup"><span data-stu-id="ccdce-174">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="ccdce-175">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="ccdce-175">Error response elements</span></span>

<span data-ttu-id="ccdce-176">**FindFolder**错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="ccdce-176">The **FindFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccdce-177">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ccdce-177">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="ccdce-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccdce-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccdce-179">MessageText</span><span class="sxs-lookup"><span data-stu-id="ccdce-179">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ccdce-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccdce-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ccdce-181">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ccdce-181">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="additional-information"></a><span data-ttu-id="ccdce-182">其他信息</span><span class="sxs-lookup"><span data-stu-id="ccdce-182">Additional Information</span></span>

- <span data-ttu-id="ccdce-183">文件夹[DisplayName （string）](displayname-string.md)元素始终包含在默认形状中。</span><span class="sxs-lookup"><span data-stu-id="ccdce-183">The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.</span></span> 
    
- <span data-ttu-id="ccdce-184">" [UnreadCount](unreadcount.md) " 元素包含在 "任务" 和 "便笺" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="ccdce-184">The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.</span></span> 
    
- <span data-ttu-id="ccdce-185">使用具有**Integer**属性类型的0X672D 的**PropertyTag**值，以使用[ExtendedFieldURI](extendedfielduri.md)元素标识托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="ccdce-185">Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ccdce-186">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ccdce-186">See also</span></span>



[<span data-ttu-id="ccdce-187">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="ccdce-187">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

