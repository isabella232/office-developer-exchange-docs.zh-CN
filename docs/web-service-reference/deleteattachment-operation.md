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
description: DeleteAttachment 操作用于从 Exchange 存储中现有项目中删除文件和项目的附件。
ms.openlocfilehash: 4b94bfd8d6333c1f52be8ad7d0d111ab2a0552b3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753790"
---
# <a name="deleteattachment-operation"></a><span data-ttu-id="46572-103">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="46572-103">DeleteAttachment operation</span></span>

<span data-ttu-id="46572-104">DeleteAttachment 操作用于从 Exchange 存储中现有项目中删除文件和项目的附件。</span><span class="sxs-lookup"><span data-stu-id="46572-104">The DeleteAttachment operation is used to delete file and item attachments from an existing item in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46572-105">注解</span><span class="sxs-lookup"><span data-stu-id="46572-105">Remarks</span></span>

<span data-ttu-id="46572-106">此操作使您可以删除一个或多个附件 id</span><span class="sxs-lookup"><span data-stu-id="46572-106">This operation allows you to delete one or more attachments by ID.</span></span>
  
## <a name="deleteattachment-request-example"></a><span data-ttu-id="46572-107">DeleteAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="46572-107">DeleteAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="46572-108">说明</span><span class="sxs-lookup"><span data-stu-id="46572-108">Description</span></span>

<span data-ttu-id="46572-109">DeleteAttachment 请求的下面的示例演示如何删除项目附件。</span><span class="sxs-lookup"><span data-stu-id="46572-109">The following example of a DeleteAttachment request shows how to delete an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="46572-110">代码</span><span class="sxs-lookup"><span data-stu-id="46572-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="46572-111">注释</span><span class="sxs-lookup"><span data-stu-id="46572-111">Comments</span></span>

<span data-ttu-id="46572-112">已缩短该附件标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="46572-112">The attachment identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="46572-113">请求元素</span><span class="sxs-lookup"><span data-stu-id="46572-113">Request elements</span></span>

<span data-ttu-id="46572-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="46572-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="46572-115">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="46572-115">DeleteAttachment</span></span>](deleteattachment.md)
    
- [<span data-ttu-id="46572-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="46572-116">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="46572-117">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="46572-117">AttachmentId</span></span>](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a><span data-ttu-id="46572-118">DeleteAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="46572-118">DeleteAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="46572-119">说明</span><span class="sxs-lookup"><span data-stu-id="46572-119">Description</span></span>

<span data-ttu-id="46572-120">下面的示例演示对 DeleteAttachment 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="46572-120">The following example shows a successful response to a DeleteAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="46572-121">代码</span><span class="sxs-lookup"><span data-stu-id="46572-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="46572-122">注释</span><span class="sxs-lookup"><span data-stu-id="46572-122">Comments</span></span>

<span data-ttu-id="46572-123">CreateAttachment 操作返回包含**RootItemId**和**RootItemChangeKey**AttachmentIdType 类型的元素。</span><span class="sxs-lookup"><span data-stu-id="46572-123">The CreateAttachment operation returns an element of AttachmentIdType type that includes a **RootItemId** and **RootItemChangeKey**.</span></span> <span data-ttu-id="46572-124">这些属性不允许 DeleteAttachment 请求中的标识符。</span><span class="sxs-lookup"><span data-stu-id="46572-124">These attributes are not permitted for identifiers within a DeleteAttachment request.</span></span> <span data-ttu-id="46572-125">DeleteAttachment 使用类型 RequestAttachmentIdType，不包括这些属性的元素。</span><span class="sxs-lookup"><span data-stu-id="46572-125">DeleteAttachment uses elements of type RequestAttachmentIdType, which does not include these attributes.</span></span>
  
<span data-ttu-id="46572-126">DeleteAttachment 响应包括父项的 ID。</span><span class="sxs-lookup"><span data-stu-id="46572-126">The DeleteAttachment response includes the ID of the parent item.</span></span> <span data-ttu-id="46572-127">当从项目中删除附件时，修改项的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="46572-127">When attachments are removed from an item, the item's change key is modified.</span></span> <span data-ttu-id="46572-128">新的项目更改密钥可以从 DeleteAttachment 响应。</span><span class="sxs-lookup"><span data-stu-id="46572-128">The new item change key can be obtained from the DeleteAttachment response.</span></span>
  
> [!NOTE]
> <span data-ttu-id="46572-129">已缩短[RootItemId](rootitemid.md)标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="46572-129">The [RootItemId](rootitemid.md) identifier and ChangeKey have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="46572-130">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="46572-130">Successful response elements</span></span>

<span data-ttu-id="46572-131">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="46572-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="46572-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="46572-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="46572-133">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="46572-133">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
    
- [<span data-ttu-id="46572-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="46572-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="46572-135">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="46572-135">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
    
- [<span data-ttu-id="46572-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="46572-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="46572-137">RootItemId</span><span class="sxs-lookup"><span data-stu-id="46572-137">RootItemId</span></span>](rootitemid.md)
    
## <a name="see-also"></a><span data-ttu-id="46572-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46572-138">See also</span></span>

- [<span data-ttu-id="46572-139">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="46572-139">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="46572-140">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="46572-140">GetAttachment operation</span></span>](getattachment-operation.md)

