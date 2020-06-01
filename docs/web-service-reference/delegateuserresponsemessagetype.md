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
description: DelegateUserResponseMessageType 元素包含单个代理用户的响应消息。
ms.openlocfilehash: d7addac2ef05d50e0043490ac20d299ece7d577b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457380"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="2b282-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="2b282-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="2b282-104">**DelegateUserResponseMessageType**元素包含单个代理用户的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2b282-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="2b282-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2b282-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2b282-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b282-106">Attributes and elements</span></span>

<span data-ttu-id="2b282-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b282-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b282-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b282-108">Attributes</span></span>

<span data-ttu-id="2b282-109">无。</span><span class="sxs-lookup"><span data-stu-id="2b282-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b282-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2b282-110">Child elements</span></span>

|<span data-ttu-id="2b282-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b282-111">**Element**</span></span>|<span data-ttu-id="2b282-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b282-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b282-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="2b282-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2b282-114">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="2b282-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2b282-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2b282-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2b282-116">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2b282-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2b282-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2b282-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2b282-118">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="2b282-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2b282-119">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="2b282-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2b282-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2b282-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2b282-121">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="2b282-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2b282-122">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="2b282-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="2b282-123">标识在委派管理响应中返回的单个代理。</span><span class="sxs-lookup"><span data-stu-id="2b282-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b282-124">父元素</span><span class="sxs-lookup"><span data-stu-id="2b282-124">Parent elements</span></span>

|<span data-ttu-id="2b282-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b282-125">**Element**</span></span>|<span data-ttu-id="2b282-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b282-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b282-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="2b282-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="2b282-128">包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2b282-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b282-129">备注</span><span class="sxs-lookup"><span data-stu-id="2b282-129">Remarks</span></span>

<span data-ttu-id="2b282-130">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b282-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b282-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b282-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b282-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b282-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2b282-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b282-133">Schema Name</span></span>  <br/> |<span data-ttu-id="2b282-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="2b282-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2b282-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b282-135">Validation File</span></span>  <br/> |<span data-ttu-id="2b282-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2b282-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2b282-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b282-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b282-138">False</span><span class="sxs-lookup"><span data-stu-id="2b282-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b282-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b282-139">See also</span></span>

- [<span data-ttu-id="2b282-140">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2b282-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="2b282-141">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2b282-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="2b282-142">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2b282-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="2b282-143">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2b282-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="2b282-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2b282-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

