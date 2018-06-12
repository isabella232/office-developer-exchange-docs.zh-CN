---
title: UpdateDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegateResponse
api_type:
- schema
ms.assetid: cd336add-fbcc-4f61-9867-d4c08a60e142
description: UpdateDelegateResponse 元素包含状态和 UpdateDelegate 操作请求的结果。
ms.openlocfilehash: b90dd7d8011cf75831481b8f2b92df80d9a67d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838358"
---
# <a name="updatedelegateresponse"></a><span data-ttu-id="e9cbe-103">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e9cbe-103">UpdateDelegateResponse</span></span>

<span data-ttu-id="e9cbe-104">**UpdateDelegateResponse**元素包含状态和[UpdateDelegate 操作](updatedelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-104">The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span> 
  
```xml
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 <span data-ttu-id="e9cbe-105">**UpdateDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e9cbe-105">**UpdateDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9cbe-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e9cbe-106">Attributes and elements</span></span>

<span data-ttu-id="e9cbe-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9cbe-108">属性</span><span class="sxs-lookup"><span data-stu-id="e9cbe-108">Attributes</span></span>

<span data-ttu-id="e9cbe-109">无。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9cbe-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e9cbe-110">Child elements</span></span>

|<span data-ttu-id="e9cbe-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9cbe-111">**Element**</span></span>|<span data-ttu-id="e9cbe-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9cbe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9cbe-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="e9cbe-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="e9cbe-114">包含为 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="e9cbe-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="e9cbe-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e9cbe-116">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e9cbe-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9cbe-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e9cbe-118">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e9cbe-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e9cbe-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e9cbe-120">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="e9cbe-121">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e9cbe-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e9cbe-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e9cbe-123">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9cbe-124">父元素</span><span class="sxs-lookup"><span data-stu-id="e9cbe-124">Parent elements</span></span>

<span data-ttu-id="e9cbe-125">无。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9cbe-126">备注</span><span class="sxs-lookup"><span data-stu-id="e9cbe-126">Remarks</span></span>

<span data-ttu-id="e9cbe-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e9cbe-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9cbe-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="e9cbe-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9cbe-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="e9cbe-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e9cbe-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="e9cbe-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e9cbe-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="e9cbe-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e9cbe-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="e9cbe-132">Validation File</span></span>  <br/> |<span data-ttu-id="e9cbe-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e9cbe-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e9cbe-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="e9cbe-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9cbe-135">False</span><span class="sxs-lookup"><span data-stu-id="e9cbe-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9cbe-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9cbe-136">See also</span></span>



[<span data-ttu-id="e9cbe-137">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="e9cbe-137">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="e9cbe-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e9cbe-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

