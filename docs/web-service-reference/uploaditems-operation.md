---
title: UploadItems 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: a88cbe99-7968-454d-a545-4f92c330909f
description: UploadItems 操作将项目的数据流上载到 Exchange 邮箱。
ms.openlocfilehash: 6b002d531c7011b18ae1f88adfc2923d5a51e81c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838434"
---
# <a name="uploaditems-operation"></a><span data-ttu-id="ff6d4-103">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="ff6d4-103">UploadItems operation</span></span>

<span data-ttu-id="ff6d4-104">**UploadItems**操作将项目的数据流上载到 Exchange 邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-104">The **UploadItems** operation uploads a stream of items into an Exchange mailbox.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ff6d4-105">**UploadItems**操作限制为 25 MB 的 base64 编码的数据的最大导入负载 MicrosoftExchange Server 2010 Service Pack 1 (SP1) 中。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-105">The **UploadItems** operation is restricted in MicrosoftExchange Server 2010 Service Pack 1 (SP1) to a maximum import payload of 25MB of base64 encoded data.</span></span> <span data-ttu-id="ff6d4-106">可以在 web.config 文件中更改该设置。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-106">The setting can be altered in the web.config file.</span></span> 
  
## <a name="uploaditems-request-example"></a><span data-ttu-id="ff6d4-107">UploadItems 请求示例</span><span class="sxs-lookup"><span data-stu-id="ff6d4-107">UploadItems request example</span></span>

### <a name="description"></a><span data-ttu-id="ff6d4-108">说明</span><span class="sxs-lookup"><span data-stu-id="ff6d4-108">Description</span></span>

<span data-ttu-id="ff6d4-109">**UploadItems**请求的下面的示例演示如何将两个项目上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-109">The following example of an **UploadItems** request shows how to upload two items into a mailbox.</span></span> <span data-ttu-id="ff6d4-110">第一项是新项目。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-110">The first item is a new item.</span></span> <span data-ttu-id="ff6d4-111">第二项是邮箱中的现有项目的更新的版本。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-111">The second item is an updated version of an existing item in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ff6d4-112">代码</span><span class="sxs-lookup"><span data-stu-id="ff6d4-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAA==" ChangeKey="AQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAAcSMAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAADACYAAAAAAAsAKQAAAAMALgAAAAAAAwA2AAAAAACwhw4=
          </t:Data>
        </t:Item>
        <t:Item CreateAction="Update">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAB==" ChangeKey="AQAAAA=="/>
          <t:ItemId Id="AAMkADhhOGU0MGM7AAA=" ChangeKey="CQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAANiAAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAALACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUA
            cwB0AGkAbgBnACAALQAgAGYAcgBvAG0AIABFAFcAUwBNAEEAAABAAD
            kAgJ2chyHuygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FOSVpBVBMO
          </t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ff6d4-113">注释</span><span class="sxs-lookup"><span data-stu-id="ff6d4-113">Comments</span></span>

<span data-ttu-id="ff6d4-114">已缩短标识符和项目数据，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-114">Identifiers and the item data have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ff6d4-115">请求元素</span><span class="sxs-lookup"><span data-stu-id="ff6d4-115">Request elements</span></span>

<span data-ttu-id="ff6d4-116">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff6d4-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ff6d4-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ff6d4-117">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="ff6d4-118">UploadItems</span><span class="sxs-lookup"><span data-stu-id="ff6d4-118">UploadItems</span></span>](uploaditems.md)
    
- [<span data-ttu-id="ff6d4-119">项目 (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="ff6d4-119">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
    
- [<span data-ttu-id="ff6d4-120">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="ff6d4-120">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
    
- [<span data-ttu-id="ff6d4-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ff6d4-121">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="ff6d4-122">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="ff6d4-122">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="ff6d4-123">ItemId</span><span class="sxs-lookup"><span data-stu-id="ff6d4-123">ItemId</span></span>](itemid.md)
    
## <a name="successful-uploaditems-response-example"></a><span data-ttu-id="ff6d4-124">成功 UploadItems 响应示例</span><span class="sxs-lookup"><span data-stu-id="ff6d4-124">Successful UploadItems response example</span></span>

### <a name="description"></a><span data-ttu-id="ff6d4-125">说明</span><span class="sxs-lookup"><span data-stu-id="ff6d4-125">Description</span></span>

<span data-ttu-id="ff6d4-126">下面的示例演示对**UploadItems**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-126">The following example shows a successful response to the **UploadItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ff6d4-127">代码</span><span class="sxs-lookup"><span data-stu-id="ff6d4-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
                         MinorVersion="1"
                         MajorBuildNumber="164"
                         MinorBuildNumber="0"
                         Version="Exchange2010_SP1"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhUFZ/AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQm"/>
        </m:UploadItemsResponseMessage>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGZ7AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQn"/>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ff6d4-128">注释</span><span class="sxs-lookup"><span data-stu-id="ff6d4-128">Comments</span></span>

<span data-ttu-id="ff6d4-129">项标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-129">Item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="ff6d4-130">响应元素</span><span class="sxs-lookup"><span data-stu-id="ff6d4-130">Response elements</span></span>

<span data-ttu-id="ff6d4-131">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff6d4-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ff6d4-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ff6d4-133">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="ff6d4-133">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="ff6d4-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ff6d4-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ff6d4-135">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ff6d4-135">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="ff6d4-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff6d4-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff6d4-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="ff6d4-137">ItemId</span></span>](itemid.md)
    
## <a name="uploaditems-error-response-example"></a><span data-ttu-id="ff6d4-138">UploadItems 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="ff6d4-138">UploadItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="ff6d4-139">说明</span><span class="sxs-lookup"><span data-stu-id="ff6d4-139">Description</span></span>

<span data-ttu-id="ff6d4-140">下面的示例演示包含由尝试更新找不到的邮箱中的项导致的错误**UploadItems**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ff6d4-140">The following example shows a response to the **UploadItems** request that contains an error caused by an attempt to update an item that cannot be found in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ff6d4-141">代码</span><span class="sxs-lookup"><span data-stu-id="ff6d4-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="ff6d4-142">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="ff6d4-142">Error response elements</span></span>

<span data-ttu-id="ff6d4-143">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff6d4-143">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="ff6d4-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ff6d4-145">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="ff6d4-145">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="ff6d4-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ff6d4-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ff6d4-147">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ff6d4-147">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="ff6d4-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ff6d4-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ff6d4-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff6d4-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff6d4-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ff6d4-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="ff6d4-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff6d4-151">See also</span></span>



[<span data-ttu-id="ff6d4-152">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="ff6d4-152">ExportItems operation</span></span>](exportitems-operation.md)


[<span data-ttu-id="ff6d4-153">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="ff6d4-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="ff6d4-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ff6d4-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

