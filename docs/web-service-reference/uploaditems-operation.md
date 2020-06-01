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
description: UploadItems 操作将项目流上载到 Exchange 邮箱中。
ms.openlocfilehash: 57e722c7775baa090736875077781cee869c3b01
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468500"
---
# <a name="uploaditems-operation"></a><span data-ttu-id="5f67a-103">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="5f67a-103">UploadItems operation</span></span>

<span data-ttu-id="5f67a-104">**UploadItems**操作将项目流上载到 Exchange 邮箱中。</span><span class="sxs-lookup"><span data-stu-id="5f67a-104">The **UploadItems** operation uploads a stream of items into an Exchange mailbox.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5f67a-105">**UploadItems**操作在 MicrosoftExchange Server 2010 Service Pack 1 （SP1）中受到限制，可在 base64 编码数据的25MB 中使用最大的导入负载。</span><span class="sxs-lookup"><span data-stu-id="5f67a-105">The **UploadItems** operation is restricted in MicrosoftExchange Server 2010 Service Pack 1 (SP1) to a maximum import payload of 25MB of base64 encoded data.</span></span> <span data-ttu-id="5f67a-106">可以在 web.config 文件中更改该设置。</span><span class="sxs-lookup"><span data-stu-id="5f67a-106">The setting can be altered in the web.config file.</span></span> 
  
## <a name="uploaditems-request-example"></a><span data-ttu-id="5f67a-107">UploadItems 请求示例</span><span class="sxs-lookup"><span data-stu-id="5f67a-107">UploadItems request example</span></span>

### <a name="description"></a><span data-ttu-id="5f67a-108">说明</span><span class="sxs-lookup"><span data-stu-id="5f67a-108">Description</span></span>

<span data-ttu-id="5f67a-109">以下示例的**UploadItems**请求显示如何将两个项目上传到邮箱中。</span><span class="sxs-lookup"><span data-stu-id="5f67a-109">The following example of an **UploadItems** request shows how to upload two items into a mailbox.</span></span> <span data-ttu-id="5f67a-110">第一项是一个新项。</span><span class="sxs-lookup"><span data-stu-id="5f67a-110">The first item is a new item.</span></span> <span data-ttu-id="5f67a-111">第二个项目是邮箱中现有项目的更新版本。</span><span class="sxs-lookup"><span data-stu-id="5f67a-111">The second item is an updated version of an existing item in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5f67a-112">代码</span><span class="sxs-lookup"><span data-stu-id="5f67a-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="5f67a-113">备注</span><span class="sxs-lookup"><span data-stu-id="5f67a-113">Comments</span></span>

<span data-ttu-id="5f67a-114">标识符和项目数据已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="5f67a-114">Identifiers and the item data have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="5f67a-115">Request 元素</span><span class="sxs-lookup"><span data-stu-id="5f67a-115">Request elements</span></span>

<span data-ttu-id="5f67a-116">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f67a-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5f67a-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5f67a-117">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="5f67a-118">UploadItems</span><span class="sxs-lookup"><span data-stu-id="5f67a-118">UploadItems</span></span>](uploaditems.md)
    
- [<span data-ttu-id="5f67a-119">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="5f67a-119">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
    
- [<span data-ttu-id="5f67a-120">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="5f67a-120">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
    
- [<span data-ttu-id="5f67a-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="5f67a-121">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="5f67a-122">Data （base64Binary）</span><span class="sxs-lookup"><span data-stu-id="5f67a-122">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="5f67a-123">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f67a-123">ItemId</span></span>](itemid.md)
    
## <a name="successful-uploaditems-response-example"></a><span data-ttu-id="5f67a-124">成功的 UploadItems 响应示例</span><span class="sxs-lookup"><span data-stu-id="5f67a-124">Successful UploadItems response example</span></span>

### <a name="description"></a><span data-ttu-id="5f67a-125">说明</span><span class="sxs-lookup"><span data-stu-id="5f67a-125">Description</span></span>

<span data-ttu-id="5f67a-126">下面的示例演示对**UploadItems**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5f67a-126">The following example shows a successful response to the **UploadItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5f67a-127">代码</span><span class="sxs-lookup"><span data-stu-id="5f67a-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
                         MinorVersion="1"
                         MajorBuildNumber="164"
                         MinorBuildNumber="0"
                         Version="Exchange2010_SP1"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="5f67a-128">备注</span><span class="sxs-lookup"><span data-stu-id="5f67a-128">Comments</span></span>

<span data-ttu-id="5f67a-129">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="5f67a-129">Item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="5f67a-130">Response 元素</span><span class="sxs-lookup"><span data-stu-id="5f67a-130">Response elements</span></span>

<span data-ttu-id="5f67a-131">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f67a-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5f67a-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f67a-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5f67a-133">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5f67a-133">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="5f67a-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f67a-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5f67a-135">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f67a-135">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="5f67a-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f67a-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f67a-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f67a-137">ItemId</span></span>](itemid.md)
    
## <a name="uploaditems-error-response-example"></a><span data-ttu-id="5f67a-138">UploadItems 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5f67a-138">UploadItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5f67a-139">说明</span><span class="sxs-lookup"><span data-stu-id="5f67a-139">Description</span></span>

<span data-ttu-id="5f67a-140">下面的示例演示对**UploadItems**请求的响应，该请求包含尝试更新无法在邮箱中找到的项目时导致的错误。</span><span class="sxs-lookup"><span data-stu-id="5f67a-140">The following example shows a response to the **UploadItems** request that contains an error caused by an attempt to update an item that cannot be found in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5f67a-141">代码</span><span class="sxs-lookup"><span data-stu-id="5f67a-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="error-response-elements"></a><span data-ttu-id="5f67a-142">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="5f67a-142">Error response elements</span></span>

<span data-ttu-id="5f67a-143">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f67a-143">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5f67a-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f67a-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5f67a-145">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5f67a-145">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="5f67a-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f67a-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5f67a-147">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f67a-147">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="5f67a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="5f67a-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5f67a-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f67a-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f67a-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5f67a-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5f67a-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f67a-151">See also</span></span>



[<span data-ttu-id="5f67a-152">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="5f67a-152">ExportItems operation</span></span>](exportitems-operation.md)


[<span data-ttu-id="5f67a-153">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="5f67a-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="5f67a-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f67a-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

