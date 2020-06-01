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
description: AddDelegateResponse 元素包含 AddDelegate 操作请求的状态和结果。
ms.openlocfilehash: 1c38563ab38facf89fd5eab119542374949244c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466456"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="7e8cc-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="7e8cc-103">AddDelegateResponse</span></span>

<span data-ttu-id="7e8cc-104">**AddDelegateResponse**元素包含[AddDelegate 操作](adddelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="7e8cc-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7e8cc-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e8cc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e8cc-106">Attributes and elements</span></span>

<span data-ttu-id="7e8cc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e8cc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7e8cc-108">Attributes</span></span>

<span data-ttu-id="7e8cc-109">无。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e8cc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7e8cc-110">Child elements</span></span>

|<span data-ttu-id="7e8cc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e8cc-111">**Element**</span></span>|<span data-ttu-id="7e8cc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e8cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e8cc-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="7e8cc-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="7e8cc-114">包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="7e8cc-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="7e8cc-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7e8cc-116">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7e8cc-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7e8cc-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7e8cc-118">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7e8cc-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7e8cc-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7e8cc-120">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="7e8cc-121">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7e8cc-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7e8cc-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7e8cc-123">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e8cc-124">父元素</span><span class="sxs-lookup"><span data-stu-id="7e8cc-124">Parent elements</span></span>

<span data-ttu-id="7e8cc-125">无。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e8cc-126">说明</span><span class="sxs-lookup"><span data-stu-id="7e8cc-126">Remarks</span></span>

<span data-ttu-id="7e8cc-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e8cc-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e8cc-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e8cc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e8cc-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e8cc-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e8cc-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e8cc-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7e8cc-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="7e8cc-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e8cc-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e8cc-132">Validation File</span></span>  <br/> |<span data-ttu-id="7e8cc-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e8cc-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e8cc-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e8cc-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e8cc-135">False</span><span class="sxs-lookup"><span data-stu-id="7e8cc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e8cc-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e8cc-136">See also</span></span>

- [<span data-ttu-id="7e8cc-137">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="7e8cc-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="7e8cc-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7e8cc-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7e8cc-139">添加委派</span><span class="sxs-lookup"><span data-stu-id="7e8cc-139">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

