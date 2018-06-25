---
title: FindFolder Operation
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
description: FindFolder 操作使用 Exchange Web 服务来查找标识的文件夹的子文件夹，并返回描述这组子文件夹的属性集。
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754328"
---
# <a name="findfolder-operation"></a><span data-ttu-id="f32d7-103">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="f32d7-103">FindFolder operation</span></span>

<span data-ttu-id="f32d7-104">**FindFolder**操作使用 Exchange Web 服务来查找标识的文件夹的子文件夹，并返回描述这组子文件夹的属性集。</span><span class="sxs-lookup"><span data-stu-id="f32d7-104">The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f32d7-105">注解</span><span class="sxs-lookup"><span data-stu-id="f32d7-105">Remarks</span></span>

<span data-ttu-id="f32d7-106">FindFolder 返回仅第一个 512 个字节的任何流式属性。</span><span class="sxs-lookup"><span data-stu-id="f32d7-106">FindFolder returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="f32d7-107">对于 Unicode，它使用以 null 结尾的 Unicode 字符串中返回的前 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="f32d7-107">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span>
  
<span data-ttu-id="f32d7-108">在公用文件夹，无法执行遍历查询。</span><span class="sxs-lookup"><span data-stu-id="f32d7-108">Deep traversal queries cannot be performed on public folders.</span></span>
  
<span data-ttu-id="f32d7-109">限制允许和应使用仅文件夹属性中，不是项目的属性。</span><span class="sxs-lookup"><span data-stu-id="f32d7-109">Restrictions are permitted and should use only the folder properties, not the item properties.</span></span> <span data-ttu-id="f32d7-110">排序功能不可用的**FindFolder**响应。</span><span class="sxs-lookup"><span data-stu-id="f32d7-110">Sorting functionality is not available for **FindFolder** responses.</span></span> <span data-ttu-id="f32d7-111">组合的查询不能用于**FindFolder**查询。</span><span class="sxs-lookup"><span data-stu-id="f32d7-111">Grouped queries are not available for **FindFolder** queries.</span></span> 
  
 <span data-ttu-id="f32d7-112">**注释****FindFolder**操作还用于查找托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f32d7-112">**Note** The **FindFolder** operation is also used to find managed folders.</span></span> 
  
### <a name="soap-headers"></a><span data-ttu-id="f32d7-113">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f32d7-113">SOAP Headers</span></span>

