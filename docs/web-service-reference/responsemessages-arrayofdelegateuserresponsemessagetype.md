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
description: ResponseMessages 元素包含 Exchange Web 服务委派管理请求的响应消息。
ms.openlocfilehash: 6b035f4ee46af1750a275e2c61b2cddea06b37a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465455"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a><span data-ttu-id="ee5e2-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="ee5e2-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>

<span data-ttu-id="ee5e2-104">**ResponseMessages**元素包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-104">The **ResponseMessages** element contains the response messages for an Exchange Web Services delegate management request.</span></span> 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="ee5e2-105">**ArrayOfDelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ee5e2-105">**ArrayOfDelegateUserResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee5e2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ee5e2-106">Attributes and elements</span></span>

<span data-ttu-id="ee5e2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee5e2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ee5e2-108">Attributes</span></span>

<span data-ttu-id="ee5e2-109">无。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee5e2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ee5e2-110">Child elements</span></span>

|<span data-ttu-id="ee5e2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee5e2-111">**Element**</span></span>|<span data-ttu-id="ee5e2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee5e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee5e2-113">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="ee5e2-113">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="ee5e2-114">包含用于委派管理操作的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-114">Contains response messages for delegate management operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee5e2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ee5e2-115">Parent elements</span></span>

|<span data-ttu-id="ee5e2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee5e2-116">**Element**</span></span>|<span data-ttu-id="ee5e2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee5e2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee5e2-118">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="ee5e2-118">AddDelegateResponse</span></span>](adddelegateresponse.md) <br/> |<span data-ttu-id="ee5e2-119">包含[AddDelegate 操作](adddelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-119">Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="ee5e2-120">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="ee5e2-120">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="ee5e2-121">包含[GetDelegate 操作](getdelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-121">Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="ee5e2-122">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="ee5e2-122">UpdateDelegateResponse</span></span>](updatedelegateresponse.md) <br/> |<span data-ttu-id="ee5e2-123">包含[UpdateDelegate 操作](updatedelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-123">Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="ee5e2-124">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="ee5e2-124">RemoveDelegateResponse</span></span>](removedelegateresponse.md) <br/> |<span data-ttu-id="ee5e2-125">包含[RemoveDelegate 操作](removedelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-125">Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee5e2-126">备注</span><span class="sxs-lookup"><span data-stu-id="ee5e2-126">Remarks</span></span>

<span data-ttu-id="ee5e2-127">此元素在[AddDelegate 操作](adddelegate-operation.md)、 [GetDelegate 操作](getdelegate-operation.md)、 [UpdateDelegate 操作](updatedelegate-operation.md)和[RemoveDelegate 操作](removedelegate-operation.md)中使用。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-127">This element is used in the [AddDelegate operation](adddelegate-operation.md), the [GetDelegate operation](getdelegate-operation.md), the [UpdateDelegate operation](updatedelegate-operation.md), and the [RemoveDelegate operation](removedelegate-operation.md).</span></span> <span data-ttu-id="ee5e2-128">委派管理操作响应的结构不同于其他响应。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-128">The delegate management operation responses are structured differently than other responses.</span></span> <span data-ttu-id="ee5e2-129">委托管理响应消息是强类型的。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-129">The delegate management response messages are strongly typed.</span></span>
  
<span data-ttu-id="ee5e2-130">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ee5e2-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee5e2-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="ee5e2-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee5e2-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="ee5e2-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ee5e2-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="ee5e2-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ee5e2-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="ee5e2-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ee5e2-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="ee5e2-135">Validation File</span></span>  <br/> |<span data-ttu-id="ee5e2-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ee5e2-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ee5e2-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="ee5e2-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee5e2-138">False</span><span class="sxs-lookup"><span data-stu-id="ee5e2-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee5e2-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee5e2-139">See also</span></span>



[<span data-ttu-id="ee5e2-140">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ee5e2-140">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="ee5e2-141">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ee5e2-141">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="ee5e2-142">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ee5e2-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
  
[<span data-ttu-id="ee5e2-143">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ee5e2-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="ee5e2-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ee5e2-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

