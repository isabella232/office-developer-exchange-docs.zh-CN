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
description: GetDelegateResponse 元素包含状态和 GetDelegate 操作请求的结果。
ms.openlocfilehash: 52731ea66420c21cf3fb8d19082aef65551c2af2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754512"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="52356-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="52356-103">GetDelegateResponse</span></span>

<span data-ttu-id="52356-104">**GetDelegateResponse**元素包含状态和[GetDelegate 操作](getdelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="52356-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="52356-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="52356-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52356-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52356-106">Attributes and elements</span></span>

<span data-ttu-id="52356-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52356-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52356-108">属性</span><span class="sxs-lookup"><span data-stu-id="52356-108">Attributes</span></span>

<span data-ttu-id="52356-109">无。</span><span class="sxs-lookup"><span data-stu-id="52356-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52356-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52356-110">Child elements</span></span>

|<span data-ttu-id="52356-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="52356-111">**Element**</span></span>|<span data-ttu-id="52356-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="52356-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52356-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="52356-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="52356-114">定义委托和主体之间确定如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="52356-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="52356-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="52356-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="52356-116">包含为 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="52356-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="52356-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="52356-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="52356-118">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="52356-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="52356-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="52356-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="52356-120">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="52356-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="52356-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="52356-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="52356-122">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="52356-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="52356-123">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="52356-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="52356-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="52356-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="52356-125">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="52356-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52356-126">父元素</span><span class="sxs-lookup"><span data-stu-id="52356-126">Parent elements</span></span>

<span data-ttu-id="52356-127">无。</span><span class="sxs-lookup"><span data-stu-id="52356-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52356-128">备注</span><span class="sxs-lookup"><span data-stu-id="52356-128">Remarks</span></span>

<span data-ttu-id="52356-129">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52356-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52356-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="52356-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52356-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="52356-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52356-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="52356-132">Schema Name</span></span>  <br/> |<span data-ttu-id="52356-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="52356-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52356-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="52356-134">Validation File</span></span>  <br/> |<span data-ttu-id="52356-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52356-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52356-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="52356-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="52356-137">False</span><span class="sxs-lookup"><span data-stu-id="52356-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52356-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52356-138">See also</span></span>



[<span data-ttu-id="52356-139">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="52356-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="52356-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52356-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

