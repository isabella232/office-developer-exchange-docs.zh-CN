---
title: 删除项操作
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
description: 删除项操作删除 Exchange 存储中的项目。
ms.openlocfilehash: 87d7853daa5db0cd87b3f6469c228a584b4d9caf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753811"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="a63e5-103">删除项操作</span><span class="sxs-lookup"><span data-stu-id="a63e5-103">DeleteItem operation</span></span>

<span data-ttu-id="a63e5-104">**删除项**操作删除 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="a63e5-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a63e5-105">代理尝试通过设置 DisposalType 为 MoveToDeletedItems 删除的主体的邮箱中的项目时，将**删除项**操作返回错误响应，其中包括 ErrorCannotDeleteObject 错误代码。</span><span class="sxs-lookup"><span data-stu-id="a63e5-105">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems.</span></span> <span data-ttu-id="a63e5-106">若要将其移动到已删除邮件文件夹中删除项，代理人必须使用[MoveItem 操作](moveitem-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="a63e5-106">To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="a63e5-107">删除项请求示例</span><span class="sxs-lookup"><span data-stu-id="a63e5-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="a63e5-108">说明</span><span class="sxs-lookup"><span data-stu-id="a63e5-108">Description</span></span>

<span data-ttu-id="a63e5-109">**删除项**请求的下面的示例演示如何从邮箱执行硬删除的项目。</span><span class="sxs-lookup"><span data-stu-id="a63e5-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a63e5-110">已缩短项目 ID 以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="a63e5-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a63e5-111">代码</span><span class="sxs-lookup"><span data-stu-id="a63e5-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="a63e5-112">请求元素</span><span class="sxs-lookup"><span data-stu-id="a63e5-112">Request elements</span></span>

<span data-ttu-id="a63e5-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a63e5-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a63e5-114">删除项</span><span class="sxs-lookup"><span data-stu-id="a63e5-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="a63e5-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a63e5-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="a63e5-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="a63e5-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="a63e5-117">若要查找的请求邮件**删除项**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a63e5-117">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a63e5-118">在[删除项](deleteitem.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a63e5-118">Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="a63e5-119">成功的删除项响应</span><span class="sxs-lookup"><span data-stu-id="a63e5-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="a63e5-120">说明</span><span class="sxs-lookup"><span data-stu-id="a63e5-120">Description</span></span>

<span data-ttu-id="a63e5-121">下面的示例演示对**删除项**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="a63e5-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a63e5-122">代码</span><span class="sxs-lookup"><span data-stu-id="a63e5-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="a63e5-123">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="a63e5-123">Successful response elements</span></span>

<span data-ttu-id="a63e5-124">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a63e5-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a63e5-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a63e5-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a63e5-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="a63e5-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="a63e5-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a63e5-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a63e5-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a63e5-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="a63e5-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a63e5-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="a63e5-130">若要查找的响应消息**删除项**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a63e5-130">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a63e5-131">启动[DeleteItemResponse](deleteitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="a63e5-131">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="a63e5-132">删除项错误响应</span><span class="sxs-lookup"><span data-stu-id="a63e5-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="a63e5-133">说明</span><span class="sxs-lookup"><span data-stu-id="a63e5-133">Description</span></span>

<span data-ttu-id="a63e5-134">下面的示例演示一个**删除项**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="a63e5-134">The following example shows an error response to a **DeleteItem** request.</span></span> <span data-ttu-id="a63e5-135">创建错误，因为该操作尝试删除找不到项 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="a63e5-135">The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a63e5-136">代码</span><span class="sxs-lookup"><span data-stu-id="a63e5-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="a63e5-137">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="a63e5-137">Error response elements</span></span>

<span data-ttu-id="a63e5-138">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a63e5-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a63e5-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a63e5-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a63e5-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="a63e5-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="a63e5-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a63e5-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a63e5-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a63e5-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="a63e5-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="a63e5-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a63e5-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a63e5-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a63e5-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a63e5-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="a63e5-146">若要查找错误响应消息的**删除项**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a63e5-146">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a63e5-147">启动[DeleteItemResponse](deleteitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="a63e5-147">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a63e5-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a63e5-148">See also</span></span>

- [<span data-ttu-id="a63e5-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a63e5-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="a63e5-150">删除联系人</span><span class="sxs-lookup"><span data-stu-id="a63e5-150">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="a63e5-151">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="a63e5-151">Deleting E-mail Messages</span></span>](http://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="a63e5-152">删除任务</span><span class="sxs-lookup"><span data-stu-id="a63e5-152">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

