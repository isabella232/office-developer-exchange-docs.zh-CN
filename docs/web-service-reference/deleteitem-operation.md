---
title: DeleteItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: DeleteItem 操作删除 Exchange 存储中的项目。
ms.openlocfilehash: f068e08ef0d0f590c9ed8274f77d4dae9f942995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526933"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="e116f-103">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="e116f-103">DeleteItem operation</span></span>

<span data-ttu-id="e116f-104">**DeleteItem**操作删除 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="e116f-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e116f-105">如果代理尝试通过将 DisposalType 设置为 MoveToDeletedItems 来删除主体邮箱中**的项目**，则将返回包含 ErrorCannotDeleteObject 错误代码的错误响应。</span><span class="sxs-lookup"><span data-stu-id="e116f-105">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems.</span></span> <span data-ttu-id="e116f-106">若要通过将项目移动到 "已删除邮件" 文件夹来删除项目，代理必须使用[MoveItem 操作](moveitem-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="e116f-106">To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="e116f-107">DeleteItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="e116f-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="e116f-108">Description</span><span class="sxs-lookup"><span data-stu-id="e116f-108">Description</span></span>

<span data-ttu-id="e116f-109">以下示例的**DeleteItem**请求显示如何从邮箱中执行项的硬删除。</span><span class="sxs-lookup"><span data-stu-id="e116f-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e116f-110">项目 ID 已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="e116f-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e116f-111">代码</span><span class="sxs-lookup"><span data-stu-id="e116f-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="e116f-112">Request 元素</span><span class="sxs-lookup"><span data-stu-id="e116f-112">Request elements</span></span>

<span data-ttu-id="e116f-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e116f-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e116f-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="e116f-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="e116f-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="e116f-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="e116f-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="e116f-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="e116f-117">若要查找**DeleteItem**操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="e116f-117">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="e116f-118">从[DeleteItem](deleteitem.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="e116f-118">Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="e116f-119">成功的 DeleteItem 响应</span><span class="sxs-lookup"><span data-stu-id="e116f-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="e116f-120">Description</span><span class="sxs-lookup"><span data-stu-id="e116f-120">Description</span></span>

<span data-ttu-id="e116f-121">下面的示例演示对**DeleteItem**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e116f-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e116f-122">代码</span><span class="sxs-lookup"><span data-stu-id="e116f-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="e116f-123">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="e116f-123">Successful response elements</span></span>

<span data-ttu-id="e116f-124">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e116f-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e116f-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e116f-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e116f-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="e116f-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="e116f-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e116f-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e116f-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e116f-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="e116f-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e116f-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="e116f-130">若要查找**DeleteItem**操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="e116f-130">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="e116f-131">从[DeleteItemResponse](deleteitemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="e116f-131">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="e116f-132">DeleteItem 错误响应</span><span class="sxs-lookup"><span data-stu-id="e116f-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="e116f-133">Description</span><span class="sxs-lookup"><span data-stu-id="e116f-133">Description</span></span>

<span data-ttu-id="e116f-134">下面的示例演示对**DeleteItem**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="e116f-134">The following example shows an error response to a **DeleteItem** request.</span></span> <span data-ttu-id="e116f-135">由于操作尝试删除在 Exchange 存储中找不到的项目，因此创建了错误。</span><span class="sxs-lookup"><span data-stu-id="e116f-135">The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e116f-136">代码</span><span class="sxs-lookup"><span data-stu-id="e116f-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="e116f-137">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="e116f-137">Error response elements</span></span>

<span data-ttu-id="e116f-138">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e116f-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="e116f-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e116f-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e116f-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="e116f-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="e116f-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e116f-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e116f-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e116f-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="e116f-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="e116f-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e116f-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e116f-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e116f-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e116f-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e116f-146">若要查找**DeleteItem**操作的错误响应消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="e116f-146">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="e116f-147">从[DeleteItemResponse](deleteitemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="e116f-147">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e116f-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e116f-148">See also</span></span>

- [<span data-ttu-id="e116f-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e116f-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e116f-150">删除联系人</span><span class="sxs-lookup"><span data-stu-id="e116f-150">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="e116f-151">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="e116f-151">Deleting E-mail Messages</span></span>](https://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="e116f-152">删除任务</span><span class="sxs-lookup"><span data-stu-id="e116f-152">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

