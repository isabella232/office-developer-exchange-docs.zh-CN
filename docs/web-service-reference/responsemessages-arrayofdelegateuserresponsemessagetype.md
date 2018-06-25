---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: ResponseMessages 元素包含 Exchange Web 服务代理管理请求的响应消息。
ms.openlocfilehash: e4b5567f3ded003e9648eb8ebebfadf8f1748d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827193"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a><span data-ttu-id="973e5-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="973e5-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>

<span data-ttu-id="973e5-104">**ResponseMessages**元素包含 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="973e5-104">The **ResponseMessages** element contains the response messages for an Exchange Web Services delegate management request.</span></span> 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="973e5-105">**ArrayOfDelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="973e5-105">**ArrayOfDelegateUserResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="973e5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="973e5-106">Attributes and elements</span></span>

<span data-ttu-id="973e5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="973e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="973e5-108">属性</span><span class="sxs-lookup"><span data-stu-id="973e5-108">Attributes</span></span>

<span data-ttu-id="973e5-109">无。</span><span class="sxs-lookup"><span data-stu-id="973e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="973e5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="973e5-110">Child elements</span></span>

|<span data-ttu-id="973e5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="973e5-111">**Element**</span></span>|<span data-ttu-id="973e5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="973e5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="973e5-113">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="973e5-113">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="973e5-114">包含委派管理操作的响应消息。</span><span class="sxs-lookup"><span data-stu-id="973e5-114">Contains response messages for delegate management operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="973e5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="973e5-115">Parent elements</span></span>

|<span data-ttu-id="973e5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="973e5-116">**Element**</span></span>|<span data-ttu-id="973e5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="973e5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="973e5-118">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="973e5-118">AddDelegateResponse</span></span>](adddelegateresponse.md) <br/> |<span data-ttu-id="973e5-119">包含状态和[AddDelegate 操作](adddelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="973e5-119">Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="973e5-120">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="973e5-120">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="973e5-121">包含状态和[GetDelegate 操作](getdelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="973e5-121">Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="973e5-122">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="973e5-122">UpdateDelegateResponse</span></span>](updatedelegateresponse.md) <br/> |<span data-ttu-id="973e5-123">包含状态和[UpdateDelegate 操作](updatedelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="973e5-123">Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="973e5-124">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="973e5-124">RemoveDelegateResponse</span></span>](removedelegateresponse.md) <br/> |<span data-ttu-id="973e5-125">包含状态和[RemoveDelegate 操作](removedelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="973e5-125">Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="973e5-126">注解</span><span class="sxs-lookup"><span data-stu-id="973e5-126">Remarks</span></span>

<span data-ttu-id="973e5-127">[AddDelegate 操作](adddelegate-operation.md)、 [GetDelegate 操作](getdelegate-operation.md)、 [UpdateDelegate 操作](updatedelegate-operation.md)和[RemoveDelegate 操作](removedelegate-operation.md)中使用此元素。</span><span class="sxs-lookup"><span data-stu-id="973e5-127">This element is used in the [AddDelegate operation](adddelegate-operation.md), the [GetDelegate operation](getdelegate-operation.md), the [UpdateDelegate operation](updatedelegate-operation.md), and the [RemoveDelegate operation](removedelegate-operation.md).</span></span> <span data-ttu-id="973e5-128">委托管理操作响应的不同于其他响应结构。</span><span class="sxs-lookup"><span data-stu-id="973e5-128">The delegate management operation responses are structured differently than other responses.</span></span> <span data-ttu-id="973e5-129">委托管理响应消息是强类型。</span><span class="sxs-lookup"><span data-stu-id="973e5-129">The delegate management response messages are strongly typed.</span></span>
  
<span data-ttu-id="973e5-130">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="973e5-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="973e5-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="973e5-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="973e5-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="973e5-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="973e5-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="973e5-133">Schema Name</span></span>  <br/> |<span data-ttu-id="973e5-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="973e5-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="973e5-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="973e5-135">Validation File</span></span>  <br/> |<span data-ttu-id="973e5-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="973e5-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="973e5-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="973e5-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="973e5-138">False</span><span class="sxs-lookup"><span data-stu-id="973e5-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="973e5-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="973e5-139">See also</span></span>



[<span data-ttu-id="973e5-140">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="973e5-140">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="973e5-141">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="973e5-141">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="973e5-142">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="973e5-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
  
[<span data-ttu-id="973e5-143">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="973e5-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="973e5-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="973e5-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

