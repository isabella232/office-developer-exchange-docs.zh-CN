---
title: AddDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegateResponse
api_type:
- schema
ms.assetid: d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429
description: AddDelegateResponse 元素包含状态和 AddDelegate 操作请求的结果。
ms.openlocfilehash: a1d56e9994b3a7916fe0fbe40be1e6d8ff473730
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753102"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="008bd-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="008bd-103">AddDelegateResponse</span></span>

<span data-ttu-id="008bd-104">**AddDelegateResponse**元素包含状态和[AddDelegate 操作](adddelegate-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="008bd-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="008bd-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="008bd-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="008bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="008bd-106">Attributes and elements</span></span>

<span data-ttu-id="008bd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="008bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="008bd-108">属性</span><span class="sxs-lookup"><span data-stu-id="008bd-108">Attributes</span></span>

<span data-ttu-id="008bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="008bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="008bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="008bd-110">Child elements</span></span>

|<span data-ttu-id="008bd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="008bd-111">**Element**</span></span>|<span data-ttu-id="008bd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="008bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="008bd-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="008bd-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="008bd-114">包含为 Exchange Web 服务代理管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="008bd-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="008bd-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="008bd-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="008bd-116">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="008bd-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="008bd-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="008bd-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="008bd-118">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="008bd-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="008bd-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="008bd-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="008bd-120">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="008bd-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="008bd-121">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="008bd-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="008bd-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="008bd-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="008bd-123">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="008bd-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="008bd-124">父元素</span><span class="sxs-lookup"><span data-stu-id="008bd-124">Parent elements</span></span>

<span data-ttu-id="008bd-125">无。</span><span class="sxs-lookup"><span data-stu-id="008bd-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="008bd-126">注解</span><span class="sxs-lookup"><span data-stu-id="008bd-126">Remarks</span></span>

<span data-ttu-id="008bd-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="008bd-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="008bd-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="008bd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="008bd-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="008bd-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="008bd-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="008bd-130">Schema Name</span></span>  <br/> |<span data-ttu-id="008bd-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="008bd-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="008bd-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="008bd-132">Validation File</span></span>  <br/> |<span data-ttu-id="008bd-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="008bd-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="008bd-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="008bd-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="008bd-135">False</span><span class="sxs-lookup"><span data-stu-id="008bd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="008bd-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="008bd-136">See also</span></span>

- [<span data-ttu-id="008bd-137">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="008bd-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="008bd-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="008bd-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="008bd-139">添加代理人</span><span class="sxs-lookup"><span data-stu-id="008bd-139">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