<span data-ttu-id="f32d7-114">**FindFolder**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f32d7-114">The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="f32d7-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="f32d7-115">**Header**</span></span>|<span data-ttu-id="f32d7-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f32d7-116">**Element**</span></span>|<span data-ttu-id="f32d7-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f32d7-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f32d7-118">模拟</span><span class="sxs-lookup"><span data-stu-id="f32d7-118">Impersonation</span></span>  <br/> |[<span data-ttu-id="f32d7-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f32d7-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f32d7-120">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="f32d7-120">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="f32d7-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f32d7-121">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="f32d7-122">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f32d7-122">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f32d7-123">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="f32d7-123">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="f32d7-124">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="f32d7-124">RequestVersion</span></span>  <br/> |[<span data-ttu-id="f32d7-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f32d7-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f32d7-126">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f32d7-126">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="f32d7-127">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="f32d7-127">ServerVersion</span></span>  <br/> |[<span data-ttu-id="f32d7-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f32d7-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f32d7-129">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="f32d7-129">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="f32d7-130">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="f32d7-130">TimeZoneContext</span></span>  <br/> |[<span data-ttu-id="f32d7-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="f32d7-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="f32d7-132">确定要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="f32d7-132">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="findfolder-request-example"></a><span data-ttu-id="f32d7-133">FindFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="f32d7-133">FindFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="f32d7-134">说明</span><span class="sxs-lookup"><span data-stu-id="f32d7-134">Description</span></span>

<span data-ttu-id="f32d7-135">**FindFolder**请求的下面的示例演示如何以形成一个请求，以查找所有收件箱中位于的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f32d7-135">The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f32d7-136">代码</span><span class="sxs-lookup"><span data-stu-id="f32d7-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="f32d7-137">注释</span><span class="sxs-lookup"><span data-stu-id="f32d7-137">Comments</span></span>

<span data-ttu-id="f32d7-138">响应[BaseShape](baseshape.md)使用默认值，它返回文件夹名称，文件夹 ID，子文件夹，该文件夹，以及的未读项目计数中找到的子文件夹数的数量。</span><span class="sxs-lookup"><span data-stu-id="f32d7-138">Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="f32d7-139">请求元素</span><span class="sxs-lookup"><span data-stu-id="f32d7-139">Request elements</span></span>

<span data-ttu-id="f32d7-140">此**FindFolder**请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="f32d7-140">This **FindFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="f32d7-141">FindFolder</span><span class="sxs-lookup"><span data-stu-id="f32d7-141">FindFolder</span></span>](findfolder.md)
    
- [<span data-ttu-id="f32d7-142">FolderShape</span><span class="sxs-lookup"><span data-stu-id="f32d7-142">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="f32d7-143">BaseShape</span><span class="sxs-lookup"><span data-stu-id="f32d7-143">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="f32d7-144">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="f32d7-144">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="f32d7-145">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="f32d7-145">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
 <span data-ttu-id="f32d7-146">其他**FindFolder**请求元素，请参阅 schema。</span><span class="sxs-lookup"><span data-stu-id="f32d7-146">For additional **FindFolder** request elements, see the schema.</span></span> 
  
## <a name="findfolder-response-example"></a><span data-ttu-id="f32d7-147">FindFolder 响应示例</span><span class="sxs-lookup"><span data-stu-id="f32d7-147">FindFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="f32d7-148">说明</span><span class="sxs-lookup"><span data-stu-id="f32d7-148">Description</span></span>

<span data-ttu-id="f32d7-149">下面的简单对象访问协议 (SOAP) 正文示例演示对**FindFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="f32d7-149">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request.</span></span> <span data-ttu-id="f32d7-150">则响应中包含的默认值为[BaseShape](baseshape.md)时返回的元素。</span><span class="sxs-lookup"><span data-stu-id="f32d7-150">The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f32d7-151">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="f32d7-151">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f32d7-152">代码</span><span class="sxs-lookup"><span data-stu-id="f32d7-152">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="f32d7-153">响应元素</span><span class="sxs-lookup"><span data-stu-id="f32d7-153">Response elements</span></span>

<span data-ttu-id="f32d7-154">如果它们使用由[BaseShape](baseshape.md)和[AdditionalProperties](additionalproperties.md)决定响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="f32d7-154">The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used.</span></span> <span data-ttu-id="f32d7-155">成功的**FindFolder**响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="f32d7-155">A successful **FindFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="f32d7-156">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f32d7-156">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="f32d7-157">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f32d7-157">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="f32d7-158">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f32d7-158">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f32d7-159">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f32d7-159">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
    
- [<span data-ttu-id="f32d7-160">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f32d7-160">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f32d7-161">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="f32d7-161">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="f32d7-162">Folders</span><span class="sxs-lookup"><span data-stu-id="f32d7-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="f32d7-163">Folder</span><span class="sxs-lookup"><span data-stu-id="f32d7-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="f32d7-164">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="f32d7-164">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="f32d7-165">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="f32d7-165">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="f32d7-166">TotalCount</span><span class="sxs-lookup"><span data-stu-id="f32d7-166">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="f32d7-167">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="f32d7-167">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="f32d7-168">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="f32d7-168">UnreadCount</span></span>](unreadcount.md)
    
### <a name="comments"></a><span data-ttu-id="f32d7-169">注释</span><span class="sxs-lookup"><span data-stu-id="f32d7-169">Comments</span></span>

 <span data-ttu-id="f32d7-170">[TotalCount](totalcount.md)和[UnreadCount](unreadcount.md)元素的公用文件夹搜索，不会返回**FindFolder**エ ・ 复 ハ 与**AllProperties**响应形状的请求。</span><span class="sxs-lookup"><span data-stu-id="f32d7-170">**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.</span></span> 
  
## <a name="findfolder-error-response-example"></a><span data-ttu-id="f32d7-171">FindFolder 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="f32d7-171">FindFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="f32d7-172">说明</span><span class="sxs-lookup"><span data-stu-id="f32d7-172">Description</span></span>

<span data-ttu-id="f32d7-173">下面的 SOAP 正文示例演示您搜索由格式不正确的文件夹标识符标识的文件夹时发生错误响应。</span><span class="sxs-lookup"><span data-stu-id="f32d7-173">The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="f32d7-174">代码</span><span class="sxs-lookup"><span data-stu-id="f32d7-174">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="f32d7-175">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="f32d7-175">Error response elements</span></span>

<span data-ttu-id="f32d7-176">**FindFolder**错误响应包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="f32d7-176">The **FindFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="f32d7-177">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f32d7-177">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="f32d7-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f32d7-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f32d7-179">MessageText</span><span class="sxs-lookup"><span data-stu-id="f32d7-179">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f32d7-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f32d7-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f32d7-181">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f32d7-181">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="additional-information"></a><span data-ttu-id="f32d7-182">其他信息</span><span class="sxs-lookup"><span data-stu-id="f32d7-182">Additional Information</span></span>

- <span data-ttu-id="f32d7-183">默认形状中始终包含文件夹[DisplayName （字符串）](displayname-string.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f32d7-183">The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.</span></span> 
    
- <span data-ttu-id="f32d7-184">任务和便笺文件夹中包含的[UnreadCount](unreadcount.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f32d7-184">The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.</span></span> 
    
- <span data-ttu-id="f32d7-185">使用与属性类型的**整数**的 0x672D **PropertyTag**值使用[ExtendedFieldURI](extendedfielduri.md)元素标识托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f32d7-185">Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f32d7-186">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f32d7-186">See also</span></span>



[<span data-ttu-id="f32d7-187">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="f32d7-187">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

