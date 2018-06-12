---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: RemoveDelegateResponse 元素包含状态和 RemoveDelegate 操作请求的结果。
ms.openlocfilehash: 45d0bcfaeb4d453f50cce8449f5cb7fdb70512a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827092"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="0581b-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="0581b-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="0581b-104">**RemoveDelegateResponse**元素包含状态和[RemoveDelegate 操作](removedelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="0581b-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="0581b-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0581b-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0581b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0581b-106">Attributes and elements</span></span>

<span data-ttu-id="0581b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0581b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0581b-108">属性</span><span class="sxs-lookup"><span data-stu-id="0581b-108">Attributes</span></span>

<span data-ttu-id="0581b-109">无。</span><span class="sxs-lookup"><span data-stu-id="0581b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0581b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0581b-110">Child elements</span></span>

|<span data-ttu-id="0581b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0581b-111">**Element**</span></span>|<span data-ttu-id="0581b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0581b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0581b-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="0581b-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="0581b-114">包含为 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0581b-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="0581b-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="0581b-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0581b-116">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0581b-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0581b-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0581b-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0581b-118">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0581b-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0581b-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0581b-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0581b-120">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0581b-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0581b-121">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="0581b-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0581b-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0581b-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0581b-123">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0581b-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0581b-124">父元素</span><span class="sxs-lookup"><span data-stu-id="0581b-124">Parent elements</span></span>

<span data-ttu-id="0581b-125">无。</span><span class="sxs-lookup"><span data-stu-id="0581b-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0581b-126">备注</span><span class="sxs-lookup"><span data-stu-id="0581b-126">Remarks</span></span>

<span data-ttu-id="0581b-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0581b-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0581b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="0581b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0581b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="0581b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0581b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="0581b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0581b-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="0581b-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0581b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="0581b-132">Validation File</span></span>  <br/> |<span data-ttu-id="0581b-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0581b-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0581b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="0581b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0581b-135">False</span><span class="sxs-lookup"><span data-stu-id="0581b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0581b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0581b-136">See also</span></span>



[<span data-ttu-id="0581b-137">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="0581b-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="0581b-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0581b-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

