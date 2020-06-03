---
title: DeleteAttachment 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: DeleteAttachment 操作用于从 Exchange 存储中的现有项目中删除文件和项目附件。
ms.openlocfilehash: 1d34ce4c5ba1d955989a35dafb8ab3c5d229d505
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457331"
---
# <a name="deleteattachment-operation"></a><span data-ttu-id="f5dae-103">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="f5dae-103">DeleteAttachment operation</span></span>

<span data-ttu-id="f5dae-104">DeleteAttachment 操作用于从 Exchange 存储中的现有项目中删除文件和项目附件。</span><span class="sxs-lookup"><span data-stu-id="f5dae-104">The DeleteAttachment operation is used to delete file and item attachments from an existing item in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5dae-105">备注</span><span class="sxs-lookup"><span data-stu-id="f5dae-105">Remarks</span></span>

<span data-ttu-id="f5dae-106">此操作允许您按 ID 删除一个或多个附件。</span><span class="sxs-lookup"><span data-stu-id="f5dae-106">This operation allows you to delete one or more attachments by ID.</span></span>
  
## <a name="deleteattachment-request-example"></a><span data-ttu-id="f5dae-107">DeleteAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="f5dae-107">DeleteAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="f5dae-108">Description</span><span class="sxs-lookup"><span data-stu-id="f5dae-108">Description</span></span>

<span data-ttu-id="f5dae-109">以下示例的 DeleteAttachment 请求显示如何删除项目附件。</span><span class="sxs-lookup"><span data-stu-id="f5dae-109">The following example of a DeleteAttachment request shows how to delete an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="f5dae-110">代码</span><span class="sxs-lookup"><span data-stu-id="f5dae-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="f5dae-111">备注</span><span class="sxs-lookup"><span data-stu-id="f5dae-111">Comments</span></span>

<span data-ttu-id="f5dae-112">附件标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="f5dae-112">The attachment identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="f5dae-113">Request 元素</span><span class="sxs-lookup"><span data-stu-id="f5dae-113">Request elements</span></span>

<span data-ttu-id="f5dae-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="f5dae-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="f5dae-115">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="f5dae-115">DeleteAttachment</span></span>](deleteattachment.md)
    
- [<span data-ttu-id="f5dae-116">会话</span><span class="sxs-lookup"><span data-stu-id="f5dae-116">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="f5dae-117">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="f5dae-117">AttachmentId</span></span>](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a><span data-ttu-id="f5dae-118">DeleteAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="f5dae-118">DeleteAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="f5dae-119">Description</span><span class="sxs-lookup"><span data-stu-id="f5dae-119">Description</span></span>

<span data-ttu-id="f5dae-120">下面的示例演示对 DeleteAttachment 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="f5dae-120">The following example shows a successful response to a DeleteAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f5dae-121">代码</span><span class="sxs-lookup"><span data-stu-id="f5dae-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage xsi:type="m:DeleteAttachmentResponseMessageType" ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="AAAtAEFkbWluaXN..." RootItemChangeKey="CQAAABYAA..."/>
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </DeleteAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="f5dae-122">备注</span><span class="sxs-lookup"><span data-stu-id="f5dae-122">Comments</span></span>

<span data-ttu-id="f5dae-123">CreateAttachment 操作返回包含**RootItemId**和**RootItemChangeKey**的 AttachmentIdType 类型的元素。</span><span class="sxs-lookup"><span data-stu-id="f5dae-123">The CreateAttachment operation returns an element of AttachmentIdType type that includes a **RootItemId** and **RootItemChangeKey**.</span></span> <span data-ttu-id="f5dae-124">DeleteAttachment 请求中的标识符不允许使用这些属性。</span><span class="sxs-lookup"><span data-stu-id="f5dae-124">These attributes are not permitted for identifiers within a DeleteAttachment request.</span></span> <span data-ttu-id="f5dae-125">DeleteAttachment 使用 RequestAttachmentIdType 类型的元素，其中不包含这些属性。</span><span class="sxs-lookup"><span data-stu-id="f5dae-125">DeleteAttachment uses elements of type RequestAttachmentIdType, which does not include these attributes.</span></span>
  
<span data-ttu-id="f5dae-126">DeleteAttachment 响应包括父项的 ID。</span><span class="sxs-lookup"><span data-stu-id="f5dae-126">The DeleteAttachment response includes the ID of the parent item.</span></span> <span data-ttu-id="f5dae-127">从项目中删除附件时，将修改项目的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="f5dae-127">When attachments are removed from an item, the item's change key is modified.</span></span> <span data-ttu-id="f5dae-128">可以从 DeleteAttachment 响应中获取新项目更改密钥。</span><span class="sxs-lookup"><span data-stu-id="f5dae-128">The new item change key can be obtained from the DeleteAttachment response.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f5dae-129">[RootItemId](rootitemid.md)标识符和 ChangeKey 已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="f5dae-129">The [RootItemId](rootitemid.md) identifier and ChangeKey have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="f5dae-130">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="f5dae-130">Successful response elements</span></span>

<span data-ttu-id="f5dae-131">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="f5dae-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="f5dae-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f5dae-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="f5dae-133">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="f5dae-133">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
    
- [<span data-ttu-id="f5dae-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f5dae-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f5dae-135">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f5dae-135">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
    
- [<span data-ttu-id="f5dae-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f5dae-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f5dae-137">RootItemId</span><span class="sxs-lookup"><span data-stu-id="f5dae-137">RootItemId</span></span>](rootitemid.md)
    
## <a name="see-also"></a><span data-ttu-id="f5dae-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5dae-138">See also</span></span>

- [<span data-ttu-id="f5dae-139">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="f5dae-139">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="f5dae-140">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="f5dae-140">GetAttachment operation</span></span>](getattachment-operation.md)

