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
description: RemoveDelegateResponse 元素包含 RemoveDelegate 操作请求的状态和结果。
ms.openlocfilehash: 4c7a8b81528435b72576c116bc97f611544c24d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468934"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="65b64-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="65b64-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="65b64-104">**RemoveDelegateResponse**元素包含[RemoveDelegate 操作](removedelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="65b64-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="65b64-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="65b64-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65b64-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="65b64-106">Attributes and elements</span></span>

<span data-ttu-id="65b64-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="65b64-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65b64-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="65b64-108">Attributes</span></span>

<span data-ttu-id="65b64-109">无。</span><span class="sxs-lookup"><span data-stu-id="65b64-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65b64-110">子元素</span><span class="sxs-lookup"><span data-stu-id="65b64-110">Child elements</span></span>

|<span data-ttu-id="65b64-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="65b64-111">**Element**</span></span>|<span data-ttu-id="65b64-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="65b64-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65b64-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="65b64-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="65b64-114">包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="65b64-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="65b64-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="65b64-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="65b64-116">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="65b64-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="65b64-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="65b64-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="65b64-118">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="65b64-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="65b64-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="65b64-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="65b64-120">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="65b64-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="65b64-121">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="65b64-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="65b64-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="65b64-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="65b64-123">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="65b64-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65b64-124">父元素</span><span class="sxs-lookup"><span data-stu-id="65b64-124">Parent elements</span></span>

<span data-ttu-id="65b64-125">无。</span><span class="sxs-lookup"><span data-stu-id="65b64-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65b64-126">说明</span><span class="sxs-lookup"><span data-stu-id="65b64-126">Remarks</span></span>

<span data-ttu-id="65b64-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="65b64-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65b64-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="65b64-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65b64-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="65b64-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65b64-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="65b64-130">Schema Name</span></span>  <br/> |<span data-ttu-id="65b64-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="65b64-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65b64-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="65b64-132">Validation File</span></span>  <br/> |<span data-ttu-id="65b64-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="65b64-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65b64-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="65b64-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="65b64-135">False</span><span class="sxs-lookup"><span data-stu-id="65b64-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65b64-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65b64-136">See also</span></span>



[<span data-ttu-id="65b64-137">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="65b64-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="65b64-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="65b64-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

