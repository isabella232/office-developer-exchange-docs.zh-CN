---
title: GetDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegateResponse
api_type:
- schema
ms.assetid: 71a418a5-5652-40e1-8f84-fe4f7c9f86af
description: GetDelegateResponse 元素包含 GetDelegate 操作请求的状态和结果。
ms.openlocfilehash: 81c5033cd67b79baa131d71ea0b866c788ae5e82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462022"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="36a34-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="36a34-103">GetDelegateResponse</span></span>

<span data-ttu-id="36a34-104">**GetDelegateResponse**元素包含[GetDelegate 操作](getdelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="36a34-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
```xml
<GetDelegateResponse>
   <DeliverMeetingRequests/>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</GetDelegateResponse>
```

 <span data-ttu-id="36a34-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="36a34-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36a34-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36a34-106">Attributes and elements</span></span>

<span data-ttu-id="36a34-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36a34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36a34-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="36a34-108">Attributes</span></span>

<span data-ttu-id="36a34-109">无。</span><span class="sxs-lookup"><span data-stu-id="36a34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36a34-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36a34-110">Child elements</span></span>

|<span data-ttu-id="36a34-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="36a34-111">**Element**</span></span>|<span data-ttu-id="36a34-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="36a34-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36a34-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="36a34-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="36a34-114">定义在委托和主体之间如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="36a34-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="36a34-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="36a34-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="36a34-116">包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="36a34-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="36a34-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="36a34-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="36a34-118">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="36a34-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="36a34-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="36a34-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="36a34-120">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="36a34-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="36a34-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="36a34-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="36a34-122">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="36a34-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="36a34-123">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="36a34-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="36a34-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="36a34-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="36a34-125">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="36a34-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36a34-126">父元素</span><span class="sxs-lookup"><span data-stu-id="36a34-126">Parent elements</span></span>

<span data-ttu-id="36a34-127">无。</span><span class="sxs-lookup"><span data-stu-id="36a34-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36a34-128">说明</span><span class="sxs-lookup"><span data-stu-id="36a34-128">Remarks</span></span>

<span data-ttu-id="36a34-129">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="36a34-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36a34-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="36a34-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36a34-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="36a34-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36a34-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="36a34-132">Schema Name</span></span>  <br/> |<span data-ttu-id="36a34-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="36a34-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="36a34-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="36a34-134">Validation File</span></span>  <br/> |<span data-ttu-id="36a34-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36a34-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36a34-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="36a34-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="36a34-137">False</span><span class="sxs-lookup"><span data-stu-id="36a34-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36a34-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36a34-138">See also</span></span>



[<span data-ttu-id="36a34-139">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="36a34-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="36a34-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="36a34-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

