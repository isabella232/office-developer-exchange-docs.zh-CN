---
title: ApplyConversationAction 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: 73d7943d-d361-4f8b-9948-d85f886efa1a
description: ApplyConversationAction 操作设置一次性或跟进对话中的所有项的操作。 ApplyConversationAction 操作可以分类、 移动、 复制、 删除和对话中的所有项设置的只读的状态。 此外可以在对话中的新邮件设置操作。
ms.openlocfilehash: 2a485b84ee87aec2ed807e3f4f0901b83432fa0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753192"
---
# <a name="applyconversationaction-operation"></a><span data-ttu-id="28d1f-105">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="28d1f-105">ApplyConversationAction operation</span></span>

<span data-ttu-id="28d1f-106">**ApplyConversationAction**操作设置一次性或跟进对话中的所有项的操作。</span><span class="sxs-lookup"><span data-stu-id="28d1f-106">The **ApplyConversationAction** operation sets a one-time or follow up action on all the items in a conversation.</span></span> <span data-ttu-id="28d1f-107">**ApplyConversationAction**操作可以分类、 移动、 复制、 删除和对话中的所有项设置的只读的状态。</span><span class="sxs-lookup"><span data-stu-id="28d1f-107">The **ApplyConversationAction** operation allows you to categorize, move, copy, delete, and set the read state on all items in a conversation.</span></span> <span data-ttu-id="28d1f-108">此外可以在对话中的新邮件设置操作。</span><span class="sxs-lookup"><span data-stu-id="28d1f-108">Actions can also be set for new messages in a conversation.</span></span> 
  
## <a name="applyconversationaction-request-example"></a><span data-ttu-id="28d1f-109">ApplyConversationAction 请求示例</span><span class="sxs-lookup"><span data-stu-id="28d1f-109">ApplyConversationAction request example</span></span>

### <a name="description"></a><span data-ttu-id="28d1f-110">说明</span><span class="sxs-lookup"><span data-stu-id="28d1f-110">Description</span></span>

<span data-ttu-id="28d1f-111">**ApplyConversationAction**请求的下面的示例演示如何将指定的对话中的项目移至另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="28d1f-111">The following example of an **ApplyConversationAction** request shows how to move the items in the specified conversation to another folder.</span></span> <span data-ttu-id="28d1f-112">添加到对话的项目还将移到指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="28d1f-112">Items that are added to the conversation will also be moved to the specified folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="28d1f-113">代码</span><span class="sxs-lookup"><span data-stu-id="28d1f-113">Code</span></span>

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
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="AAQkADVkNjM1EH39AWcDUGrnrnJ32hHpdc="/>
          <t:DestinationFolderId>
            <t:FolderId Id="AAMkADVkNjM1ODI3LTEwYTAtNDUBTTT6tWal35iSoKAAAABZZWAAA="/>
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

### <a name="remarks"></a><span data-ttu-id="28d1f-114">注解</span><span class="sxs-lookup"><span data-stu-id="28d1f-114">Remarks</span></span>

<span data-ttu-id="28d1f-115">对话和文件夹标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="28d1f-115">The conversation and folder identifiers have been shortened to preserve readability.</span></span>
  
## <a name="applyconversationaction-response-example"></a><span data-ttu-id="28d1f-116">ApplyConversationAction 响应示例</span><span class="sxs-lookup"><span data-stu-id="28d1f-116">ApplyConversationAction response example</span></span>

### <a name="description"></a><span data-ttu-id="28d1f-117">说明</span><span class="sxs-lookup"><span data-stu-id="28d1f-117">Description</span></span>

<span data-ttu-id="28d1f-118">下面的示例演示对**ApplyConversationAction**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="28d1f-118">The following example shows a successful response to an **ApplyConversationAction** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="28d1f-119">代码</span><span class="sxs-lookup"><span data-stu-id="28d1f-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ApplyConversationActionResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ApplyConversationActionResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:ApplyConversationActionResponseMessage>
      </m:ResponseMessages>
    </m:ApplyConversationActionResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="28d1f-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28d1f-120">See also</span></span>

- [<span data-ttu-id="28d1f-121">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="28d1f-121">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="28d1f-122">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="28d1f-122">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="28d1f-123">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="28d1f-123">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="28d1f-124">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="28d1f-124">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

