---
title: DeleteItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponse
api_type:
- schema
ms.assetid: 86463d66-fe47-4a19-a81b-e24841e816ab
description: DeleteItemResponse 元素定义一个删除项请求的响应。
ms.openlocfilehash: 8a35033c744fbcb0829d2c79a8d79557f77137bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753813"
---
# <a name="deleteitemresponse"></a><span data-ttu-id="ab22b-103">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="ab22b-103">DeleteItemResponse</span></span>

<span data-ttu-id="ab22b-104">**DeleteItemResponse**元素定义一个删除项请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ab22b-104">The **DeleteItemResponse** element defines a response to a single DeleteItem request.</span></span> 
  
```xml
<DeleteItemResponse>
   <ResponseMessages/>
</DeleteItemResponse>
```

 <span data-ttu-id="ab22b-105">**DeleteItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="ab22b-105">**DeleteItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab22b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ab22b-106">Attributes and elements</span></span>

<span data-ttu-id="ab22b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ab22b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab22b-108">属性</span><span class="sxs-lookup"><span data-stu-id="ab22b-108">Attributes</span></span>

<span data-ttu-id="ab22b-109">无。</span><span class="sxs-lookup"><span data-stu-id="ab22b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab22b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ab22b-110">Child elements</span></span>

|<span data-ttu-id="ab22b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ab22b-111">**Element**</span></span>|<span data-ttu-id="ab22b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ab22b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab22b-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ab22b-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ab22b-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ab22b-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab22b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ab22b-115">Parent elements</span></span>

<span data-ttu-id="ab22b-116">无。</span><span class="sxs-lookup"><span data-stu-id="ab22b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab22b-117">备注</span><span class="sxs-lookup"><span data-stu-id="ab22b-117">Remarks</span></span>

<span data-ttu-id="ab22b-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ab22b-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab22b-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="ab22b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab22b-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="ab22b-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab22b-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="ab22b-121">Schema Name</span></span>  <br/> |<span data-ttu-id="ab22b-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="ab22b-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab22b-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="ab22b-123">Validation File</span></span>  <br/> |<span data-ttu-id="ab22b-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ab22b-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab22b-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="ab22b-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab22b-126">False</span><span class="sxs-lookup"><span data-stu-id="ab22b-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab22b-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ab22b-127">See also</span></span>

- [<span data-ttu-id="ab22b-128">删除项操作</span><span class="sxs-lookup"><span data-stu-id="ab22b-128">DeleteItem operation</span></span>](deleteitem-operation.md)  
- [<span data-ttu-id="ab22b-129">删除项</span><span class="sxs-lookup"><span data-stu-id="ab22b-129">DeleteItem</span></span>](deleteitem.md)
- [<span data-ttu-id="ab22b-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ab22b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

