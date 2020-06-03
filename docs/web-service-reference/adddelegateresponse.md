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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466456"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="9afff-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="9afff-103">AddDelegateResponse</span></span>

<span data-ttu-id="9afff-104">**AddDelegateResponse**元素包含[AddDelegate 操作](adddelegate-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="9afff-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="9afff-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9afff-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9afff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9afff-106">Attributes and elements</span></span>

<span data-ttu-id="9afff-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9afff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9afff-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9afff-108">Attributes</span></span>

<span data-ttu-id="9afff-109">无。</span><span class="sxs-lookup"><span data-stu-id="9afff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9afff-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9afff-110">Child elements</span></span>

|<span data-ttu-id="9afff-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9afff-111">**Element**</span></span>|<span data-ttu-id="9afff-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9afff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9afff-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="9afff-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="9afff-114">包含 Exchange Web 服务委派管理请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9afff-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="9afff-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="9afff-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9afff-116">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="9afff-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9afff-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9afff-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9afff-118">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="9afff-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9afff-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9afff-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9afff-120">当前未使用，并保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="9afff-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9afff-121">它包含值0。</span><span class="sxs-lookup"><span data-stu-id="9afff-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9afff-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9afff-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9afff-123">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="9afff-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9afff-124">父元素</span><span class="sxs-lookup"><span data-stu-id="9afff-124">Parent elements</span></span>

<span data-ttu-id="9afff-125">无。</span><span class="sxs-lookup"><span data-stu-id="9afff-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9afff-126">说明</span><span class="sxs-lookup"><span data-stu-id="9afff-126">Remarks</span></span>

<span data-ttu-id="9afff-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9afff-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9afff-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="9afff-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9afff-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="9afff-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9afff-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="9afff-130">Schema Name</span></span>  <br/> |<span data-ttu-id="9afff-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="9afff-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9afff-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="9afff-132">Validation File</span></span>  <br/> |<span data-ttu-id="9afff-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9afff-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9afff-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="9afff-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="9afff-135">False</span><span class="sxs-lookup"><span data-stu-id="9afff-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9afff-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9afff-136">See also</span></span>

- [<span data-ttu-id="9afff-137">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="9afff-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="9afff-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9afff-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="9afff-139">添加委派</span><span class="sxs-lookup"><span data-stu-id="9afff-139">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

