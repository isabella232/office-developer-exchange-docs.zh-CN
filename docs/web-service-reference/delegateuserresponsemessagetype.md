---
title: DelegateUserResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUserResponseMessageType
api_type:
- schema
ms.assetid: 3dc9552c-1e2d-40ac-a137-827883c2bb88
description: DelegateUserResponseMessageType 元素包含单个委托用户响应消息。
ms.openlocfilehash: ac99e0ca219fc1f1e117f9288d895e27a1df4700
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753784"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="2d6b0-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="2d6b0-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="2d6b0-104">**DelegateUserResponseMessageType**元素包含单个委托用户响应消息。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="2d6b0-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2d6b0-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2d6b0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d6b0-106">Attributes and elements</span></span>

<span data-ttu-id="2d6b0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d6b0-108">属性</span><span class="sxs-lookup"><span data-stu-id="2d6b0-108">Attributes</span></span>

<span data-ttu-id="2d6b0-109">无。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d6b0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d6b0-110">Child elements</span></span>

|<span data-ttu-id="2d6b0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d6b0-111">**Element**</span></span>|<span data-ttu-id="2d6b0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d6b0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d6b0-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="2d6b0-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2d6b0-114">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2d6b0-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2d6b0-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2d6b0-116">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2d6b0-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2d6b0-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2d6b0-118">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2d6b0-119">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2d6b0-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2d6b0-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2d6b0-121">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2d6b0-122">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="2d6b0-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="2d6b0-123">标识委派管理响应中返回单个委托。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d6b0-124">父元素</span><span class="sxs-lookup"><span data-stu-id="2d6b0-124">Parent elements</span></span>

|<span data-ttu-id="2d6b0-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d6b0-125">**Element**</span></span>|<span data-ttu-id="2d6b0-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d6b0-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d6b0-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="2d6b0-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="2d6b0-128">包含为 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d6b0-129">注解</span><span class="sxs-lookup"><span data-stu-id="2d6b0-129">Remarks</span></span>

<span data-ttu-id="2d6b0-130">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d6b0-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d6b0-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d6b0-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d6b0-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d6b0-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d6b0-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d6b0-133">Schema Name</span></span>  <br/> |<span data-ttu-id="2d6b0-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="2d6b0-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d6b0-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d6b0-135">Validation File</span></span>  <br/> |<span data-ttu-id="2d6b0-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d6b0-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d6b0-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d6b0-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d6b0-138">False</span><span class="sxs-lookup"><span data-stu-id="2d6b0-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d6b0-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d6b0-139">See also</span></span>

- [<span data-ttu-id="2d6b0-140">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2d6b0-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="2d6b0-141">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2d6b0-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="2d6b0-142">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2d6b0-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="2d6b0-143">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2d6b0-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="2d6b0-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d6b0-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

